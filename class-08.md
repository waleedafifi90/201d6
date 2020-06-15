![](https://i.pinimg.com/originals/93/c1/f2/93c1f27ecfcd1ce98a684b300ec2a41b.jpg)

# Coding An HTML 5 Layout From Scratch

## Best practice to learn HTML and CSS is a coding example

At the end of this article you'll learn how to:

* Use Graceful Degradation techniques and technologies to keep things in place for legacy browsers.
* Use Progressive Enhancement techniques and technologies to be up to date with the latest trends.
* Use HTML5 alongside a rising technology: Microformats.
* Have a clear vision of some of the most exciting new features HTML5 and CSS3 will bring.


## The HTML 5 Layout - Before We Begin…

There’s a couple of things you have to bear in mind before adventuring on the new markup boat. HTML5 is not for everyone. Therefore, you must be wise and select how and where to use it. Think of all the markup flavours you’ve got available as tools: use the right one for the right job. Therefore, if your website is coded in standards compliant **XHTML strict** there’s no real need to change to HTML5.

### The Design
This will be the sample layout we’ll be coding:

![](https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/12dfc62a-6854-414b-97c7-2c4f3a50f7ae/design-thumb.png)

A very basic layout brilliantly named Smashing _HTML5!_ which covers most of the elements we can start coding using HTML5. Basically: the page’s name and it’s slogan, a menu, a highlighted (featured) area, a post listing, an extras section with some external links, an about box and finally a copyright statement.


### The Markup
As a very basic start to our markup, this is our html file skeleton:

```
 
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8" />
<title>Smashing HTML5!</title>

<link rel="stylesheet" href="css/main.css" type="text/css" />

<!--[if IE]>
  <script src="http://html5shiv.googlecode.com/svn/trunk/html5.js"></script><![endif]-->
<!--[if lte IE 7]>
  <script src="js/IE8.js" type="text/javascript"></script><![endif]-->
<!--[if lt IE 7]>

  <link rel="stylesheet" type="text/css" media="all" href="css/ie6.css"/><![endif]-->
</head>

<body id="index" class="home">
</body>
</html>
```

![](https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/acff5986-b283-45ac-949e-e8a690259ba9/design-x-ray.png)

**THE HEADER**

![](https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/4c15d404-c38a-4e32-aae2-e37d981ec060/header-block.png)

The layout header is as simple as it gets. The new `<header>` tag spec reads as follows:

_The header element represents a group of introductory or navigational aids_


Thus it is more than logic that we use this to markup our header. We’ll also use the `<nav>` tag. The spec reads:


```

<header id="banner" class="body">
  <h1><a href="#">Smashing HTML5! <strong>HTML5 in the year <del>2022</del> <ins>2009</ins></strong></a></h1>

  <nav><ul>
    <li class="active"><a href="#">home</a></li>
    <li><a href="#">portfolio</a></li>

    <li><a href="#">blog</a></li>
    <li><a href="#">contact</a></li>
  </ul></nav>

</header><!-- /#banner -->

```

**FEATURED BLOCK**
![](https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/7640bcbe-eae9-4942-b7c5-e92e5084341d/featured-block.png)

Next is the featured block. This is best marked up as an `<aside>` since it’s spec says:

The **aside** element represents a section of a page that consists of content that is tangentially related to the content around the aside element, and which could be considered separate from that content. Such sections are often represented as sidebars in printed typography.

That pretty much sums up our featured block, so let’s go for it. Now, inside of this block there’s a lot going on. Firstly, this is an article, so alongside the `<aside>` tag, we should be using `<article>` right away.


Featured block code will look like this in the end:

```

<aside id="featured" class="body"><article>
  <figure>
    <img src="images/temp/sm-logo.gif" alt="Smashing Magazine" />
  </figure>
  <hgroup>

    <h2>Featured Article</h2>
    <h3><a href="#">HTML5 in Smashing Magazine!</a></h3>
  </hgroup>
  <p>Discover how to use Graceful Degradation and Progressive Enhancement techniques to achieve an outstanding, cross-browser <a href="http://dev.w3.org/html5/spec/Overview.html" rel="external">HTML5</a> and <a href="http://www.w3.org/TR/css3-roadmap/" rel="external">CSS3</a> website today!</p>

</article></aside><!-- /#featured -->
```

**THE LAYOUT’S BODY**
![](https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/24818cac-5cdb-4ae3-91e1-4646eb41685b/body-block.png)


**Sections**

Next is our document’s body, where all the content will be. Since this block represents a generic document section and a section is a thematic grouping of content, this one is without a doubt a `<section>` tag.

```

<section id="content" class="body">

  <ol id="posts-list" class="hfeed">

    <li><article class="hentry">  
      <header>
        <h2 class="entry-title"><a href="#" rel="bookmark" title="Permalink to this POST TITLE">This be the title</a></h2>
      </header>

      <footer class="post-info">
        <abbr class="published" title="2005-10-10T14:07:00-07:00"><!-- YYYYMMDDThh:mm:ss+ZZZZ -->
          10th October 2005
        </abbr>

        <address class="vcard author">
          By <a class="url fn" href="#">Enrique Ramírez</a>

        </address>
      </footer><!-- /.post-info -->

      <div class="entry-content">
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque venenatis nunc vitae libero iaculis elementum. Nullam et justo <a href="#">non sapien</a> dapibus blandit nec et leo. Ut ut malesuada tellus.</p>

      </div><!-- /.entry-content -->
    </article></li>

    <li><article class="hentry">
      ...
    </article></li>

    <li><article class="hentry">
      ...
    </article></li>
  </ol><!-- /#posts-list -->

</section><!-- /#content -->

```

![](https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/f503db25-b6f2-42bf-b78a-b83e29f9615b/extras-block.png)

The extras block is yet another section of our document. You might struggle for a while deciding whether an `<aside>` or a `<section>` tag would be best for this section. In the end, this section could not be considered separate from the main content since it contains the blogroll links and some social information of the website. Thus, a `<section>` element is more appropriate.

For the rest of the block there’s nothing much to decide. It’s the everyday `<ul>` accommodated set of links on both sections, which in the end may look like this:


```

<section id="extras" class="body">
  <div class="blogroll">
    <h2>blogroll</h2>
    <ul>

      <li><a href="#" rel="external">HTML5 Doctor</a></li>
      <li><a href="#" rel="external">HTML5 Spec (working draft)</a></li>
      <li><a href="#" rel="external">Smashing Magazine</a></li>

      <li><a href="#" rel="external">W3C</a></li>
      <li><a href="#" rel="external">Wordpress</a></li>
      <li><a href="#" rel="external">Wikipedia</a></li>

      <li><a href="#" rel="external">HTML5 Doctor</a></li>
      <li><a href="#" rel="external">HTML5 Spec (working draft)</a></li>
      <li><a href="#" rel="external">Smashing Magazine</a></li>

      <li><a href="#" rel="external">W3C</a></li>
      <li><a href="#" rel="external">Wordpress</a></li>
      <li><a href="#" rel="external">Wikipedia</a></li>

      <li><a href="#" rel="external">HTML5 Doctor</a></li>
      <li><a href="#" rel="external">HTML5 Spec (working draft)</a></li>
      <li><a href="#" rel="external">Smashing Magazine</a></li>

      <li><a href="#" rel="external">W3C</a></li>
      <li><a href="#" rel="external">Wordpress</a></li>
      <li><a href="#" rel="external">Wikipedia</a></li>

    </ul>
  </div><!-- /.blogroll -->

  <div class="social">
    <h2>social</h2>
    <ul>

      <li><a href="http://delicious.com/enrique_ramirez" rel="me">delicious</a></li>
      <li><a href="http://digg.com/users/enriqueramirez" rel="me">digg</a></li>
      <li><a href="http://facebook.com/enrique.ramirez.velez" rel="me">facebook</a></li>

      <li><a href="http://www.lastfm.es/user/enrique-ramirez" rel="me">last.fm</a></li>
      <li><a href="http://website.com/feed/" rel="alternate">rss</a></li>
      <li><a href="http://twitter.com/enrique_ramirez" rel="me">twitter</a></li>

    </ul>
  </div><!-- /.social -->
</section><!-- /#extras -->
```


### SUMMING IT ALL UP

So, after all this mess, the complete code looks like this:

```

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8" />
<title>Smashing HTML5!</title>

<link rel="stylesheet" href="css/main.css" type="text/css" />

<!--[if IE]>
  <script src="http://html5shiv.googlecode.com/svn/trunk/html5.js"></script><![endif]-->
<!--[if lte IE 7]>
  <script src="js/IE8.js" type="text/javascript"></script><![endif]-->

<!--[if lt IE 7]>
  <link rel="stylesheet" type="text/css" media="all" href="css/ie6.css"/><![endif]-->
</head>

<body id="index" class="home">

<header id="banner" class="body">
  <h1><a href="#">Smashing HTML5! <strong>HTML5 in the year <del>2022</del> <ins>2009</ins></strong></a></h1>

  <nav><ul>
    <li class="active"><a href="#">home</a></li>
    <li><a href="#">portfolio</a></li>

    <li><a href="#">blog</a></li>
    <li><a href="#">contact</a></li>
  </ul></nav>

</header><!-- /#banner -->  

<aside id="featured" class="body"><article>
  <figure>
    <img src="images/temp/sm-logo.gif" alt="Smashing Magazine" />
  </figure>
  <hgroup>

    <h2>Featured Article</h2>
    <h3><a href="#">HTML5 in Smashing Magazine!</a></h3>
  </hgroup>
  <p>Discover how to use Graceful Degradation and Progressive Enhancement techniques to achieve an outstanding, cross-browser <a href="http://dev.w3.org/html5/spec/Overview.html" rel="external">HTML5</a> and <a href="http://www.w3.org/TR/css3-roadmap/" rel="external">CSS3</a> website today!</p>

</article></aside><!-- /#featured -->

<section id="content" class="body">
  <ol id="posts-list" class="hfeed">
    <li><article class="hentry">  
      <header>
        <h2 class="entry-title"><a href="#" rel="bookmark" title="Permalink to this POST TITLE">This be the title</a></h2>

      </header>

      <footer class="post-info">
        <abbr class="published" title="2005-10-10T14:07:00-07:00"><!-- YYYYMMDDThh:mm:ss+ZZZZ -->
          10th October 2005
        </abbr>

        <address class="vcard author">

          By <a class="url fn" href="#">Enrique Ramírez</a>
        </address>
      </footer><!-- /.post-info -->

      <div class="entry-content">

        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque venenatis nunc vitae libero iaculis elementum. Nullam et justo <a href="#">non sapien</a> dapibus blandit nec et leo. Ut ut malesuada tellus.</p>
      </div><!-- /.entry-content -->
    </article></li>

    <li><article class="hentry">
      ...
    </article></li>

    <li><article class="hentry">
      ...
    </article></li>

  </ol><!-- /#posts-list -->
</section><!-- /#content -->

<section id="extras" class="body">
  <div class="blogroll">
    <h2>blogroll</h2>

    <ul>
      <li><a href="#" rel="external">HTML5 Doctor</a></li>
      <li><a href="#" rel="external">HTML5 Spec (working draft)</a></li>

      <li><a href="#" rel="external">Smashing Magazine</a></li>
      <li><a href="#" rel="external">W3C</a></li>
      <li><a href="#" rel="external">Wordpress</a></li>

      <li><a href="#" rel="external">Wikipedia</a></li>
      <li><a href="#" rel="external">HTML5 Doctor</a></li>
      <li><a href="#" rel="external">HTML5 Spec (working draft)</a></li>

      <li><a href="#" rel="external">Smashing Magazine</a></li>
      <li><a href="#" rel="external">W3C</a></li>
      <li><a href="#" rel="external">Wordpress</a></li>

      <li><a href="#" rel="external">Wikipedia</a></li>
      <li><a href="#" rel="external">HTML5 Doctor</a></li>
      <li><a href="#" rel="external">HTML5 Spec (working draft)</a></li>

      <li><a href="#" rel="external">Smashing Magazine</a></li>
      <li><a href="#" rel="external">W3C</a></li>
      <li><a href="#" rel="external">Wordpress</a></li>

      <li><a href="#" rel="external">Wikipedia</a></li>
    </ul>
  </div><!-- /.blogroll -->

  <div class="social">

    <h2>social</h2>
    <ul>
      <li><a href="http://delicious.com/enrique_ramirez" rel="me">delicious</a></li>
      <li><a href="http://digg.com/users/enriqueramirez" rel="me">digg</a></li>

      <li><a href="http://facebook.com/enrique.ramirez.velez" rel="me">facebook</a></li>
      <li><a href="http://www.lastfm.es/user/enrique-ramirez" rel="me">last.fm</a></li>
      <li><a href="http://website.com/feed/" rel="alternate">rss</a></li>

      <li><a href="http://twitter.com/enrique_ramirez" rel="me">twitter</a></li>
    </ul>
  </div><!-- /.social -->
</section><!-- /#extras -->

<footer id="contentinfo" class="body">
  <address id="about" class="vcard body">
    <span class="primary">
      <strong><a href="#" class="fn url">Smashing Magazine</a></strong>

      <span class="role">Amazing Magazine</span>
    </span><!-- /.primary -->

    <img src="images/avatar.gif" alt="Smashing Magazine Logo" class="photo" />
    <span class="bio">Smashing Magazine is a website and blog that offers resources and advice to web developers and web designers. It was founded by Sven Lennartz and Vitaly Friedman.</span>

  </address><!-- /#about -->
  <p>2005-2009 <a href="http://smashingmagazine.com">Smashing Magazine</a>.</p>
</footer><!-- /#contentinfo -->

</body>
</html>

```


# CSS
Just like our markup, the CSS will also have a very basic start. Call this a frameworks of sorts which I’ve been using for a long time and works fairly well. Here’s the code for our main.css file:

```

/*
  Name: Smashing HTML5
  Date: July 2009
  description: >-
  Sample layout for HTML5 and CSS3 goodness.
  Version: 1.0
  Author: Enrique Ramírez
  Autor URI: http://enrique-ramirez.com
*/

/* Imports */
@import url("reset.css");
@import url("global-forms.css");

/***** Global *****/
/* Body */
  body {
    background: #F5F4EF url('../images/bg.png');
    color: #000305;
    font-size: 87.5%; /* Base font size: 14px */
    font-family: 'Trebuchet MS', Trebuchet, 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
    line-height: 1.429;
    margin: 0;
    padding: 0;
    text-align: left;
  }

/* Headings */
h2 {font-size: 1.571em} /* 22px */
h3 {font-size: 1.429em} /* 20px */
h4 {font-size: 1.286em} /* 18px */
h5 {font-size: 1.143em} /* 16px */
h6 {font-size: 1em} /* 14px */

h2, h3, h4, h5, h6 {
  font-weight: 400;
  line-height: 1.1;
  margin-bottom: .8em;
}

/* Anchors */
a {outline: 0;}
a img {border: 0px; text-decoration: none;}
a:link, a:visited {
  color: #C74350;
  padding: 0 1px;
  text-decoration: underline;
}
a:hover, a:active {
  background-color: #C74350;
  color: #fff;
  text-decoration: none;
  text-shadow: 1px 1px 1px #333;
}

/* Paragraphs */
p {margin-bottom: 1.143em;}
* p:last-child {margin-bottom: 0;}

strong, b {font-weight: bold;}
em, i {font-style: italic;}

::-moz-selection {background: #F6CF74; color: #fff;}
::selection {background: #F6CF74; color: #fff;}

/* Lists */
ul {
  list-style: outside disc;
  margin: 1em 0 1.5em 1.5em;
}

ol {
  list-style: outside decimal;
  margin: 1em 0 1.5em 1.5em;
}

dl {margin: 0 0 1.5em 0;}
dt {font-weight: bold;}
dd {margin-left: 1.5em;}

/* Quotes */
blockquote {font-style: italic;}
cite {}

q {}

/* Tables */
table {margin: .5em auto 1.5em auto; width: 98%;}

  /* Thead */
  thead th {padding: .5em .4em; text-align: left;}
  thead td {}

  /* Tbody */
  tbody td {padding: .5em .4em;}
  tbody th {}

  tbody .alt td {}
  tbody .alt th {}

  /* Tfoot */
  tfoot th {}
  tfoot td {}

```

* For optimum coding, a few basic information on the .css file is at the top in comments form.
* 2 imports at the beginning of the file. The first one is Eric Meyer’s CSS reset file. Second one is a personalized global forms file which I’ll discuss more deeply later on.
* Very basic styling for the default tags.

### EXPLAINING SOME PROPERTIES

For this very part, there’s little to be mentioned. Firstly there’s the `text-shadow` CSS3 property. To explain it, here’s a sample:

```
  text-shadow: 1px 5px 2px #333;
```

This will give us a `#333` shadow on our text that’s 1px to the right, 5px down and with a 2px blur. Simple, right? 


```
  * p:last-child {margin-bottom: 0;}
```

This line will remove the margin bottom of any `<p>` tag that’s the last child of it’s parent. Useful when using boxes (like we’re doing) to avoid large vertical gaps.

```
  ::-moz-selection {background: #F6CF74; color: #fff;}
  ::selection {background: #F6CF74; color: #fff;}
```

`::selection` is a CSS3 selector that lets us style how the text selection looks. It only allows `color` and `background` CSS properties, so keep it simple. `::-moz-selection` needs to go here since Mozilla haven’t implemented the `::selection` selector.

### ENABLING HTML5 ELEMENTS

Perhaps it’s fair to assume that most browsers apply something like `display: inline` for all unknown tags that they might encounter. This is not what we want for some of them, such as `<section>`, so we need to tell explicitly to the browser how to display these elements:

```

/* HTML5 tags */
header, section, footer,
aside, nav, article, figure {
  display: block;
}

```

### LIMITING OUR BLOCKS
```

/***** Layout *****/
.body {clear: both; margin: 0 auto; width: 800px;}
img.right figure.right {float: right; margin: 0 0 2em 2em;}
img.left, figure.left {float: right; margin: 0 0 2em 2em;}

```

### HEADER STYLING
We’ll begin with our header. This one is fairly easy. We just want a couple of spacing and a few text styling here and there. Nothing we haven’t done before.

```

/*
  Header
*****************/
#banner {
  margin: 0 auto;
  padding: 2.5em 0 0 0;
}

  /* Banner */
  #banner h1 {font-size: 3.571em; line-height: .6;}
  #banner h1 a:link, #banner h1 a:visited {
    color: #000305;
    display: block;
    font-weight: bold;
    margin: 0 0 .6em .2em;
    text-decoration: none;
    width: 427px;
  }
  #banner h1 a:hover, #banner h1 a:active {
    background: none;
    color: #C74350;
    text-shadow: none;
  }

  #banner h1 strong {font-size: 0.36em; font-weight: normal;}

```

We now pass on to the navigation. Pretty much the same as before, nothing really new here. The regular horizontal list, a couple of colour edits. Nothing fancy.

```

  /* Main Nav */
  #banner nav {
    background: #000305;
    font-size: 1.143em;
    height: 40px;
    line-height: 30px;
    margin: 0 auto 2em auto;
    padding: 0;
    text-align: center;
    width: 800px;

    border-radius: 5px;
    -moz-border-radius: 5px;
    -webkit-border-radius: 5px;
  }

  #banner nav ul {list-style: none; margin: 0 auto; width: 800px;}
  #banner nav li {float: left; display: inline; margin: 0;}

  #banner nav a:link, #banner nav a:visited {
    color: #fff;
    display: inline-block;
    height: 30px;
    padding: 5px 1.5em;
    text-decoration: none;
  }
  #banner nav a:hover, #banner nav a:active,
  #banner nav .active a:link, #banner nav .active a:visited {
    background: #C74451;
    color: #fff;
    text-shadow: none !important;
  }

  #banner nav li:first-child a {
    border-top-left-radius: 5px;
    -moz-border-radius-topleft: 5px;
    -webkit-border-top-left-radius: 5px;

    border-bottom-left-radius: 5px;
    -moz-border-radius-bottomleft: 5px;
    -webkit-border-bottom-left-radius: 5px;
  }

```


### EXTRAS BLOCK STYLING
Here things begin to get interesting. We’ll begin with basic styling for the block itself:

```

/*
  Extras
*****************/
#extras {margin: 0 auto 3em auto; overflow: hidden;}

#extras ul {list-style: none; margin: 0;}
#extras li {border-bottom: 1px solid #fff;}
#extras h2 {
  color: #C74350;
  font-size: 1.429em;
  margin-bottom: .25em;
  padding: 0 3px;
}

#extras a:link, #extras a:visited {
  color: #444;
  display: block;
  border-bottom: 1px solid #F4E3E3;
  text-decoration: none;
  padding: .3em .25em;
}

  /* Blogroll */
  #extras .blogroll {
    float: left;
    width: 615px;
  }

  #extras .blogroll li {float: left; margin: 0 20px 0 0; width: 185px;}

  /* Social */
  #extras .social {
    float: right;
    width: 175px;
  }
```

![](https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a5373ebd-6908-4f07-a06e-7692417c77b1/extras-border.png)

```

  #extras li:last-child, /* last <li>*/
  #extras li:last-child a /* <a> of last <li> */
  {border: 0}

```

![](https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/8d87221f-a346-4be6-9fc0-5e8b5474de76/extras-border2.png)


Well, meet `:nth-last-child()`.

```

#extras .blogroll li:nth-last-child(2),
#extras .blogroll li:nth-last-child(3),
#extras .blogroll li:nth-last-child(2) a,
#extras .blogroll li:nth-last-child(3) a {border: 0;}
```


![](https://cloud.netlifyusercontent.com/assets/344dbf88-fdf9-42bb-adb4-46f01eedd629/a4e71550-3c4b-431f-acdf-bc4dbad75186/opera-thumb.png)

