# Read: 05 - HTML Images; CSS Color & Text

## JS Book by Jon Duckett
<h1>Chapter 5: “Images” (pp.94-125)</h1>

`<img>` elements are used to add images to a webpage.

You must alway specify `src` attribute for the source of the image and `alt` atribute to describe the content of an image (Perhaps for supportive of screen readers).

`title` attributes provide additional info about the image. Most browsers will display this attribute in a tooltip while the user hovers over the image.

```
<img src="images/quokka.jpg" alt="A family of quokka" title="The quokka is and Australian marsupial that is similar in size to the domestic cat."/>
```

Images should be saved at the size and in the appropriate format for what they will be used as on the webpage.

JPEG - Best for saving photographs with many different colors

GIF or PNG - Best of illustraitions or logos that use flat colors

### When choosing Images for a website should consider:
- Be relevant
- Convey info
- Convey the right mood
- Be instantly recognizable
- Fit the color palette

---

## Adding an image:

use `<img>` tag - no need for closing tag
`src` tells the browser where the file is located
`alt` provides a text description
`title` provides additional information about the image
`width` & `height` can be added to size images in pixels

example:
`<img src="images/image.jpg" alt="This is a picture"/>`

---
## Three Rules for Creating Images
- Save images in the right format
- Save images at the right size
- Measure images in pixels

---

## Height and Width of Images
```
<img src="images/quokka.jpg" alt="A family of quokka" width="600" height="450" />
```
`height=` - specifies the height of the image in pixel

`width=` - specifies the width of the image in pixels

---

## Image Dimensions

- Reducing Image Size - creats a smaller version of an image
- Increasing Image Size - cannot increase the size of photos significantly without affecting the image quality
- Changing Shape - only some images can be cropped iwthout losing valuable info

---

## Cropping Images
It is important not to lose valuable information. It is best to source images that are the correct shape if possible.

## Measuring Images and Resolutions
- Pixels - images on a screen are made oup of lots of tiny squares known as pixels

- Resolution - number of pixels represneted on the screen. On most computers one can increase and decrease this number

- Dimesions - on the web the resolution of an image is irrelevant, and we need to think of the size of the image in terms of its dimensions in pixels

## Vector Images
differ from bitmap images and are resolution-independent.

- Scalable Vector Graphics (SVG) are the format used to display vector images directly from the web.
- Vecto format allows an increase in dimesions of an image without affecting the quality.

## Animated GIFs
show several frames of an image in sequence. Each extra frame of an image increases the size of the fle and the time for the image to download.

## Transparency
creating an image that is partially transparent from the web involves selecting on of two formats:
- Transparent GIF - IF the transparent part has straight edges and it is 100% tranparent, the image can be saved as a GIF witht he transparency option selected
- PNG - if the transparent part has diagonal or rounde edges or there is a need for semi-opaque transparency or drop shadow, then save it as a PNG.

## Where to Place Images in Code

Examples:

- Before a paragraph - pp starts on a new line after the image

- Inside the start of a paragraph - first row of text alignes with the bottom of the image

- In the middle of a paragraph - image is placed between the words of pp that it appears in

_Block elements always appear on a new line - Example, the image is followed by a block level element (such as a pp), then the block level elemetn will sit on a new line after the image._

_Inline elelments sit within a block level element and do not start on a new line. If the `<img>` element is inside a block level element, any text or other inline elements will flow around the image._

## Aligning Images Horizontally

`align` - attribute indicats how other parts of page should flow around an image.

`align left` aligns the image to the left allowing text to slow around it's right-hand side.

`align right` aligns the image to the right allowing text to flow around its left-hand side.

## Aligning Images Vertically

`top` aligns the first line of the surround text with the top of the image.

`middle` aligns first line of surround text with middle of image.

`bottom` aligns the first line of the surroundign text with the bottomof the image.


## HTML5: Figure and Figure Caption
`<figure>` element contains images and their caption so that the two are associated.

You can have more than one image inside the `<figure>` element so long as they all share the smae caption.

`<figcaption>` element has been added to HTML5 in order to allow web page authors to add a caption to an image.


<h1>Chapter 11: “Color” (pp.246-263)</h1>

## Color brigns a site to life, but also helps to covey the mood and evoke reactions.

There are three was to specify colors in CSS:
- RGB Values - red, green, blue - expressed as numbers between 0 and 255 : `rgb(123,123,123)`
- Hex Codes - red, green, blue - hexadecimal code : `#87cdae`
- Color Names

Hue - a color or shade Saturation - the amount of gray in the color - max would be no gray Brightness - how much black is in the color - max would be no black

## Contrast
It is important to ensure there is enought contrast between any text and the background color for readability.

## CSS3
Introduced an extra value for RGB colors to indicate opacity. It is called RGBA.

Allows the specification of colors as HSL values with an option opacity value known as HSLA.

`color` property sets the color of text inside an element.

`background-color` propety sets the color of the background for that box

<h1>Chapter 12: “Text” (pp.264-299)</h1>

## There are properties to control the choice of font, size, weight, style, and spacing.

- Assume there is a limited choice of fonts that most people have installed
- There is a wide range of Tyhpefaces, but you need to have the right license to use them.
- Text can be alignes to the left, right, center, or justified.
- The space between lines of text, individual letters, and words can be controlled. It can also be indented.

## Typeface Terminology

- SERIF - extra details on the end of the letters
- SANS-SERIF - no details on the end of the letters
- MONOSPACE - every letter is the same width
- WEIGHT - adds emphasis and affects the amount of whitespace
- STYLE - normal, italic
- STRETCH

## Font Size
`font-size`
- `px` Pixels
- `%`Percentages - default size of text in browsers is 16px. 
- `ems` - qquivalent to the width fo the letter m.

## Font Family
`font-family`

## Font Formats
- `: bold;)`
- `: italic;)`

## Font Weight
`font-weight`
- `bolder`

## Font Style
`font-style`

## Text Decoration
`text-decoration`
- `none`
- `underline`
- `overline`
- `line-through`
- `blink`

## Alignment
- `text-align: `
- `vetrical-align:`

* left
* right
* center
* justify

## Responding to Users
- `:hover `
- `:active `
- `:focuse `

<h1>Blog Post</h1>

[JPEG vs PNG vs GIF — which image format to use and when?](https://blog.imagekit.io/jpeg-vs-png-vs-gif-which-image-format-to-use-and-when-c8913ae3e01d)

- red, green, blue - expressed as numbers between 0 and 255 : rgb(123,123,123)
