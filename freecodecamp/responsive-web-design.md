# Applied Visula Design

 The `opacity` property in CSS is used to adjust the opacity, or conversely, the transparency for an item. \(0-1\) 

## Text

### Align

Text is often a large part of web content. CSS has several options for how to align it with the `text-align` property.

`text-align: justify;` causes all lines of text except the last line to meet the left and right edges of the line box.

`text-align: center;` centers the text

`text-align: right;` right-aligns the text

And `text-align: left;` \(the default\) left-aligns the text.



To make text bold, you can use the `strong` tag. This is often used to draw attention to text and symbolize that it is important. With the `strong` tag, the browser applies the CSS of `font-weight: bold;` to the element.



To underline text, you can use the `u` tag. This is often used to signify that a section of text is important, or something to remember. With the `u` tag, the browser applies the CSS of `text-decoration: underline;` to the element.

  
 To emphasize text, you can use the `em` tag. This displays text as italicized, as the browser applies the CSS of `font-style: italic;` to the element.



 To strikethrough text, which is when a horizontal line cuts across the characters, you can use the `s` tag. It shows that a section of text is no longer valid. With the `s` tag, the browser applies the CSS of `text-decoration: line-through;` to the element.

### color

**Adjust the background-color Property of Text**

Instead of adjusting your overall background or the color of the text to make the foreground easily readable, you can add a `background-color` to the element holding the text you want to emphasize. This challenge uses `rgba()` instead of `hex` codes or normal `rgb()`.

> rgba stands for:  
>   r = red  
>   g = green  
>   b = blue  
>   a = alpha/level of opacity

The RGB values can range from 0 to 255. The alpha value can range from 1, which is fully opaque or a solid color, to 0, which is fully transparent or clear. `rgba()` is great to use in this case, as it allows you to adjust the opacity. This means you don't have to completely block out the background.

### Text Transform

The `text-transform` property in CSS is used to change the appearance of text. It's a convenient way to make sure text on a webpage appears consistently, without having to change the text content of the actual HTML elements.

The following table shows how the different `text-transform`values change the example text "Transform me".

| Value | Result |
| :--- | :--- |
| `lowercase` | "transform me" |
| `uppercase` | "TRANSFORM ME" |
| `capitalize` | "Transform Me" |
| `initial` | Use the default value |
| `inherit` | Use the `text-transform` value from the parent element |
| `none` | **Default:** Use the original text |



 The `font-weight` property sets how thick or thin characters are in a section of text. \(number\)

 CSS offers the `line-height` property to change the height of each line in a block of text. As the name suggests, it changes the amount of vertical space that each line of text gets.



## More

 **Add a box-shadow to a Card-like Element**

The `box-shadow` property applies one or more shadows to an element.

The `box-shadow` property takes values for

* `offset-x` \(how far to push the shadow horizontally from the element\),
* `offset-y` \(how far to push the shadow vertically from the element\),
* `blur-radius`,
* `spread-radius` and
* `color`, in that order.

The `blur-radius` and `spread-radius` values are optional.

Multiple box-shadows can be created by using commas to separate properties of each `box-shadow` element.

Here's an example of the CSS to create multiple shadows with some blur, at mostly-transparent black colors:

```text
box-shadow: 0 10px 20px rgba(0,0,0,0.19), 0 6px 6px rgba(0,0,0,0.23);
```

## Anchors

### Hover

This challenge will touch on the usage of pseudo-classes. A pseudo-class is a keyword that can be added to selectors, in order to select a specific state of the element.

For example, the styling of an anchor tag can be changed for its hover state using the `:hover` pseudo-class selector. Here's the CSS to change the `color` of the anchor tag to red during its hover state:

```text
a:hover {
  color: red;
}
```

##  **Change an Element's Relative Position**

CSS treats each HTML element as its own box, which is usually referred to as the CSS Box Model. Block-level items automatically start on a new line \(think headings, paragraphs, and divs\) while inline items sit within surrounding content \(like images or spans\). The default layout of elements in this way is called the normal flow of a document, but CSS offers the position property to override it.

When the position of an element is set to `relative`, it allows you to specify how CSS should move it _relative_ to its current position in the normal flow of the page. It pairs with the CSS offset properties of `left` or `right`, and `top` or `bottom`. These say how many pixels, percentages, or ems to move the item _away_ from where it is normally positioned. The following example moves the paragraph 10 pixels away from the bottom:

```text
p {
  position: relative;
  bottom: 10px;
}
```

Changing an element's position to relative does not remove it from the normal flow - other elements around it still behave as if that item were in its default position.

**Note:** Positioning gives you a lot of flexibility and power over the visual layout of a page. It's good to remember that no matter the position of elements, the underlying HTML markup should be organized and make sense when read from top to bottom. This is how users with visual impairments \(who rely on assistive devices like screen readers\) access your content.

###  **Move a Relatively Positioned Element with CSS Offsets**

The CSS offsets of `top` or `bottom`, and `left` or `right` tell the browser how far to offset an item relative to where it would sit in the normal flow of the document. You're offsetting an element away from a given spot, which moves the element away from the referenced side \(effectively, the opposite direction\). As you saw in the last challenge, using the `top` offset moved the `h2` downwards. Likewise, using a `left` offset moves an item to the right.

###  **Lock an Element to its Parent with Absolute Positioning**

The next option for the CSS `position` property is `absolute`, which locks the element in place relative to its parent container. Unlike the `relative` position, this removes the element from the normal flow of the document, so surrounding items ignore it. The CSS offset properties \(top or bottom and left or right\) are used to adjust the position.

One nuance with absolute positioning is that it will be locked relative to its closest _positioned_ ancestor. If you forget to add a position rule to the parent item, \(this is typically done using `position: relative;`\), the browser will keep looking up the chain and ultimately default to the `body` tag.

###  **Lock an Element to the Browser Window with Fixed Positioning**

The next layout scheme that CSS offers is the `fixed` position, which is a type of absolute positioning that locks an element relative to the browser window. Similar to absolute positioning, it's used with the CSS offset properties and also removes the element from the normal flow of the document. Other items no longer "realize" where it is positioned, which may require some layout adjustments elsewhere.

One key difference between the `fixed` and `absolute` positions is that an element with a fixed position won't move when the user scrolls.

### **Push Elements Left or Right with the float Property**

 The next positioning tool does not actually use `position`, but sets the `float` property of an element. Floating elements are removed from the normal flow of a document and pushed to either the `left` or `right` of their containing parent element. It's commonly used with the `width` property to specify how much horizontal space the floated element requires.

### **z-index Property Change the Position of Overlapping Elements with the** 

 When elements are positioned to overlap \(i.e. using `position: absolute | relative | fixed | sticky`\), the element coming later in the HTML markup will, by default, appear on the top of the other elements. However, the `z-index` property can specify the order of how elements are stacked on top of one another. It must be an integer \(i.e. a whole number and not a decimal\), and higher values for the `z-index` property of an element move it higher in the stack than those with lower values. **\(not decimal\)**

### **Center an Element Horizontally Using the margin Property**

Another positioning technique is to center a block element horizontally. One way to do this is to set its `margin` to a value of auto.

This method works for images, too. Images are inline elements by default, but can be changed to block elements when you set the `display` property to `block`.

## **Colors**

**Learn about Complementary Colors**

Color theory and its impact on design is a deep topic and only the basics are covered in the following challenges. On a website, color can draw attention to content, evoke emotions, or create visual harmony. Using different combinations of colors can really change the look of a website, and a lot of thought can go into picking a color palette that works with your content.

The color wheel is a useful tool to visualize how colors relate to each other - it's a circle where similar hues are neighbors and different hues are farther apart. When two colors are opposite each other on the wheel, they are called complementary colors. They have the characteristic that if they are combined, they "cancel" each other out and create a gray color. However, when placed side-by-side, these colors appear more vibrant and produce a strong visual contrast.

Some examples of complementary colors with their hex codes are:

> red \(\#FF0000\) and cyan \(\#00FFFF\)  
> green \(\#00FF00\) and magenta \(\#FF00FF\)  
> blue \(\#0000FF\) and yellow \(\#FFFF00\)

This is different than the outdated RYB color model that many of us were taught in school, which has different primary and complementary colors. Modern color theory uses the additive RGB model \(like on a computer screen\) and the subtractive CMY\(K\) model \(like in printing\). Read [here](https://en.wikipedia.org/wiki/Color_model) for more information on this complex subject.

There are many color picking tools available online that have an option to find the complement of a color.

**Note:** Using color can be a powerful way to add visual interest to a page. However, color alone should not be used as the only way to convey important information because users with visual impairments may not understand that content. This issue will be covered in more detail in the Applied Accessibility challenges.



**Learn about Tertiary ColorsPassed**

Computer monitors and device screens create different colors by combining amounts of red, green, and blue light. This is known as the RGB additive color model in modern color theory. Red \(R\), green \(G\), and blue \(B\) are called primary colors. Mixing two primary colors creates the secondary colors cyan \(G + B\), magenta \(R + B\) and yellow \(R + G\). You saw these colors in the Complementary Colors challenge. These secondary colors happen to be the complement to the primary color not used in their creation, and are opposite to that primary color on the color wheel. For example, magenta is made with red and blue, and is the complement to green.

Tertiary colors are the result of combining a primary color with one of its secondary color neighbors. For example, within the RGB color model, red \(primary\) and yellow \(secondary\) make orange \(tertiary\). This adds six more colors to a simple color wheel for a total of twelve.

There are various methods of selecting different colors that result in a harmonious combination in design. One example that can use tertiary colors is called the split-complementary color scheme. This scheme starts with a base color, then pairs it with the two colors that are adjacent to its complement. The three colors provide strong visual contrast in a design, but are more subtle than using two complementary colors.

Here are three colors created using the split-complement scheme:

| Color | Hex Code |
| :--- | :--- |
| orange | \#FF7F00 |
| cyan | \#00FFFF |
| raspberry | \#FF007F |

 **Adjust the Color of Various Elements to Complementary Colors**

\*\*\*\*

**Adjust the Hue of a Color**

Colors have several characteristics including hue, saturation, and lightness. CSS3 introduced the `hsl()` property as an alternative way to pick a color by directly stating these characteristics.

**Hue** is what people generally think of as 'color'. If you picture a spectrum of colors starting with red on the left, moving through green in the middle, and blue on right, the hue is where a color fits along this line. In `hsl()`, hue uses a color wheel concept instead of the spectrum, where the angle of the color on the circle is given as a value between 0 and 360.

**Saturation** is the amount of gray in a color. A fully saturated color has no gray in it, and a minimally saturated color is almost completely gray. This is given as a percentage with 100% being fully saturated.

**Lightness** is the amount of white or black in a color. A percentage is given ranging from 0% \(black\) to 100% \(white\), where 50% is the normal color.

Here are a few examples of using `hsl()` with fully-saturated, normal lightness colors:

| Color | HSL |
| :--- | :--- |
| red | hsl\(0, 100%, 50%\) |
| yellow | hsl\(60, 100%, 50%\) |
| green | hsl\(120, 100%, 50%\) |
| cyan | hsl\(180, 100%, 50%\) |
| blue | hsl\(240, 100%, 50%\) |
| magenta | hsl\(300, 100%, 50%\) |

**Adjust the Tone of a Color**

The `hsl()` option in CSS also makes it easy to adjust the tone of a color. Mixing white with a pure hue creates a tint of that color, and adding black will make a shade. Alternatively, a tone is produced by adding gray or by both tinting and shading. Recall that the 's' and 'l' of `hsl()` stand for saturation and lightness, respectively. The saturation percent changes the amount of gray and the lightness percent determines how much white or black is in the color. This is useful when you have a base hue you like, but need different variations of it.



### **Create a Gradual CSS Linear Gradient**

Applying a color on HTML elements is not limited to one flat hue. CSS provides the ability to use color transitions, otherwise known as gradients, on elements. This is accessed through the `background` property's `linear-gradient()` function. Here is the general syntax:

```text
background: linear-gradient(gradient_direction, color 1, color 2, color 3, ...);
```

The first argument specifies the direction from which color transition starts - it can be stated as a degree, where `90deg` makes a horizontal gradient \(from left to right\) and `45deg` makes a diagonal gradient \(from bottom left to top right\). The following arguments specify the order of colors used in the gradient.

Example:

```text
background: linear-gradient(90deg, red, yellow, rgb(204, 204, 255));
```

 **CSS Linear Gradient to Create a Striped Element**

The `repeating-linear-gradient()` function is very similar to `linear-gradient()` with the major difference that it repeats the specified gradient pattern. `repeating-linear-gradient()` accepts a variety of values, but for simplicity, you'll work with an angle value and color stop values in this challenge.

The angle value is the direction of the gradient. Color stops are like width values that mark where a transition takes place, and are given with a percentage or a number of pixels.

In the example demonstrated in the code editor, the gradient starts with the color `yellow` at 0 pixels which blends into the second color `blue` at 40 pixels away from the start. Since the next color stop is also at 40 pixels, the gradient immediately changes to the third color `green`, which itself blends into the fourth color value `red` as that is 80 pixels away from the beginning of the gradient.

For this example, it helps to think about the color stops as pairs where every two colors blend together.

```text
0px [yellow -- blend -- blue] 40px [green -- blend -- red] 80px
```

If every two color stop values are the same color, the blending isn't noticeable because it's between the same color, followed by a hard transition to the next color, so you end up with stripes.

**Create Texture by Adding a Subtle Pattern as a Background Image**

One way to add texture and interest to a background and have it stand out more is to add a subtle pattern. The key is balance, as you don't want the background to stand out too much, and take away from the foreground. The `background` property supports the `url()` function in order to link to an image of the chosen texture or pattern. The link address is wrapped in quotes inside the parentheses.

## Transform

**Scale Property to Change the Size of an Element**

To change the scale of an element, CSS has the `transform` property, along with its `scale()` function. The following code example doubles the size of all the paragraph elements on the page:

```text
p {
  transform: scale(2);
}
```

 **skewX to Skew an Element Along the X-Axis**

The next function of the `transform` property is `skewX()`, which skews the selected element along its X \(horizontal\) axis by a given degree.

The following code skews the paragraph element by -32 degrees along the X-axis.

```text
p {
  transform: skewX(-32deg);
}
```

## **Create a Graphic Using CSS**

By manipulating different selectors and properties, you can make interesting shapes. One of the easier ones to try is a crescent moon shape. For this challenge you need to work with the `box-shadow` property that sets the shadow of an element, along with the `border-radius` property that controls the roundness of the element's corners.

You will create a round, transparent object with a crisp shadow that is slightly offset to the side - the shadow is actually going to be the moon shape you see.

In order to create a round object, the `border-radius` property should be set to a value of 50%.

You may recall from an earlier challenge that the `box-shadow` property takes values for `offset-x`, `offset-y`, `blur-radius`, `spread-radius` and a color value in that order. The `blur-radius` and `spread-radius` values are optional.



