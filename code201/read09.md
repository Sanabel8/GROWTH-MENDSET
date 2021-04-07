j.s
chapter 6
* INTERACTIONS CREATE EVENTS ,when user click or tap on link ...
*  ul events:
1. load     Web page has finished loading 
2. unload   Web page is unloading (usually because a new page was requested) 
3. error    Browser encounters a JavaScript error or an asset doesn't exist 
4.resize    Browser window has been resized 
5.scroll   User has scrolled up or down the page

* KEYBOARD EVENTS :
1.keydown
2.keyup
3.keypress

* mouse events:
1.click
2.dbclick
3.mousedown
4.mouseup
5.mousemove
6.mmouseover
7.mouseout

* fired(raised): when event occurred.
* focus event :- focus / focus in 
               - blur / focusout

* form event :nput ,change ,submit ,reset ,cut ,copy, paste ,select .
* event handling : steps to trigger j.s code 
1.Select the element node(s) you want the script to respond to
2.Indicate which event on the selected node(s) will trigger the response. 
3.State the code you want to run when the event occurs

* types of event handlers:
1.HTML EVENT HANDLERS 
2.TRADITIONAL DOM EVENT HANDLERS.
 element.oneeven=functionName;
 like:
 ```
 function checkUsername() { 
 code;
 }
 var el = document.getElementByld('username') ; 
 el . onblur = checkUsername; 
 ```
3.DOM LEVEL 2 EVENT LISTENERS 
. it can deal with one more function at atime.
. not supported in older browsers.
```element.addEventListener('event',function name ,[ boolean]);```


html
chapter 7
There are several types of form controls that you can use to collect information from visitors to your site.
1. adding text.( text input ,password input ,text area).
2. making choises:( radio buttons ,checkboxes ,drop-down boxes)
3. submitting forms(submit buttons ,Image buttons )
4. uploading files(file uplad).

* form structure:
```
<form action="http://www.example.com/subscribe.php" 
method="get">
<p>This is where the form controls will appear.
 </p>
</form>
```
atribute:
. action to url
. method :get or post.
. id 
. for text input```<input type="text" name="username" size="width of the text" maxlength="for limit of caracters">```
example:

```<form action="http://www.example.com/login.php">
<p>Username:
 <input type="text" name="username" size="15" 
 maxlength="30" />
</p>
<p>Password:
 <input type="password" name="password" size="15" 
 maxlength="30" />
</p>
</form>```

. radio button example

```<form action="http://www.example.com/profile.php">
<p>Please select your favorite genre:
 <br />
 <input type="radio" name="genre" value="rock" 
 checked="checked" /> Rock
 <input type="radio" name="genre" value="pop" /> 
 Pop
 <input type="radio" name="genre" value="jazz" /> 
 Jazz
</p>
</form>```

. for checkbox example:

```<input type="checkbox" name="service" 
 value="itunes" checked="checked" /> iTunes
 <input type="checkbox" name="service" 
 value="lastfm" /> Last.fm
 <input type="checkbox" name="service" 
 value="spotify" />``` 

. image button 
```
<input type="image" src="images/subscribe.jpg" 
 width="100" height="20" />
```

chapter 14
* list-style-type to control the shape of style.
* for unorder list : none ,disc circle ,square
* for ordrer list :- decimal  1 2 3
                   - lower-alpha  a b c
                   - upper-alpha  A B C
                   - lower-roman i. ii. iii.
                   -upper-roman  I II III

* list-style-image we can use list-style-image:``` url("images/star.png");``` to show like stars.
* for table :
 border-spacing;
 border-collapse:colapse or separate;


































