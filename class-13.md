![](https://webdev.imgix.net/storage-for-the-web/hero.jpg?auto=format&fit=max&w=2880)

# Local Storage

### Storage for the web

Before HTML5, all attempts to achieve this were ultimately unsatisfactory in different ways.

![](https://res.cloudinary.com/de4rvmslk/image/upload/f_auto,q_auto,w_1440/v1/LocalStorage-cover_photo.png)
**What is HTML Web Storage?**

HTML5 Storage is based on named key/value pairs. You store data based on a named key, then you can retrieve that data with the same key. The named key is a string. The data can be any type supported by JavaScript, including strings, Booleans, integers, or floats. However, the data is actually stored as a string. If you are storing and retrieving anything other than strings, you will need to use functions like `parseInt()` or `parseFloat()` to coerce your retrieved data into the expected JavaScript datatype.


With web storage, web applications can store data locally within the user's browser.


Before HTML5, application data had to be stored in cookies, included in every server request. Web storage is more secure, and large amounts of data can be stored locally, without affecting website performance.

Before local storage cookies are used to save some of data but it's going to slow your application, cookies size 4KB only but in local storage it can gives you at least 5MB

### STORAGEEVENT OBJECT
| PROPERTY  |  TYPE |  DESCRIPTION |
|---|---|---|
| key  |  string |  the named key that was added, removed, or modified |
| oldValue  | any  |  the previous value (now overwritten), or null if a new item was added |
| newValue  | any  | the new value, or null if an item was removed  |
| url*	  |  string | the page which called a method that triggered this change  |


![](https://techglimpse.com/wp-content/uploads/2013/05/Pass-LocalStorage-data-to-PHP-using-jQuery.jpeg)
### HTML Web Storage Objects
HTML web storage provides two objects for storing data on the client:

* `window.localStorage` - stores data with no expiration date
* `window.sessionStorage` - stores data for one session (data is lost when the browser tab is closed)


Before we can start using the local storage we need to check if the browser supports storage or not by using this code in your web applicatiion
```
if (typeof(Storage) !== "undefined") {
  // Code for localStorage/sessionStorage.
} else {
  // Sorry! No Web Storage support..
}
```

### The localStorage Object
The localStorage object stores the data with no expiration date. The data will not be deleted when the browser is closed, and will be available the next day, week, or year.

![](https://gblobscdn.gitbook.com/assets%2F-LAn5scXl2uqUJUOqkJo%2F-LAn5wecEraNWaG7Ig2g%2F-LAn6Egc5yhMFI-0p1O6%2Flocal-storage-%E2%9C%95-fig-1.png?alt=media)
```
// Store
localStorage.setItem("lastname", "Afifi");

// Retrieve
document.getElementById("result").innerHTML = localStorage.getItem("lastname");
```

explaine:

* Create a localStorage name/value pair with name="lastname" and value="Afifi"
* Retrieve the value of "lastname" and insert it into the element with id="result"

To remove lastname from the Storage as below
```
localStorage.removeItem("lastname");
```

### The sessionStorage Object
The `sessionStorage` object is equal to the localStorage object, **except** that it stores the data for only one session. The data is deleted when the user closes the specific browser tab.

The following example counts the number of times a user has clicked a button, in the current session:

```
if (sessionStorage.clickcount) {
  sessionStorage.clickcount = Number(sessionStorage.clickcount) + 1;
} else {
  sessionStorage.clickcount = 1;
}
document.getElementById("result").innerHTML = "You have clicked the button " + sessionStorage.clickcount + " time(s) in this session.";
```

![](https://i.ytimg.com/vi/k8yJCeuP6I8/maxresdefault.jpg)
## localStorage in JavaScript apps
To use localStorage in your web applications, there are five methods to choose from:

1. `setItem()`: Add key and value to `localStorage`
2. `getItem()`: Retrieve a value by the key from `localStorage`
3. `removeItem()`: Remove an item by key from `localStorage`
4. `clear()`: Clear all `localStorage`
5. `key()`: Passed a number to retrieve nth key of a `localStorage`


**setItem()**
Just as the name implies, this method allows you to store values in the `localStorage` object.

```
window.localStorage.setItem('name', 'Waleed Afifi');
```

Where name is the key and Waleed Afifi is the value. Also note that localStorage can only store strings.

**getItem()**
The `getItem()` method allows you to access the data stored in the browser’s localStorage object.

```
window.localStorage.getItem('user');

// Return
“{“name”:Waleed Afifi,”location”:”Lagos”}”

```

**removeItem()**
When passed a key name, the `removeItem()` method will remove that key from the storage if it exists. If there is no item associated with the given key, this method will do nothing.

```
window.localStorage.removeItem('name');
```

**clear()**
This method, when invoked, clears the entire storage of all records for that domain. It does not receive any parameters.

```
window.localStorage.clear();
```

**key()**
The `key()` method comes in handy in situations where you need to loop through keys and allows you to pass a number or index to `localStorage` to retrieve the name of the key.

```
var KeyName = window.localStorage.key(index);
```


### localStorage limitations
As easy as it is to use `localStorage`, it is also easy to misuse it. The following are limitations, and also ways to NOT use `localStorage`:

1. Do not store sensitive user information in localStorage
2. It is not a substitute for a server based database as information is only stored on the browser
3. localStorage is limited to 5MB across all major browsers
4. localStorage is quite insecure as it has no form of data protection and can be accessed by any code on your web page
5. localStorage is synchronous, meaning each operation called would only execute one after the other
