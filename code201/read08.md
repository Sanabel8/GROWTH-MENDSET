
html
chapter4
* links allows us to move from one page to another.
* writing links``` <a href=" the linke">text of link</a>```
* absolute url when the link move me to different website .
* relative url when i linking to another pages within the same site.
* Web servers are usually set up to return the index.html file .
* The main homepage of a site written in HTML
* when we write the link should folow apath that where it place like :
- in the same folder``` <a href="reviews.html">Reviews</a>```
- another we will follow the path of the folder.like```<a href="movies/dvd/reviews.html">Reviews</a>```
* email links``` <a href="mailto:jon@example.org">Email Jon</a>```
* Opening Links in a New WindoW using targt atrribute``` <a href="http://www.imdb.com" target="_blank">```


chapter 15
Key Concepts in Positioning Elements
- Building Blocks :is the main blicks of any layout ,it start on a new line ,like``` <h1> <p> <ul> <li>```
-  To separate boxes, you can use borders, margins, padding, and background colors. 
- Inline elements flow in between surrounding text Examples include:``` <img> <b> <i>.```
- when we have box inside box the the outer box is known as the containing or parent element using div tag.
- Relative Positioning: moves an element from the position it would be in normal flow shifting it to the top, right, bottom, or left of where it would have been placed. 
- Absolute positioning: elements move as users scroll up and down the page.
- Floating Elements: take that element to the far left or right of a containing box
- z-index: to control which element sits on top, and how have higher value will apper in the top.
- float :to move the element to left or right .
- clear: allows you to say that no element should touch the left or righthand sides of a box
- screen resolution : the number of dots a screen shows per inch
- Liquid Layouts : designs stretch and contract as the user increases or decreases the size of their browser window. 
-  960 pixel grid set consistent proportions and spaces between items
* for using it in my code should inter linke in the head ```<link rel="stylesheet" type="text/css"href="css/960_12_col.css" />```
* then use the class name :
container_12 clearfix to ensure that browsers know the height of the containing box 
* grid_number of columns wide.
- multiple style sheets:
```
 <link rel="stylesheet" type="text/css" href="css/site.css" />
 <link rel="stylesheet" type="text/css" <link rel="stylesheet" type="text/css" href="css/tables.css" />
 <link rel="stylesheet" type="text/css"href="css/typography.css" /> href="css/site.css" />
```

j.s chapter3
function : series of statements together to perform a specific task and it use to store steps needed to achieve a task.
* structure of function 
```
function name(parameters) { 
code ; 
 //parameters used like variables within the funcion.
} ;
name(arguments);

*** var name = function(parameters) {
code to run; 
} ; 
var name2= name(3, 4) ; 
```

* return :is used to return avalue to the function.

* the variable's scope(local) : If you declare it within a function, it can only be used within that function

* global scope: if you create a variable outside of a function, then it can be used anywhere within the script

artical

six reason for pair programming:
1.Greater efficiency
2.Engaged collaboration
3.Learning from fellow students
4.Social skills
5.Job interview readiness
6.Work environment readiness




