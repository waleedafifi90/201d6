# HTML Tables; JS Constructor Functions

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


![](https://www.homeandlearn.co.uk/javascript/images/chapter_4/two_arguments.gif)
## Functions
A function is a collection of JavaScript statements. These statements usually have a single purpose, such as performing a complex calculation or verifying the data entered into an HTML form. Functions can be passed copies of objects or variables to work with. This is done in the parameter list.

JavaScript functions can be placed inside script tags anywhere in the document. However, they should be placed in the head of the document to guarantee they are loaded before being called from script statements in the body of the document.

```
function functionName( parameter_1, parameter_2, ..  parameter_n ) {
   statement1;
   statement2;
   .
   .
   .
   statementn;
}
```

Here is a function that finds the maximum value of two numbers.

```
function getMax( n1, n2 ) {
   if ( n1 < n2 ) {
      return n2;
   } else {
      return n1;
   }
```

Here is an example of how this function might be used.

```
<html>
  <head>
    <script>
    function getMax( n1, n2 ) {
       if ( n1 < n2 ) {
          return n2;
       } else {
          return n1;
       }
    }
    </script>
  </head>
  <body>
   <script>
     document.write( "<p>" );
     document.write( "The largest number of 5 or 6 is: " + getMax( 5, 6 ) );
     document.write( "</p>" );
    </script>
  </body>
</html>
```

A function to check the length of a student username

```
html>
  <head>
    <script>
    function checkUserName( form ) {
       if ( form.reg.value.length != 8 ) {
          alert( "You have not entered an eight character string" );
          return false;
       } else {
          alert( "This is correct" );
          return true;
       }
    }
    </script>
  </head>
  <body>
   <p> Please enter your student username: <input type="text" name="reg" />
   <input type="button" onclick="checkUserName(form);" value="check validity"/> 
  </body>
</html>
```

## JavaScript Methods
JavaScript methods are actions that can be performed on objects.

A JavaScript `method` is a property containing a `function definition`.

**Adding a Method to an Object**

```
person.name = function () {
  return this.firstName + " " + this.lastName;
};
```