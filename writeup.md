# Web Typography

While surfing on the internet we found that 95% of the content is in text format. There are two important terms in typography :

- ***Typography***

It's the design of a collection of glyphs(e.g. letters, numbers, symbols). A typeface is what we see, how the text looks, feels, and reads.

- ***Font***

On the other hand font is the file that contains typeface. A specific size, weight, or style of a typeface is defined inside font (e.g. regular, bold, italic).

For better understanding, a typeface is like a song and the font is like an MP3 file.

## Embeding Web Fonts

We can upload a font to the sever by CSS and HTML in two methods :

### CSS(@font-face or @import)

The CSS "@font-face" at-rule includes font-family and src property. The font-family property identifies the font's name and the src determines the source file of the font-family. Thereafter we can use the font-family property on elements.

```
@font-face {
    font-family: "Lobster";
    src: local("Lobster"), url("lobster.woff") format("woff");
  }
  body {
    font-family: "Lobster", "Comic Sans", cursive;
  }
```

Or else we can also directly embed in our existing stylesheet using @import rule.

```
<!-- CSS -->
  @import url('https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;500;700&display=swap');

  body {
    font-family: 'Roboto', sans-serif;
  }
```

### HTML(<link>)

We can also embed a font using its online soucrce, that can be added inside the head using <link> tag in the HTML document. For example:

```
<!-- HTML -->
  <head>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;500;700&display=swap" rel="stylesheet">
  </head>

  <!-- CSS -->
  body {
    font-family: 'Roboto', sans-serif;
  }
```

## Adding Color to Text

To change the color of text we can use "color" property .

```
p {
  color: #777;
  }
```

>>So we have some font based and some text based property .

## Font Based Properties

### Font Family

```
body {
    font-family: 'Roboto', 'Lato' sans-serif;
  }
```

The font-family property determines which font will be used to display text on a page. Multiple values for the font names can be defined under font-family property comma separated. As you can see in the above code. Here we have two values Roboto and Lato and the third value is fallback. The first value will be primarily choice. In case the first font won't available the next value will be the alternative choice and so on. Last font family will be the system's default font .

### Font Size

The font-size property sets the size of the text used on a page. It accepts all the length values, pixel(px)s, em, percentage, points, or keywords.

```
body {
    font-size: 16px;
  }
```

### Font Style

The "font-style" property is used to italicize the text . This property accepts four values "italic", "oblique", "normal" and "inherit". The "italic" and "oblique" value italicize the text . The "normal" value make the text normal and "inherit" value inherits the  parent's text style.

```
span {
    font-style: italic;
  }
```

### Font Variant

The font-variant property is rarely used. It accepts three values: "small-caps", "normal", and "inherit". The "small-caps" value is occasionally used to make the text in small capitals. The "normal" value dose not make any changes i.e. make the text normal and "inherit" value takes the parent's text style.

```
.small-caps {
    font-variant: small-caps;
  }
```

### Font Weight

The font-weight property is used to make text light or bold. The property accepts either keyword values(normal, bold, lighter, bolder and inherit) or numeric values(100, 200, 300, 400, 500, 600, 700, 800, 900).The 100 is thinnest and 900 is the boldest. The 400 is equivalent to normal and 700 is equivalent to bold weight. You can choose any of these weights. If a font embedded in our page doesn't include any of these weights, you cannot apply that value. However, if you applied then the nearest value of that particular weight will be applied. For example, if you chose 900 weight and 900 is not available then the nearest value may be 800 or 700 will be applied.

```
.span {
    font-weight: bold;
  }
```

### Line Height

The line-height property determines the distance between two lines (often referred to as leading). It accepts all the general length values. The standar value for this property is 1.5 or 150%.

```
body {
    line-height: 1.5;
  }
```
```
.btn {
    line-height: 24px;
  }
```

### Shorthand Font Properties

All these font-based properties can also be applied using just font shorthand property. The order of the property values should be from left right: font-style, font-variant, font-weight, font-size, line-height, and font-family. The values of all these properties are optional while using shorthand font property except the **font-size** and **font-family**.

```
body {
    font: italic small-caps bold 16px/24px "Roboto", "Lato", sans-serif;
  }
```

## Text Based Properties

### Text Align

The text-align property is used to align the content inside an element. The values for the text-align properties are left, right, center, justify, and inherit. The left value is the default value align the text to the left and right value will align the text to the right and center value will align the text in center of the content . The justify value makes the text align in such a way that first word of the line is starting from left edge and last word of the line will align to the right edge of the content and inherit value takes the parent's property value.

```
p {
    text-align: center;
  }
```

### Text Decoration

This property accepts five values : none, underline, overline, line-through and inherit. The "none" value is for remove the decoration of the text . The "underline" value make a line at the bottom of the text and "overline" value make a line at the top and "line-through" value make a line in the middle of the text . The "inherit" value takes the parent's value.

```
.heading {
    text-decoration: underline.
  }
```

We can also style the line by using "text-decoration-color" and "text-decoration-style" property . The "text-decoration-color" property accepts the color values and the "text-decoration-style" property accepts some value which are wavy, dotted, dashed, double.

```
.heading {
    text-decoration-color: blue;
  }
```

```
.heading {
    text-decoration-style: dotted;
  }
```

### Text Indent

The text-indent property specifies how much horizontal space should be left before the starting of the first line within an element. All common length values are accepted by the text-indent property.

```
p {
    text-indent: 32px;
  }
```

### Text Shadow

The text-shadow property is very similar to the box-shadow property. The only difference is that the text-shadow property doesn't accept fourth(spread) value, which optional in the box-shadow property.

```
.heading {
    text-shadow: 3px 6px 2px rgba(0, 0, 0, .3);
  }
```
In the above example first value is for vertical align and second value is for horizontal align and the third value is for width of the shadow.

### Text Transform

The text-transform property controls the case and capitalization of the text. The property accepts five different values: none, capitalize, uppercase, lowercase, and inherit. The "none" value is for remove other value or nothing to assign . The "capitalize" value make the first letters of every word capital. The "uppercase" value makes the text uppercase and "lowercase" makes the text lowercase. The "inherit" value takes the parent's property value.

```
h1 {
    text-transform: uppercase;
  }
```

### Letter Spacing

The letter-spacing property controls the amount of space between each character in an element. Space can be increased or decreased. It accepts all the common length values, none, and inherit value. The positive values increases the space and negative value decreases the space and none will bring back to normal space size and inherits takes the parent's property value.

```
p {
   letter-spacing: 2px;
 }
```

### Word Spacing

The word-spacing property is similar to the letter-spacing property, but it controls the space between each word within an element. The word-spacing property also accepts all the common length values, none, and inherit as the letter-spacing accepts.

```
p {
    letter-spacing: 32px;
  }
```

>>We have some other properties also :

## Quotation and Citation in HTML

It is common to find that incorrect tags are used to markup quotes in an HTML document. Usually, beginners treat regular text and quotes in the same way. But actually, they are different. To cover all types of quotation HTML provides different semantic tags: <cite>, <q> and <blockquote>.

### Quoting with <q>

The q tag is an inline-level element often used to markup inline quotes within other text. The <q> tag is used to semantically represent the dialogue and prose in the HTML document. By default, the browser will insert proper quotation marks for the content wrapped inside the q element.

```
<p><q>Programming isn't about what you know; it's about what you can figure out.</q> said by Chris Pine</p>
```

### Blockquote

To markup, a large block of text as quote, the <blockquote> tag is used. The <blockquote> is a block-level element that may have another block-level element nested inside it (should be a quote).

```
<blockquote>
    <h2>...</h2>
    <p>&#8220;In most people&#8217;s vocabularies, design is a veneer. It&#8217;s interior decorating. It&#8217;s the fabric of the curtains, of the sofa. But to me, nothing could be further from the meaning of design. Design is the fundamental soul of a human-made creation that ends up expressing itself in successive outer layers of the product.&#8221;</p>
    <ul>
      <li>...</li>
      <li>...</li>
      <li>...</li>
    </ul>
  </blockquote>
```

### The Citation Attribute

Both <q> and <blockquote> can have an optional cite attribute. The cite attribute holds a URL that acts as a reference to the quote. This attribute does not alter the appearance of the element, just add value for screen readers and other devices.

```
<p>The officer left a note saying <q cite="https://johnrhea.com/summons">You have been summoned to appear on the 4th day of January on charges of attempted reader bribery.</q></p>
```

### The <cite> Element

The <cite> tag is used for citing or referencing any creative work by a person. The tag should not be used for citing or referencing a person who said or wrote the quote. By default, browsers italicize cite tags.

```
<p>My favorite book is <cite>The Reality Dysfunction</cite> by
  Peter F. Hamilton. My favorite comic is <cite>Pearls Before
  Swine</cite> by Stephan Pastis. My favorite track is <cite>Jive
  Samba</cite> by the Cannonball Adderley Sextet.</p>
```
