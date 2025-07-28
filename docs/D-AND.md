# 🤖 Inclusive features and programming for Android

!!! Info "In this module"
    This module introduces trainees to Android's accessibility features, and to the practice of inclusive programming for Android.

**⛳️ Section**: D. Programming inclusive and accessible software

**👥 Audience**: Android developers and product teams

**⏱️ ️Duration**: 15'

**📚 Prerequisites**: [👩‍💻 Inclusive code 101](D-ICO.md)

---

## When to use

This module should be used with trainees who program Android apps, product designers and managers who would like to better understand what is possible on Android when it comes to accessibility.

!!! Info
    As we are not Android developers and didn't get the chance to dive deep into Android accessibility as of the time of writing, this module's content could be significantly improved. For now, this page will mainly redirect to useful resources we found along with some key takeaways. If you have experience with Android accessibility and you feel like helping the project, [please contribute](https://github.com/alterity-git/building-inclusive-open-source-software).

## Android's accessibility model

Accessibility is presented by Google as one of [Material 3's foundations](https://m3.material.io/foundations/overview/principles). Indeed, like iOS, Material native components come with built-in accessibility that represent most of the hard work. Consequently, if you use native components, most of your work as a developer is to contextualize those elements by customizing the labels, actions and by building a consistent navigation through the accessibility tree.

Android's **accessibility tree** is a hierarchical organization of your app's on-screen components that is made available to assistive technologies. It is automatically derived from your code (whether XML or Compose). Design decisions like custom labels, grouping or changing the focus order can be implemented by applying changes to the nodes, using Android's accessibility API.

This API is not very well documented by Android themselves, but there are great resources out there to learn how to implement accessibility for this platform:

- [APPT's technical documentation](https://appt.org/en/docs/android/samples) is very extensive and can provide you with code samples and explanations through the whole Android accessibility API. They provide the same for [Jetpack Compose](https://appt.org/en/docs/jetpack-compose/samples).
- [Rob Whitaker's *Developing Inclusive Mobile Apps: Building Accessible Apps for iOS and Android*](https://www.researchgate.net/publication/340927171_Developing_Inclusive_Mobile_Apps_Building_Accessible_Apps_for_iOS_and_Android) is a very pedagogical book that has a chapter dedicated to implementation of Android accessibility. While it does not cover Jetpack Compose (the book was published in January of 2020), the author gives insightful guidelines that can be applied anyway.

## Android's assistive technologies and features

### TalkBack

TalkBack is the most prominent assistive technology available on Android. It works very much like VoiceOver, letting users navigate through your app (via the accessibility tree) without needing to see the screen. By making your app work with TalkBack, you are doing most of (if not all) the job required for it to be usable with any assistive technology.

Testing how you app works with TalkBack is the first thing to do to get a idea of what are the main issues. The best way of doing so is by dimming or hiding your screen (Android has a feature called "Dark screen" that allows to do so) to actually get an idea of how a blind or low-vision user would perceive your app. Look for missing labels, missing features (like unreachable elements or unavailable actions), grouping issues, etc. For more details on how to build an interface that is usable with assistive technologies, refer to [🎨 Inclusive design 101](C-IDE.md).

!!! Tip
    Here is [APPT's full list of TalkBack gestures](https://appt.org/en/docs/android/features/talkback). They also have an [app made to teach you how to use it](https://screenreader.app/).


### Switch Access

Switch Access is Android's accessibility feature allowing to control the device using a switch, that can either be external, a keyboard, or even the phone's buttons. If your accessibility tree is already well organized, navigating through your app with a switch should be fine. That said, make sure to check that actions requiring complex gestures, like drag-and-dropping, are supported by adding accessibility actions. Also, if you've implemented a tap listener on an element that is not marked as actionable, Switch Access won't pick it up.

### Keyboard Access

Android allows users to control their device using a keyboard. While, again, TalkBack support should mean that the app can be used with a keyboard, this does not guarantee a good user experience. Providing keyboard shortcuts ([Jetpack Compose](https://appt.org/en/docs/jetpack-compose/samples/keyboard-shortcuts), [XML](https://appt.org/en/docs/android/samples/keyboard-shortcuts)) and custom keyboard order ([Jetpack Compose](https://appt.org/en/docs/jetpack-compose/samples/keyboard-order), [XML](https://appt.org/en/docs/android/samples/keyboard-order)) will contribute to delivering a great UX to keyboard users.

!!! Tip
    Here is [APPT's guide to navigating apps with an external keyboard](https://appt.org/en/docs/android/features/keyboard-access#overview).

### Voice Access

Voice Access is an accessibility service developed by Google and available in the Play Store. It aims at providing vocal access to the whole device. Unlike Apple's Voice Control, this software uses numbers rather than labels to interact with elements. Users can also use text values (and not content description) to select an item of the UI.

### Third-party assistive technologies

Unlike Apple, Android has opened their accessibility API, allowing anyone to build their own accessibility service. While you probably don't want to implement one specifically for your app (unless you *really* have specific accessibility needs), it's good to know that there are plenty of tools to choose from!

### Display size, text size

Display and text sizes might vary dramatically based on user needs. Making your app adaptable to those variables is quite straightforward:

- Make sure your text font sizes are indeed affected by system settings. If not, [consider using *sp* as unit](https://developer.android.com/training/multiscreen/screendensities) for your sizes where you are required to use fixed values.
- Be careful when using ```maxLines``` to prevent text truncation as there is only few scenarios where it's the most relevant approach.

### Captions

Captions can easily be implemented in your Android app for media content. Refer to the APPT documentation for details (Jetpack Compose: [standard](https://appt.org/en/docs/jetpack-compose/samples/captions), [live](https://appt.org/en/docs/jetpack-compose/samples/live-captions); XML: [standard](https://appt.org/en/docs/android/samples/captions), [live](https://appt.org/en/docs/android/samples/live-captions)).

### Reduced animations

Some users prefer or need to reduce animations. While Android doesn't directly indicate through the API whether the user has the option activated or not, you can determine it with [this little workaround](https://appt.org/en/docs/android/samples/reduced-animations). Stopping automatic and repeating animations, as well as flashes or blinkings, zooms and parallax effects is crucial to make sure users can use your app safely and comfortably.

## Resources

[APPT's technical documentation for Android XML](https://appt.org/en/docs/android/samples)
[APPT's technical documentation for Jetpack Compose](https://appt.org/en/docs/jetpack-compose)
[Rob Whitaker's *Developing Inclusive Mobile Apps: Building Accessible Apps for iOS and Android*](https://www.researchgate.net/publication/340927171_Developing_Inclusive_Mobile_Apps_Building_Accessible_Apps_for_iOS_and_Android)