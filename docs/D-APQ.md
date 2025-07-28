# 📗 Accessible programming with Qt


!!! Info "In this module"
    This module provides information needed for building accessible code using the Qt
    framework.

**⛳️ Section**: *D. Programming inclusive and accessible software*

**👥 Audience**: Qt Developers and product teams

**⏱️ ️Duration**: 10'

**📚 Prerequisites**: [👩‍💻 Inclusive code 101](D-ICO.md)

---

## When to use?
Go through this module if your app uses Qt, or if you consider using it for your app. Please note that this module requires the trainees to follow [👩‍💻 Inclusive code 101](D-ICO.md) first.

## Introduction

There are only few example of good accessibility implementation using Qt. Even the one provided by Qt themselves are limited to a single static page with a few elements. Therefore, we will go through all of Qt's main accessibility elements while taking a look at a complex UI element, a chat view.

!!! Info
    In this module, we will be using for example purposes some code extracts from [the Jami Qt client](https://git.jami.net/savoirfairelinux/jami-client-qt), which is licensed under the [GPLv3 license](https://github.com/savoirfairelinux/jami-client-qt/blob/master/COPYING).

## Accessibility labels

Screen-readers and other accessibility technologies need specific information in order to navigate through your app. We are lucky that Qt provides a way of setting it automatically using the [QAccessible Class](https://doc.qt.io/qt-6/qaccessible.html#Role-enum). This class is inherited by all of Qt's items.

It will try to automatically fill the accessibility fields but this often fails. Therefore you should set those fields manually in order to make your interface accessible. The bare minimum is setting:

- The **role**: this will indicate to the accessibility technology users (like a screen-reader or a braille display) how they can interact with this specific object. It can take values such as Button, StaticText, Heading, dialog... You can find the full list in the according [Qt's documentation of QAccessible::Role](https://doc.qt.io/qt-6/qaccessible.html?search=item#Role-enum).
- The **name**: this is the main title of your component, like for example "Create account Button" or "Language selection ComboBox".
- The **description**: this should explain to the user what will happen if they interact with this component as well as any additional context information. It can be for example "Display your QR code to allow other users to scan it and add you as a contact" or "Use arrows to switch between available accounts".

In QML code this would look like:

```QML
Accessible.role: Accessible.Button
Accessible.name: toolTipText
Accessible.description: JamiStrings.qrCodeExplanation
```

For many elements, like a message for example, you would want the accessibility to be grouped in ways that are not as obvious as the example above. Let's say that we want to design it for our chat-view. We only want the message to be focusable and it should contain all the information needed. In the [🎨 Inclusive design 101](C-IDE.md) module, we stated that the label should read something like:

    "Michel Berger. 3 unread messages. You said: Thanks! at 9:07.
    Message status: sent. Pinned. Actions available.”

The code producing an implementation close to this one would be:
```cpp
    Accessible.role: Accessible.StaticText
    Accessible.name: {
        let name = isOutgoing ? JamiStrings.inReplyToYou: UtilsAdapter.getBestNameForUri(CurrentAccount.id, Author)
        return name + ": " + Body + " " + formattedTime + " " + formattedDay
    }
    Accessible.description: {
        let status = ""
        if (bubble.isEdited) status += JamiStrings.edited + " "
        if (IsLastSent) status += JamiStrings.sent + " "
        return status + (readers.length > 0 ? JamiStrings.readBy + " " + readers.join(", "): "")
    }
```
## Keyboard navigation

As stated in [👩‍💻 Inclusive code 101](D-ICO.md), keyboard and focus navigation is mostly automatically set by Qt, but the framework often fails to navigate complex elements. **You need to make sure that all focusable elements are reached**. Before manually setting keyboard navigation, you should try and use the base focus property of Qt. For example, setting the focus of a component to true might be enough for Qt to recognize it as a reachable interactive element. These will largely depend of the component you will be working on but you will get used to seeing some of the following variables.

```QML
    keyNavigationEnabled: true
    keyNavigationWraps: false
    focus: true
    activeFocusOnTab: true
```
That said, you will often need to set manually the keyboard navigation using [Qt's KeyNavigation class](https://doc.qt.io/qt-6/qml-qtquick-keynavigation.html#details).

A very easy example would be:
```QML
KeyNavigation.backtab: addAccountItem
KeyNavigation.tab: shareButton
KeyNavigation.up: addAccountItem
KeyNavigation.down: shareButton
```

Regarding our chat view, we previously stated in [🎨 Inclusive design 101](C-IDE.md) that "*we would typically focus the last element of the discussion first, because it is typically the one of interest, and because it gives a quick access to the text input. But this is clearly a design choice that must be well-thought and tested in the context of your app.*" This is only one of the many possible implementations. We could also want to send users directly to the text stating the current discussion's name.

Inside the list of messages, we could want users to navigate between elements using the arrows and TAB to directly go to the text input field - but once again, this is a design choice.
```cpp
// Rather than doing this inside the message itself, we do it at the ListView level
ListView {
    id: root
    // We try to minimize custom code for navigation and therefore use
    // the Qt base property of a List view rather than setting
    // KeyNavigation.tab each time
    keyNavigationEnabled: true
    keyNavigationWraps: false
}
```

## The AccessibleInterface Class

The [QAccessibleInterface Class](https://doc.qt.io/qt-6/qaccessibleinterface.html) is useful to create inclusive user interfaces. It implements a pure virtual API that allows assistive technologies like braille displays or screen readers to directly access information about accessible objects. We have less experience with it as we haven't implemented it on applications we are working on yet.

## Sources
[Qt's documentation of QAccessible Class](https://doc.qt.io/qt-6/qaccessible.html#Role-enum)

[Qt's documentation of QAccessible::Role](https://doc.qt.io/qt-6/qaccessible.html?search=item#Role-enum)

[Qt's documentation of KeyNavigation class](https://doc.qt.io/qt-6/qml-qtquick-keynavigation.html#details)

[Qt's documentation of QAccessibleInterface Class](https://doc.qt.io/qt-6/qaccessibleinterface.html)
