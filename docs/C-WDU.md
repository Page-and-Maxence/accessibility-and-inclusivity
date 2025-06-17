# 🫂 C-WDU We are all disabled and unique : accessibility, plurality and intersectionality

>**💡 In this module, we will explore the concepts of intersectionality and inclusiveness and it’s use in software development**

**⛳️ Section**: D. Designing inclusive and accessible software

**👥 Audience**: Designers

**⏱️ ️Duration**: 30'

**📚 Prerequisites**: Accessibility, inclusion & exclusion, We are all disabled and unique

**📖 Is a prerequisite to**: None

---


# When to use ?

This module is necessary in order to go further than the idea that accessibility is merely about designing for low vision or deaf users.

---

# Inclusiveness and co-creation
## Who is disabled ?

Since the beginning of this formation, we have been speaking about disabled peoples in the 3rd person as if they were "others". The truth is, some of us writing this are disabled, some of you reading it are and we will all become disabled some days. The barrier between able-bodied and disabled is a lot more porous than we could think at first glance.

A lot of persons that think of themselves as valid use the screen zoom feature in order too have bigger text and people with less technical experience that struggle with using a device are also a core target for accessibility features like simplified UI.

The line blurs further once we realize that accessibility features are useful to everybody no matter what. VIM users are the first ones to profit from good keyboard navigation, a lot of folks use subtitles on a daily basis and mobile gesture typing started as an accessibility feature.

**Therefore, it's crucial to not think disabled peoples as a minority but rather as the living diversity that we we will all become**

## What is inclusiveness ?

The [Cambridge dictionary](https://dictionary.cambridge.org/dictionary/english/inclusiveness) would define inclusiveness as :
>the quality of including many different types of people and treating them all fairly and equally

Inclusiveness is a core concept when talking about diversity. It's often a preferred term to accessibility that would be limited to disability. It highlights that we need to not only think about designing and programming accounting for accessability but also for varying cultural and social context. **In simpler words, not being ableist is not enough. We must be sure that we are also not perpetuating other oppressions.** For example, using neutral language and icons when referring to a user and not having fixed first and last name fields as those can vary between cultures.

It's also important to know that we cannot pretend trying to address inclusiveness without knowing about intersectionality. That's why the rest of this module will be dedicated to it.

# Intersectionality and plurality of experiences

## What is intersectionality ?

Kimberle Crenshaw, in [Mapping the Margins: Intersectionality, Identity Politics, and Violence against Women of Color](https://www.jstor.org/stable/1229039) defines intersectionality in order to face an issue that she encountered as a US jurist in the late 80’s. When filling cases about discriminations in work environment, the lawyer must at that time select the discrimination which their client is facing (for example racism or sexism).

But some over Crenshaw’s clients are black woman and their cases were dismissed because their employer did hired white woman and black men and therefore could protect themselves from accusations of sexism or racism.

That’s why Crenshaw defined intersectionality to designate a specific living experience of someone situated at the intersection of two communities. In her case, to showcase the specific oppression that black women lived and that couldn’t be explained by sexism and racism alone. The intersection of “black” and “women” produced a different oppression that isn’t simply the addition of the two.

## Intersectionality in software

What do we need the concept of intersectionality for in software development ?

It’s actually very useful for two main reasons !

- Most disabled people have more than one disability. Thinking about designing for a disability leaves out blank spot for most users having that disability but also other conditions. For example, deaf users with low vision are often overlooked when thinking about accessibility. We will take a closer look at the appropriate stance to account for diversity in [Developer stance & user collaboration](B-DSU.md)

- It’s a common biases to forget that disabled people are not just disabled, but first and foremost people with their own unique life experiences and specificities. We need to think about disabled women, disabled queers, disabled Arabs and those who are all of that at once!

**Certain issues only arise for people with a specific intersectional background.**

Take for example this main account creation page. If you ask someone that you know with vision to test it or do it yourself you probably won't find any issue. Can you guess what kind of users can have trouble with it.

![A screenshot of an account creation page with a Create Jami account button, a I already have an account button, an Advanced features button, an about Jami button, a user interface language combobox, a back arrow button and a logo.](ressources/B-HowToStartIncroporatingAccessibility/jamiAccountCreationPage.png)

This one was hard and required a lot of intuition. The "user interface language" label and the actual combo box look like two separate elements, because they are, making them inaccessible as is with keyboard navigation. If you speak a niche language and are low vision you cannot access the combobox to change it to a language that you speak.

Therefore, a low vision, english speaking user will not encounter any issue on this page and might consider it totally accessible while a non-english speaking one will encounter issues navigating it.

This is fixed by this page adapting to your system language dynamically.

Another intersectional example is presented to us by Apple in their [The practice of inclusive design](https://developer.apple.com/videos/play/wwdc2021/10275/) video.They encountered this issue when developing a system capable of automatically generate description of images for low vision users using a generative AI model. Can you guess what it is?

![The accessible text of the previous image of this page (the account creation page) as seen in the markdown](ressources/B-HowToStartIncroporatingAccessibility/accessibleDescription.png)
*The accessible text of the previous image of this page (the account creation page) as seen in the markdown*

The model generating descriptions had the tendency to assign gender to people on the images it was captioning, therefore regularly misgendering cis, trans and especially non-binary folks. This issue encountered by folks at the intersection of the low vision and queer community prevented them from affirming their identify.

The solution that Apple choose to adopt was to train their model to concentrate on other elements of an image, like the clothes that a person is wearing, their facial expression or where they are standing. By avoiding oppressive biases, the model ended up being better for all users.



# Sources
[Crenshaw, Kimberle. “Mapping the Margins: Intersectionality, Identity Politics, and Violence against Women of Color.” Stanford Law Review, vol. 43, no. 6, 1991, pp. 1241–99.](https://www.jstor.org/stable/1229039)

[Apple. "The practice of inclusive design". Accessed the 17 July 2025](https://developer.apple.com/videos/play/wwdc2021/10275/)

[Cambridge's dictionary's definition of inclusiveness](https://dictionary.cambridge.org/dictionary/english/inclusiveness)

