![](https://3kllhk1ibq34qk6sp3bhtox1-wpengine.netdna-ssl.com/wp-content/uploads/2019/01/artboard-18-copy-8@3x-1560x760.png)

# JS Debugging

## Execution context

![](https://lh3.googleusercontent.com/Kslrk3U4J-QrkOX7zp3hUC2UIBxorVssUHX_ybRAUKELW8686sptO1exa9rM-87sI5A30N74aIQZh8NyCeqVQO1D469aNIbH8TwFFs1ybPcx1a0Xpg9_m84GrM3S6lkSgr3zWsN5KZrG3P34mWa_Zz_fWzz_7MFmjqsChDcrNLqazE8wkwGlbLt_bb_aaleUh26GEwCD_Wvgv5ijvPK2QwJnU6I2Wm-JMXZENdSxhPuijJD-6ve7T8MqlJ5H6Ufi1WuzXKSs-llulsMfBPkAz2LitwjGhKoPibij8ObYlgILT90EK6ZlR8qKbnCG193CJfG0EaO98UQaZ6ZHJBSDRW1C5gQEcAtYCSi5bM2RCcVFZAZV8zBEVwec4yfd0iQHlNGklpphLzwv7zPG3yhtwav9VWq-ORP0brJ2i7o3ISIKFT5IY8sO8NWNkzx9EN7jg2TEU58SSKNXatjG52l0bC-_rWuK4bXpennNZl142UzBkFGsRn6Rw89ePPQcyhlSA98gw3veq4DLjIufio3Oo6_jxdxP-MHP62W0_B5L81e8EqoNrbt_MO9XwZLJtKaamt_56_L3qe3L71mCmYVqAk0CoFLrn8qXF-_LQmRjWGNwGfOtgMlLeEKweqov4KTou7oPyZmIQ0WDyTDmK3O4rTLy3uAJXjhNMRBNqXAg0g=w1440-h805-no)

Execution context (EC) is defined as the environment in which the JavaScript code is executed. By environment, I mean the value of this, variables, objects, and functions JavaScript code has access to at a particular time.

```
var a = 10;

function functionA() {

	console.log("Start function A");

	function functionB(){
		console.log("In function B");
	}

	functionB();

}

functionA();

console.log("GlobalContext");
```

![](https://miro.medium.com/max/1400/1*bDebsOuhRx9NMyvLHY2zxA.gif)

As soon as the above code loads into the browser, JS engine pushes the global execution context in the execution context stack. When functionA is called from global execution context, JS engine pushes functionA execution context in the execution context stack and starts executing functionA.

When functionB is called from functionA execution context, JS engine pushes functionB execution context in the execution context stack. Once all the code of functionB gets executed, JS engine pops out functionB execution context. After this, as functionA execution context is on top of the execution context stack, JS engine starts executing the remaining code of functionA.

Once all the code from functionA gets executed, JS engine pops out functionA execution context from execution context stack and starts executing remaining code from the global execution context.

![](https://res.cloudinary.com/practicaldev/image/fetch/s--Zjmd_28H--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://thepracticaldev.s3.amazonaws.com/i/7c9pbcb63avm83drprur.png)




## Error Objects

![](https://lh3.googleusercontent.com/proxy/9L5d49PiO-KcIfE6JjaUw2pTl8hXf997Nd88ujbri8_gu-NfrnhZfOVQNv2RJPo-kB6W0vjRb9mxl1g_E7-gCBh-UgxqGEpDpx4CCrvIvAPiFh_1gNDsrSqV-qQtUy3D7MV_)

Error objects can help you find where your mistakes are and browser have tool to help you read them>

The error object provides two useful properties: name and message.

### Error Object Properties

| Property  | Description |
| ------------- | ------------- |
| name  | Sets or returns an error name  |
| message  | Sets or returns an error message (a string)  |


### Error Name Values

| Error Name  | Description |
| ------------- | ------------- |
| EvalError  | An error has occurred in the eval() function  |
| RangeError  | A number "out of range" has occurred  |
| ReferenceError  | An illegal reference has occurred  |
| SyntaxError  | A syntax error has occurred)  |
| TypeError  | A type error has occurred  |
| URIError  | An error in encodeURI() has occurred  |	


__Eval Error__
An `EvalError` indicates an error in the eval() function.


__Range Error__
A `RangeError` is thrown if you use a number that is outside the range of legal values.

For example: You cannot set the number of significant digits of a number to 500.

```
var num = 1;
try {
  num.toPrecision(500);   // A number cannot have 500 significant digits
}
catch(err) {
  document.getElementById("demo").innerHTML = err.name;
}
```

__Reference Error__
A `ReferenceError` is thrown if you use (reference) a variable that has not been declared:

```
var x;
try {
  x = y + 1;   // y cannot be referenced (used)
}
catch(err) {
  document.getElementById("demo").innerHTML = err.name;
}
```

__Syntax Error__
A `SyntaxError` is thrown if you try to evaluate code with a syntax error.

```
try {
  eval("alert('Hello)");   // Missing ' will produce an error
}
catch(err) {
  document.getElementById("demo").innerHTML = err.name;
}
```

__Type Error__
A `TypeError` is thrown if you use a value that is outside the range of expected types:

```
var num = 1;
try {
  num.toUpperCase();   // You cannot convert a number to upper case
}
catch(err) {
  document.getElementById("demo").innerHTML = err.name;
}
```

__URI (Uniform Resource Identifier) Error__

A `URIError` is thrown if you use illegal characters in a URI function:

```
try {
  decodeURI("%%%");   // You cannot URI decode percent signs
}
catch(err) {
  document.getElementById("demo").innerHTML = err.name;
}
```


## JavaScript Errors - Throw and Try to Catch

The `try` statement lets you test a block of code for errors.

The `catch` statement lets you handle the error.

The `throw` statement lets you create custom errors.

The `finally` statement lets you execute code, after try and catch, regardless of the result.


### Errors Will Happen!

When executing JavaScript code, different errors can occur.

Errors can be coding errors made by the programmer, errors due to wrong input, and other unforeseeable things.

```
<p id="demo"></p>

<script>
try {
  adddlert("Welcome guest!");
}
catch(err) {
  document.getElementById("demo").innerHTML = err.message;
}
</script>
```

### JavaScript try and catch

The `try` statement allows you to define a block of code to be tested for errors while it is being executed.

The `catch` statement allows you to define a block of code to be executed, if an error occurs in the `try` block.

The JavaScript statements `try` and `catch` come in pairs:

```
try {
  Block of code to try
}
catch(err) {
  Block of code to handle errors
}
```

### JavaScript Throws Errors
When an error occurs, JavaScript will normally stop and generate an error message.

The technical term for this is: JavaScript will **throw an exception (throw an error)**.

JavaScript will actually create an **Error object** with two properties: **name** and **message**.


### The throw Statement
The `throw` statement allows you to create a custom error.

Technically you can **throw an exception (throw an error)**.

The exception can be a JavaScript `String`, a `Number`, a `Boolean` or an `Object`:

```
throw "Too big";    // throw a text
throw 500;          // throw a number
```

If you use `throw` together with `try` and `catch`, you can control program flow and generate custom error messages.


### Input Validation Example

This example examines input. If the value is wrong, an exception (err) is thrown.

The exception (err) is caught by the catch statement and a custom error message is displayed:

```
<!DOCTYPE html>
<html>
<body>

<p>Please input a number between 5 and 10:</p>

<input id="demo" type="text">
<button type="button" onclick="myFunction()">Test Input</button>
<p id="p01"></p>

<script>
function myFunction() {
  var message, x;
  message = document.getElementById("p01");
  message.innerHTML = "";
  x = document.getElementById("demo").value;
  try {
    if(x == "") throw "empty";
    if(isNaN(x)) throw "not a number";
    x = Number(x);
    if(x < 5) throw "too low";
    if(x > 10) throw "too high";
  }
  catch(err) {
    message.innerHTML = "Input is " + err;
  }
}
</script>

</body>
</html>
```


```
try {
  Block of code to try
}
catch(err) {
  Block of code to handle errors
}
finally {
  Block of code to be executed regardless of the try / catch result
}
```


```
function myFunction() {
  var message, x;
  message = document.getElementById("p01");
  message.innerHTML = "";
  x = document.getElementById("demo").value;
  try {
    if(x == "") throw "is empty";
    if(isNaN(x)) throw "is not a number";
    x = Number(x);
    if(x > 10) throw "is too high";
    if(x < 5) throw "is too low";
  }
  catch(err) {
    message.innerHTML = "Error: " + err + ".";
  }
  finally {
    document.getElementById("demo").value = "";
  }
}
```

![](https://www.bitdegree.org/learn/storage/media/images/de2e3e9e-6bf6-4082-b507-90ac4e58eeb6.o.jpg)
## Use developer tool web browser

![](https://developers.google.com/web/tools/chrome-devtools/images/open-from-main.png)


1. Rearrange the text and images on a page

With Chrome Dev Tools, you can easily change of the order of elements as they appear on a page by simply dragging them with your mouse. Click the magnifying glass icon, hover over any element of the page - be it text paragraphs, images, or list items - and then drag that selection to place it at a different location.

![](https://www.labnol.org/37a3a9259bd1b48d496b30f9c257722b/order-list-items.gif)


2. Experiment with different colors

Web pages often use the hexadecimal format for writing colors but if the #AABBCC format makes no sense to you, just write the color names in plain English like Gold, Aqua and more. Just type the first character and Chrome Dev Tools will show all the available colors that begin with that letter.

![](https://www.labnol.org/b39af9b628ab91bfe3eb8d4f87b32319/change-colors.gif)


3. Reveal the Hidden Passwords
Chrome may auto-fill the password field on a login form of a web page but you can’t view that password as it’s hidden behind asterisk characters. You can however use Chrome Dev Tools to change the type of the password input field from “password” to “text” and reveal the hidden password.


4. Edit your Web Pages inline
Web pages are non-editable in the browser but there’s a little trick that will let you edit web pages inline as you do in a word processor. Open Chrome Dev Tools, switch to the Console tab and type document.body.contenteditable=true at the command prompt. Voila! The page becomes editable.

![](https://www.labnol.org/afaaedba411fcaf392b26bd5b9cffbc7/content-editable.gif)


5. Chrome as a Calculator
While the Console tab is active, you can write arithmetic expressions and also perform date calculations like how many days between two dates or write a date as a human-readable string. A little know of the Date object in JavaScript will come handy. Chrome stores the value of the previous calculation in a special \$_ variable that can be used in lengthy calculations.

![](https://www.labnol.org/8e81b10af7075cef3609c06577ab32fb/date-calculations.gif)


