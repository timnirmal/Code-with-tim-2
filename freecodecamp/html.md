# Html

## Basic

h1 - Main Heading

h2 - Subheadings \(h2-h6\)

Comment - `<!--`    `-->`

 HTML5 introduces more descriptive HTML tags. These include `main`, `header`, `footer`, `nav`, `video`, `article`, `section` and others.

  The `main` HTML5 tag helps search engines and other developers find the main content of your page.

 The `div` element, also known as a division element, is a general purpose container for other elements.



## Image

```text
<img src="https://www.freecatphotoapp.com/your-image.jpg">
<img src="https://www.freecatphotoapp.com/your-image.jpg" alt="A cat.">
```

All `img` elements **must** have an `alt` attribute. The text inside an `alt` attribute is used for screen readers to improve accessibility and is displayed if the image fails to load.

**Note:** If the image is purely decorative, using an empty `alt` attribute is a best practice.

Ideally the `alt` attribute should not contain special characters unless needed.



## Link

You can use `a` \(_anchor_\) elements to link to content outside of your web page.

`a` elements need a destination web address called an `href` attribute. They also need anchor text. Here's an example:

```text
<a href="https://freecodecamp.org">this links to freecodecamp.org</a>
```

`target="_blank"` ****for open in new tab

###  **Link to Internal Sections**

To create an internal link, you assign a link's `href` attribute to a hash symbol `#` plus the value of the `id` attribute for the element that you want to internally link to, usually further down the page. You then need to add the same `id` attribute to the element you are linking to. An `id` is an attribute that uniquely describes an element.

Below is an example of an internal anchor link and its target element:

```text
<a href="#contacts-header">Contacts</a>
...
<h2 id="contacts-header">Contacts</h2>
```

When users click the `Contacts` link, they'll be taken to the section of the webpage with the **Contacts** header element.

**Make Dead Links Using the Hash Symbol**

Sometimes you want to add `a` elements to your website before you know where they will link.

 `href="#"`

 

## List

display: inline;

**Create a Bulleted Unordered List**

Unordered lists start with an opening `<ul>` element, followed by any number of `<li>` elements. Finally, unordered lists close with a `</ul>`

```markup
<ul>
  <li>milk</li>
  <li>cheese</li>
</ul>
```

 **Create an Ordered List**

Ordered lists start with an opening `<ol>` element, followed by any number of `<li>` elements. Finally, ordered lists are closed with the `</ol>` tag.

For example:

```markup
<ol>
  <li>Garfield</li>
  <li>Sylvester</li>
</ol>
```

##  **Create a Text Field**

`input` elements are a convenient way to get input from your user.

You can create a text input like this:

```markup
<input type="text">
```

Note that `input` elements are self-closing.

###  **Add Placeholder Text to a Text Field**

```markup
<input type="text" placeholder="this is placeholder text">
```

### **Create a Form Element**

You can build web forms that actually submit data to a server using nothing more than pure HTML. You can do this by specifying an `action` attribute on your `form` element.

```text
<form action="/url-where-you-want-to-submit-form-data">
  <input>
</form>
```

 **Use HTML5 to Make a Filed Required**

You can require specific form fields so that your user will not be able to submit your form until he or she has filled them out.

For example, if you wanted to make a text input field required, you can just add the attribute `required` within your `input` element, like this: `<input type="text" required>`

##  **Create a Set of Radio Buttons**

You can use radio buttons for questions where you want the user to only give you one answer out of multiple options.

Radio buttons are a type of `input`.

Each of your radio buttons can be nested within its own `label` element. By wrapping an `input` element inside of a `label` element it will automatically associate the radio button input with the label element surrounding it.

All related radio buttons should have the same `name` attribute to create a radio button group. By creating a radio group, selecting any single radio button will automatically deselect the other buttons within the same group ensuring only one answer is provided by the user.

Here's an example of a radio button:

```text
<label> 
  <input type="radio" name="indoor-outdoor">Indoor 
</label>
```

It is considered best practice to set a `for` attribute on the `label` element, with a value that matches the value of the `id` attribute of the `input` element. This allows assistive technologies to create a linked relationship between the label and the child `input` element. For example:

```text
<label for="indoor"> 
  <input id="indoor" type="radio" name="indoor-outdoor">Indoor 
</label>
```

 **Each of your two radio button elements should be nested in its own `label` element.**

## **Create a Set of Checkboxes**

Forms commonly use checkboxes for questions that may have more than one answer.

Checkboxes are a type of `input`.

Each of your checkboxes can be nested within its own `label` element. By wrapping an `input` element inside of a `label` element it will automatically associate the checkbox input with the label element surrounding it.

All related checkbox inputs should have the same `name` attribute.

It is considered best practice to explicitly define the relationship between a checkbox `input` and its corresponding `label` by setting the `for` attribute on the `label` element to match the `id` attribute of the associated `input` element.

Here's an example of a checkbox:

```text
<label for="loving"><input id="loving" type="checkbox" name="personality"> Loving</label>
```

### **Use the value attribute with Radio Buttons and Checkboxes**

When a form gets submitted, the data is sent to the server and includes entries for the options selected. Inputs of type `radio` and `checkbox` report their values from the `value` attribute.

For example:

```text
<label for="indoor">
  <input id="indoor" value="indoor" type="radio" name="indoor-outdoor">Indoor
</label>
<label for="outdoor">
  <input id="outdoor" value="outdoor" type="radio" name="indoor-outdoor">Outdoor
</label>
```

Here, you have two `radio` inputs. When the user submits the form with the `indoor` option selected, the form data will include the line: `indoor-outdoor=indoor`. This is from the `name` and `value` attributes of the "indoor" input.

If you omit the `value` attribute, the submitted form data uses the default value, which is `on`. In this scenario, if the user clicked the "indoor" option and submitted the form, the resulting form data would be `indoor-outdoor=on`, which is not useful. So the `value` attribute needs to be set to something to identify the option.

###  **Check Radio Buttons and Checkboxes by Default**

You can set a checkbox or radio button to be checked by default using the `checked` attribute.

To do this, just add the word `checked` to the inside of an input element. For example:

```text
<input type="radio" name="test-name" checked>
```

## Format

```markup
<!DOCTYPE html>
<html>
<head>
    <meta />
</head>
<body>
    <div>
    </div>
 </body>

</html>
```

You tell the browser this information by adding the `<!DOCTYPE ...>` tag on the first line, where the `...` part is the version of HTML. For HTML5, you use `<!DOCTYPE html>`.

The `!` and uppercase `DOCTYPE` is important, especially for older browsers. The `html` is not case sensitive.

Next, the rest of your HTML code needs to be wrapped in `html` tags. The opening `<html>` goes directly below the `<!DOCTYPE html>` line, and the closing `</html>` goes at the end of the page.

Here's an example of the page structure. Your HTML code would go in the space between the two `html` tags.

You can add another level of organization in your HTML document within the `html` tags with the `head` and `body` elements. Any markup with information about your page would go into the `head` tag. Then any markup with the content of the page \(what displays for a user\) would go into the `body` tag.

Metadata elements, such as `link`, `meta`, `title`, and `style`, typically go inside the `head` element.

## Id

In addition to classes, each HTML element can also have an `id` attribute.

There are several benefits to using `id` attributes: You can use an `id` to style a single element and later you'll learn that you can use them to select and modify specific elements with JavaScript.

`id` attributes should be unique. Browsers won't enforce this, but it is a widely agreed upon best practice. So please don't give more than one element the same `id` attribute.

Here's an example of how you give your `h2` element the id of `cat-photo-app`:

```text
<h2 id="cat-photo-app">
```

## Units

**Understand Absolute versus Relative Units**

The last several challenges all set an element's margin or padding with pixels \(`px`\). Pixels are a type of length unit, which is what tells the browser how to size or space an item. In addition to `px`, CSS has a number of different length unit options that you can use.

The two main types of length units are absolute and relative. Absolute units tie to physical units of length. For example, `in` and `mm` refer to inches and millimeters, respectively. Absolute length units approximate the actual measurement on a screen, but there are some differences depending on a screen's resolution.

Relative units, such as `em` or `rem`, are relative to another length value. For example, `em` is based on the size of an element's font. If you use it to set the `font-size` property itself, it's relative to the parent's `font-size`.

**Note:** There are several relative unit options that are tied to the size of the viewport. They are covered in the Responsive Web Design Principles section.

