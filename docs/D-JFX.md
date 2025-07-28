# ☕️ Inclusive programming with JavaFX

!!! Info "In this module"
    This module provides basic information and resources for accessibility with Java Fx.

**⛳️ Section**: *D. Programming inclusive and accessible software*

**👥 Audience**: JavaFX developers

**⏱️ Duration**: 10'

**📚 Prerequisites**: [👩‍💻 Inclusive code 101](D-ICO.md)

---

!!! Info
    As we are not Java developers and didn't get the chance to dive deep into JavaFX accessibility as of the time of writing, this module's content could be significantly improved. For now, this page will mainly redirect to useful resources we found along with some key takeaways. If you have experience with JavaFX accessibility and you feel like helping the project, [please contribute](https://github.com/alterity-git/building-inclusive-open-source-software).

## JavaFX's accessibility API

It has been approximately a decade that JavaFX have launched their full accessibility API. Nevertheless, when implementing accessibility using this framework, the first challenge you'll encounter will be to find documentation. While all the classes and methods are fully documented on [Oracle's official API](https://openjfx.io/javadoc/24/), there is no clear documentation page stating clearly what are the available accessibility features. Through this module, we'll cover some common accessibility needs and their JavaFX implementation.

### Understanding basic properties

Each JavaFX Node on your scenes have accessibility attributes which you can set to achieve the desired result.

- The [`accessibleRole`](https://openjfx.io/javadoc/24/javafx.graphics/javafx/scene/Node.html#accessibleRoleProperty()) gives information to assistive technologies so they can behave accordingly. There are [many roles possible](https://openjfx.io/javadoc/24/javafx.graphics/javafx/scene/AccessibleRole.htmll) from which you can choose for example `BUTTON`.
- The [`accessibleRoleDescription`](https://openjfx.io/javadoc/24/javafx.graphics/javafx/scene/Node.html#accessibleRoleDescriptionProperty()) can be used to override `accessibleRole`'s textual representation, which is read by the screen reader. This is useful, for example, if you have an element with the role `Button` that you would like the screen reader to call *"biscuit dispenser"*.
- The [`accessibleText`](https://openjfx.io/javadoc/24/javafx.graphics/javafx/scene/Node.html#accessibleRoleProperty()) should describe the content of the Node. For our example, the accessible text could read *"3 biscuits left"*. For some scenarios like for buttons, it might not be necessary to set it as labels will automatically be read out loud by screen readers if linked accordingly.
- The [`accessibleHelp`](https://openjfx.io/javadoc/24/javafx.graphics/javafx/scene/Node.html#accessibleHelpProperty) should be used to give contextual hints to help users understand where they are or what are the possible interactions with an element. For our previous example, this could read *"dispenses a biscuit when activated"*.
- The [`labelFor`](https://openjfx.io/javadoc/24/javafx.controls/javafx/scene/control/Label.html#labelForProperty()) property is used to link a label to an input (like a text field or a slider). This is not to be confused with an accessibility label as called in many other frameworks - the equivalent is `accessibleText` in JavaFX. It could for example be a (visual) label saying *"edit the biscuit dispenser's name"* next to an associated text field.

Each of theses properties can be retrieved or set using getAccessible{Property}(), setAccessible{Property}(AccessibleRole).

### Notifying assistive technologies about changes

By default, changes on elements might not be notified. To make sure they are, you can use the [`notifyAccessibleAttributeChanged(AccessibleAttribute attributes)`](https://openjfx.io/javadoc/24/javafx.controls/javafx/scene/control/Label.html#labelForProperty()). As explained in [Jonathan Giles' presentation of the JavaFX accessibility API for Oracle](https://download.jonathangiles.net/downloads/presentations/2015/Accessibility.pdf), the method can for example be called in an override of the `invalidated()` Node's method.

### Checking if an assistive technology is running

To adapt your app conditionally, depending on whether an assistive technology is running, you can use [Platform's `accessibilityActiveProperty`](https://openjfx.io/javadoc/24/javafx.graphics/javafx/application/Platform.html#accessibilityActiveProperty()).

### Making an element focusable

By default, some elements you provide in your UI might not be focusable. When relevant, to allow screen reader and keyboard users to focus an element, you use the [`setFocusTraversable(boolean value)`](https://openjfx.io/javadoc/24/javafx.graphics/javafx/scene/Node.html#setFocusTraversable(boolean)) property. Additionally, you can programmatically request input focus with [`requestFocus()`](https://openjfx.io/javadoc/24/javafx.graphics/javafx/scene/Node.html#setFocusTraversable(boolean)).

To adjust the order of traversal of elements, you can sort them accordingly in the parent panel of the scene builder.

### Customizing accessibility actions behavior

By overriding the [`executeAccessibleAction`](https://openjfx.io/javadoc/24/javafx.graphics/javafx/scene/Node.html#executeAccessibleAction(javafx.scene.AccessibleAction,java.lang.Object...)) method, it is possible to execute custom behaviors when the user triggers an action like `FIRE` or `EXPAND` using a screen reader. More rarely, this method can also be useful to execute accessibility actions programmatically on behalf of the user.

### Providing dynamic accessibility properties

One way of providing dynamic accessibility properties is by overriding the [`queryAccessibleAttribute`](https://openjfx.io/javadoc/24/javafx.controls/javafx/scene/control/skin/MenuButtonSkin.html#queryAccessibleAttribute(javafx.scene.AccessibleAttribute,java.lang.Object...)) method and providing custom computed values for some cases of the enum, and calling the super by default.

## Resources

[Oracle's official JavaFX API](https://openjfx.io/javadoc/24/)

[Jonathan Giles (Oracle), *The JavaFX Accessibility API* (slides)](https://download.jonathangiles.net/downloads/presentations/2015/Accessibility.pdf)
