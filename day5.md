Design web pages with CSS

CSS - Cascading Style Sheets. CSS describes how HTML elements are to be displayed on screen, paper, or in other media. CSS saves a lot of work. It can control the layout of multiple web pages all at once.

RGB - RGB Value is a formula of Red, Green, Blue. Each parameter defines the intensity of the color between 0 and 255.

RGB (255,0,0) is displayed as red. The indicator should be that red is the highest value (255), and the other are set to 0.

RGB (0,0,0) is black
RGB (255,255,255) is white

HSL - HSL color can be specified using the hue, saturation, and lightness in the form of (hue, saturation, lighness)

   Hue is a degree (0 to 360)
   Saturation is a percentage, 0% is a shade of gray, and 100% is the full color
   Lightness is also a percentage. 0% iis black, 50% is neighter light or dark, 100% is white

Hex codes - HEX color can be specified using a hexadecimal value in the form of #rrggbb

    rr(red), gg(green), and bb(blue) are hexadecimal values between 00 and ff (same as decimal 0-255)

    for example, #ff0000 is displayed as red, because red is set to the highest value (ff) and the others are set to the lowest value (00).

Layout - how a website is divided into headers, menues, content, and a footer

Rule - CSS comprises of style rules interpreted by the browser and then applied to the corresponding elements. A style rule is made of three parts:

Selector - an HTML tag at which a style will be applied. This could be any tage like <h1> or <table> etc.

Property & value - a property is a type of attribute of HTML tag. all the HTML attributes are converted into CSS properties. They could be color, border, etc. Values assigned to properities. For example, the color property can have value either red or  #F1F1F1 etc.

Example CSS Style Rule Syntax:

selector { property: value }

Example: all <p> elements will be center-aligned, with red text color

p {
  color: red;
  text-align: center;
}

Example Explained:

p is a selector in CSS (it points to the HTML element you want to style: <p>).
color is a property, and red is the property value
text-align is a property, and center is the property value


Curly braces - surround declaration blocks. Declaration blocks contain one or more declarations separated by semicolons. Each declaration includes a CSS property name and a value, seperated by a colon.

Example CSS rule-set consists of a selector and a declaration block:

Selector {Declaration - property:value; property:value;}
h1 {color:blue;font-size:12pxx;}
