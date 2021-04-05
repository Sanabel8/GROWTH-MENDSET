html 
cgapter 6
* table : represents information in a grid format
* each block in the grid is table call.
* the table in html written out row by row.
* table structure 
```
<table>
   <tr>
      <th scope="col"> head of col</th>
      <th scope="col">head of col</th>
      <td> data</td>
      <td> data</td>
      <td>data </td>
   </tr>
   <tr>
      <th scope="row">head of row</th>
      <td>data</td>
      <td>data</td>
      <td>data</td>
   </tr>
   <tr>
      <td colspan="2"> data</td>
      <td rowspan="2">data</td>
      <td>data</td>
      <td>data</td>
      <td>data</td>
   </tr>
</table>
```
* tr is stand to table row.
* td every cell of table ,it is stand to table data
* th table headings it is use to show heading of column or arow.
* we should put ```<th>``` or```<td>```even no data in the cell.
* colspan to determine the space in col or row, in the column.
* rowspan to determine row space in the row.
* ```<thead>``` the heading should but inside it .
* thae body of table should inside the ```<tbody>```
* ```<tfoot>```the footer inside it.

J.S
chapter 3
create object :constructor natation:
blank object:
```
let name =new object ();
name.key=value;
name.key=value;
name.key=value;
name. key=function(){
code;
};```
* to create empty object 
let name ={};
* we can access object using dot notation
* to adding for object name .key =value;
* for delete delete name .key; 
* type of object :1. literal notation like:
```
var hotel = {} 
hotel .name= 'Quay'; 
hotel .rooms = 40; 
hotel.booked = 25; 
hotel.checkAvailabil ity =function() 
return this.rooms - this .booked; 
} ; ```
                   2.OBJECT CONSTRUCTOR NOTATION like: 
```
var hotel = new Object(); 
hotel.name = 'Quay'; 
hotel .rooms = 40; 
hotel . booked= 25; 
hotel.checkAvailability =function() 
return this .rooms - this.booked; 
} ; ```
* arrays are object.
* we can use obj in arry {key:value , key ;value}
* object modle: groub of object ,each project represent thing
* PROPERTY 
document.title 
document.lastModified 
document .URL 
document.domain

*method
document.write() Writes text to document.
document . getElementByld() Returns element 
document. querySe 1ectorA11 () Returns list of elements that match a CSS selector, which is specified as a parameter  
document.createElement() Creates new element 
document.createTextNode() creates new text node


* 
. toUpperCase () Changes string to uppercase characters 
. tolowerCase () Changes string to lowercase characters 
. indexOf() Returns index number of the first time a character or set of characters is found within the string 
. lastindexOf() Returns index number of the last time a character or set of characters is found within the string 

COMMONLY USED TERMS: 
• An integer is a whole number (not a fraction). 
• A real number is a number that can contain a fractional part. 
• A floating point number is a real number that uses decimals to represent a fraction. The term floating point 
refers to the decimal point. 
• Scientific notation is a way of writing numbers that are too big or too small to be conveniently written in 
decimal form. For example: 3,750,000,000 can be represented as 3.75 x109 or 3.75e+12







  