![](https://i.ytimg.com/vi/TXJB8QymWkY/maxresdefault.jpg)

# JS Object Literals; The DOM

## Object Literals in JavaScript

**What are Object literals in JavaScript?**
In plain English, an object literal is a comma-separated list of name-value pairs inside of curly braces.

Those values can be properties and functions. Here’s a snippet of an object literal with one property and one function.


![](https://miro.medium.com/max/2012/1*gslNlU_BKtZuSyjLMbmp7Q.png)

```
var greeting = {
    fullname: "Michael Jackson",
    greet: (message, name) => {
        console.log(message + " " + name + "!!");
    }
};
```

Here’s the snippet to use the object we just created to log the `fullname` and call the `greet` function with the `fullname` value.

![](https://qph.fs.quoracdn.net/main-qimg-b67729396d8dca0175296ce84833e18c.webp)

```
greet = (message)=> {
     console.log(message + " " + fullname + "!!");
}
```

However, you can create a function (e.g. `getFullName()`)that accesses the `fullname` value using the `this` keyword, which is just the current object context.

```
getFullName: () => {
     return this.fullname;
}
```

The greet function now would look like this:

```
greet: (message) => {
    console.log(message + " " + this.getFullName() + "!!");
}
```

All members of an object literal in JavaScript, both properties and functions, are public. The only place you can put private members is inside of a function.

For instance, I can add a private variable inside of the `greet` function to further customize the message. The function’s code now would look something like this.

```
(message, name) => {
    var customMessage = message + " " + name +
        "!!! It's nice to meet you."
    console.log(customMessage);
}
```

The `customMessage` variable is only visible in your function, but if it was placed outside of the function as a property, then it would be public.

Assigning an object literal to another variable only performs a shallow copy, which means you get the reference of the object instead of the actual value.

Let’s say I wanted to create another `greeting` object by using the greeting object we created earlier.

`var anotherGreeting = greeting;`

Doing this might look fine at first, but any change made to the copied object (`anotherGreeting`) will reflect in the original object (greeting).

```
var copiedGreeting = greeting;
copiedGreeting.fullname = "Waleed Afifi";
console.log(greeting.fullname + " == " + copiedGreeting.fullname);

---------------output----------------
Waleed Afifi == Waleed Afifi
```

You cannot copy an object literal without manually copying all the values.

Lastly, you can mutate members of an object literal, meaning you can add and remove them as you please.

If I need to remove the `fullname` property from the object and add other properties (e.g. first and last name), I can simply do this.

```
delete greeting["fullname"];
greeting.firstname = "Michael";
greeting.lastname = "Jackson";
```

![](https://i.ytimg.com/vi/8-q21K0w2WE/maxresdefault.jpg)

# The HTML DOM (Document Object Model)

With the HTML DOM, JavaScript can access and change all the elements of an HTML document.

When a web page is loaded, the browser creates a Document Object Model of the page.

The HTML DOM model is constructed as a tree of Objects:

_The HTML DOM Tree of Objects_
![](https://www.w3schools.com/js/pic_htmltree.gif)

With the object model, JavaScript gets all the power it needs to create dynamic HTML:

* JavaScript can change all the HTML elements in the page
* JavaScript can change all the HTML attributes in the page
* JavaScript can change all the CSS styles in the page
* JavaScript can remove existing HTML elements and attributes
* JavaScript can add new HTML elements and attributes
* JavaScript can react to all existing HTML events in the page
* JavaScript can create new HTML events in the page


![](https://i.ytimg.com/vi/_GxpmQ54aqg/maxresdefault.jpg)

## What is the DOM?

The DOM is a W3C (World Wide Web Consortium) standard.

The DOM defines a standard for accessing documents:

"The W3C Document Object Model (DOM) is a platform and language-neutral interface that allows programs and scripts to dynamically access and update the content, structure, and style of a document."

The W3C DOM standard is separated into 3 different parts:

1. Core DOM - standard model for all document types
1. XML DOM - standard model for XML documents
1. HTML DOM - standard model for HTML documents

![](https://lh3.googleusercontent.com/proxy/gfBM7X7Lpi0CgFDquf2UoiYOD8RHM92a6ORl60b9JXcjBwzFLotQzP8SkJIjfCmtJkLUIe8-t1OjbMO62EQK9dmTDK5L3XBp8wuSV_nnCaRXIifO1bp7PyS3xvTupB2PwCCQcdOaZbL0)

__What is the HTML DOM?__
The HTML DOM is a standard object model and programming interface for HTML. It defines:

* The HTML elements as objects
* The properties of all HTML elements
* The methods to access all HTML elements
* The events for all HTML elements

__In other words:__ The HTML DOM is a standard for how to get, change, add, or delete HTML elements.


## JavaScript - HTML DOM Methods

HTML DOM methods are `actions` you can perform (on HTML Elements).

HTML DOM properties are `values` (of HTML Elements) that you can set or change.


**The DOM Programming Interface**

The HTML DOM can be accessed with JavaScript (and with other programming languages).

In the DOM, all HTML elements are defined as `objects`.

The programming interface is the properties and methods of each object.

A `property` is a value that you can get or set (like changing the content of an HTML element).

A `method` is an action you can do (like add or deleting an HTML element).

__Example__
The following example changes the content (the `innerHTML`) of the `<p>` element with `id="demo"`:

```
<html>
    <body>

        <p id="demo"></p>

        <script>
            document.getElementById("demo").innerHTML = "Hello World!";
        </script>
        
    </body>
</html>
```

In the example above, `getElementById` is a **method**, while `innerHTML` is a **property**.

**The getElementById Method**

The most common way to access an HTML element is to use the id of the element.

In the example above the `getElementById` method used `id="demo"` to find the element.


**The innerHTML Property**

The easiest way to get the content of an element is by using the `innerHTML` property.

The `innerHTML` property is useful for getting or replacing the content of HTML elements.

