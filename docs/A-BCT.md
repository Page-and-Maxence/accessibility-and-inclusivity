# 🗺️ Brief cartography of today’s accessibility landscape

!!! Info "In this module"
    We will cover the main actors of today's accessibility landscape as well as their dynamics.

**⛳️ Section**: A. What is accessibility ?

**👥 Audience**: Everyone

**⏱️ Duration**: 10'

**📚 Prerequisites**: [👩‍🦽 A-AIE: Accessibility & Ableism](A-AIE.md)

---

## When to use ?

This module is useful as an introduction to understand what are the current dynamics in the accessibility landscape, what actors are considered as reference, and which ones are disregarded by most experts.

## Disclaimer

We -the original authors- are not experts by any mean, only engineers working on accessibility and inclusiveness trying to provide others with the resources we wished we had when starting working on accessibility and inclusiveness. We don't have a complete understanding of all stakes of the accessibility landscape. Keep in mind that the following cartography will certainly miss some precisions. If you want to help completing it with your own knowledge, feel free to contact us or to open a pull request on [our repository](https://github.com/alterity-git/building-inclusive-open-source-software).

## The actors of accessibility

The actors can be separated in four main categories: the publics actors, non-profit collectives, consulting firms, small companies (including start-ups) and bigger corporate actors. We could also mention researchers and book writers - but this would probably turn this module into a full bibliography.

### Countries & institutions

#### Countries

Countries plays an increasing role in the accessibility landscape. As awareness rises, the law evolves to guarantee access to technology as a fundamental human right. We briefly mentioned the law of some countries in [Accessibility & Ableism](A-AIE.md). Additionally, [this map](https://github.com/Tanaguru/Map-of-Web-Accessibility-Laws-Policies) holds current laws for many countries (despite having a strong bias towards western countries).

#### European Union

The European Union adopted in 2019 the [European Accessibility Act (EAA)](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX:32019L0882), which requires digital service providers to make their product accessible. Deque, a well-known accessibility consulting firm, has [a detailed article on the subject](https://www.deque.com/european-accessibility-act-eaa-compliance/).

### Non-profit collectives

Non-profit organizations are at the core of producing resources about accessibility and inclusiveness, especially from a design and platform agnostic perspective. They are also a great sources for critical subjects on the current state of accessibility for different platforms as they often have less conflicts of interest.

#### The World Wide Web Consortium (W3C)

The [World Wide Web Consortium](https://www.w3.org/about/) is the organization behind multiple accessibility guidelines and standards recognized worldwide. With over 30 years of existence, it's mostly known for its work on the WCAG which are the worldwide standards in term of web accessibility.

They also created and updated a very extensive documentation on how to meet those standards with their [Quick Reference on How to Meet WCAG](https://www.w3.org/WAI/WCAG22/quickref/). They are definitely one of the most important organizations providing resources on accessibility.

![A screenshot of the main page of the W3C stating 'The World Wide Web Consortium (W3C) develops standards and guidelines to help everyone build a web based on the principles of accessibility, internationalization, privacy and security'.](resources/a-what-is-accessibility/w3cScreenshot.png)

**They have full time employees but also rely on volunteers contributions, so if you want to help them, [go ahead](https://www.w3.org/get-involved/)!**

Sadly, despite the amazing work that they do on accessibility, they still lack diversity. They are trying to do better on this topic, providing [yearly detailed statistics of their diversity](https://www.w3.org/about/diversity/diversity-report-2024/) for their Advisory board, technical architecture group, board of directors and management. We can notice that their inclusiveness seems to improve over time.

![Stats about the diversity in the technical architecture group of the W3C. While it's getting better, they had no women nor non binary people until 2011. The full chart in tabular version is available at this link: https://www.w3.org/2024/07/diversity/descriptions.html#tag-gender](resources/a-what-is-accessibility/w3cStats.png)

#### The Appt Foundation

The Appt foundation is a non-profit organization started in the netherlands that specialize on mobile applicative accessibility. It doesn't have employees but work with experts and industrial partners. They have multiple extensive documentations including code samples about accessibility for mobile frameworks that are often way clearer than the official ones.

![A screenshot of the frameworks documented by the Appt foundation: android, Jetpack compose, iOS, swiftUI, Flutter, React Native. .NET MAUI and Xamarin](resources/a-what-is-accessibility/apptFondationFrameworks.png)

It's definitely a very useful resource if they have documentation for the framework you are working with. You can contribute on [their repository](https://github.com/appt-org/appt-website).

#### The A11Y Project

The A11Y Project mostly focuses on web accessibility but isn't limited to it, also hosting a very extensive and useful list of resources. Their posts are informative. They have a "spotlight" section which is useful to get to know the contributions of amazing people working on software accessibility. Most importantly, their list of medias is well furnished with [dozen of carefully selected resources](https://www.a11yproject.com/resources/). **We strongly invite you to take a look at it.**

![The a11y project home page stating "a11y stands for accessibility'. The phrase '11 characters'. Arrows are pointing to the first letter c and the letter t in the word 'accessibility' to show how the numeronym is formed.The A11Y Project is a community-driven effort to make digital accessibility easier."](resources/a-what-is-accessibility/a11yHomePage.png)

#### The Accessibility Book Club

The Accessibility Book club is a small organization releasing a [yearly book list about accessibility](https://www.a11ybookclub.com/annual-book-lists). Their selection is a very useful tool to stay up to date with the developments of the accessibility and inclusiveness publications.

![The 2025 book list of the Accessibility book club. The full list is available through the link in the previous paragraph.](resources/a-what-is-accessibility/a11yBookClubHomePage.png)

### Consulting firms

There are many consulting firms about accessibility and inclusiveness. The quality of their services vary greatly in quality. Therefore we won't be recommending much of them as we cannot certify of the expertise of structures we haven't directly worked with.

#### Deque

While we cannot blindly recommend firms, Deque is an actor of the accessibility landscape that we need to mention. They built [Axe](https://www.deque.com/axe/auditor/) which is one of the most trusted web accessibility tool with over two billion downloads. Additionally, they are behind the accessibility of some of the biggest companies worldwide (working with Google, Microsoft and other large structures) and publish very relevant books on the topic. If you are looking for training, tools or an audit, you should consider their expertise.

### Corporate actors

Corporate actors and especially operating system providers can take an important role in accessibility and inclusiveness measures, either by their good or their bad will.

#### Apple

For years, Apple has been the reference for accessibility. Their tools and resources are among the best out there. Unfortunately, these tools and resources are directly targeted for their platforms. While some of them can be useful when developing for other platforms, their power really lies in the control they have on the whole technological stack, from hardware to framework. That said, their investments in setting the bar high with accessibility really pushed their competitors to try and do the same. While most third party apps still lack accessibility, the tools are here.

Recently, Apple announced their new design system, called Liquid Glass. This announcement have been heavily criticized for structural accessibility issues introduced by this redesign. As of the time of writing, we'll need to wait for the official release of the OS to see the impacts of these changes at scale.

#### Microsoft

While we do not endorse all of their content (especially the one related to "inclusive AI"), Microsoft has been publishing great extensive design resources about inclusiveness on [their dedicated website](https://inclusive.microsoft.design/).


## What to look for and what to avoid

### Accessibility and AI powered tools

If you search for some accessibility tools online, it's very probable that the first sponsored results to pop up will be something like *"Automated Web Accessibility Solution"*, often powered by AI. Those solutions are largely criticized by accessibility experts. In an open letter signed by more han 400 accessibility advocates, we can read:

!!!quote "Sarah Gooding, *[Accessibility Advocates Sign Open Letter Urging People Not To Use AccesiBe and Other Overlay Products](https://wptavern.com/accessibility-advocates-sign-open-letter-urging-people-not-to-use-accesibe-and-other-overlay-products)*. 2021"
    1. We will never advocate, recommend, or integrate an overlay which deceptively markets itself as providing automated compliance with laws or standards.
    2. We will always advocate for the remediation of accessibility issues at the source of the original error.
    3. We will refuse to stay silent when overlay vendors use deception to market their products.
    4. More specifically, we hereby advocate for the removal of accessiBe, AudioEye, UserWay, User1st, MK-Sense, MaxAccess, FACIL’iti, and all similar products and encourage the site owners who’ve implemented these products to use more robust, independent, and permanent strategies to making their sites more accessible.

Accessibility needs to be baked into an application from the very beginning. And while some work can be done to make existing interfaces more accessible, **there is no magic band-aid fix that will make your app accessible**. Indeed, accessibility is all about nuance, context and diverse user feedback. Trying to automate its whole process is paradoxical. Doing so will only result in your app striving to match arbitrary accessibility rulesets when the whole point is to embrace diversity and the uniqueness of ways to interact with a UI. **The rulesets, rather than being a tool to guide you, becomes the goal, effectively silencing disabled users.** Relying on those tools doesn't make your app usable for a disabled user. It will simply make sure no failure is triggered when running an automated test. Its lack of context will often lead them to the implementation of confusing and non-usable solutions.

!!! Tip
    **Accessibility is not a goal, it's a process. A process which cannot be done without disabled users and experts.**

### Green and red flags for choosing accessibility experts

The previous section should help you what to avoid, but what qualities should you be looking for when choosing experts ?

!!! success "Look for..."
    * Structures that have disabled experts or value directly working with disabled people
    * Structures that talk about inclusiveness rather than accessibility alone
    * Structures that provide transparency about their own diversity distribution

!!! Failure "Avoid..."
    * Automated accessibility overlay products
    * Products that claims to have automated AI accessibility fixes
    * Promises of quick fixes
    * Structures that delivers a one time accessibility enhancement without maintenance or knowledge transmission to your team


## Sources

[Sarah Gooding, *Accessibility Advocates Sign Open Letter Urging People Not To Use AccesiBe and Other Overlay Products*. 2021](https://wptavern.com/accessibility-advocates-sign-open-letter-urging-people-not-to-use-accesibe-and-other-overlay-products)
