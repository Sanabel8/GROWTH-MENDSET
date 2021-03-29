html 
chapter2
3 type of lists:1. order list(ol):each items in the list is numberes.
                2. unorder list(ul):list begin with bullets point .
                3. defintion list(dl) :are made up of a set of terms along with the definitions for each of those terms.(dt/term-dd/defintion).
                4. nested lists.

chapter13
. box dimension: height, width
. to specify the size of abox we use px ,% ,ems .
. limiting width (min-width, max-width) we use it to inture that the content of pages are legible .
 
overflow content
when ehe box contain inside it another box larger than itself will happe one of the two:
1.hidden 
2.scroll to see missing content.

properties for box
. border  :every box have border, px or (thin,medium , thick).
border-style(soild,dotted ,dashed ,groove ,ridge ,inset ,outset ,hidden/non)
border-color
shorthand border :uesd to determine the width ,style and  color in one property.
p {
width: 250px;
border: 3px dotted #0088dd;} 
.  margin :distance between two border boxes,(px or ems)
. pandding: distance between border of the box and what it contain.
. visibiblity: allows to hide bokes from users and it leaves a space .(hidden ,visible0.
. box-shadows :Horizontal offset ,Vertical offset ,Blur distance ,Spread of shadow.
. rounder corner :by usin border-radius: px;


html
chapter3

array used to store list of values are related to each other. *array literal: to create the array var name [1vaue , 2value ,...]; or write like that

colors= ['white', 
         'black', 
         'custom'];

array constructor : var colors =new Array('white ' , 
                                          'black', 
                                          'custom'); to changing the value on array colors[2]='beige';
* to accesses items in array like: var itemthree=color[2];

* to tedarmine number of items (lenght of array) var numColor=color.lenght;
  
* to change value of array like color[2] ='red';


chapter 4

if...else statment 

if (condition){ 
code; 
} else { 
code;
}

* if the condition is true will run the code for if part if not will run the code of else part.

switch statment

switch (value) { 
case 1:
code ; 
break; 
case 2: 
code; 
break; 
case 3: 
code; 
break; 
default : 
code'; 
break; 
}
* first switch have value, if the value matching with one case between {}will run code and after ended will go out the switch statment (break)
if the value doesn't matching any case will run the default code.

* type coercion :j.s convert data types by make scenes to make compleat operation.
PURPOSE of string is Text 
PURPOSE of number is number 
PURPOSE of Boolean is true or false 
PURPOSE of null is Empty value 
PURPOSE of undefined is Variable has been declared but not yet assigned a value

* j.s use week typing because the data type for a value can change.
* falsy values:treated as if they are false.
 var highScore=false;       the traditional boolean false
 var highScore=0;          the number zero
 var highScore='';          nan(not number)
 var highScore=10/'score';   empty value
 var highScore=;             variable with no value assigned to it
* Truthy values are treated as if they are true 
var highScore = true;       The traditional Boolean true 
var highScore = l;           Numbers other than zero 
var highScore = 'carrot ';   Strings with content 
var highScore = 10/5;        Number calculations 
var highScore = 'true';      true written as a string 
var hi ghScor e = ' O' ;      Zero written as a string 
var highScore = ' fal se';    fa1se written as a string

*(false == 0)  true
(false === 0)  false 
(false== ' ') true 
(false === ' ') false 
(0 ==' ') true
(O === ' ') false 
(undefined ==null) true 
(null == false) false 
(undefined == false) false 
(null == 0) false 
(undefined == O) false 
(undefined === null) false 
(Nan == null) false
(NaN == NaN) false

*looping
type of loops
1.for 

for ( initialization; condition; update){

code.....
}
* we also can use -- instead of ++ for 

2.while

while ( i<number) {
code
i++
}

3.do while
