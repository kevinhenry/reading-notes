# Read: 11 - Assorted Topics

## HTML Book by Jon Duckett
<h1>Introduction</h1>

HTML Chapter 16: Images 406-427
HTML Chapter 19: Practical Information 476-492
MDN Video Audio and Video Elements
HTML chapter 9: Flash 201-206

## Sizing in CSS - you can control the sizes of images in CSS using the width and height properties

- Commonly used dimensions:

  - Small portrait: 220 x 360
  - Small Landscape: 330 x 210
  - Feature photo: 620 x 400

## Aligning in CSS - using float and margin left/right can help align images on the page

## Centering in CSS - by default, images are inline element. Use the display: block; to center the image

- Once image is changed into a block element you can center in 2 ways:

  - `text-align: center;`
  - use the `margin` property setting the left and right margins to auto

## Background Images
Setting a background image: `background-image: url("images/pattern.gif");`

## Repeating Images
`background-repeat:`
`repeat:` repeated both horizontially and vertically
`repeat-x:` repeated horizontially only
`repeat-y:` repeated vertically only
`no-repeat:` image only shown once

`background-attachment:`
- fixed: image stays in the same position on the page
- scroll: image moves up and down as the user scrolls the page

<h1>Chapter 19 HTML Book: Practical Information</h1>

## SEO - Search Engine Optimization - SEO is the practice of trying to help your site appear nearer the top of search engine results when people look for topics your website covers

There are on-page and off-page SEO techniques

- On-page SEO
  - Page Title
  - URL/Web Address
  - Headings
  - Text
  - Link Text
  - Image Alt Text
  - Page Descriptions

## Analytics - you can analize information about your site visitors through tools that track how they found your site, what they are looking at and when they are leaving. Google Analytics is a great free service

## Domain Names & Hosting - in order to put your site on the web you will need a domain name and web hosting.

- Domain name = web address

- Web Hosting - uploading your site to a web server

## MDN Article: Audio and Video Elements
HTML5 comes with elements for embedding rich media in docs
`<video>`
`<audio>`
Example of writing out a video

```
<video controls>

<source src="video.mp4" type="video/mp4>

</video>
```

Using the `controls` attribute enables the default set of playback controls

## HTMLMediaElementAPI
`HTMLMediaElement` provides features to allow you to control video and audio players programmatically
Examples:

`HTMLMediaElement.play()`
`HTMLMediaElement.pause()`

## JavaScript
You can use JS to wire up controls
Add EventListeners to create things like:
  - play/pause button
  - stop button
  - rewind or fast-forward

