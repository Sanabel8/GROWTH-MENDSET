Java OO Tutorial (only the Object and Class ones)
Object-Oriented Programming Concepts
 objects, classes, inheritance, interfaces, and packages.
 objects: An object is a software bundle of related state and behavior.like car ,person ..
 class : A class is a blueprint or prototype from which objects are created. 
 Inheritance :Inheritance provides a powerful and natural mechanism for organizing and structuring your software.
 classes inherit state and behavior from their superclasses
 interfaces :An interface is a contract between a class and the outside world
 packages:A package is a namespace for organizing classes and interfaces in a logical manner.

Java Classes (do NOT do the Nested Classes section)
examole
```
public class Bicycle {
    public int cadence;
    public int gear;
    public int speed;        
    public Bicycle(int startCadence, int startSpeed, int startGear) {
        gear = startGear;
        cadence = startCadence;
        speed = startSpeed;
    }
    public void setCadence(int newValue) {
        cadence = newValue;
    }        
    public void setGear(int newValue) {
        gear = newValue;
    }        
    public void applyBrake(int decrement) {
        speed -= decrement;
    }        
    public void speedUp(int increment) {
        speed += increment;
    }        
}
```
Binary, Decimal and Hexadecimal Numbers
Decimals
* Every digit in a decimal number has a "position" ,is also called "Base 10" 
* the decimal point helps us to know which position is which:like:  17.591 (tens1 ,ones7 . tenths5 ,thundredths9,thousandths1)
* Every position further to the left is 10 times bigger, and every position further to the right is 10 times smaller
 
Bases
* The Decimal Number System  based on the number 10,with these 10 symbols:0, 1, 2, 3, 4, 5, 6, 7, 8 and 9

Counting with Different Number Systems
* Count up until just before the "Base Number", then start at 0 again, but first you add 1 to the number on your left.

Binary Numbers(0,1)
*  are just "Base 2" instead of "Base 10". 
* So you start counting at 0 then 1 ,then you run out of digits , so you start back at 0 again, but increase the number on the left by 1.
* there is no "2" in binary, so start back at 0 
* 1101.101 (eights , fours ,twos . halves1/2 ,1/4 ,1/8) 
This is 1×8 + 1×4 + 0×2 + 1 + 1×(1/2) + 0×(1/4) + 1×(1/8)
= 13.625 in Decimal

Hexadecimal Numbers
* They look the same as the decimal numbers up to 9
* but then there are the letters ("A',"B","C","D","E","F") in place of the decimal numbers 10 to 15.
* Start back at 0 again, but add 1 on the left










