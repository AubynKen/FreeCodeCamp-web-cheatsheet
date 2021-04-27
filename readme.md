# FreeCodeCamp HTML CSS Cheatsheet

This cheatsheet **ISN'T FOR LEARNING HTML** but made for reviewing basic HTML syntax.

---

## Basic HTML and HTML5

### Say Hello to HTML elements

This is a h1 element: 

```html
<h1>Hello, World</h1>
```



### Headlines with h2 elements

```html
<h2>This is a section title.</h2>
<h3>This is a subsection of h2.</h3>
<h4>And so on and so forth.</h4>
<h6>It dosn't go beyond h6.</h6>
```

Notice that these tags should not be used for sizing the text. That should be done in CSS.



### Inform with the paragraph element

```html
<p>This is a paragraph</p>
```



### Comment html

```html
<!-- This is an HTML Comment -->

<!--
  Comments can span over multiple lines.
  just like this.
-->
```

Comments are not read by the browser. They are here for programmers to read it.



### Main Element

```html
<main> 
  <h1>Hello World</h1>
  <p>Hello Paragraph</p>
</main>
```



### Image

```html
<img src="https://www.link-to-the-image.com/image-example.jpg" alt="text description">
```

- **src** : sets the source of the image.
- **alt** : alternative text, this is shown when the image can't be accessed. Also used for accessibility.

### Anchor tags

```html
<a href="https://www.google.com">This links to google.</a>
```

* **href** : sets the URL of the link.
* 

### Internal links

```html
<a href="#contact-header">Contacts</a>
<!-- putting "#" in front of id links the anchor tag to somewhere else on the same page -->
<h2 id="contact-header">Contacts</h2>
```



### Nest an anchor tag within a p element

```html
<p><a>This paragraph can be clicked.</a></p>
```



### Make dead links using the hash symbol

```html
<a href="#">cat photos</a>
```

This acts as a **temporary place holder** when we don't know where we're setting the link to yet.



### Turn an image into a link

Simply wrap the **img** image tag inside an **a** anchor tag:

```html
<a href="#"><img src="https://bit.ly/fcc-running-cats" alt="Three kittens running towards the camera."></a>
```



### Create a bulleted unordered list

```html
<ul>
  <li>milk</li>
  <li>cheese</li>
</ul>
```

This will be shown:

- **milk**
- **cheese**



### Create an ordered list

```html
<ol>
  <li>Garfield</li>
  <li>Sylvester</li>
</ol>
```

This will be shown:

1. **Garfield**
2. **Sylvester**



### Create a text field

```html
<input type="text">
```



### Placeholder

```html
<input type="text" placeholder="this is placeholder text">
```

The placeholder text is shown before the user inputs anything.



### Creating a form and submitting data

```html
<form action="/url-where-you-want-to-submit-form-data">
  <!-- exeample of action:
	action="mailto:yourname@domain.com"
	-->
  <input>
  <button type="submit">Submit</button> <!-- submit button -->
</form>


```



### Creating a set of radio buttons in the form

```html
<input type="radio" id="indoor" value="indoor" name="indoor-outdoor">
<label for="indoor">Indoor</label>

<br>

<input type="radio" id="outdoor" value="indoor" name="indoor-outdoor">
<label for="outdoor">Outdoor</label>
```

- The **name** attribute groups the two radio buttons together, so that only one can be selected.
- The **for** attribute in the label links the label to the radio button, for accessibility (ie. for screen readers)
- The ***value*** attribute is important. This tells the server "indoor-outdoor:indoor" if the indoor button is chosen. Otherwise the default value would be "on". 

Another way of associating label and radio button is nesting:

```html
<label for="indoor"><input type="radio" id="indoor" name="indoor-outdoor" value="indoor"></label>

<!-- here the for attribute is used for best practice -->
```



### Make options checked by default

```html
<!-- simply add the "checked" boolean attribute -->
<input type="radio" name="test-name" checked>
```



### The div element

```html
<div>
  <input ... ...>
  <input ... ...>
  <input ... ...>
</div>
```

The **div** elements itself doesn't do anything. It is used for better code organization and easier styling with CSS.



### Doctype

```html
<!DOCTYPE html>
<html>

</html>
```

The **doctype** tag simply tells the browser that we are using html5.



### The general structure of an HTML5 file

```html
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



---

## Basic HTML and HTML5

### Inline CSS

```html
<h2 style="color: blue;">CatPhotoApp</h2>
```

Using the **style** attribute, we can set the style of a specific html element using CSS syntax.



### Style block and selector

```html
<style>
  h2 {
    color: red;
  }
</style>
```

This changes the color of all h2 elements.



### Class selector

```html
<style>
  .blue-text 
    color: blue;
  }
</style>
<!-- Don't forget the dot in front of "blue-text" -->

<p class="blue-text">This text will be shown in blue.</p>
<h1 class="blue-text">One class selector can be applied to multiple</h1>
```



### Font size

```css
h1 {
  font-size: 30px;
  font-family: sans-serif;
}
```

Three common types of font family: serif, sans-serif and monospace.





### Comments

```css
/* Here is a comment in CSS. */
```



### Fallback font

Not all fonts are available to users across different platforms. A generic fallback font can used to replace the unavailable font:

```css
font-family: FAMILY_NAME, GENERIC_NAME;
```

##### eg.

###### Eg stands for exeample

```css
p {
  font-family: Helvetica, sans-serif;
}

```



### Width and height of an image

```css
.image-class {
  height: 100px;
  width: 150px;
}
```



### Add borders around elements

```css
<style>
  .thin-red-border {
    border-color: red;
    border-width: 5px;
    border-style: solid; /* makes the border solid */
    border-radius: 3px; /* This rounds off the border */
  }
</style>

/* In order to make an image circular, simply set the border-radius to 50%  */
```



### Background color

```css
.green-background {
  background-color: green;
}
```



### Id selector

```css
#cat-photo-element {
  background-color: green;
}
```

The above CSS code should make the following html element's background green:

```html
<img id="cat-photo-element" class=... src=... alt=...>
```

Notice that unlike the **class** attribute, an **id** attribute should be unique to the element. 



### Padding and margin

In CSS, a **margin is** the space around an element's border, while **padding** is the space **between** an element's border and the element's content.

```css
.some-class {
  margin: 10px;
  padding: 20px;
}
```



#### Negative margins

You can set the margin of an element to a **negative value** to make the element bigger/grow out of the parent element.



### Setting different paddings / margins to differents sides of an element:

```css
#some-id {
  margin-top: 10px;
  margin-right: 20px;
  margin-bottom: 30px;
  margin-left: 40px;
}
```

The same goes for paddings, just replace margin with padding in the above code.



### Circular shorthand notation

Below is the shorthand for the above code:

```css
#some-id {
  margin: 10px 20px 30px 40px; /* Goes clockwise, starting from top */
}
```

Same goes for paddings.



### Style inheritance

An element's **default style** is **inherited** **from its parent element**, and can be overriden if a more specific style is applied to the element (either inline or in a CSS sheet).

##### eg.

```html
<style>
  body {
    background-color: black;
    color: white; /* Doesn't do anything to body, but changes the color of the h1 element contained inside the body */
    font-family: monospace; /* Changes the font-family of everything inside the body, here the h1 tag. */
  }
</style>

<h1>Hello World</h1>
<h2 style="color: yellow">Hello Sky.</h2>
<!-- We overrode h2's color -->
```

The code above should produce a **white monospace** "Hello World" in a **dark background** and a **yellow monospace** "Hello Sky".



### Style overriding in subsequent CSS

```html
<style>
  .pink-text {
    color: pink;
  }

  .blue-text {
    color: blue;
  }
</style>
<!-- the order of class declarations above matters -->

<h1 class="blue-text pink-text">Hello World!</h1>
<!-- the order above doesn't matter -->
```

Here we specified two classes for the h1 class, but code inside the "blue-text" selector overrides that of "pink text" because it comes later in the style block.



### Selector precedence

**inline CSS** >**id selector** > **class selector** > **element selector**

">" stands for "overrides".

The more specific one overrides the more general one.



### The !important keyword

```css
color: red !important; /* This overrides everything */
```

Using the **!important** keyword, you can override all other styles.



### HexCode

```css
color: #FF0000; /* This is the red color */
color: #00FF00 /* This is green */
color: #0000FF /* This is blue */
```

You can use HexCode for declaring colors. It goes from #000000 to #FFFFFF in **hexadecimal numbers**. the first two digits correspond to the red color, second two digits correspond to green and last two digits blue.



### Abbreviated hex code

```css
color: #F00 /* This is also the red color */
```

Abbreviated hex code is less precise. It reduces the number of possible colors to 16x16x16 (from 256x256x256).



### RGB Colors

If you don't want to use hexadecimal numbers, you can also use the equivalent RGB notation:

```css
color: rgb(255, 0, 0); /* Again, this is red */
```



### Creating Custom CSS variables

After declaring the my-color variable and assigning it a value:

```css
--my-color: RGB(283, 55, 167); 
```

You can use "my-color"  without explicitly specifying the RGB values:

```css
background: var(--my-color);
```



### Attaching fallback values to CSS variables:

```CSS
background: var(--penguin-skin, black); /* Black will be applied if the penguin-skin color becomes unavailable */
```



### Improve compatibility using browser fallbacks

If a browser doesn't incorporate a certain feature, we should use fallbacks. 

```css
  :root {
    --red-color: red;
  }

  .red-box {
    background: var(--red-color);
    background: red;
  }
```

Internet Explorer doesn't recognize var(), so it ignores that line and applies red to the background.



### Variable Inheritance

A variable inside a class is available only in **that class and in its descendents.**

Variables declared inside the **:root pseudoclass** is **available everywhere**:

```css
  :root {
    --penguin-belly: pink;
  }
```

This can be **overwritten** in a *more specific class*:

```css
  .penguin {
    --penguin-belly: white;
    color: var(--penguin-belly); /* White and not pink is applied */
  }
```



### Media Query

```css
  :root {
    color: black;
  }

  @media (max-width: 350px) {
    :root {
      color: white; /* Color changes to white when the screen width is less than 350 pixels */
    }
  }
```

---

## Applied Visual Design

### Text align (CSS)

```css
  h4 {
    text-align: center; 
    /* This aligns all the text elements to the center */
  }
```

Other options for the text-align property include:

```css
text-align: center; /* Centers the text */
text-align: left; /* left aligns the text */
text-align: right; /* right aligns the text */
text-align: justify; /* make text meet both left and right edges */
```



### HTML text formatting

```html
<b>This text is bold.</b>
<strong>Bold and strong.</strong>
<!-- Visually, strong and b achieve the same effect. However strong helps the search engine figure out which part of the text is trong -->

<i>Italic</i>
<em>Italic and emphasized</em>

<sub>Subscript text</sub>
<sup>Superscript text</sup>

<u>Underlined text</u>
<s>Striked-through text</s>
```



### Self closing tags

Some tags are self-closing tags which don't require a closing tag.

```html
<hr> <!-- This creates a horizontal rule -->
<br> <!-- This is a line break -->
```



### RGBA color

An rgba color is an rgb color with an opacity argument, ranging from 0 to 1.

```css
background-color: rgba(255, 0, 0, 1) /* This is a solid red color */
text-color: rgba(0, 255, 0, 0.5) /* This green color is half transparent */
```



### Changing font size

```css
p {
  font-size: 20px; /* Sets the font size of paragraphs to 20 pixels */
}
```



### Box shadow

```css
.some-class {
  box-shadow: 0 10px 20px 10px rgba(0,0,0,0.2);
  /* This adds a shadow 10px to the bottom, with 20 pixels of blurring radius and 10 pixels of spreading radius, with a 80 percent transparent black color */
}
```

Parameters of the box-shadow property:

- **offset-x**: How much to the right
- **offset-y**: How much to the buttom
- **blur-radius**: Optional, how much the shadow border should be blurred
- **spread-radius**: Optional, how much bigger the shadow is compared to the box
- **color**: self explanatory



### Opacity property

```css
#some-element {
  opacity: 0.1;
} /* some-element is now 10% opaque, ie. 90% transparent */

#some-other-element {
  opacity: 0.9;
} /* some-other-element is now 90% opaque */
```

The parameter goes from 0 (totally transparent) to 1 (totally opaque).



### Text transform

```html
<p class="my-paragraph">HELLO my friend</p>
```

```css
p {
  text-transform: lowercase; /* hello my friend */
  text-transform: uppercase; /* HELLO MY FRIEND */
  text-transform: capitalize; /* Hello My Friend */
}
```

Other possible values for this property include:

* ***None***: Use the original text
* ***Inherit***: Use the text transform property of parent element

*p.s*:  *If we apply **"initial"** to this property, **None** will be applied because it's the default value of the text-transform property. Same goes for other properties in CSS.*



### Font weight

This property adjusts the **thickness** of the text.

```css
font-weight: 200; /* The value is unitless. Do not use px. */
```



### Line height

```css
p {
  line-height: 40px; 
}
/* Now each line of the paragraph element is 40 pixels in height. */
```



### The hover pseudo-class

```css
a {
  color: grey; /* The anchor element is grey */
}

a:hover {
  color: red; /* But when the cursur hovers over it, the element becomes red */ 
}
```



### Changing an elements's relative position

```css
.my-block {
  position: relative;
  bottom: 10px;
} /* This moves my-block away from the bottom, without changing the normal flow of the document */
```



### Absolute position

```css
  #searchbar {
    position: absolute;
    top: 50px;
    right: 50px;
  }
/* This removes the searchbar from the normal flow of the document. The position is relative to its closest ancestor */
```



### Float

Pushes element to the left / right side of the parent.

```css
#left-block {
  float: left;
} /* This box is moved to the left */

#right-block {
  float: right;
} /* This box is moved to the right */
```



### Z-index

When multiple elements **overlap** with each other, the **z-index property** is what decides which one is **on top.** Only integers are accepted.

*eg.* *Say we have two elements, red-block and blue-block that overlap*:

```css
#red-block {
  ...
  z-index: 2;
}

#blue-block {
  ...
  z-index: 1; /* 1 < 2 so red-block is on top */
}
```



### Centering an element in CSS

```css
#element {
  margin: auto; /* Now the element is centered */
}
```



### Hue, Saturation, Lighness

We've seen **rgb()** and **rgba()**. Another way to set a color is to use the **hsl()** function.

```css
#some-element {
  background-color: hsl(0, 100%, 50%); /* You guessed it, this is red */
}
```

* **Hue**: Basically a circular color wheel with RED at 0 degrees, GREEN at 120 and BLUE at 240.
* **Saturation**: Goes from 0% (grey) to 100%(totally vibrant and saturated)
* **Lightness**: Goes from 0%(black) to 100%(white)



### Linear gradient

```css
#some-element {
  color: linear-gradient(direction, color1, color2 ...);
}
```

The **direction** parameter is in degree. It start from the top (0 degrees) and goes clockwise *(eg. 90 degrees is the (left to) right direction.)*



### Repeating linear gradient

For more precision on the pattern, we may use the repeating-linear-gradient which allows us to specify the positions of the colours more precisely. 

```css
#some-element {
  color: repeating-linear-gradient(
      90deg,
      yellow 0px,
      blue 40px,
      green 40px,
      red 80px
    );
}
```



### The url() function

```css
body {
  background: url(https://cdn-media-1.freecodecamp.org/imgr/MJAkxbh.png);
  /* This sets the background color to the given url */
}
```



### Transform, scale

```css
p:hover {
  transform: scale(2);
} /* This doubles the size of the phrase when being hovered over. */
```



### Skew

```css
#some-element {
  transform: skewX(20deg);
  transform: skewY(-20deg);
}
```



### Before and After pseudo elements

```html
<style>
  p::before {
    content: "Before element";
  }
  
  p::after {
    conten: "After element";
    font-size: 20px;
    color: red;
  }
</style>

<p class="my-paragraph">This is my paragraph.</p>
```

The page renders as if the following code was written:

```html
Before element

<p class="my-paragraph">This is my paragraph.</p>

<div style="font-size: 20px; color: red;">
  After element
</div>
```



### Keyframes and animation

```css
.animated-class {
  ...
  animation-name: rainbow; /* Tells "@keyframes rainbow" below to act on this class */
  animation-duration: 3s;
  ...
}

@keyframes rainbow {
  0% {
    background-color: red;
  }
  50% {
    background-color: green;
  }
  100% {
    background-color: blue;
  }
}

/* This creates an animation for the animation-class class, with background color starting at red, graduately transitioning to green and graduately transitioning to blue */
```

 In order to **lock the animation at 100% after it finishes**:

```css
animation-fill-mode: forwards;
```

For the animation to repeat indefinitely:

```css
animation-iteration-count: 3;
```

##### Timing function:

```css
animation-timing-function: ease; /* Default value. Slow -> Fast -> Slow */
animation-timing-function: linear; /* Self explanatory */
animation-timing-function: ease-in; /* Slow -> Fast */
animation-timing-function: ease-out; /* Fast -> Slow */
```

You can create your custom timing function with **cubic-bezier()**:

```css
animation-timing-function: cubic-bezier(0.25, 0.25, 0.75, 0.75);
```

This creates the $bezier_{cubic}(x_1, y_1, x_2, y_2)$ curve. Where the four paratmeters range from 0 to 1, creating the two control points, with time on the x axis and position on the y axis.

---

## Applied Accessibility

- When an image **dosen't need further explaination** because of it **context** or its **use**, we can **leave the alternative text blank**.
- **Headings** should show **hierarchical relationships** of content.



### Semantic elements:

Semantic elements is preferred to div becuase it provides better structuring and helps assistive devices to figure out what is what, although visually they are equivalent to div.

```html
<header>This is a header.</header>
<nav>Navigation bar.</nav>
<main>
  <section>Section one.</section>
  <section>Section two.</section>
  <article>Use article instead of section only if the content is self-contained. If the content doesn't make sense when taken out of the context of the website, use section.</article>
</main>
<footer>Author copyright blah blah...</footer>
```

### Audio

```html
    <audio id="Cat-meowing" controls>
    <!-- The controls attribute is boolean. It adds the play/pause buttom and keyboard control -->
      <source src="link-to-the-audio.mp3" type="audio/mpeg">
    </audio>
```



### Figure and figcaption

By wrapping an image and its caption together in a figure tag improves accessibility:

```html
<figure>
  <img src="Mouse.jpeg" alt="mouse-photo">
  <br>
  <figcaption>
    Jerry eating a piece of cheese.
  </figcaption>
</figure>
```



### Fieldset

We can group radio buttons in a fieldset for better accessibility:

```html
<form>
  <fieldset> <!-- This groups the following radio buttons together -->
    <legend>Choose one of these three items:</legend> <!-- Legend adds extra info -->
    <input id="one" type="radio" name="items" value="one">
    <label for="one">Choice One</label><br>
    <input id="two" type="radio" name="items" value="two">
    <label for="two">Choice Two</label><br>
    <input id="three" type="radio" name="items" value="three">
    <label for="three">Choice Three</label>
  </fieldset>
</form>
```



### Date

Set the type attribute of an input tag to "date" and you get a date picker.

```html
<label for="input1">Enter a date:</label>
<input type="date" id="input1" name="input1">
```



### Datetime attribute

The date tag, along with the datetime attribute, provides a standardized version of date which avoids any confusion.

```html
We went to the supermarket <time datetime="2013-02-13">last Wednesday</time>.
<!-- datetime="year-month-day" -->
```



### Access keys

```html
<button accesskey="b">Press b to </button>
```



### Tab index

```html
<div tabindex="0">This element is tabbable due to tab index.</div>
```

- When tab index is set to **zero**, the element becomes **tabbable**.
- When its set to any **negative value** (typically -1), it's **focusable** (you can click on it to focus) but **not tabbable.**
- When its set to a **positive integer**, it's tabbable and the **tabbing order is increasing**. (eg. When tab is tapped multiple times, elements with tab index set to zero are selected, then 1, 2, 3 etc.)

---

## Responsive Web Design

### Viewport width, viewport height

**vw** and **vh** correspond respectively to the viewport width and the viewport height. They are expressed in percentage.

```css
body {
  width: 70vw; /* This means 70% of the viewport width */
  height: 50vh; /* Half of the viewport height */
}
```



### Vmin and vmax

Instead of using vw and vh, you can also use **vmin** and **vmax**. :

- if **viewport width > viewport height**: **vmax = vw** and **vmin = vh**
- if **viewport width < viewport height**: **vmax = vh** and **vmin = vw**

---

## CSS Flexbox

