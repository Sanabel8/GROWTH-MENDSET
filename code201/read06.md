```
JS
chapter5
DOM(document object model):is determine how acssess and update contents of web page in the browser window ,and how create model from html page.
* DOM is sperate part from html add JS as set of rules.
* DOM covers :1. MAKING A MODEL OF THE HTM L PAGE
              2. ACCESSING AND CHANGING THE HTML PAGE
* DOM(object model) is made objects .
* DOM (Application Programming Interface (API).)
* DOM it is contain 4 type of nodes:
1. THE DOCUMENT NODE 
2. ELEMENT NODES 
3. ATTRIBUTE NODES
4. ATTRIBUTE NODES

DOM TREE 
pic

To acsses the elements:
1. Locate the node that represents the element you want to work with. 
2. Use its text content, child elements, and attributes.

* to select an individual element node : getElementById()
                                         querySelector()....css selector

* to select multiple elements (nodelists) : - getElementsByClassName('class') 
                                            - getElementsByTagName('tagname')
                                            - querySelectorAll() ... css selector


* travilling between element nodes : - parentNode 
                                     - previousSibl ing / nextSibling 
                                     - firstChild / lastChild 
* we can store the location of the elements in a var is called caching the selection.
var itemOne = getElementById('one'); 

*  getElementByTagName(); always return acollection of nodes(node list).

*  static Nodelist: he NodeList is not updated to reflect the changes made by the script
*  live Nodelist :when your script updates the page, the Nodelist is updated at the same time. 
*  SELECTING AN ELEMENT FROM A NODELIST :1. The item() method 
                                         2. array syntax. 
* we use length to determine the how many items in the nodelist .
* array syntax  method is faster than item() .
* querySelector() returns the first element node that matches the CSS-style selector. 
* querySelectorA11 () returns a Nodelist of all of the matches.
* we can loop through each node in the coloction .
* PREVIOUS & NEXT SIBLING we can use it when there is no whitespace between elements.
 previousSibling 
 nextSiblfng 
* FlRST & LAST CHILD :return inconsistent results if there is whitespace between elements.
 firstChild 
 lastChild 

* ADDING ELEMENTS USING DOM MANIPULATION :1.createElement()
                                          2.createTextNode()
                                          3.appendChild()

chapter 3
* object :a set of variables and functions to create a model of a something you would recognize from the real world
* in object the variables become properties.
* and function called method .
* creating object:literal notation .



understanding the problem domian
# hardest thing about writing code :
. Learning a new technology
. Naming things
. Testing your code
. Debugging
. Fixing bugs
. Making software maintainable

* to clear components :
. Figure out what the major components of the picture are
. Sort the pieces by color or component
. Put together all the border pieces
. Put together each component of the picture from the piles you created
 
* Many of the problem domains we face as programmers are difficult to understand and look completely different depending on your viewpoint.
* reading domain driven design book.
* ADDING ELEMENTS USING DOM MANIPULATION :1.createElement()
                                          2.createTextNode()
                                          3.appendChild()



```