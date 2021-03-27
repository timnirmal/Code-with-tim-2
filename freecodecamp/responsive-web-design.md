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

![](https://cdn-media-1.freecodecamp.org/imgr/eWWi3gZ.gif)



