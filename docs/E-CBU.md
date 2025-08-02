# 🎯 Conclusion, bibliography and useful resources

!!! Info "In this module"
    This module concludes the training by giving its key takeaways and linking them together, as well as recapitulating our bibliography, including resources that infused our work even if they were not explicitly cited.

**⛳️ Section**: *E. To conclude and go further*

**👥 Audience**: Everyone

**⏱️ Duration**: 10'

**📚 Prerequisites**: None

---

## When to use?

This module should be used as a synthesis of the main points of this training as well as a comprehensive list of resources for you to go further than what we covered here.

## What to take away from this training?

This section is a reorganized synthesis of the whole training.

### What is accessibility?

Accessibility is about designing and building for people who experience disabilities.
- From a product standpoint, it's about ensuring everything you build can be used by anyone, no matter their physical or cognitive abilities.
- From a legal standpoint, it is an obligation in many countries, guaranteeing an equal right to autonomy and participation of all.
- From a software standpoint, digital accessibility comes down to making apps optimally perceivable, operable and understandable to people who live with disabilities.
- From a political standpoint, accessibility is striving fight back against the structural tendency to exclusion of disabled people and attempting to provide them with a place (virtual or not) where they feel at ease and free to express themselves.

When products are not built with accessibility in mind, they end up excluding many people, denying them access to places, tools or even communication. This unfair exclusion is called ableism.

### Accessibility calls for inclusiveness

Inclusiveness is a core concept when talking about diversity. It's often a preferred term to accessibility, that is rather limited to the inclusion of people with disabilities. It highlights that we need to be designing and programming not only for people who experience disabilities, but also for the ever-varying pluralities of human experiences and discriminations emerging from them. In simpler words, focusing only on accessibility will result in the exclusion of the vas majority of users enduring oppressions.

Here is a *non-exhaustive* list of human characteristics to keep in mind in order to try and include as many user as possible:

- Age
- Culture
- Digital literacy
- Education
- Ethnicity
- Gender, gender identity
- Historical context
- Language
- Mental health
- Nationality
- Physical *and* cognitive (dis)abilities
- Sexuality
- Socio-economic context

Intersectionality is a framework for understanding specific living experiences of people situated at the intersection of discriminations and privileges.
It’s very useful, for two main reasons:

- The proportion of users with disabilities who happen to have more than one is important ([17.7% in 2016](https://pmc.ncbi.nlm.nih.gov/articles/PMC11545900/)). Thinking about designing for one disability leaves out a blank spot for users having that disability but also other conditions. For example, deaf users with low vision are often overlooked when thinking about accessibility.

- It’s a common bias to forget that disabled people are not just disabled, but first and foremost people with their own unique life experiences and specificities. We need to think about women who rely on wheelchairs, LGBTQIA+ people who don't speak the language of they country they live in, blind users who can't afford an iPhone - and those who are all of that at once!

!!!Tip
    **It's crucial to not think disabled peoples as a minority but rather as the living diversity in which we all evolve.**

### Accessibility and inclusiveness need to be intentional

Disability shouldn't be thought as an individual characteristic. Environment - and the way it is designed - plays an equal role as the body when it comes to disability. For example, in an environment built to be completely flat and non-obstructed, people who walk are way slower than people using a wheelchair.

!!! Quote "Rob Whitaker, *[Developing Inclusive Mobile Apps](https://link.springer.com/book/10.1007/978-1-4842-5814-9)*"
    Disability is not a binary state. We all have "abilities and limits to those abilities. Disability happens when we have built something that doesn’t work for someone with particular skills.

Additionally, by default, we naturally tend to design, program and test for people like us or the people we spend time with. Not thinking about accessibility is a privilege because most disabled people don't have the choice to think about it. Not developing with accessibility and inclusiveness in mind will reinforce biases against minorities in software.

Accessibility and inclusiveness are very hard to automate. No amount of checklists and tests in CI can replace feedback and testing from diverse user groups. Instead of listening blindly to automated tools, we encourage developing your empathetic gaze and listening to diverse feedback.

!!! Tip
    **Accessibility and inclusiveness are a shift in how you perceive and take into account otherness through your building processes, not a task to be done.**


### Disabled people are the real experts on accessibility

We cannot replace the perspectives of people with disabilities simply by reading about them or running a series of automated tests. We highly encourage recruiting people from diverse backgrounds in your team. The whole project will benefit from varying perspectives and it could help to leverage against systemic exclusion and hiring discriminations which affect minorities.

!!! Quote "Ashley Shew, *[Against Technoableism, Rethinking Who Needs Improvement](https://wwnorton.com/books/9781324036661)*"
    Disabled people are “the real experts” (the title of Michelle Sutton’s 2015 edited volume about and authored by autistic people) when it comes to technology and disability. We use technologies. We also reject them, grapple with them, or repurpose them. The views on technology we get from listening to disabled people often look very different from those of people educated in the medical and “helping” professions.

As we need to embrace diversity, it is crucial to fight a natural urge of all software creators: the will to personally find, design, and implement the solution to every problem. There is no one solution, and if there were, you would probably not be the one to find it. Your role as a software builder is to reach out to the real accessibility experts: those who rely on accessibility and experience its flaws every day, i.e. people with disabilities. Therefore, rather than trying to produce a "perfectly accessible" and inclusive product, we would rather suggest to try and make the main features as inclusive as possible and then get feedback from diverse users on what are their main issues with your software are.

This does not mean either that your expertise is useless if you are not experiencing the discriminations for which you are assessing your products. As you know the product you are building and what experience you are aiming for, you - as a product engineer, designer, or even developer - will be necessary to understanding what can be enhanced.

!!! Tip
    **We encourage following this motto: "nothing about them without them"**

### There isn't one *"accessible and inclusive design"*

While implementation plays an important role in the inclusiveness, and especially the accessibility of applications, the designers and product managers hold an important responsibility in the process of building an experience that will resonate and be welcoming to the widest range of users possible.

Product design documents, including specifications, user stories and prototypes act as the team’s compass for delivering products. That is why having inclusiveness in mind from the design is absolutely essential. You don’t ever have to “make this feature accessible” if it is built from the ground up with inclusiveness in mind.

Moreover, human experiences are complex and evolving as they always emerge from intersections of those characteristics. Consequently, building an inclusive app is all about staying up to date and actively open to feedback, knowing that we can never reach perfect inclusiveness while doing our best to get there.

!!! Tip
    **People are diverse, solutions to their needs too. Experiment, fail, get feedback, improve and nurture empathy!**

### Accessible code is good code

Bad accessibility can often be a symptom of flawed code. Accessibility and inclusiveness in programming have one key benefit: making you think twice about your code. Stumbling into an accessibility issue might mean that you could be doing something better in a different way.

You code can be good but will likely never be as robust as one iterated upon by a community of developers or a big company. Therefore, before implementing anything, check rigorously that your framework (or a library) doesn’t provide a tool that would meet most of your needs.

!!! Tip
    **Your code cannot be good without being accessible and if it's not accessible, it's probably hiding something more.**

### The Quick Inclusiveness check

Before submitting a commit or reviewing it, you can also use a template of a checklist containing the main elements to be sounded and share it with your team. We provide you with our own accessibility checklist template. Feel free to iterate upon it and to contribute with your enhancements on [this repository](https://github.com/Page-and-Maxence/accessibility-and-inclusiveness).

Remember: this **should not** be seen as a way to make your UI accessible, but rather to be sure you commit won't break any existing accessibility that was implemented. For new features, it is essential to design the UI with accessibility in mind from the very start of the process.

![Diagram showing an "A very basic accessibility checklist not to break anything when committing. Did you change/create a UI component? If no: skip to the question about data manipulation. Can you access it in a practical way with your keyboard or VoiceOver/TalkBack alone? If no: Fix it! All elements should be accessible without a mouse. Most users would expect the navigation to take place using TAB and BACKTAB. Arrows are also useful inside of lists. A top bar would typically be accessible with ALT. Shortcuts can make this navigation smoother. Are all information and labels properly transcribed using a screen reader? If no: Fix it! You can test this using your system screen reader on the settings or NVDA on Windows. You can then navigate through the app and hear if the labels are relevant. All information like the state of a component or wether it's selected must be transcribed. Expect to provide in your code.- A name for the element - A description of its effect - its role (for example static text or button). Does it work with different text scaling? - If no: Fix it! Most operating systems have text scaling options.  Some apps have their own too. Check if your UI isn't cropped by changing the size of the font. Try it for smaller and for bigger text. Did you affect another component? - If yes: repeat the previous questions for the other component Is the data manipulated in your code easily accessible from UI components? - If no: Make functions in  your API that allow  UI components to access relevant information. For example, the time of a message is often in a separated component from the message itself but the accessibility label of this message could need access to the date where it was sent. Does it work well for all languages? (including non UTF8 and RTL ones )? - If no: Fix it! Some languages like Greek are often not encoded in UTF8. Be sure to account for them. Also check that RTL (right to left) languages like Arabic displays correctly. To test this, you can use parts of local newspapers as placeholders! Does it has elements showing cultural significance? - If no: You are good to go! - If yes: Does it enable people from various cultural background to feel represented? - If you for no: Fix it! For example, a picture of a cheeseburger or a pizza as an illustration for food will only enable a certain demographic of users to feel represented. Having separate field for first and last name will not allow users from certain cultures to use the app properly. The only way to try and make our application more inclusive is to show it to people from varied background ans ask them about their needs to use it properly. - If you hope yes: You are good to go!"](resources/d-programming-inclusive-and-accessible-software/inclusivenessChecklist.png)

You can modify it for your needs by [downloading this file](resources/d-programming-inclusive-and-accessible-software/quickInclusivenessCheck.excalidraw) and opening it in [excalidraw](https://excalidraw.com/).

## Perspectives

This training is already coming to a close. - If you are doing this training collectively, you are not *quite yet* finished as their is still two modules awaiting you. -

We dearly hope it was somewhat useful to you. We feel that there is a lack of resources that dive deep into technical consideration while reflecting on them through a systemic gaze, and placing empathy as a core element of decision-making. We hope this training helps on your path to inclusiveness. As we said multiple time, we are not experts, only people trying to help. If you have expertise on those topics and feel like helping, **please contribute**. You can also [star the repository](https://github.com/Page-and-Maxence/accessibility-and-inclusiveness). If you have any question, feel free to contact us!

## Bibliography & useful resources

=== "Design"

    ### Tools

    [Color Contrast Checker & Accessibility Checker | Figma](https://www.figma.com/color-contrast-checker/?background=ffffff&foreground=b50202)

    [WillowTree. Contrast Plugin](https://www.figma.com/community/plugin/748533339900865323/contrast)

    ### Articles, book and masterclasses

    [Winner, Langdon. *Do artifacts have politics?*, 1980. Daedalus 109 (1): pp. 121--136.](https://faculty.cc.gatech.edu/~beki/cs4001/Winner.pdf)

    [Apple Human Interface Guidelines: *Accessibility*](https://developer.apple.com/design/human-interface-guidelines/accessibility)

    [Apple. *Principles of Inclusive App Design*](https://developer.apple.com/videos/play/wwdc2025/316)

    [Whitaker, Rob (2020). *Developing Inclusive Mobile Apps: Building Accessible Apps for iOS and Android*, Apress Berkley.](https://doi.org/10.1007/978-1-4842-5814-9)

    [Apple. *The practice of inclusive design*](https://developer.apple.com/videos/play/wwdc2021/10275/)

    [Apple. *The process of inclusive design*](https://developer.apple.com/videos/play/wwdc2021/10304/)

    [The A11Y Project. *Software, books, blogs, online tools, etc.*](https://www.a11yproject.com/resources/)

    [McRuer Robert. *Crip Theory : Cultural Signs of Queerness and Disability*, 1966](https://archive.org/details/criptheorycultur0000mcru)

    [Microsoft. *Accessibility (Design basics)*](https://learn.microsoft.com/en-us/windows/win32/uxguide/inter-accessibility)

=== "Politics"

    ### FOSS in the army

    [U.S. Department of Defense. *Use of Free and Open-source software (FOSS) in the U.S. Department of Defense*, 2003](https://dodcio.defense.gov/Portals/0/Documents/FOSS/dodfoss_pdf.pdf)

    [U.S. Department of Defense. *DoD Open Source Software FAQ*](https://dodcio.defense.gov/open-source-software-faq/)

    [Capt. Noe Lorona. *Leveraging Free and Open-Source Software on the battlefield.*, 2024](https://www.army.mil/article/276750/the_power_of_foss)

    ### FOSS and capitalism

    [Teemu Mikkonen, Tere Vadén, Niklas Vainio. *Open source developers and the ethics of  capitalism*, 2007](https://firstmonday.org/ojs/index.php/fm/article/view/1623/1538)

    [Böhm Mirko, *Economics of Open Source* 2022](https://academic.oup.com/book/44727/chapter/378967711?login=false)

    [Ross Daniel. *The Place of Free and Open Source Software in the Social Apparatus of Accumulation*, 2013](https://guilfordjournals.com/doi/abs/10.1521/siso.2013.77.2.202)
    [Josh Lerner, Parag A. Pathak, Jean Tirole. *The Dynamics of Open-Source Contributors*](https://economics.mit.edu/sites/default/files/publications/Dynamics%20of%20Open%20Source.pdf)

    [Manuel Hoffmann, Frank Nagle, Yanuo Zhou. *The Value of Open Source Software*](https://www.hbs.edu/ris/Publication%20Files/24-038_51f8444f-502c-4139-8bf2-56eb4b65c58a.pdf)

    ### Inclusion in software

    [The Chartered Institute for IT, *Nearly 90,000 disabled people are 'missing' from tech industry, says professional body*. 2024](https://www.bcs.org/articles-opinion-and-research/nearly-90-000-disabled-people-are-missing-from-tech-industry-says-professional-body/)

    [Shew Ashley, *Against Technoableism: rethinking who needs improvement*. 2023](https://wwnorton.com/books/9781324036661)

    [Nathan L. Ensmenger. *The computer boys take over*, 2010](https://www.jstor.org/stable/j.ctt5hhjdh)

    [Goodin Dan, *“Microsoft has simply given us no other option,” Signal says as it blocks Windows Recall* 2025](https://arstechnica.com/security/2025/05/signal-resorts-to-weird-trick-to-block-windows-recall-in-desktop-app/)

    [Sarah Gooding, *Accessibility Advocates Sign Open Letter Urging People Not To Use AccesiBe and Other Overlay Products*. 2021](https://wptavern.com/accessibility-advocates-sign-open-letter-urging-people-not-to-use-accesibe-and-other-overlay-products)

    Blondy Marie Herminie *L’idéologie libertaire des pionniers d’internet : Contradictions d’un humanisme industriel*, 2025

=== "Desktop"

    ### Open source desktop app with good accessibility

    [BearWare. *TeamTalk5*](https://github.com/BearWare/TeamTalk5)

    [Signal. *Signal*](https://github.com/signalapp/Signal-Desktop)

    ### Tools

    [NVDA. *NVDA*](https://www.nvaccess.org/download/)

    [FreedomScientific. *Jaws*](https://www.freedomscientific.com/products/software/jaws/)

    [Apple. *VoiceOver*](https://www.apple.com/voiceover/info/guide/_1121.html)

    [Microsoft. *Accessibility Insights for Windows*](https://accessibilityinsights.io/)

    [WebAIM. *Wave*](https://wave.webaim.org/)

    [Apple. *Accessibility Inspector*](https://developer.apple.com/documentation/accessibility/accessibility-inspector)

    ## Articles and videos

    [Expand the room. *Accessibility Testing Tools Overview*](https://www.youtube.com/watch?v=yV_ENQZq3fs&t=418s)

    [Deque. *NVDA Keyboard Shortcuts*](https://dequeuniversity.com/screenreaders/nvda-keyboard-shortcuts)

    [Challenge Solutions. *Screen Reader Comparison*](https://www.youtube.com/watch?v=9_K5-4ngDtE)

    [VLE Guru *Introduction to Keyboard Navigation and Accessibility*](https://www.youtube.com/watch?v=FvpUNiB-2T0)

    [Expand the room. *How to Check Web Accessibility with a Screen Reader and Keyboard*](https://www.youtube.com/watch?v=yV_ENQZq3fs&t=418s)

    [Chrome for Developers. *Screen Reader Basics: NVDA -- A11ycasts #09 *](https://www.youtube.com/watch?v=Jao3s_CwdRU)

    [Andreea-QA. *Accessibility Testing on Windows Apps*, 2023.](https://medium.com/testing-thoughts/accessibility-testing-on-windows-apps-6567906bb24f)

    [The A11Y Project. *Software, books, blogs, online tools, etc.*](https://www.a11yproject.com/resources/)

    ### Documentation

    [Microsoft. *Accessibility overview*](https://learn.microsoft.com/en-us/windows/apps/design/accessibility/accessibility-overview#main)

    [Microsoft. *Accessibility (Design basics)*](https://learn.microsoft.com/en-us/windows/win32/uxguide/inter-accessibility)

    [Direction Interministérielle du Numérique. *RGAA-APPS : le guide officiel pour des applications accessibles*](https://disic.github.io/rgaa-apps/)

    [Direction Interministérielle du Numérique.*Guide du concepteur RGAA 3*](https://disic.github.io/guide-concepteur/)

    [Oracle's official JavaFX API](https://docs.oracle.com/javase/8/javafx/api/overview-summary.html)

    [Jonathan Giles (Oracle), *The JavaFX Accessibility API* (slides)](https://download.jonathangiles.net/downloads/presentations/2015/Accessibility.pdf)


=== "Mobile"

    ### Introduction to tools

    [Apple. *WWDC21 Challenge: VoiceOver Maze*](https://developer.apple.com/documentation/accessibility/wwdc21_challenge_voiceover_maze)

    [Senjam, S. S., Manna, S., & Bascaran, C. *Smartphones-Based Assistive Technology: Accessibility Features and Apps for People with Visual Impairment, and its Usage, Challenges, and Usability Testing*, 2021](https://www.tandfonline.com/doi/full/10.2147/OPTO.S336361?scroll=top&needAccess=true)

    ### Documentation

    [Direction Interministérielle du Numérique. *RGAA-APPS : le guide officiel pour des applications accessibles*](https://disic.github.io/rgaa-apps/)

    [Direction Interministérielle du Numérique.*Guide du concepteur RGAA 3*](https://disic.github.io/guide-concepteur/)

    [Direction Interministérielle du Numérique.*Référentiel spécifique aux plateformes mobiles/tactiles*](https://github.com/DISIC/referentiel-mobile-tactile)

    [Orange. *Accessibility Guidelines*](https://a11y-guidelines.orange.com/en/)

    [Appt. *A guide for making apps accessible*](https://appt.org/en/)

    [Whitaker, Rob. *Developing Inclusive Mobile Apps: Building Accessible Apps for iOS and Android*](https://link.springer.com/book/10.1007/978-1-4842-5814-9)

    ### Articles

    [Brooke Nelson Alexander. *25 Smartphone Accessibility Settings You Need to Know About*](https://www.rd.com/article/accessibility-settings/)

    [Senjam, S. S., Manna, S., & Bascaran, C. *Smartphones-Based Assistive Technology: Accessibility Features and Apps for People with Visual Impairment, and its Usage, Challenges, and Usability Testing*, 2021.](https://www.tandfonline.com/doi/full/10.2147/opto.s336361#abstract)

    ### Apple

    [CVS Health. *Accessibility Annotation Kit for iOS*](https://www.figma.com/community/file/1331647574396908226/accessibility-annotation-kit-for-ios)

    ### Android

    [Android. *Principles for improving app accessibility*](https://developer.android.com/guide/topics/ui/accessibility/principles?hl=en)


=== "WebApp"

    ### Articles

    [W3C. *How to Meet WCAG (Quick Reference)*](https://www.w3.org/WAI/WCAG22/quickref/)

    [inclusive-components.design. *Inclusive components project*](https://inclusive-components.design/#components)

    [Cristian Díaz. *A Guide To Keyboard Accessibility: HTML And CSS (Part 1)*](https://www.smashingmagazine.com/2022/11/guide-keyboard-accessibility-html-css-part1/)

    [ExpandTheRoom. *How to Check Web Accessibility with a Screen Reader and Keyboard*](https://www.youtube.com/watch?v=yV_ENQZq3fs&t=418s)

    [Heydon Pickering. *Building Accessible Menu Systems*](https://www.smashingmagazine.com/2017/11/building-accessible-menu-systems/)

    [inclusive-components.design. *Menus & Menu Buttons*](https://inclusive-components.design/menus-menu-buttons/)

    [Cristian Díaz. *A Guide To Keyboard Accessibility: JavaScript (Part 2)*](https://www.smashingmagazine.com/2022/11/guide-keyboard-accessibility-javascript-part2/)

    [W3C. *WCAG 2 Overview*](https://www.w3.org/WAI/standards-guidelines/wcag/)

    [Microsoft. *Test accessibility using Lighthouse*](https://learn.microsoft.com/en-ca/microsoft-edge/devtools/accessibility/lighthouse)

    ### Testing Software

    [Wave](https://wave.webaim.org/)

    [Lighthouse](https://learn.microsoft.com/en-us/microsoft-edge/devtools/lighthouse/lighthouse-tool?source=recommendations)

    [Axe](https://www.deque.com/axe/)

=== "Development Pipeline"

    [Barrell Dylan. *Agile Accessibility Handbook*](https://accessibility.deque.com/agile-accessibility-handbook)

=== "Qt"

    [Qt. *Qt's documentation of QAccessible Class*](https://doc.qt.io/qt-6/qaccessible.html#Role-enum)

    [Qt. *Qt's documentation of QAccessible::Role*](https://doc.qt.io/qt-6/qaccessible.html?search=item#Role-enum)

    [Qt. *Qt's documentation of KeyNavigation class*](https://doc.qt.io/qt-6/qml-qtquick-keynavigation.html#details)

    [Qt. *Qt's documentation of QAccessibleInterface Class*](https://doc.qt.io/qt-6/qaccessibleinterface.html)

