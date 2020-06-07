# Readings : Basics of HTML, CSS & JS

## Text

1. Headings and paragraphs
1. Bold, italic, emphasis
1. Structural and semantic markup

When creating a web page, you add tags (known as markup) to the contents of the page. These tags provide extra meaning and allow browsers to show users the appropriate structure for the page

**Structural markup:** the elements that you can use to describe both headings and paragraphs

**Semantic markup:** which provides extra information; such as where emphasis is placed in a sentence, that something you have written is a quotation (and who said it), the meaning of acronyms, and so on

![Wallpaper](https://i.pinimg.com/originals/e0/17/a8/e017a811b7188c70db4c9168b39a3634.jpg)

### Headings

```
<h1>
<h2>
<h3>
<h4>
<h5>
<h6>


<h1>This is a Main Heading</h1>
<h2>This is a Level 2 Heading</h2>
<h3>This is a Level 3 Heading</h3>
<h4>This is a Level 4 Heading</h4>
<h5>This is a Level 5 Heading</h5>
<h6>This is a Level 6 Heading</h6>

```

![Heading Image](https://mark.ie/sites/default/files/styles/widescreen_television/public/media/images/2018-03/heading-tag-hierarchy.jpg?h=be3129e6&itok=ngidaZ2r)

**<h1>** is used for main headings 
**<h2>** is used for subheadings

### Paragraphs

![Paragraph](https://codebridgeplus.com/wp-content/uploads/html_paragraph.jpg)

To create a paragraph, surround the words that make up the paragraph with an opening ```<p>``` tag and closing ```</p>``` tag.

```
<p>This is a paragraph.</p>
<p>This is a paragraph.</p>
<p>This is a paragraph.</p>
```

_Rendered text_

This is a paragraph.

This is a paragraph.

This is a paragraph.

### Bold & iTalic

__<b>__
By enclosing words in the tags `<b>` and `</b>` we can make characters appear bold.

![Bold](https://line25.com/wp-content/uploads/2009/html-crimes/bold.png)

__<i>__
By enclosing words in the tags `<i>` and `</i>` we can make characters appear italic.

![Italic](https://javascript.info/article/selection-range/range-example-p-2-b-3-range.svg)


### Superscript & Supscript

`<sup>` element is used to contain characters that should be superscript such as the suffixes of dates or mathematical concepts like raising a number to a power such as 2^5.

`<sub>` element is used to contain characters that should be subscript. It is commonly used with foot notes or chemical formulas such as H20.

![subs](https://support.content.office.net/en-us/media/0e396025-76a9-4051-8960-74ca0aeeb739.png)


### White Space

In order to make code easier to read, web page authors often add extra spaces or start some elements on new lines.

When the browser comes across two or more spaces next to each other, it only displays one space. Similarly if it comes across a line break, it treats that as a single space too. This is known as white space collapsing.


![hr](https://clearlydecoded.com/assets/images/posts/2017-09-04-anatomy-of-html-tag/opening-tag-only.png)

### Linebreak & Horizintal rule

`<br />` As you have already seen, the browser will automatically show each new paragraph or heading on a new line. But if you wanted to add a line break inside the middle of a paragraph you can use the line break tag `<br />`.

![br](https://codescracker.com/html/images/html-line-breaks.jpg)

`<hr />` To create a break between themes — such as a change of topic in a book or a new scene in a play — you can add a horizontal rule between sections using the `<hr />` tag.

![hr](https://www.w3docs.com/uploads/media/default/0001/01/0c46c334f0f566736856790f751c5a29799a6734.png)


## Full TEXT example

This is a very simple HTML page that demonstrates text markup.
Structural markup includes elements such as `<h1>`, `<h2>`, and `<p>`. Semantic information is carried in elements such as `<cite>` and `<em>`.

```
<html>
    <head>
        <title>Text</title>
    </head>
    <body>
        <h1>The Story in the Book</h1>

        <h2>Chapter 1</h2>
        
        <p>
            Molly had been staring out of her window for about
            an hour now. On her desk, lying between the copies of <i>Nature</i>, <i>New Scientist</i>, and all the other scientific journals her work had appeared in, was a well thumbed copy of <cite>On The Road</cite>. It had been Molly's favorite book since college, and the longer she spent in these four walls the more she felt she needed to be free.
        </p>

        <p>
            She had spent the last ten years in this room, sitting under a poster with an Oscar Wilde quote proclaiming that <q>Work is the refuge of people who have nothing better to do</q>. Although many considered her pioneering work, unraveling the secrets of the llama <abbr title="Deoxyribonucleic acid">DNA</abbr>, to be an outstanding achievement, Molly <em>did</em> think she had something better to do.
        </p>
    </body>
</html>
```



![CSS](https://colorlib.com/wp/wp-content/uploads/sites/2/creative-css3-tutorials.jpg)
# CSS

_into_

In this section, we will look at how to make your web pages more attractive, controlling the design of them using CSS.

**Content table**

1. Introduce you to how CSS works
2. Teach you how to write CSS rules
3. Show you how CSS rules apply to HTML pages


**What is CSS?**

CSS allows you to create rules that specify how the content of an element should appear. For example, you can specify that the background of the page is cream, all paragraphs should appear in gray using the Arial typeface, or that all level one headings should be in a blue, italic, Times typeface.

**Why CSS?**
CSS allows you to create rules that control the way that each individual box (and the contents of that box) is presented.


CSS works by associating rules with HTML elements. These rules govern how the content of specified elements should be displayed. A CSS rule contains two parts: a selector and a declaration.

```
p {
    font-family: Arial;
}
```

![CSS Rule](https://mdn.mozillademos.org/files/9461/css-declaration-small.png)

This rule indicates that all "p" elements should be shown in the Arial typeface.

Selectors indicate which element the rule applies to. The same rule can apply to more than one element if you separate the element names with commas.

Declarations indicate how the elements referred to in the selector should be styled. Declarations are split into two parts (a property and a value), and are separated by a colon.


**How to write CSS**
First you need to find the selector you want to apply **CSS** on it like paragraph or anything else like bellow
```
p, h1, h2, li {
    color: #cccccc;
    font-weight: 700; // 700 will give you a Bold text
}
```

![CSS](https://disenowebakus.net/en/images/articles/css-fundamentals-syntax-structure-instruction.jpg)


## How to apply CSS in your page

There are three way to implement your CSS with
1. Inline CSS
2. Add style tag into head and put your css on it
3. External CSS file the link it to you page


You can do you style in head like image below
![Head-Style](https://webdev.imgix.net/codelab-extract-and-inline-critical-css/inline-critical-css.png)

Or you can create new file called style.css and link it with Link in head tag
![CSS-File](https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcTEa8945FoKgb64v8jcXRvrdOxQ7gkrUUEFqrcaP5Ji69A5HPU1&usqp=CAU)

![css](https://www.bitdegree.org/learn/storage/media/images/8c4493d3-110c-4a95-8b70-7626ce2d2f4e.jpg)


![javascript](https://4.bp.blogspot.com/-PQHNOWFNS9o/XAkNsyPerCI/AAAAAAAALks/ONXxkKH3lRwskA3cfiqPa-cGKlt8u-l6wCLcBGAs/s1600/javascript.jpg)

# javascript

## Statment

A script is a series of instructions that a computer can follow one-by-one. Each individual instruction or step is known as a statement, Statements should end with a semicolon.

```
<p id="demo"></p>

<script>
    document.getElementById("demo").innerHTML = "Hello Dolly.";
</script>

```

## Comments
You should write comments to explain what your code does. They help make your code easier to read and understand. This can help you and others who read your code.

```
<script>
    // Change heading:
    document.getElementById("myH").innerHTML = "JavaScript Comments";
    // Change paragraph:
    document.getElementById("myP").innerHTML = "My first paragraph.";
    </script>
```

## Variable
A script will have to temporarily store the bits of information it needs to do its job. It can store this data in variables.

![](https://1.bp.blogspot.com/-8UmWFTngfwY/XkVRuoPFfkI/AAAAAAAACmI/93j-FMkA9EYyoRIT1qlJ2sMUbobnWT1UgCLcBGAsYHQ/w1200-h630-p-k-no-nu/javascript_var.png)

Think about calculating the area of a wall; in math the area of a rectangle is obtained by multiplying two numbers:
``` width x height = area ```

You may be able to do calculations like this in your head, bu t when writing a script to do this calculation, you need to give the computer very detailed instructions. You might tell it to perform the following four steps in order:

1. Remember the value for width
2. Remember the value for height
3. Multiply width by height to get the area 
4. Return the result to the user

```
<script>
    var x = 5;
    var y = 6;
    var z = x + y;
    document.getElementById("demo").innerHTML = "The value of z is: " + z;
</script>
```

![](https://miro.medium.com/max/4810/1*ZoFXjX8IoLLm69M4yl78Ww.png)


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


# Decisions and Loops

### Arithmetic Operators

| Operator	    | Description                                           | 
| +	            | Adds two numeric operands.                            |
| -	            | Subtract right operand from left operand              |
| *	            | Multiply two numeric operands.                        |
| /	            | Divide left operand by right operand.                 |
| %	            | Modulus operator. Returns remainder of two operands.  |
| ++	        | Increment operator. Increase operand value by one.    |
| '--'	        | Decrement operator. Decrease value by one.            |


__Example: Arithmetic Operator__
```
var x = 5, y = 10, z = 15;

x + y; //returns 15

y - x; //returns 5

x * y; //returns 50

y / x; //returns 2

x % 2; //returns 1

x++; //returns 6

x--; //returns 4
```

__Example: + operator__
```
var a = 5, b = "Hello ", c = "World!", d = 10;

a + b; // "5Hello "

b + c; // "Hello World!"

a + d; // 15
```


### Comparison Operators

JavaScript language includes operators that compare two operands and return Boolean value true or false.

![](https://res.cloudinary.com/practicaldev/image/fetch/s--iAbnVv87--/c_imagga_scale,f_auto,fl_progressive,h_900,q_auto,w_1600/https://cl.ly/7d9cf8370380/Image%25202018-11-15%2520at%25209.59.47%2520AM.png)

| Operator	    | Description                                                                                                       | 
| ------------- | ----------------------------------------------------------------------------------------------------------------- |
| ==	        | Compares the equality of two operands without considering type.                                                   |
| ===           | Compares equality of two operands with type.                                                                      |
| !=            | Compares inequality of two operands.                                                                              |
| >             | Checks whether left side value is greater than right side value. If yes then returns true otherwise false.        |
| <	            | Checks whether left operand is less than right operand. If yes then returns true otherwise false.                 |
| >=	        | Checks whether left operand is greater than or equal to right operand. If yes then returns true otherwise false.  |
| <=	        | Checks whether left operand is less than or equal to right operand. If yes then returns true otherwise false.     |


__Example: Comparison Operators__
```
var a = 5, b = 10, c = "5";
var x = a;

a == c; // returns true

a === c; // returns false

a == x; // returns true

a != b; // returns true

a > b; // returns false

a < b; // returns true

a >= b; // returns false

a <= b; // returns true

a >= c; // returns true

a <= c; // returns true
```


### Logical Operators

Logical operators are used to combine two or more conditions. JavaScript includes following logical operators.

__Example: Logical Operators__
```
var a = 5, b = 10;

(a != b) && (a < b); // returns true

(a > b) || (a == b); // returns false

(a < b) || (a == b); // returns true

!(a < b); // returns false

!(a > b); // returns true
```



# Loops

![](https://data-flair.training/blogs/wp-content/uploads/sites/2/2019/07/JavaScript-Loops-1280x720.jpg)

## JavaScript for Loop

JavaScript includes for loop like Java or C#. Use for loop to execute code repeatedly.

```
for(initializer; condition; iteration)
{
    // Code to be executed
}
```

__The for loop requires following three parts.__
1. Initializer: Initialize a counter variable to start with
1. Condition: specify a condition that must evaluate to true for next iteration
1. Iteration: increase or decrease counter

![](https://media.geeksforgeeks.org/wp-content/uploads/Loop1.png)
__Example: for loop__
```
for (var i = 0; i < 5; i++)
{
    console.log(i);
}
```

- Output:
` 0 1 2 3 4 `

### Points to Remember :
1. JavaScript for loop is used to execute code repeatedly.
1. for loop includes three parts: initialization, condition and iteration. e.g.for(initializer; condition; iteration){ ... }
1. The code block can be wrapped with { } brackets.
1. An initializer can be specified before starting for loop. The condition and increment statements can be included inside the block.


## JavaScript while loop
JavaScript includes while loop to execute code repeatedly till it satisfies a specified condition. Unlike for loop, while loop only requires condition expression.

_Syntax:_
```
while(condition expression)
{
    /* code to be executed 
    till the specified condition is true */
}
```

__Example: while loop__

```
var i =0;

while(i < 5)
{
    console.log(i);
    i++;
}

//Output: 0 1 2 3 4

```

As you can see in the above example, while loop will execute the code block till i < 5 condition turns out to be false. Initialization statement for a counter variable must be specified before starting while loop and increment of counter must be inside while block.
