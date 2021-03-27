# CSS

## Basic

### CSS selectors

At the top of your code, create a `style` block like this: 

Inside that style block, you can create a CSS selector for all `h2` elements. For example, if you wanted all `h2` elements to be red, you would add a style rule that looks like this:

```css
<style>
  h2 {
    color: red;
  }
</style>
```

### **CSS Class to Style an Element**

Classes are reusable styles that can be added to HTML elements.

Here's an example CSS class declaration:

```css
<style>
  .blue-text {
    color: blue;
  }
</style>
```

You can see that we've created a CSS class called `blue-text` within the `<style>` tag. You can apply a class to an HTML element like this: `<h2 class="blue-text">CatPhotoApp</h2>`.

Remember that you can apply multiple classes to an element using its `class` attribute, by separating each class name with a space. For example:

```markup
<img class="class1 class2">
```

**Note:** It doesn't matter which order the classes are listed in the HTML element.

However, the order of the `class` declarations in the `<style>` section is what is important. The second declaration will always take precedence over the first. 

### Id

```css
#cat-photo-element {
  background-color: green;
}
```

 However, an `id` is not reusable and should only be applied to one element. An `id` also has a higher specificity \(importance\) than a class so if both are applied to the same element and have conflicting styles, the styles of the `id` will be applied.

This is Priotarized when styles added.

**!important &gt; Inline &gt; Id &gt; Class -&gt; Style overriding**

 **Attribute Selectors to Style Elements**

```css
[type='radio'] {
  margin: 20px 0px 20px 0px;
}
```

## Variables

To create a CSS variable, you just need to give it a name with two hyphens in front of it and assign it a value like this:

```css
--penguin-skin: gray;
```

**Using it**

```css
background: var(--penguin-skin);
```

and a value can be assigned again

```css
--penguin-skin: white;
```

**Fallback Value**

```css
background: var(--penguin-skin, black);
```

In class we can use another background with color we need before adding variable.

### Root

```css
:root {
    --variables: value;
}
```

To make use of inheritance, CSS variables are often defined in the :root element.

`:root` is a pseudo-class selector that matches the root element of the document, usually the `html` element. By creating your variables in `:root`, they will be available globally and can be accessed from any other selector in the style sheet.

### **Use a media query to change a variable**

CSS Variables can simplify the way you use media queries.

For instance, when your screen is smaller or larger than your media query break point, you can change the value of a variable, and it will apply its style wherever it is used.

In the `:root` selector of the `media query`, change it so `--penguin-size` is redefined and given a value of `200px`. Also, redefine `--penguin-skin` and give it a value of `black`. Then resize the preview to see this change in action.

## Color

```markup
<h2 style="color: blue;">CatPhotoApp</h2>

background-color: green;

```

Note that it is a good practice to end inline `style` declarations with a `;` .

```text
#00FF00
#0F0
rgb(0, 0, 0)
```

  


## Fonts

```text
font-size: 30px;
font-family: sans-serif;
```

In addition to specifying common fonts that are found on most operating systems, we can also specify non-standard, custom web fonts for use on our website. There are many sources for web fonts on the Internet.

To import a Google Font, you can copy the font's URL from the Google Fonts library and then paste it in your HTML. For this challenge, we'll import the `Lobster` font. To do this, copy the following code snippet and paste it into the top of your code editor \(before the opening `style` element\):

```text
<link href="https://fonts.googleapis.com/css?family=Lobster" rel="stylesheet" type="text/css">
```

Now you can use the `Lobster` font in your CSS by using `Lobster` as the FAMILY\_NAME as in the following example:

```text
font-family: FAMILY_NAME, GENERIC_NAME;
ex:
font-family: Lobster, monospace;
```

The GENERIC\_NAME is optional, and is a fallback font in case the other specified font is not available. 

Family names are **case-sensitive** and need to be wrapped in quotes if there is a space in the name. For example, you need quotes to use the `"Open Sans"` font, but not to use the `Lobster` font.

**Generic Name \(Specify How Fonts Should Degrade\)**

There are several default fonts that are available in all browsers. These generic font families include `monospace`, `serif` and `sans-serif`

When one font isn't available, you can tell the browser to "degrade" to another font.Generic font family names are **not case-sensitive**. Also, they do not need quotes because they are CSS keywords.

## Size

can use `px` or `%` to specify.

### width

## Borders

 CSS borders have properties like `style`, `color` and `width`.

```markup
<style>
  .thin-red-border {
    border-color: red;
    border-width: 5px;
    border-style: solid;
    border-radius: 10px;
  }
</style>
```

Border-radius `50%` will give circle

Space Around HTML elements

You may have already noticed this, but all HTML elements are essentially little rectangles.

Three important properties control the space that surrounds each HTML element: `padding`, `border`, and `margin`.

#### Padding

An element's `padding` controls the amount of space between the element's content and its `border`.

 CSS allows you to control the `padding` of all four individual sides of an element with the `padding-top`, `padding-right`, `padding-bottom`, and `padding-left` properties.

 **Use Clockwise Notation to Specify the Padding of an Element**

```css
padding: 10px 20px 10px 20px;
```

These four values work like a clock: top, right, bottom, left,

#### Margin

An element's `margin` controls the amount of space between an element's `border` and surrounding elements.

 If you set an element's `margin` to a negative value, the element will grow larger.

 CSS allows you to control the `margin` of all four individual sides of an element with the `margin-top`, `margin-right`, `margin-bottom`, and `margin-left` properties.

 **Use Clockwise Notation to Specify the Margin of an Element**

```text
margin: 10px 20px 10px 20px;
```

These four values work like a clock: top, right, bottom, left



