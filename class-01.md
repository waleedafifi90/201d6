![HTML](https://html.com/wp-content/uploads/html-hpg-featured-new.png)

# HTML

_Introduction_

In this course, you will learn more about HTML and CSS and to create your first web page

**Why HTML?**
1. HTML describes the structure of a web page 
2. HTML is a tags language so every tag describe it's content


## HTML describes tHe Structure of Pages

 To describe the structure of a web page, we add code to the words we want to appear on the page.

```
html>
    <body>
        <h1>
            This is the Main Heading
        </h1>
        <p>
            This text might be an introduction to the rest of
            the page. And if the page is a long one it might
            be split up into several sub-headings.
        <p> 
        <h2>
            This is a Sub-Heading
        </h2>
        <p>
            Many long articles have sub-headings so to help
            you follow the structure of what is being written. There may even be sub-sub-headings (or lower-level headings).
        </p>
        <h2>
            Another Sub-Heading
        </h2>
        <p>
            Here you can see another sub-heading.
        </p> 
    </body>
</html>
```

Each tag in HTML must have a close tag `<p></p>` and every tag can have one or more attribute like if I need to say that this `<p>` language is English  so the tag will be like this
```
<p lang="en-us"> Waleed A. Afifi </p>
```

## body, head & title

#### body

You met the body element
in the first example we created. Everything inside this element is shown inside the main browser window.


#### Head

Before the body element you will often see a head element. This contains information
about the page (rather than information that is shown within the main part of the browser window that is highlighted in blue on the opposite page).
You will usually find a title element inside the head element.


#### Title

The contents of the title element are either shown in the top of the browser, above where you usually type in the URL of the page you want to visit, or
on the tab for that page (if your browser uses tabs to allow you to view multiple pages at the same time).


## How you can create Your first HTML page?

You can use and code editor like VSC, Notepad++, XCode, Atom, etc..
Or you can use the Notepad that installed in you PC the one that came with your Windows OS **Notepad** all you new is open Notepad and copy the code in the top of this page and paste it in Notepad then save the file with extension  _.html_  and that's it.


### HTML Summary

1. HTML pages are text documents.
2. HTML uses tags (characters that sit inside angled brackets) to give the information they surround special meaning.
3. Tags are often referred to as elements.
4. Tags usually come in pairs. The opening tag denotes the start of a piece of content; the closing tag denotes the end.
5. Opening tags can carry attributes, which tell us more about the content of that element.
6. Attributes require a name and a value.
7. To learn HTML you need to know what tags are available for you to use, what they do, and where they can go.


# Extra Markup

# Doctypes
Html5 must have Doctypes in the beginning file like below
```
<!DOCTYPE html>
```

**Comment in the HTML**
```
<!-- Comment goes here -->
```

**ID Attribute**

You can add ID for one element only and it can not be repeated like
```
<p id="MYParagraph"></p>
```

**Class Attribute**

Class can be implemented to more than one element
```
<p class="paragraph"></p>
```

**Block element**

Some elements will always appear to start on a new line in the browser window. These are known as block-level elements.
```
<ul>
    <li>Science: 21 Nov - 20 Feb 2010/11</li>
    <li>Architecture: 6 Mar - 15 May 2011</li>
    <li>History: 29 May - 21 Aug 2011</li>
    <li>Religion: 28 Aug - 6 Nov 2011</li>
</ul>
```
Examples of block elements are h1, p, ul, and li.


# HTML layout
![Html Layout](https://www.w3schools.com/html/img_sem_elements.gif)



# Process and Design

## Who is the site For?

Every website should be designed for the target audience—not just for yourself or the site owner. It is therefore very important to understand who your target audience is.

**target auDience: inDiviDuals**

1. What is the age range of your target audience?
1. Will your site appeal to more women or men? What is the mix? ● Which country do your visitors live in?
1. Do they live in urban or rural areas?
1. What is the average income of visitors?
1. What level of education do they have?
1. What is their marital or family status?
1. What is their occupation?
1. How many hours do they work per week?
1. How often do they use the web?
1. What kind of device do they use to access the web?

**Why PeoPle visit your Website**

Now that you know who your visitors are, you need to consider why they are coming. While some people will simply chance across your website, most will visit for a specific reason.

*Key motivations*

1. Are they looking for general entertainment or do they need to achieve a specific goal?
1. If there is a specific goal, is it a personal or professional one?
1. Do they see spending time on this activity as essential or a luxury?

*Specific goals*

1. Do they want general information / research (such as background on a topic / company), or are they after something specific (such as a particular fact or information on a product)?
1. Are they already familiar with the service or product that you offer or do they need to be introduced to it?
1. Are they looking for time sensitive information, such as the latest news or updates on a particular topic?
1. Do they want to discover information about a specific product or service to help them decide whether to buy it or not?
1. Do they need to contact you? If so, can they visit in person (which might require opening hours and a map)? Or might they need email or telephone contact details?

**Site maps**

Now that you know what needs to appear on your site, you can start to organize the information into sections or pages.

![Sitemap Example](https://online.visual-paradigm.com/repository/images/be01eb75-3594-4ba1-9c25-b04dedb02b7c.png)

**WireFrames**

A wireframe is a simple sketch of the key information that needs to go on each page of a site. It shows the hierarchy of the information and how much space it might require.

![Wireframe example](https://www.comentum.com/images/wireframes-sample/ecommerce/home.png)



**Getting your message across using Design**

The primary aim of any kind of visual design is to communicate. Organizing and prioritizing information on a page helps users understand its importance and what order to read it in.

* Content
* Prioritizing
* Organizing

**content**

Web pages often have a lot of information to communicate. For example, the pages of online newspapers will have information that does not appear on every page of the print equivalent:

* A masthead or logo
* Links to navigate the site
* Links to related content and other popular articles
* Login or membership options
* Ability for users to comment
* Copyright information
* Links to privacy policies, terms and conditions, advertising information, RSS feeds, subscription options


**Prioritizing**

If everything on a page appeared in the same style, it would be much harder to understand. (Key messages would not stand out.)

By making parts of the page look distinct from surrounding content, designers draw attention to (or away from) those items.

Designers create something known as a visual hierarchy to help users focus on the key messages that will draw people's attention, and then guide them to subsequent messages 

**organizing**

Grouping together related content into blocks or chunks makes the page look simpler (and easier to understand).

Users should be able to identify the purpose of each block without processing each individual item.

By presenting certain types of information in a similar visual style (such as using the same style for all buttons or all links), users will learn to associate that style with a particular type of content.


### visual hierarchy

Most web users do not read entire pages. Rather, they skim to find information. You can use contrast to create a visual hierarchy that gets across your key message and helps users find what they are looking for.

![Visual](https://image.slidesharecdn.com/uxlesson6visualhierarchy-150728121120-lva1-app6892/95/ux-lesson-6-visual-hierarchy-7-638.jpg?cb=1438746786)

visual hierarchy refers to the order in which your eyes perceive what they see. It is created by adding visual contrast between the items being displayed. Items with higher contrast are recognized and processed first.

![HTML Website](https://www.onextrapixel.com/wp-content/uploads/2012/06/best-psd-freebies.jpg)

### Designing navigation

Site navigation not only helps people find where they want to go, but also helps them understand what your site is about and how it is organized. Good navigation tends to follow these principles...

![](https://www.orbitmedia.com/wp-content/uploads/2016/09/website-navigation-dropdown.jpg)




![](https://hackernoon.com/hn-images/1*bxEkHw1xewxOFjmGunb-Cw.png)
# JavaScript & jQuery

How JavaScript make web pages more interactive?
1. Access content
2. Modify content
3. Program Rouls
4. React to event

![](https://cdn-images-1.medium.com/max/2000/1*OF0xEMkWBv-69zvmNs6RDQ.gif)

- JavaScript can reload the content of page without reload the paage itself.
- Filtering data

## The ABC of prgramming
1. A - Whatt is a script and how do I create one?
2. B - How do computter fit in with the world around them?
3. C - How do I write a script for a web page?

A script is a series of insttructions that a computer can follow tto achive goals

To write a script you need to first state your goals and then list tthe tasks that need to be completed in order to achive it.


_start with big picture of what you want to achieve, and break that down into smaller steps._

1. DEFINE THE GOAL
First, you need to define the task you want to achieve. You can think of this as a puzzle for the computer to solve.

2. DESIGN THE SCRIPT
To design a script you split the goal out into a series of tasks that are going to be involved in solving this puzzle. This can be represented using a flowchart.

3. CODE EACH STEP
Each of the steps needs to be written in a programming language that the compu ter understands. In our case, this is JavaScript.


![](https://media.giphy.com/media/GVd19DZmvRO80/giphy.gif)
## FROM STEPS TO CODE
Every step for every task shown in a flowchart needs to be written in a language the computer can understand and follow.
Just like learning any new language, you need to get to grips with the:
1. __Vocabulary:__ The words that computers understand
2. __Syntax:__ How you put those words together to create instructions computers can follow


You need to learn to "think" like a computer because they solve tasks in different ways than you or I might approach them

For example, when you look at the picture on the left how do you tell which person is the tallest? A computer would need explicit, step-by-step instructi0ns, such as:
1. Find the height of the first person
2. Assume he or she is the "tallest person"
3. Look at the height of the remaining people one- by-one and compare their height to the "tallest person" you have found so far
4. At each step, if you find someone whose height is greater than the current "tallest person", he or she becomes the new "tallest person"
5. Once you have checked all the people, tell me which one is the tallest


# EXPRESSIONS
An expression evaluates into (results in) a single value. Broadly speaking there are two types of expressions.

- EXPRESSIONS THAT JUST ASSIGN A VALUE TO A VARIABLE
```
var color = 'beige';
//The value of co1or is now beige
```

- EXPRESSIONS THAT USE TWO OR MORE VALUES TO RETURN A SINGLE VALUE
```
var area = 3 * 2;
//The value of area is now 6.
```

![](https://i1.wp.com/pandabunnytech.com/wp-content/uploads/2018/11/types-of-statements-in-javascript-e1543313160116.png)
# OPERATORS
Expressions rely on things called operators; they allow programmers to create a single value from one or more values.

- ASSIGNMENT OPERATORS
```
color = 'beige';
```

- ARITHMETIC OPERATORS
```
area = 3 * 2;
```

- STRING OPERATORS
```
greeting= 'Hi 1 + 'Molly';
```

- COMPARISON OPERATORS
```
buy = 3 > 5;
```

- LOGICAL OPERATORS
```
buy= (5 > 3) && (2 < 4);
```

## USING ARITHMETIC OPERATORS
```
var subtotal = (13 + 1) * 5;
var shipping = 0.5 * (13 + 1) ;

var total = subtotal + shipping;

var elSub = document.getElementByid('subtotal ');
elSub.textContent =subtotal ;

var elShip =document.getElementByid('shipping');
elShip.textContent =shipping;

var elTotal = document.getElementByid('total ');
elTotal .textContent =total;

```

## STRING OPERATOR
```
var firstName = 'Ivy ';
var lastName = ' Stone' ;
var fullName = firstName + lastName;
```

__MIXING NUMBERS AND STRINGS TOGETHER__

When you place quotes around a num~er, it is a string (not a numeric data type), and you cannot perform addition operations on strings.
```
var costl = '7';
var cost2 = '9';
var total = costl + cost2;
```

If you try to add a numeric data type to a string, then the number becomes part of the string, e.g., adding a house number to a street name:
```
var number = 12;
var street= 'Ivy Road'; 
var add = number + street
```

If you try to use any of the other arithmetic operators on a string, then the value that results is usually a value called NaN. This means "not a number."
```
var score= 'seven';
var score2 = 'nine';
var total = score * score2;
```

## USING STRING OPERATORS

_JaavaScript_
```
var greeting= 'Howdy ';
var name= 'Molly';
var welcomeMessage = greeting+ name+ '!';
var el =document.getElementByld('greeting'); el .textContent = welcomeMessage;
```

_HTML_
```
<hl>Elderflower</ hl> 
<div id="content">
    <div id="greeting" class="message">Hello 
        <span id="name">friend</span>!
    </div>
</div>
<script src="js/string-operator.js"></script>
```

![](https://chrissainty.com/content/images/size/w2000/2019/02/blazor-bites-javascript-interop.jpg)
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