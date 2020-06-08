![](https://744025.smushcdn.com/1245953/wp-content/uploads/2020/02/HTML-LISTS.jpg?lossy=1&strip=1&webp=1)

# HTML Lists, CSS Boxes, JS Control Flow

## Lists
1. UnOrdered list
1. Ordered list
1. Description Lists


### Ordered Lists
* `<ol>` The ordered list is created with the `<ol>` element.
* `<li>` Each item in the list is placed between an opening `<li>` tag and a closing `</li>` tag. (The li stands for list item.)

```
<ol>
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ol>  
```
1. Coffee
2. Tea
3. Milk

![](https://webdesy.com/webdesy-wp/wp-content/uploads/2012/02/html-list-3.jpg)

### UnOrdered List
* `<ul>` The unordered list is created with the `<ul>` element.
* `<li>` Each item in the list is placed between an opening `<li>` tag and a closing `</li>` tag. (The li stands for list item.)

```
<ul>
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ul>
```

. Coffee
. Tea
. Milk

![](https://lh3.googleusercontent.com/proxy/F9VDjTnVNtn7yeWKQNmpgvWWMAkeG1vbmgs-zF29d69tgyCdGUcJSPS2l_jTfhfahyxE5ca9n_SXvX5wQDNQfqmWdsgIPZkouuSsSBFHf4SME0zmy-eO-uVkQKMDRDZ8LFCZMyePHg)

### Description Lists
A description list is a list of terms, with a description of each term.
The `<dl>` tag defines the description list, the `<dt>` tag defines the term (name), and the `<dd>` tag describes each term:

```
<dl>
  <dt>Coffee</dt>
  <dd>- black hot drink</dd>
  <dt>Milk</dt>
  <dd>- white cold drink</dd>
</dl>
```
Coffee
    - black hot drink
Milk
    - white cold drink


![](https://www.dummies.com/wp-content/uploads/398569.image0.jpg)



![](https://learnhtmlandcss.com/images/5_menus/5.3_module_menus/5.3.01.jpg)
## Boxes

At the beginning of this section on CSS, you saw how CSS treats each HTML element as if it lives in its own box.

### Box Dimension
width, height

By default a box is sized just big enough to hold its contents. To set your own dimensions for a box you can use the height and width properties.
The most popular ways to specify the size of a box are to use pixels, percentages, or ems. Traditionally, pixels have been the most popular method because they allow designers to accurately control their size.

```
<!-- HTML -->
<div>
    <p>
        The Moog company pioneered the commercial manufacture of modular voltage-controlled analog synthesizer systems in the early 1950s.
    </p>
</div>
```

```
// CSS
div.box {
    height: 300px;
    width: 300px; background-color: #bbbbaa;
}
p {
    height: 75%;
    width: 75%; background-color: #0088dd;
}
```

![](https://lh3.googleusercontent.com/proxy/gNKzUOwIhc-IAbfzduM3mHDrksNwQeCHURK5MFZCNPkKzkmM6Lz7VtbtYRBJc7XlJ2AWxX0EnMLMj6v7AApZXX6yTcUK_m9Qq4I)

### Limited Width
min-width, max-width

Some page designs expand and shrink to fit the size of the user's screen. In such designs, the min-width property specifies the smallest size a box can be displayed at when the browser window is narrow, and the max-width property indicates the maximum width a box can stretch to when the browser window is wide.

```
<!-- HTML -->
<tr>
    <td>
        <img src="images/rhodes.jpg" width="200" height="100" alt="Fender Rhodes" />
    </td>
    <td class="description">
        The Rhodes piano is an electro-mechanical piano, invented by Harold Rhodes during the fifties and later manufactured in a number of models ...
    </td>
    <td>
        $1400
    </td>
</tr>
```

```
// CSS
td.description { 
    min-width: 450px; 
    max-width: 650px; 
    text-align: left; 
    padding: 5px; 
    margin: 0px;
}
```

And there are alsom __Limited Height__ and __Overflowing Content__

### Border and Margin
1. Border
2. Margin
3. PAdding

#### Border
Every box has a border (even if it is not visible or is specified to be 0 pixels wide). The border separates the edge of one box from another.

#### Margin
Margins sit outside the edge of the border. You can set the width of a margin to create a gap between the borders of two adjacent boxes.

#### Padding 
Padding is the space between the border of a box and any content contained within it. Adding padding can increase the readability of its contents.

![Border](https://66.media.tumblr.com/ab75c239d85c8b240829d92908114107/tumblr_n9k1ifz3fa1st1te9o1_640.gifv)

**White space & Vertical Margin**

The padding and margin properties are very helpful in adding space between various items on the page.

![Whitespace](https://lh4.googleusercontent.com/-2cKrA4IZNXzCY7BA2pqJNx6sR0nBkjueWUhazmLOsK-TLQH3i5nZuKRIrGl5RtO_BjguhjY61KAReQQYvoc5zof71dDlUzS6StF39oWGNuuCPdxiZkLHNQyB-PuFBRud5VVxqWG)

**Border width**
`border-width`

The border-width property is used to control the width of a border. The value of this property can either be given in pixels or using one of the following values:

* thin
* medium
* thick

You can control the individual size of borders using four separate properties:
```
border-top-width
border-right-width 
border-bottom-width 
border-left-width
```

```
<!-- HTML -->
<p class="one">Hohner's "Clavinet" is essentially an electric clavichord.</p>
<p class="two">Hohner's "Clavinet" is essentially an electric clavichord.</p>
<p class="three">Hohner's "Clavinet" is essentially an electric clavichord.</p>
```

```
// CSS
p.one { 
    border-width: 2px;
}
p.two {
    border-width: thick;
}
p.three {
    border-width: 1px 4px 12px 4px;
}
```

![](https://lh3.googleusercontent.com/proxy/HHiGNkKmvh4lKUQBEwnIPDCmCpap7wa7Zs2jsC5mbQeJ9FJV-KahhAZqMtF4GO7L82nASUXyrDIWDOWbvIB2RP3MEpudcx5yF64de5AVuDd1F9Bo1AngUw2rHoCbEz8otl_aO8oKMB3ZtbY-1EOyaBQIBfTX9BzrtLGWVBMQ78z9QWHMk15cSHL8xJzknAkSnIsXTIh_mVDRsA)

**Border Style**
`border-style`

```
<p class="one">Wurlitzer Electric Piano</p>
<p class="two">Wurlitzer Electric Piano</p>
<p class="three">Wurlitzer Electric Piano</p>
<p class="four">Wurlitzer Electric Piano</p>
<p class="five">Wurlitzer Electric Piano</p>
<p class="six">Wurlitzer Electric Piano</p>
<p class="seven">Wurlitzer Electric Piano</p>
<p class="eight">Wurlitzer Electric Piano</p>
```

```
p.one {border-style: solid;} 
p.two {border-style: dotted;} 
p.three {border-style: dashed;} 
p.four {border-style: double;} 
p.five {border-style: groove;} 
p.six {border-style: ridge;} 
p.seven {border-style: inset;} 
p.eight {border-style: outset;}
```

![](https://docs.microsoft.com/en-us/previous-versions/windows/internet-explorer/ie-developer/platform-apis/images/ff975616.border-style%28en-us%2Cvs.85%29.png)

**Border Color**
`border-color`

You can specify the color of a border using either RGB values, hex codes or CSS color names
It is possible to individually control the colors of the borders on different sides of a box using:
```
border-top-color
border-right-color 
border-bottom-color 
border-left-color
```

![](https://www.formget.com/wp-content/uploads/2014/09/border-color-example.png)


#### Padding
`padding`
The padding property allows you to specify how much space should appear between the content of an element and its border.
You can specify different values for each side of a box using:

```
padding-top 
padding-right 
padding-bottom 
padding-left
```

Or you can use a shorthand (where the values are in clockwise order: top, right, bottom, left):

`padding: 10px 5px 3px 1px;`

![](https://www.wikihow.com/images/thumb/7/74/Use-Padding-in-CSS-Step-6.jpg/aid6158881-v4-728px-Use-Padding-in-CSS-Step-6.jpg.webp)

#### Margin
`margin`
The margin property controls the gap between boxes. Its value is commonly given in pixels, although you may also use percentages or ems.
You can specify values for each side of a box using:

```
margin-top 
margin-right 
margin-bottom 
margin-left
```

You can also use the shorthand (where the values are in clockwise order: top, right, bottom, left):

`  margin: 1px 2px 3px 4px;`

Sometimes you might see the following, which means that the left and right margins should be 10 pixels and the top and bottom margins should be 20 pixels: 

`margin: 10px 20px;`

![](https://i.stack.imgur.com/FNT9b.gif)

#### Changing Inline/Block
`display`

The display property allows you to turn an inline element into a block-level element or vice versa, and can also be used to hide an element from the page.

The values this property can take are:

`inline` This causes a block-level element to act like an inline element.

`block` This causes an inline element to act like a block-level element.

`inline-block` This causes a block-level element to flow like an inline element, while retaining other features of a block-level element.

`none` This hides an element from the page. In this case, the element acts as though it is not on the page at all (although a user could still see the content of the box if they used the view source option in their browser).

#### Hidding Box
`visability`

The visibility property allows you to hide boxes from users but It leaves a space where the element would have been. 

This property can take two values:

`hidden` This hides the element.

`visible` This shows the element.



![](https://www.bitdegree.org/tutorials/wp-content/uploads/2018/10/Top-10-Tips-To-Learn-JavaScript.jpg)
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
