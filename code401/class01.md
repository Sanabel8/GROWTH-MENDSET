JAVA BASICS 

* Variables 
KINKS OF VARIABLES IN JAVA :
1.Instance variables (Non-Static Fields)
2. class variables (Static Fields)
3. local variables  
4.parameters in (public static void main(String[] args)) variable args consider as parameter 

Naming 
. statrt the variables with letter ,$ , _ 
. must not be a keyword or reserved word and should be clear words               
. if the variable have two words we will used the camel case or _ to split between them 
* Operators
|| or 
&& and 
+ - 
<< >> >>> shift 
< > <= >= instanceof
== != equality
& AND
^ OR
= += -= *= /= %= &= ^= |= <<= >>= >>>= assigment 
++expr --expr +expr -expr ~ !


* Expressions, Statements, and Blocks

statment :
1. declaration like :double aValue = 8933.234;
2. A statement forms a complete unit of execution :
 . Assignment expressions
 . Any use of ++ or --
 . Method invocations
 . Object creation expressions
Block more than statement between balanced braces
```class BlockDemo {
     public static void main(String[] args) {
          boolean condition = true;
          if (condition) { // begin block 1
               System.out.println("Condition is true.");
          } // end block one
          else { // begin block 2
               System.out.println("Condition is false.");
          } // end block 2
     }
}
```

* Control Flow Statements executed from top to bottom , break up the flow of execution by employing decision making, looping, and branching,

ELI5: What does it mean to compile code?
WE made the machine language  1's and 0's higher level languages like Java and C# to write code in . these languages alot easier to write and maintain 
 compile code:  (usually another program) takes the program the human wrote, and converts it into the program the computer can understand (machine language )


Reading Java Documentation




