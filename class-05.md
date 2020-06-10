![](https://i.ytimg.com/vi/Bor5lkRyeGo/hqdefault.jpg)

# HTML Images

## Inserting Images into Web Pages

Images enhance visual appearance of the web pages by making them more interesting and colorful.

The `<img>` tag is used to insert images in the HTML documents. It is an empty element and contains attributes only. The syntax of the `<img>` tag can be given with:

```
<img src="url" alt="some_text">
```

![](https://www.miltonmarketing.com/wp-content/uploads/2018/03/mmhtmlimgtag424243image-tag-example.jpg)

The following example inserts three images on the web page:

```
<img src="kites.jpg" alt="Flying Kites">
<img src="sky.jpg" alt="Cloudy Sky">
<img src="balloons.jpg" alt="Balloons">
```

Each image must carry at least two attributes: the `src` attribute, and an `alt` attribute.

The `src` attribute tells the browser where to find the image. Its value is the URL of the image file.

Whereas, the `alt` attribute provides an alternative text for the image, if it is unavailable or cannot be displayed for some reason. Its value should be a meaningful substitute for the image.

![](https://www.jquery-az.com/wp-content/uploads/2015/12/2.3-HTML-img-src-not-exist.jpg)

**Note:** Like `<br>` , the `<img>` element is also an empty element, and does not have a closing tag. However, in XHTML it closes itself ending with "/>".

**Tip:** The required `alt` attribute provides alternative text description for an image if a user for some reason cannot able to view it because of slow connection, image is not available at the specified URL, or if the user uses a screen reader or non-graphical browser.


```
<img src="kites.jpg" alt="Flying Kites" width="300" height="300">
<img src="sky.jpg" alt="Cloudy Sky" width="250" height="150">
<img src="balloons.jpg" alt="Balloons" width="200" height="200">
```

You can also use the `style` attribute to specify width and height for the images. It prevents style sheets from changing the image size accidently, since inline style has the highest priority.


```
<img src="kites.jpg" alt="Flying Kites" style="width: 300px; height: 300px;">
<img src="sky.jpg" alt="Cloudy Sky" style="width: 250px; height: 150px;">
<img src="balloons.jpg" alt="Balloons" style="width: 200px; height: 200px;">
```

## Using the HTML5 Picture Element
Sometimes, scaling an image up or down to fit different devices (or screen sizes) doesn't work as expected. Also, reducing the image dimension using the width and height attribute or property doesn't reduce the original file size. To address these problems HTML5 has introduced the `<picture>` tag that allows you to define multiple versions of an image to target different types of devices.

```
<picture>
    <source media="(min-width: 1000px)" srcset="logo-large.png">
    <source media="(max-width: 500px)" srcset="logo-small.png">
    <img src="logo-default.png" alt="My logo">
</picture>
```

![](https://pbs.twimg.com/media/D6Hub1UWsAAACWz.jpg)

**Note:** The browser will evaluate each child `<source>` element and choose the best match among them; if no matches are found, the URL of the `<img>` element's src attribute is used. Also, the `<img>` tag must be specified as the last child of the `<picture>` element.


### Resize image proportionally with CSS

```
<!DOCTYPE html> 
<html> 
	<head> 
		<title>cell padding</title> 
		<style> 
			.gfg { 
				width:auto; 
				text-align:center; 
				padding:20px; 
			} 
			img { 
				max-width:100%; 
						height:auto; 
			} 
		</style> 
	</head> 
	<body> 
		<div class = "gfg"> 
			<p id="my-image"><img src= 
                "https://media.geeksforgeeks.org/wp-content/uploads/geeksforgeeks-17.png"> 
			</p> 
		</div> 
	</body> 
</html> 
```

![](https://media.geeksforgeeks.org/wp-content/uploads/resize1-1.png)



![](https://html.com/wp-content/uploads/css-colors-1024x512.png)

# CSS Color

## Setting Color Property

The `color` property defines the text color (foreground color in general) of an element.

For instance, the `color` property specified in the `body` selector defines the default text color for the whole page. Let's try out the following example to see how it works:

```
h1 {
    color: #ff5722;
}
```

![](https://s3.amazonaws.com/videos_mxm/caretas/estructura-css_37167_1_11380.jpg)

**Note:** The color property normally inherits the color value from their parent element, except the case of anchor elements. For example, if you specify color for the body element it will automatically be passed down to the headings, paragraphs, etc.


## Defining Color Values

Colors in CSS most often specified in the following formats:

1. a color name - like "red"
2. a HEX value - like "#ff0000"
3. an RGB value - like "rgb(255, 0, 0)"

![](https://i.ytimg.com/vi/oeovZTgMj0Y/maxresdefault.jpg)

## Color Keywords
CSS defines the few color keywords which lets you specify color values in an easy way.

These basic color keywords are: aqua, black, blue, fuchsia, gray, green, lime, maroon, navy, olive, purple, red, silver, teal, white, and yellow. The color names are case-insensitive.

```
h1 {
    color: red;
}
p {
    color: purple;
}
```

![](https://www.wikihow.com/images/thumb/b/be/122247-12-1.jpg/aid122247-v4-728px-122247-12-1.jpg.webp)

## HEX Color Values
Hex (short for Hexadecimal) is by far the most commonly used method of defining color on the web.

Hex represent colors using a six-digit code, preceded by a hash character, like `#rrggbb`, in which `rr`, `gg`, and `bb` represents the red, green and blue component of the color respectively.

```
h1 {
    color: #ffa500;
}
p {
    color: #00ff00;
}
```

![](https://datashoptalk.com/wp-content/uploads/2018/05/review-1.png)

**Note:** Hexadecimal or Hex refers to a numbering scheme that uses 16 characters as its base. It uses the numbers 0 through 9 and the letters A, B, C, D, E and F which corresponds to the decimal numbers 10, 11, 12, 13, 14 and 15 respectively.

**Tip:** If hexadecimal code of a color has value pairs, it can also be written in shorthand notation to avoid extra typing, for example, the hex color value #ffffff can be also be written as #fff, #000000 as #000, #00ff00 as #0f0, #ffcc00 as #fc0, and so on.


## RGB Color Values

Colors can be defined in the RGB model (Red, Green, and Blue) using the rgb() functional notation.

```
h1 {
    color: rgb(255, 165, 0);
}
p {
    color: rgb(0, 255, 0);
}
```

![](https://lh3.googleusercontent.com/proxy/_J7mChITD3JWsogUhHKXLYK_n0Dr-V0XB4v4ecr2hv5WQaTOC3mp2CIXq_ajoG1z21HBHOL5z7ng5FgANhNZOQWDbjF9xhqxU88-MQIILOqUoU_czfRq-pPT-l-q2toyRTiWv6RX3RYtT8f9FHcaoX1btJB_2xiH9MMEeEeg0T8LhHP53Pn0Z-mvLVmOjQ)



![](https://www.pluralsight.com/content/pluralsight/en/blog/creative-professional/wha/whats-stuff-top-html5-document/_jcr_content/main/hero_blog_block/image-res.img.jpg/1501612385518.jpg)
# Text

## Formatting Text with HTML

HTML provides several tags that you can use to make some text on your web pages to appear differently than normal text, for example, you can use the tag `<b>` to make the text bold, tag `<i>` to make the text italic, tag `<mark>` to highlight the text, tag `<code>` to display a fragment of computer code, tags `<ins>` and `<del>` for marking editorial insertions and deletions, and more.

```
<p>This is <b>bold text</b>.</p>
<p>This is <strong>strongly important text</strong>.</p>
<p>This is <i>italic text</i>.</p>
<p>This is <em>emphasized text</em>.</p>
<p>This is <mark>highlighted text</mark>.</p>
<p>This is <code>computer code</code>.</p>
<p>This is <small>smaller text</small>.</p>
<p>This is <sub>subscript</sub> and <sup>superscript</sup> text.</p>
<p>This is <del>deleted text</del>.</p>
<p>This is <ins>inserted text</ins>.</p>
```

![](https://steemitimages.com/DQmaK9do4yiQuBComi9Qv21ZR1h9iHYxk7tN1bSjdN9zExN/Example.png)

## Difference between <strong> and <b> tag
Both `<strong>` and `<b>` tags render the enclosed text in a bold typeface by default, but the `<strong>` tag indicates that its contents have strong importance, whereas the `<b>` tag is simply used to draw the reader's attention without conveying any special importance.

```
<p><strong>WARNING!</strong> Please proceed with caution.</p>
<p>The concert will be held at <b>Hyde Park</b> in London.</p>
```

## Difference between <em> and <i> tag
Similarly, both `<em>` and `<i>` tags render the enclosed text in italic type by default, but the `<em>` tag indicates that its contents have stressed emphasis compared to surrounding text, whereas the `<i>` tag is used for marking up text that is set off from the normal text for readability reasons, such as a technical term, an idiomatic phrase from another language, a thought, etc.

```
<p>Cats are <em>cute</em> animals.</p>
<p>The <i>Royal Cruise</i> sailed last night.</p>
```

**Note:** Use the `<em>` and `<strong>` tags when the content of your page requires that certain words or phrases should have strong emphasis or importance. Also, in HTML5 the `<b>` and `<i>` tags have been redefined, earlier they don't have semantic meaning.


# CSS Text

## Formatting Text with CSS
CSS provides several properties that allows you to define various text styles such as color, alignment, spacing, decoration, transformation, etc. very easily and effectively.

The commonly used text properties are: `text-align`, `text-decoration`, `text-transform`, `text-indent`, `line-height`, `letter-spacing`, `word-spacing`, and more. These properties give you precise control over the visual appearance of the characters, words, spaces, and so on.

## Text Color
The color of the text is defined by the CSS `color` property.

```
body {
    color: #434343;
}
```

## Text Alignment
The `text-align` property is used to set the horizontal alignment of the text.

Text can be aligned in four ways: to the left, right, centre or justified (straight left and right margins).

```
h1 {
    text-align: center;
}
p {
    text-align: justify;
}
```

**Note:** When text-align is set to justify, each line is stretched so that every line has equal width (except the last line), and the left and right margins are straight. This alignment is generally used in publications such as magazines and newspapers.

![](https://www.tutorialrepublic.com/lib/images/text-align-illustration.png)


![](https://i.ytimg.com/vi/WbDNbRKRPEA/maxresdefault.jpg)
## Text Decoration

The `text-decoration` property is used to set or remove decorations from text.

This property typically accepts one of the following values: `underline`, `overline`, `line-through`, and none. You should avoid underline text that is not a link, as it might confuse the visitor.

```
h1 {
    text-decoration: overline;
}
h2 {
    text-decoration: line-through;
}
h3 {
    text-decoration: underline;
}
```


## Removing the Default Underline from Links
The `text-decoration` property is extensively used to remove the default underline from the HTML hyperlinks. You can further provide some other visual cues to make it stand out from the normal text, for example, using dotted border instead of solid underline.

```
a {
    text-decoration: none;
    border-bottom: 1px dotted;
}
```

![](https://i2.wp.com/css-tricks.com/wp-content/uploads/2016/09/familiar.png?ssl=1)