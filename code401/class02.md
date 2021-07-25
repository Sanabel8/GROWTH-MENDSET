Java Imports (ignore the parts about NetBeans)
* Package = directory
* Java classes can be grouped together in packages
*  package name =directory (folder) name 
* import  : name the packages you want to use from other libraries
* Package declaration should be in The first statement, other than comments,
* Default package: what java create packages when it's common to omit it .
* Sun recommends that you do not use default packages.


The statement order is as follows.
1. Package statment (optional).
2. Imports (optional).
3. Class or interface definitions.

```package illustration;
import java.awt.*;
public class Drawing {
    . . .
}```

* Comments can go anywhere.

Imports: three options
*  The wildcard character (*) : used to specify that all classes with that package are available to your program 
import javax.swing.*;

* Common imports
* There are 166 packages containing 3279 classes and interfaces in Java 5. 


- import java.awt.*;	         Common GUI elements.
- import java.awt.event.*;	 The most common GUI event listeners.
- import javax.swing.*;	         More common GUI elements. Note "javax".
- import java.util.*;	         Data structures (Collections), time, Scanner, etc classes.
- import java.io.*;	         Input-output classes.
- import java.text.*;	         Some formatting classes.
- import java.util.regex.*;	 Regular expression classes.

import FAQ
* import only tells the compiler where to look for symbols.

NetBeans will create your imports
 Just right click on the source file and choose Fix Imports. It will add all necessary import statements.



Different types of loops in Java

looping is a feature which facilitates the execution of a set of instructions until the controlling Boolean-expression evaluates to false.
types of loops :
1. Simple for loop
2. Enhanced for-each loop
3. While loop
4. Do-While loop

for Loop
A for loop is a control structure that allows us to repeat certain operations by incrementing and evaluating a loop counter.

While Loop
It repeats a statement or a block of statements while its controlling Boolean-expression is true.

Do-While Loop
 the first condition evaluation happens after the first iteration of the loop.
