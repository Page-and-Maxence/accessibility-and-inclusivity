# 📲 Assistive technologies: Mobile

!!! Info "In this module"
    This module allows participants to get to know the major assistive technologies used on mobile devices. The goal is not to get in depth on how to use them but rather to help designers and developers get an idea of what is commonly used, and to find the relevant tools for their use cases.

**⛳️ Section**: *A. What is accessibility ?*

**👥 Audience**: Everyone

**⏱️ Duration**: 5'

**📚 Prerequisites**: [🎨 Inclusive design 101](C-IDE.md)

---

## Introduction

There are infinite unique (and combining) ways of interacting with mobile devices. In this module, we'll try to cover the most commonly used assistive technologies so that you can get an idea of the ways your users might be interacting with your app.

## Screen readers

Just like computers, screen readers constitute an assistive technology that is essential to many users. Nevertheless, the way they are designed, implemented and used differ a lot from [what you will commonly see on desktop platforms](A-ITD.md):

- They are almost always directly built and deeply integrated into the OS, while desktop screen readers are typically third party apps.
- They embed an alternative way of navigating using specific gestures, while desktop screen readers commonly rely on keyboard navigation.

On Android, the feature's name is [TalkBack](https://appt.org/en/docs/android/features/talkback). On iOS, it's [VoiceOver](https://appt.org/en/docs/ios/features/voiceover). While they have many differences when it comes to advanced use, their basic usage is very similar. On both platforms:

- Quickly scan the interface by running your finger through the screen as if you were reading braille.
- Swipe left of right to navigate to the previous or next element in the interface.
- Double-tap to activate an element (e.g. a push button)

[Here is a video from Android showcasing how TalkBack works from a user perspective.](https://www.youtube.com/watch?v=_1yRVwhEv5I&t=28s)

## Alternative peripherals

Some people prefer or need to interact with mobile devices through external peripherals. These can either be switches (with typically two buttons), sticks, game controllers, keyboards, *etc*.

Making an app accessible to these is most commonly done by making it accessible to screen readers. If the right elements are focusable, those should work just fine. Making them work *great* mainly comes down to providing shortcuts and good headings management.

[Here is a video from Apple Developer showing some Full Keyboard support on iOS apps.](https://www.youtube.com/watch?v=Zybw0IPGles)

### Switch control

Often combined with other controls (like eye, voice or head motion), switch control allows users to interact with app without needing the ability to precisely aim for the touchscreen elements. Users can have custom various actions (like go next, go previous, interact, etc.) on each switch, allowing for highly specific setups.

<figure markdown="span">
  ![Picture of a switch with two buttons, one is white and the other is yellow.](resources/a-what-is-accessibility/switch.jpg){ width="300" }
  <figcaption>Accessibility switch</figcaption>
</figure>

[Here is an example use of a single switch to control an iPhone.](https://www.youtube.com/watch?v=HBo2BZ-Zzwg)

### Eye and face control

Eye-tracking (fully supported on iOS, still experimental on Android) is another way of interacting with interfaces via gaze. Users can look at an element for a certain amount of time or perform a sound, move their head or even tap a switch while looking at an element to take action on it.

### Voice control

Users can also use their voice to choose which elements to select. Labeling your app properly allows them to call elements by their name rather than by numbers.

## Accessibility settings

Depending on the OS, there are many ways users can fine-tune their experience through accessibility settings. Your role as a software builder is to test your interface with many combinations of settings to make sure it works well. While we won't go through these here, you can browse your device's settings to discover all the possibilities your OS offers, as well as check out [this great resource](https://appt.org/en/docs) for general information on platform-specific mobile assistive technologies.

## Resources

[APPT's Accessibility documentation](https://appt.org/en/docs)
