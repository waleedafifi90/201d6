![](https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcR4wGS9p-Xiu4k9F8Fa9PViUGRJAFUnR99G8WxkgDpYnmuvFGsn&usqp=CAU)

# HTML Forms

HTML Forms are required, when you want to collect some data from the site visitor. For example, during user registration you would like to collect information such as name, email address, credit card, etc.

The HTML `<form>` tag is used to create an HTML form and it has following syntax −

```
<form action = "Script URL" method = "GET|POST">
   form elements like input, textarea etc.
</form>
```

## Form Attributes
Apart from common attributes, following is a list of the most frequently used form attributes −

**action** Backend script ready to process your passed data.
**method** Method to be used to upload data. The most frequently used are GET and POST methods.
**target** Specify the target window or frame where the result of the script will be displayed. It takes values like _blank, _self, _parent etc.
**enctype** You can use the enctype attribute to specify how the browser encodes the data before it sends it to the server. Possible values are −

**application/x-www-form-urlencoded** − This is the standard method most forms use in simple scenarios.

**mutlipart/form-data** − This is used when you want to upload binary data in the form of files like image, word file etc.

![](https://dropdownmenu.com/data/upload/2013/08/30/5220cd1403f85.png)
## HTML Form Controls
There are different types of form controls that you can use to collect data using HTML form −

* Text Input Controls
* Checkboxes Controls
* Radio Box Controls
* Select Box Controls
* File Select boxes
* Hidden Controls
* Clickable Buttons
* Submit and Reset Button

## Text Input Controls
There are three types of text input used on forms −

![](https://media.geeksforgeeks.org/wp-content/uploads/20191113100712/django-forms-python.png)

* **Single-line text input controls** − This control is used for items that require only one line of user input, such as search boxes or names. They are created using HTML <input> tag.
* **Password input controls** − This is also a single-line text input but it masks the character as soon as a user enters it. They are also created using HTMl `<input>` tag.
* **Multi-line text input controls** − This is used when the user is required to give details that may be longer than a single sentence. Multi-line input controls are created using HTML `<textarea>` tag.


**Example**
Here is a basic example of a single-line text input used to take first name and last name −

```
<!DOCTYPE html>
<html>

   <head>
      <title>Text Input Control</title>
   </head>
	
   <body>
      <form >
         First name: <input type = "text" name = "first_name" />
         <br>
         Last name: <input type = "text" name = "last_name" />
      </form>
   </body>
	
</html>
```

## Attributes
Following is the list of attributes for `<input>` tag for creating text field.

`type` Indicates the type of input control and for text input control it will be set to text.
`name` Used to give a name to the control which is sent to the server to be recognized and get the value
`value` This can be used to provide an initial value inside the control.
`size` Allows to specify the width of the text-input control in terms of characters.
`maxlength` Allows to specify the maximum number of characters a user can enter into the text box.


## Password input controls
This is also a single-line text input but it masks the character as soon as a user enters it. They are also created using HTML `<input>` tag but type attribute is set to **password**.

![](https://cdn.dribbble.com/users/408001/screenshots/3524092/login-form.gif)

**Example**
```
<!DOCTYPE html>
<html>

   <head>
      <title>Password Input Control</title>
   </head>
	
   <body>
      <form >
         User ID : <input type = "text" name = "user_id" />
         <br>
         Password: <input type = "password" name = "password" />
      </form>
   </body>
	
</html>
```

## Multiple-Line Text Input Controls
This is used when the user is required to give details that may be longer than a single sentence. Multi-line input controls are created using HTML `<textarea>` tag.

**Example**
```
<!DOCTYPE html>
<html>

   <head>
      <title>Multiple-Line Input Control</title>
   </head>
	
   <body>
      <form>
         Description : <br />
         <textarea rows = "5" cols = "50" name = "description">
            Enter description here...
         </textarea>
      </form>
   </body>
</html>
```

_Attributes_
`name` Used to give a name to the control which is sent to the server to be recognized and get the value.
`rows` Indicates the number of rows of text area box.
`cols` Indicates the number of columns of text area box

## Checkbox Control
Checkboxes are used when more than one option is required to be selected. They are also created using HTML `<input>` tag but type attribute is set to **checkbox**.

![](https://lh3.googleusercontent.com/proxy/HOUV68P4EftI8lwl5U2vE7Sf-rmeS_1EeUm9he4x3IcnQYvGa4Py1gjBJiTrgyXrezp8NtvWTJKRA26bCoBouNpCPCucNOek--lpxFChukRjyYx7nu0)

```
<!DOCTYPE html>
<html>

   <head>
      <title>Checkbox Control</title>
   </head>
	
   <body>
      <form>
         <input type = "checkbox" name = "maths" value = "on"> Maths
         <input type = "checkbox" name = "physics" value = "on"> Physics
      </form>
   </body>
	
</html>
```

## Select Box Control
A select box, also called drop down box which provides option to list down various options in the form of drop down list, from where a user can select one or more options.

```
<!DOCTYPE html>
<html>

   <head>
      <title>Select Box Control</title>
   </head>
	
   <body>
      <form>
         <select name = "dropdown">
            <option value = "Maths" selected>Maths</option>
            <option value = "Physics">Physics</option>
         </select>
      </form>
   </body>
	
</html>
```

## File Upload Box

If you want to allow a user to upload a file to your web site, you will need to use a file upload box, also known as a file select box. This is also created using the `<input>` element but type attribute is set to **file**.

![](https://sites.google.com/site/pghopenmrsmodules/home/image-upload-in-html-forms/image1.png?attredirects=0)

```
<!DOCTYPE html>
<html>

   <head>
      <title>File Upload Box</title>
   </head>

   <body>
      <form>
         <input type = "file" name = "fileupload" accept = "image/*" />
      </form>
   </body>
	
</html>
```

## Button Controls

There are various ways in HTML to create clickable buttons. You can also create a clickable button using `<input>` tag by setting its type attribute to **button**. The type attribute can take the following values −

![](https://www.android-examples.com/wp-content/uploads/2016/03/submit-button.png)

```
<!DOCTYPE html>
<html>

   <head>
      <title>File Upload Box</title>
   </head>
	
   <body>
      <form>
         <input type = "submit" name = "submit" value = "Submit" />
         <input type = "reset" name = "reset"  value = "Reset" />
         <input type = "button" name = "ok" value = "OK" />
         <input type = "image" name = "imagebutton" src = "/html/images/logo.png" />
      </form>
   </body>
	
</html>
```

# HTML - Lists
HTML offers web authors three ways for specifying lists of information. All lists must contain one or more list elements. Lists may contain −

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



![](https://3.bp.blogspot.com/-m3yVfQjKy50/VWr2wjykduI/AAAAAAAAO-4/DEe2-YYq6Pw/s1600/HTML-table-shortcode.jpg)
## HTML - Tables

The HTML tables allow web authors to arrange data like text, images, links, other tables, etc. into rows and columns of cells.

The HTML tables are created using the `<table>` tag in which the `<tr>` tag is used to create table rows and `<td>` tag is used to create data cells. The elements under `<td>` are regular and left aligned by default

![](https://1.bp.blogspot.com/-Z3gIwonB54A/WtOcwFhYxII/AAAAAAAAARE/cIRGmSVZ_HAuuJttImPoi8jRZOVJ3MjWACLcBGAs/s640/firstrow-firstcolumn.png)
Example

```
<!DOCTYPE html>
<html>

   <head>
      <title>HTML Tables</title>
   </head>
	
   <body>
      <table border = "1">
         <tr>
            <td>Row 1, Column 1</td>
            <td>Row 1, Column 2</td>
         </tr>
         
         <tr>
            <td>Row 2, Column 1</td>
            <td>Row 2, Column 2</td>
         </tr>
      </table>
      
   </body>
</html>
```

Here, the border is an attribute of `<table>` tag and it is used to put a border across all the cells. If you do not need a border, then you can use border = "0".


![](https://static.javatpoint.com/htmlpages/images/tableevenodd.png)
### Table Heading

Table heading can be defined using `<th>` tag. This tag will be put to replace `<td>` tag, which is used to represent actual data cell. Normally you will put your top row as table heading as shown below, otherwise you can use `<th>` element in any row. Headings, which are defined in `<th>` tag are centered and bold by default.

**Example**
```
<!DOCTYPE html>
<html>

   <head>
      <title>HTML Table Header</title>
   </head>
	
   <body>
      <table border = "1">
         <tr>
            <th>Name</th>
            <th>Salary</th>
         </tr>
         <tr>
            <td>Ramesh Raman</td>
            <td>5000</td>
         </tr>
         
         <tr>
            <td>Shabbir Hussein</td>
            <td>7000</td>
         </tr>
      </table>
   </body>
   
</html>
```


![](https://i.stack.imgur.com/tg2Jl.png)
### Cellpadding and Cellspacing Attributes

There are two attributes called cellpadding and cellspacing which you will use to adjust the white space in your table cells. The cellspacing attribute defines space between table cells, while cellpadding represents the distance between cell borders and the content within a cell.

```
<!DOCTYPE html>
<html>

   <head>
      <title>HTML Table Cellpadding</title>
   </head>
	
   <body>
      <table border = "1" cellpadding = "5" cellspacing = "5">
         <tr>
            <th>Name</th>
            <th>Salary</th>
         </tr>
         <tr>
            <td>Ramesh Raman</td>
            <td>5000</td>
         </tr>
         <tr>
            <td>Shabbir Hussein</td>
            <td>7000</td>
         </tr>
      </table>
   </body>
	
</html>
```

### Colspan and Rowspan Attributes

You will use **colspan** attribute if you want to merge two or more columns into a single column. Similar way you will use **rowspan** if you want to merge two or more rows.

```
<!DOCTYPE html>
<html>

   <head>
      <title>HTML Table Colspan/Rowspan</title>
   </head>
	
   <body>
      <table border = "1">
         <tr>
            <th>Column 1</th>
            <th>Column 2</th>
            <th>Column 3</th>
         </tr>
         <tr>
            <td rowspan = "2">Row 1 Cell 1</td>
            <td>Row 1 Cell 2</td>
            <td>Row 1 Cell 3</td>
         </tr>
         <tr>
            <td>Row 2 Cell 2</td>
            <td>Row 2 Cell 3</td>
         </tr>
         <tr>
            <td colspan = "3">Row 3 Cell 1</td>
         </tr>
      </table>
   </body>
	
</html>
```


![](https://templatefor.net/wp-content/uploads/2019/09/HTML-Table-CSS-Table.jpg)
### Table Header, Body, and Footer

Tables can be divided into three portions − a header, a body, and a foot. The head and foot are rather similar to headers and footers in a word-processed document that remain the same for every page, while the body is the main content holder of the table.

The three elements for separating the head, body, and foot of a table are −

`<thead>` − to create a separate table header.

`<tbody>` − to indicate the main body of the table.

`<tfoot>` − to create a separate table footer.

A table may contain several `<tbody>` elements to indicate different pages or groups of data. But it is notable that `<thead>` and `<tfoot>` tags should appear before `<tbody>`


```
<!DOCTYPE html>
<html>

   <head>
      <title>HTML Table</title>
   </head>
	
   <body>
      <table border = "1" width = "100%">
         <thead>
            <tr>
               <td colspan = "4">This is the head of the table</td>
            </tr>
         </thead>
         
         <tfoot>
            <tr>
               <td colspan = "4">This is the foot of the table</td>
            </tr>
         </tfoot>
         
         <tbody>
            <tr>
               <td>Cell 1</td>
               <td>Cell 2</td>
               <td>Cell 3</td>
               <td>Cell 4</td>
            </tr>
         </tbody>
         
      </table>
   </body>
	
</html>
```


## CSS Tables

![](https://steemitimages.com/640x0/https://res.cloudinary.com/hpiynhbhq/image/upload/v1519058638/xfjgtsuxa49milh9gpkl.png)
### Table Borders
To specify table borders in CSS, use the `border` property.

The example below specifies a black border for `<table>`, `<th>`, and `<td>` elements:

__EXAMPLE__
```
table, th, td {
  border: 1px solid black;
}
```

### Collapse Table Borders
The `border-collapse` property sets whether the table borders should be collapsed into a single border:

```
table {
  border-collapse: collapse;
}

table, th, td {
  border: 1px solid black;
}

```

### Striped Tables

![](https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcRC5X9-Vff9RuIpUBDBqEpW626ngU16GlL7Mcu4XTVfBonscT4B&usqp=CAU)

For zebra-striped tables, use the `nth-child()` selector and add a `background-color` to all even (or odd) table rows:

```
tr:nth-child(even) {background-color: #f2f2f2;}
```


![](https://www.simplilearn.com/ice9/free_resources_article_thumb/X_Reasons_to_learn_Javascript.jpg)
# Functions, Methods, and Objects

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1576395857500/Him6j7txy.png)
## JavaScript Objects
In JavaScript, an object is data, with properties and methods.

When you declare a JavaScript variable like this:

`var message="Hello World!";`

You create a JavaScript String object.

The String object has a built-in property called length. For the string above, length has the value 12.

The String object also have several built-in methods.

### Accessing Object Properties

`objectName.propertyName`

```
var message = "Hello world!";
var messageLength = message.length; //12
```
### Accessing Object Methods

`objectName.methodName()`

```
var message = "Hello world!";
var newMessage = message.toUpperCase(); //HELLO WORLD!
```

### Object Method

![](https://nandokakimoto.files.wordpress.com/2011/05/example1.png)

```
var person = {
  firstName: "John",
  lastName : "Doe",
  id       : 5566,
  fullName : function() {
    return this.firstName + " " + this.lastName;
  }
};
```


![](https://lenadesignorg.files.wordpress.com/2020/02/2.jpg)
# JavaScript Form Event
A form event is fired when a form control receive or loses focus or when the user modify a form control value such as by typing text in a text input, select any option in a select box etc. Here're some most important form events and their event handler.

## The Focus Event (onfocus)
This event occurs when an element gets focused on a web page. The `onfocus` event handler is used to handle this event.

The following example will highlight the background of text input in green color when it receives the focus.

![](https://i.stack.imgur.com/MeKwz.gif)

```
<!DOCTYPE html>

<html lang="en">

<head>

   <meta charset="UTF-8">

   <title> JavaScript Handling the Focus Event </title>

</head>

<body>

    <script>

        function highlightInput(elm){

            elm.style.background = "lightgreen";

        }    

    </script>

    <input type="text" onfocus="highlightInput(this)">

    <button type="button">Button</button>

</body>

</html>
```

## The Blur Event (onblur)
This event occurs when the user takes the focus away from a form element. The `onblur` event handler is used to handle this event.

![](https://user-images.githubusercontent.com/4082216/45522897-f6978200-b793-11e8-99ce-7a5f34c2e042.gif)

```
<!DOCTYPE html>

<html lang="en">

<head>

   <meta charset="UTF-8">

   <title> JavaScript OnBlur Event </title>

</head>

<body>

 <input type="text" onblur="alert('Text input loses focus!')">

 <button type="button">Submit</button>


</body>

</html>
```

## The Change Event (onchange)
This event occurs when the value of a form element is changed. The `onchange` event handler is used to handle this event.

![](https://4.bp.blogspot.com/-OJJptRAKJYM/W2MzoSL_usI/AAAAAAAAFpA/wDKy1kdUfBMMuidNaYCnnB50o1OFoPWkwCLcBGAs/s1600/%2540InputTwoWayBinding.gif)

```
<!DOCTYPE html>

<html lang="en">

<head>

   <meta charset="UTF-8">

   <title> JavaScript OnChange Event </title>

</head>

<body>

   <select onchange="alert('You have changed the selection!');">

    <option>Select</option>

    <option>OnePlus</option>

    <option>Samsung</option>

    </select>

  <p><strong>Note:</strong> Select any option in select box to see how it works.</p>

</body>

</html>
```

## The Submit Event (onsubmit)
The submit event occurs when the submit button is clicked. The `onsubmit` event handler is used to handle this event.

![](https://miro.medium.com/max/2560/1*GQ2x60myrsftTcLXzFY9Lg.gif)

```
<!DOCTYPE html>

<html lang="en">

<head>

   <meta charset="UTF-8">

   <title> JavaScript OnSubmit Event </title>

</head>

<body>

  <form action="../index.php" method="post" onsubmit="alert('Form data will be submitted to 

  the server!');">

     <label>First Name:</label>

     <input type="text" name="first-name" required>

     <input type="submit" value="Submit">

  </form>

</body>

</html>
```