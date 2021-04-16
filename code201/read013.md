local storage
* persistent local storage is one of the areas where native client applications have held an advantage over web applications.
* Before HTML5, all attempts to achieve this were ultimately unsatisfactory in different ways.
What we really want is

. a lot of storage space
. on the client
. that persists beyond a page refresh
. and isn’t transmitted to the server
* L.S before HTML5 
. DHTML Behaviors, and one of these behaviors was called userData to end browser wars .
. userData allows web pages to store up to 64 KB of data per domain.
* Certain browser vendors also refer to it as “Local Storage” or “DOM Storage.” 
* HTML5 Storage: it’s a way for web pages to store named key/value pairs locally, within the client web browser. 
*  this data persists even after you navigate away from the web site, close your browser tab, exit your browser.
* HTML5 STORAGE SUPPORT
. IE 8.0+	. FIREFOX 3.5+	. SAFARI 4.0+	. CHROME 4.0+	. OPERA 10.5+	 . IPHONE 2.0+	. ANDROID 2.0+
* you’ll access HTML5 Storage through the localStorage object on the global window object.
* you can use Modernizr to detect support for HTML5 Storage.			
```if (Modernizr.localstorage) {
  // window.localStorage is available!
} else {
  // no native support for HTML5 storage :(
  // maybe try dojox.storage or a third-party solution
}
```
* HTML5 Storage is based on named key/value pairs. You store data based on a named key.
* The data can be any type supported by JavaScript, including strings, Booleans, integers, or floats.
*  the data is actually stored as a string
*  Calling getItem() with a non-existent key will return null rather than throw an exception.
* you can treat the localStorage object as an associative array:
``` var foo = localStorage.getItem("bar");
// ...
localStorage.setItem("bar", foo);
```
* There are also methods for removing the value for a given named key
```interface Storage {
  deleter void removeItem(in DOMString key);
  void clear();
};
```































