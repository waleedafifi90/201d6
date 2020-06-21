![](https://beautifulthemes.com/blog/wp-content/uploads/2017/12/wordpress-header-image.png)
# Audio, Video, Images

## HTML Images

Images can improve the design and the appearance of a web page.

_example_
```
<img src="pic_trulli.jpg" alt="Italian Trulli">
```

![](https://www.w3schools.com/html/pic_trulli.jpg)

```
<img src="img_girl.jpg" alt="Girl in a jacket" width="500" height="600">
```
![](https://www.w3schools.com/html/img_girl.jpg)

### HTML Images Syntax

The HTML `<img>` tag is used to embed an image in a web page.

Images are not technically inserted into a web page; images are linked to web pages. The `<img>` tag creates a holding space for the referenced image.

The `<img>` tag is empty, it contains attributes only, and does not have a closing tag.

The `<img>` tag has two required attributes:

* src - Specifies the path to the image
* alt - Specifies an alternate text for the image

_Syntax_
```
<img src="url" alt="alternatetext">
```

### The src Attribute
The required `src` attribute specifies the path (URL) to the image.

**Note:** When a web page loads; it is the browser, at that moment, that gets the image from a web server and inserts it into the page. Therefore, make sure that the image actually stay in the same spot in relation to the web page, otherwise your visitors will get a broken link icon. The broken link icon is shown if the browser cannot find the image.


_Example_
```
<img src="img_chania.jpg" alt="Flowers in Chania">
```

### The alt Attribute
The required `alt` attribute provides an alternate text for an image, if the user for some reason cannot view it (because of slow connection, an error in the src attribute, or if the user uses a screen reader).

The value of the `alt` attribute should describe the image:

```
<img src="img_chania.jpg" alt="Flowers in Chania">
```

If a browser cannot find an image, it will display the value of the `alt` attribute:

```
<img src="wrongname.gif" alt="Flowers in Chania">
```

### Image Size - Width and Height
You can use the `style` attribute to specify the width and height of an image.


```
<img src="img_girl.jpg" alt="Girl in a jacket" style="width:500px;height:600px;">
```

![](https://www.w3schools.com/html/img_girl.jpg)

Alternatively, you can use the `width` and `height` attributes:

```
<img src="img_girl.jpg" alt="Girl in a jacket" width="500" height="600">
```

### Images in Another Folder

If you have your images in a sub-folder, you must include the folder name in the `src` attribute:

```
<img src="/images/html5.gif" alt="HTML5 Icon" style="width:128px;height:128px;">
```

### Images on Another Server

Some web sites store their images on another server.

Actually, you can access images from any web address in the world:

```
<img src="https://www.w3schools.com/images/w3schools_green.jpg" alt="W3Schools.com">
```


* Use the HTML `<img>` element to define an image
* Use the HTML `src` attribute to define the URL of the image
* Use the HTML `alt` attribute to define an alternate text for an image, if it cannot be displayed
* Use the HTML `width` and `height` attributes or the CSS `width` and `height` properties to define * the size of the image
* Use the CSS `float` property to let the image `float` to the left or to the right


# HTML5 video and audio

## Video

The `<video>` and `<audio>` elements allow us to embed video and audio into web pages.
```
<video controls>
  <source src="rabbit320.mp4" type="video/mp4">
  <source src="rabbit320.webm" type="video/webm">
  <p>Your browser doesn't support HTML5 video. Here is a <a href="rabbit320.mp4">link to the video</a> instead.</p>
</video>
```

Below is a video that will play in all modern browsers
![](https://miro.medium.com/max/1276/0*5toJU_IX8aOYIzE3)


You can review what all the HTML features do in the article linked above; for our purposes here, the most interesting attribute is `controls`, which enables the default set of playback `controls`. If you don't specify this, you get no playback `controls`:


Below is a video that will play in all modern browsers
![](https://www.brid.tv/wp-content/uploads/2018/07/bridtv-html5-video-player-3-1200x675.jpg)

```
<div class="player">
  <video controls>
    <source src="video/sintel-short.mp4" type="video/mp4">
    <source src="video/sintel-short.webm" type="video/webm">
    <!-- fallback content here -->
  </video>
  <div class="controls">
    <button class="play" data-icon="P" aria-label="play pause toggle"></button>
    <button class="stop" data-icon="S" aria-label="stop"></button>
    <div class="timer">
      <div></div>
      <span aria-label="timer">00:00</span>
    </div>
    <button class="rwd" data-icon="B" aria-label="rewind"></button>
    <button class="fwd" data-icon="F" aria-label="fast forward"></button>
  </div>
</div>
```


### Implementing the JavaScript
```
const media = document.querySelector('video');
const controls = document.querySelector('.controls');

const play = document.querySelector('.play');
const stop = document.querySelector('.stop');
const rwd = document.querySelector('.rwd');
const fwd = document.querySelector('.fwd');

const timerWrapper = document.querySelector('.timer');
const timer = document.querySelector('.timer span');
const timerBar = document.querySelector('.timer div');
```



## The `<audio>` element

The `<audio>` element works just like the `<video>` element, with a few small differences as outlined below. A typical example might look like so:

```
<audio controls>
  <source src="viper.mp3" type="audio/mp3">
  <source src="viper.ogg" type="audio/ogg">
  <p>Your browser doesn't support HTML5 audio. Here is a <a href="viper.mp3">link to the audio</a> instead.</p>
</audio>
```

![](https://mdn.mozillademos.org/files/12798/audio-player.png)

### Restarting media playback
At any time, you can reset the media to the beginning—including the process of selecting the best media source, if more than one is specified using `<source>` elements—by calling the element's `load()` method:

```
const mediaElem = document.getElementById("my-media-element");
mediaElem.load();
```


# Search engine optimization
### The Beginner's Guide to SEO

Rankings and Traffic Through Search Engine Optimization

_Welcome to your SEO learning journey!_

**What is SEO & Why is it Important?**

You’ve likely heard of SEO, and if you haven’t already, you could obtain a quick Wikipedia definition of the term, but understanding that SEO is “the process of affecting the visibility of a website or a web page in a search engine's unpaid results” doesn’t really help you answer important questions for your business and your website, such as:

* How do you, for your site or your company’s site, “optimize” for search engines?
* How do you know how much time to spend on SEO?
* How can you differentiate “good” SEO advice from “bad” or harmful SEO advice?


**Why Should You Care About SEO?**

Lots and lots of people search for things. That traffic can be extremely powerful for a business not only because there is a lot of traffic, but because there is a lot of very specific, high-intent traffic.

![](https://wordstream-files-prod.s3.amazonaws.com/s3fs-public/styles/simple_image/public/images/the-basics-of-seo.png?p6FXQNzRLNKd_UAdknHK0bWU8owxiAgO&itok=ae-9lLiO)


**What Actually Works for Driving Traffic from Search Engines?**
First it’s important to note that Google is responsible for most of the search engine traffic in the world (though there is always some flux in the actual numbers). This may vary from niche to niche, but it’s likely that Google is the dominant player in the search results that your business or website would want to show up in, and the best practices outlined in this guide will help position your site and its content to rank in other search engines, as well.


![](https://wordstream-files-prod.s3.amazonaws.com/s3fs-public/styles/simple_image/public/images/seo-basics-google-market-share.png?AkDUxiDffxIfMuiDofOyPRvhPTegkyJr&itok=pyCsdgSY)

Google is looking for pages that contain high-quality, relevant information about the searcher’s query.

![](https://wordstream-files-prod.s3.amazonaws.com/s3fs-public/styles/simple_image/public/images/moz-ranking-factors-seo-basics.gif?HouwX2eHePJQQ61h.1Dh0OQu2wumXGO8&itok=oCRw2J0X)


## On-Page Optimization
Once you have your keyword list, the next step is actually implementing your targeted keywords into your site’s content. Each page on your site should be targeting a core term, and a “basket” of related terms. In his overview of the perfectly optimized page Rand Fishkin offers a nice visual of what a well (or perfectly) optimized page looks like:

![](https://wordstream-files-prod.s3.amazonaws.com/s3fs-public/styles/simple_image/public/images/seo-basics-guide-perfectly-optimized-page.gif?cCBFcgPnC_z1unbdhzwkao4i5y48WPl6&itok=8cdwBGV-)

### Title Tags
![](https://wordstream-files-prod.s3.amazonaws.com/s3fs-public/styles/simple_image/public/images/seo-basics-what-is-a-title-tag.png?Lt1wfLdrz.KU.e_h9SkLDJ.N3qkTjGov&itok=1zim-XHh)

### Meta Descriptions
![](https://wordstream-files-prod.s3.amazonaws.com/s3fs-public/styles/simple_image/public/images/wordstream-meta-description-example.png?aFGswNzl_JojqLtjnEbNquEdA0ESgFMb&itok=ogrf1vRf)

### Body Content
1. Thick & Unique Content
2. Engagement
3. Sharability

### Alt Attributes
### URL Structure

### Schema & Markup
![](https://wordstream-files-prod.s3.amazonaws.com/s3fs-public/styles/simple_image/public/images/learn-seo-basics-schema-markup.png?HD3BWsr26jmnuPEQ7YNsWyFXwyc_7l78&itok=B8CNjEw6)



#### Summary
* Search engine optimization helps visitors find your sites when using search engines.
* Analytics tools such as Google Analytics allow you to see how many people visit your site, how they find it, and what they do when they get there.
* To put your site on the web, you will need to obtain a domain name and web hosting.
* FTP programs allow you to transfer files from your local computer to your web server.
* Many companies provide platforms for blogging, email newsletters, e-commerce and other popular website tools (to save you writing them from scratch).


