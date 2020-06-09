# HTML Links, CSS Layout, JS Functions

![](https://tutorialdeep.com/wp-content/uploads/2017/04/anchortag.png)

## HTML - Text Links

A webpage can contain various links that take you directly to other pages and even specific parts of a given page. These links are known as hyperlinks.

Hyperlinks allow visitors to navigate between Web sites by clicking on words, phrases, and images. Thus you can create hyperlinks using text or images available on a webpage.

**Note −** I recommend you to go through a short tutorial on Understanding URL

### Linking to other website
A link is specified using HTML tag `<a>`. This tag is called anchor tag and anything between the opening `<a>` tag and the closing `</a>` tag becomes part of the link and a user can click that part to reach to the linked document. Following is the simple syntax to use `<a>` tag.

![](https://lh3.googleusercontent.com/proxy/aE99u_FKEI5QUcxfXUNDufiddXrUw7ms_4cO-GaXc927KKkgdhmOZE57kLp2Y7lSQqsw9qn8b8j4sR4-9_kDV8UvNoGDwFxKDoxogizEWrnUCL20hebCBCtwmtBAcR4KAue96jAB-FQsrMRPq-ZfsGOFBIN3PfXfg1-pINC1)

```
<a href = "Document URL" ... attributes-list>Link Text</a> 
```

_Example_
Let's try following example which links https://www.waleedafifi.com at your page −

```
<!DOCTYPE html>
<html>
   
   <head>
      <title>Hyperlink Example</title>
   </head>
	
   <body>
      <p>Click following link</p>
      <a href = "https://www.waleedafifi.com" target = "_self">Tutorials</a>
   </body>
	
</html>
```

### Linking to another page

When you are linking to other pages within the same site, you do not need to specify the domain name in the URL. You can use a shorthand known as a relative URL.

![](https://www.computerhope.com/jargon/h/html-tag.gif)

```
<p>
    <ul>
        <li>
            <a href="index.html">Home</a>
        </li> 
        <li>
            <a href="about-us.html">About</a>
        </li> 
        <li>
            <a href="movies.html">Movies</a>
        </li> 
        <li>
            <a href="contact.html">Contact</a>
        </li>
    </ul>
</p>
```

### Directory structure
On larger websites it's a good idea to organize your code by placing the pages for each different section of the site into a new folder. Folders on a website are sometimes referred to as directories.

![](https://stuyhsdesign.files.wordpress.com/2015/09/directory-structure1.png?w=656)

**structure**

The diagram on the right shows the directory structure for a fictional entertainment listings website called ExampleArts.
The top-level folder is known as the root folder. (In this example, the root folder is called examplearts.) The root folder contains all of the other files and folders for a website.

**RelationShips**

The relationship between files and folders on a website is described using the same terminology as a family tree.

**HomePages**

![](https://blog.hubspot.com/hs-fs/hubfs/hubspot-homepage-design-update.png?width=730&height=381&name=hubspot-homepage-design-update.png)

The main homepage of a site written in HTML (and the homepages of each section in a child folder) is called index.html.

### Relative URL
Relative URLs can be used when linking to pages within your own website. They provide a shorthand way of telling the browser where to find your files.


### Email Link

`mailto:` To create a link that starts up the user's email program and addresses an email to a specified email address, you use the `<a>` element. However, this time the value of the href attribute starts with mailto: and is followed by the email address you want the email to be sent to.

![](https://3.bp.blogspot.com/_nv0jFbWmHs8/SiE9C5BQvGI/AAAAAAAAAck/ZkRV38sLd7U/s400/HTML-Codes_EmailLink.jpg)

### Opnning links in a new window

`target` If you want a link to open in a new window, you can use the target attribute on the opening `<a>` tag. The value of this attribute should be `_blank`.


### Linking specific part on the same page

`#` At the top of a long page you might want to add a list of contents that links to the corresponding sections lower down. Or you might want to add a link from part way down the page back to the top of it to save users from having to scroll back to the top.



# HTML - Layouts

![](https://i.pinimg.com/originals/46/e2/1c/46e21c46e7001fca6554cd45562268fa.jpg)

A webpage layout is very important to give better look to your website. It takes considerable time to design a website's layout with great look and feel.

Now-a-days, all modern websites are using CSS and JavaScript based framework to come up with responsive and dynamic websites but you can create a good layout using simple HTML tables or division tags in combination with other formatting tags. This chapter will give you few examples on how to create a simple but working layout for your webpage using pure HTML and its attributes.

## Key ConCepts in positioning eLements

![](https://miro.medium.com/max/2800/1*AFeOAqXNJJdfYAjfXiJ9AQ.jpeg)

### Building Blocks
CSS treats each HTML element as if it is in its own box. This box will either be a block-level box or an inline box.
Block-level boxes start on a new line and act as the main building blocks of any layout, while inline boxes flow between surrounding text. You can control how much space each box takes up by setting the width of the boxes (and sometimes the height, too). To separate boxes, you can use borders, margins, padding, and background colors.

_Block-level elements_

start on a new line Examples include:
```
 <h1>
 <p> 
 <ul> 
 <li>
```

_inline elements_

flow in Between surrounding text Examples include:
```
<img> 
<b> 
<i>
```
![](https://i.ibb.co/R353HRd/Screen-Shot-2020-06-09-at-15-45-22.png)

### Containing Element
If one block-level element sits inside another block-level element then the outer box is known as the containing or parent element.
It is common to group a number of elements together inside a `<div>` (or other block-level) element. For example, you might group together all of the elements that form the header of a site (such as the logo and the main navigation). The `<div>` element that contains this group of elements is then referred to as the containing element.

![](https://i.ibb.co/kggJkXN/Screen-Shot-2020-06-09-at-15-46-07.png)


### ControLLing the position of eLements

![](https://miro.medium.com/max/880/1*vv_brCwJNVFsBHQEfYC7zQ.png)

CSS has the following positioning schemes that allow you to control the layout of a page: normal flow, relative positioning, and absolute positioning. You specify the positioning scheme using the position property in CSS. You can also float elements using the float property.

1. Normal flow
2. Relative Positioning
3. Absolute Positioning
4. fixed Positioning
5. floating elements

**Normal flow:** Every block-level element appears on a new line, causing each item to appear lower down the page than the previous one. Even if you specify the width
of the boxes and there is space for two elements to sit side-by- side, they will not appear next to each other. This is the default behavior (unless you tell the browser to do something else).

**Relative Positioning:** This moves an element from the position it would be in normal flow, shifting it to the top, right, bottom, or left of where it would have been placed. This does not affect the position of surrounding elements; they stay in the position they would be in in normal flow.

**Absolute Positioning:** This positions the element in relation to its containing element. It is taken out of normal flow, meaning that it does not affect the position
of any surrounding elements (as they simply ignore the space it would have taken up). Absolutely positioned elements move as users scroll up and down the page.

**fixed Positioning:** This is a form of absolute positioning that positions the element in relation to the browser window, as opposed to the containing element. Elements with fixed positioning do not affect the position of surrounding elements and they do not move when the user scrolls up or down the page

**floating elements:** Floating an element allows you to take that element out of normal flow and position
it to the far left or right of a containing box. The floated element becomes a block-level element around which other content can flow.

![](https://kovshenin.com/wp-content/uploads/sites/5/2010/03/position-relative-4.png)


### Position in code
_anrotrimCLaeL fLow_ `position:static`

In normal flow, each block-level element sits on top of the next one. Since this is the default way in which browsers treat HTML elements, you do not need a CSS property to indicate that elements should appear in normal flow, but the syntax would be:
`position: static;`

_reLative Posionining_ `position:relative`

Relative positioning moves an element in relation to where it would have been in normal flow. For example, you can move it 10 pixels lower than it would have been in normal flow or 20% to the right.

You then use the offset properties (top or bottom and left or right) to indicate how far to move the element from where it would have been in normal flow.

_Absolute Positioning_ `position:absolute`

When the position property is given a value of absolute, the box is taken out of normal flow and no longer affects the position of other elements on the page. (They act like it is not there.)
The box offset properties (top or bottom and left or right) specify where the element should appear in relation to its containing element.

_Fixed Positioning_ `position:fixed`

Fixed positioning is a type of absolute positioning that requires the position property to have a value of fixed.
It positions the element in relation to the browser window. Therefore, when a user scrolls down the page, it stays in the exact same place. It is a good idea to try this example in your browser to see the effect.

![](https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcQMWCxsHRXvnp4JfiOGytoYlZ86An1nDmt6krmrOAnibSmO9nLu&usqp=CAU)

_Overlapping Element_ `z-index`

![](https://elementor.com/wp-content/uploads/2017/06/z-index.png)

When you use relative, fixed, or absolute positioning, boxes can overlap. If boxes do overlap, the elements that appear later in the HTML code sit on top of those that are earlier in the page.

_Floating_ `float`

The float property allows you to take an element in normal flow and place it as far to the left or right of the containing element as possible.

**Using float to place element side by side**
```
<!DOCTYPE html>
<html>
    <head>
        <style>
            img {
                float: left;
            }
        </style>
    </head>
    <body>

        <p>
            In this example, the image will float to the left in the paragraph, and the text in the paragraph will wrap around the image.
        </p>

        <p>
            <img src="pineapple.jpg" alt="Pineapple" style="width:170px;height:170px;margin-right:15px;">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus imperdiet, nulla et dictum interdum, nisi lorem egestas odio, vitae scelerisque enim ligula venenatis dolor. Maecenas nisl est, ultrices nec congue eget, auctor vitae massa. Fusce luctus vestibulum augue ut aliquet. Mauris ante ligula, facilisis sed ornare eu, lobortis in odio. Praesent convallis urna a lacus interdum ut hendrerit risus congue. Nunc sagittis dictum nisi, sed ullamcorper ipsum dignissim ac. In at libero sed nunc venenatis imperdiet sed ornare turpis. Donec vitae dui eget tellus gravida venenatis. Integer fringilla congue eros non fermentum. Sed dapibus pulvinar nibh tempor porta. Cras ac leo purus. Mauris quis diam velit.
        </p>

    </body>
</html>

```

![](https://www.formget.com/wp-content/uploads/2014/09/float-left.png)


**Creating multi column with float**

![](https://i.stack.imgur.com/UhSyI.jpg)



![](https://miro.medium.com/max/880/1*dgaBPGGBIvFJM9BGlzkQQg.png)
## Screen Size and Reselution

![](https://www.seobility.net/en/wiki/images/6/6f/Media-Queries.png)

* Screen Size: Different visitors to your site will have different sized screens that show different amounts of information, so your design needs to be able to work on a range of different sized screens.

* Resolution refers to the number of dots a screen shows per inch. Some devices have a higher resolution than desktop computers and most operating systems allow users to adjust the resolution of their screens


## page sizes

Because screen sizes and display resolutions vary so much, web designers often try to create pages of around 960-1000 pixels wide (since most users will be able to see designs this wide on their screens).


![](https://image.slidesharecdn.com/pagelayout-150929142530-lva1-app6891/95/page-layouts-flexible-and-fixed-layout-with-css-11-638.jpg?cb=1443536908)

## fixed width Layouts
Fixed width layout designs do not change size as the user increases or decreases the size of their browser window. Measurements tend to be given in pixels.

**Advantages**
● Pixel values are accurate at controlling size and positioning of elements.
● The designer has far greater control over the appearance and position of items on the page than with liquid layouts.
● You can control the lengths of lines of text regardless of the size of the user's window.
● The size of an image will always remain the same relative to the rest of the page.

**Dissadvantages**
● You can end up with big gaps around the edge of a page.
● If the user's screen is a much higher resolution than the designer's screen, the page can look smaller and text can be harder to read.
● If a user increases font sizes, text might not fit into the allotted spaces.
● The design works best on devices that have a site or resolution similar to that of desktop or laptop computers.
● The page will often take up more vertical space than a liquid layout with the same content.


## Liquid Layouts
Liquid layout designs stretch and contract as the user increases or decreases the size of their browser window. They tend to use percentages.

**Advantages**
● Pages expand to fill the entire browser window so there are no spaces around the page on a large screen.
● If the user has a small window, the page can contract to fit it without the user having to scroll to the side.
● The design is tolerant of users setting font sizes larger than the designer intended (because the page can stretch).

**Dissadvantages**
● If you do not control the width of sections of the page then the design can look very different than you intended, with unexpected gaps around certain elements or items squashed together.
● If the user has a wide window, lines of text can become very long, which makes them harder to read.
● If the user has a very narrow window, words may be squashed and you can end up with few words on each line.
● If a fixed width item (such as an image) is in a box that is too small to hold it (because the user has made the window smaller) the image can overflow over the text.


![](https://i.ytimg.com/vi/Rpm7cSWjiGA/maxresdefault.jpg)

## Layout grids
Composition in any visual art (such as design, painting, or photography) is the placement or arrangement of visual elements — how they are organized on a page. Many designers use a grid structure to help them position items on a page, and the same is true for web designers.

possibLe Layouts: 960 pixeL wide 12 CoLumn grid



## Css frameworKs

CSS frameworks aim to make your life easier by providing the code for common tasks, such as creating layout grids, styling forms, creating printer-friendly versions of pages and so on. You can include the CSS framework code in your projects rather than writing the CSS from scratch.

**advantages**

● They save you from repeatedly writing code for the same tasks.
● They will have been tested across different browser versions (which helps avoid browser bugs).

**disadvantages**
● They often require that you use class names in your HTML code that only control the presentation of the page (rather than describe its content).
● In order to satisfy a wide variety of needs, they often contain more code than you need for your particular web page (commonly referred to as code “bloat”).


## Multiple styLe sheets
`@import`
`link`

There are two ways to add multiple style sheets to a page:
1. Your HTML page can link to one style sheet and that stylesheet can use the @import rule to import other style sheets.
2. In the HTML you can use a separate `<link>` element for each style sheet.

```
// CSS File

@import url("tables.css"); 
@import url("typography.css"); 
body {
    color: #666666; background-color: #f8f8f8; text-align: center;
}
#page {
    width: 600px;
    text-align: left; margin-left: auto; margin-right: auto; border: 1px solid #d6d6d6; padding: 20px;
}
h3 {
  color: #547ca0;
}

```

```
<!-- HTML -->

<!DOCTYPE html>
<html>
    <head>
        <title>Multiple Style Sheets - Import</title>
        <link rel="stylesheet" type="text/css"
        href="css/styles.css" />
    </head>
    <body>
        <!-- HTML page content here -->
    </body>
</html>



<!DOCTYPE html>
<html>
    <head>
        <title>Multiple Style Sheets - Link</title> 
        <link rel="stylesheet" type="text/css" href="css/site.css" />
        <link rel="stylesheet" type="text/css" href="css/tables.css" />
        <link rel="stylesheet" type="text/css"href="css/typography.css" /> 
    </head>
    <body>
        <!-- HTML page content here -->
    </body>
</html>

```



![](https://www.jstips.co/assets/images/share-fb.png)

# Functions

__WHAT IS A FUNCTION?__
Functions let you group a series of statements together to perform a specific task. If different parts of a script repeat the same task, you can reuse the function (rather than repeating the same set of statements).

### A BASIC FUNCTION
```
var msg = 'Sign up to receive our newsletter for 10% off!';
function updateMessage() {
    var el = document.getElementByld('message'};
    el .textContent = msg; 
}
updateMessage(};
```

In this example, the user is shown a message at the top of the page. The message is held in an HTML element whose id attribute has a value of message. The message is going to be changed using JavaScript.

To call the function whe do like this `FunctionName();`


![](https://i2.wp.com/www.helloitsliam.com/wp-content/uploads/2018/06/062318_1553_IsJavaScrip1.png?ssl=1)
### Declaring a function with Args
```
function MyFunction(width, height) {
    return widtth * height;
}
```
And to call this function like `MyFunction(3, 5);`