# 📗 E-APQ Accessible programming with Qt


    This module provides information needed for building accessible code using the Qt
    framework.

**⛳️ Section**: E. Programming inclusive and accessible software

**👥 Audience**: Developers

**⏱️ ️Duration**: 10'

**📚 Prerequisites**: [👩‍💻 E-ICO Inclusive code 101](E-ICO.md)

---

# When to use ?
Go through this module if your app uses Qt or if you consider using it and what to see how does it holds out from an accessibility perspective. Please note that it is not usable at all without [👩‍💻 E-ICO Inclusive code 101](E-ICO.md).

# Description

There are only few example of good accessibility implementation using Qt. Even the one provided by Qt themselves are limited to a single static page with a few elements. Therefor, we will go through all Qt's main accessibility elements while taking a look at a complex UI element as a chat view.
## Accessibility labels
Screen-readers and other accessibility technologies need specific information in order to navigate through your app. We are lucky that Qt provides a way of setting it automatically using the [QAccessible Class](https://doc.qt.io/qt-6/qaccessible.html#Role-enum). This class is inherited by all Qt's items.

It will try to automatically fill the accessibility fields but this often fails. Therefore you should set those fields manually in order to make your interface accessible. The bare minimum is setting :

- The **role**: this will indicate to the user using an accessibility technology like a screen-reader or a braille display how they can interact with this specific object. It can takes values such as Button, StaticText, Heading, dialog... You can find the full list in the according [Qt's documentation of QAccessible::Role](https://doc.qt.io/qt-6/qaccessible.html?search=item#Role-enum).
- The **name**: this is the main title of your component like for example "create account button" or "Language selection ComboBox".
- The **description**: this should explain to the user what will happen if they interact with this component as well as any additional context information. It can be for example "Display your QR code to allow other users to scan it and add you as a contact" or "Use arrows to switch between available account".

In QML code this would look like :
```QML
Accessible.role: Accessible.Button
Accessible.name: toolTipText
Accessible.description: JamiStrings.qrCodeExplanation
```
For a lot of elements like a message, you would want the accessibility to be grouped in ways that are not as evident as the example above. Let's say that we want to design it for our chat-view. We only want the message to be focusable and it should contains all information needed. In the [🎨 D-IDE: Inclusive design 101](D-IDE.md) module, we stated that the label should read something like:

    "Michel Berger. 3 unread messages. You said : Thanks ! at 9:07.
    Message status : sent. Pinned. Actions available.”

Code producing an implementation close to this one would be :
```cpp
    Accessible.role: Accessible.StaticText
    Accessible.name: {
        let name = isOutgoing ? JamiStrings.inReplyToYou : UtilsAdapter.getBestNameForUri(CurrentAccount.id, Author)
        return name + ": " + Body + " " + formattedTime + " " + formattedDay
    }
    Accessible.description: {
        let status = ""
        if (bubble.isEdited) status += JamiStrings.edited + " "
        if (IsLastSent) status += JamiStrings.sent + " "
        return status + (readers.length > 0 ? JamiStrings.readBy + " " + readers.join(", ") : "")
    }
```
## Keyboard navigation
As stated in [👩‍💻 E-ICO Inclusive code 101](E-ICO.md), keyboard and focus navigation is mostly automatically set by Qt but the framework often fails to navigate complex elements. **You need to make sure that all focusable elements are reached**. Before manually setting keyboard navigation, you should try and use the base focus property of Qt. For example setting the focus of a component to true might be enough for Qt to recognize it as a reachable interactive element. These will largely depend of the component you will be working on but you will get use to seeing some of the following variables.

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

In some case like a contextual menu, you might want to add conditional navigation:
```QML
KeyNavigation.backtab: index === 0 ? settingsButton : null
KeyNavigation.tab: index === listView.count - 1 ? addAccountItem : null
KeyNavigation.up: KeyNavigation.backtab
KeyNavigation.down: KeyNavigation.tab
```
Concerning our chat view, we previously stated in [🎨 D-IDE: Inclusive design 101](D-IDE.md) that "*we would typically focus the last element of the discussion first, because it is typically the one of interest, and because it gives a quick access to the text input. But this is clearly a design choice that must be well-thought and tested in the context of your app.*" This is only one of the possible implementation. We also could want to send users directly to the text input stating in which conversation they are.

Inside the list of messages we could want users to navigate between messages using the arrows and TAB to directly go to the text input field but once again, this is a design choice.
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

The [QAccessibleInterface Class](https://doc.qt.io/qt-6/qaccessibleinterface.html) is useful to create inclusive user interface. It implements a pure virtual API that allows accessible technologies like braille displays or screen readers to directly access information about accessible objects. We have less experience with it as we didn't implemented it on applications we are working on yet. You can find very comprehensive information about it in [this typevar article](https://typevar.dev/en/docs/qt/qaccessibleinterface)

# Sources
[Qt's documentation of QAccessible Class](https://doc.qt.io/qt-6/qaccessible.html#Role-enum)
[Qt's documentation of QAccessible::Role](https://doc.qt.io/qt-6/qaccessible.html?search=item#Role-enum)
[Qt's documentation of KeyNavigation class](https://doc.qt.io/qt-6/qml-qtquick-keynavigation.html#details)
[Qt's documentation of QAccessibleInterface Class](https://doc.qt.io/qt-6/qaccessibleinterface.html)
[Enhancing Accessibility with QAccessibleInterface in Qt Applications ](https://typevar.dev/en/docs/qt/qaccessibleinterface)