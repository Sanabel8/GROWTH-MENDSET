Java Primitives versus Objects

* primitive type such as int, boolean and it live in the stack
* reference types such as Integer, Boolean

to decleared the two type 
1. int i =5;
2. Integer j = 1; or Integer j = new Integer(1);

* autoboxing : The process of converting a primitive type to a reference one .
* unboxing  : The process of converting a reference type to primitive  a one

* to choose object should based on : 
1. what application performance we try to achieve
2. how much available memory we have
3. the amount of available memory
4. what default values we should handle.

* the size of memory take the  primitive type variables 
boolean – 1 bit
byte – 8 bits
short, char – 16 bits
int, float – 32 bits
long, double – 64 bits

* The reference types are objects, they live on the heap and are relatively slow to access
* the size for reference type :
Boolean – 128 bits
Byte – 128 bits
Short, Character – 128 bits
Integer, Float – 128 bits
Long, Double – 192 bits

* The performance of a Java code it depends on :
1. the hardware on which the code runs. 
2. on the compiler that might perform certain optimizations. 
3. on the state of the virtual machine. 
4. on the activity of other processes in the operating system.

usage 
* the primitive types are much faster and require much less memory


Exceptions in Java (read the first three sections on the left: What is an Exception, The Catch or Specify Requirement, Catching and Handling Exceptions)
What Is an Exception?
An exception is an event that occurs during the execution of a program that disrupts the normal flow of instructions
 shorthand for the phrase "exceptional event."


Using Scanner to read in a file in Java
* Objects of type Scanner are useful for breaking down formatted input into tokens and translating individual tokens according to their data type.
```
public class ScanXan {
    public static void main(String[] args) throws IOException {

        Scanner s = null;

        try {
            s = new Scanner(new BufferedReader(new FileReader("xanadu.txt")));

            while (s.hasNext()) {
                System.out.println(s.next());
            }
        } finally {
            if (s != null) {
                s.close();
            }
        }
    }
}
```

* To use a different token separator, invoke useDelimiter()
* to separator by the  a comma s.useDelimiter(",\\s*");
* Scanner also supports tokens for all of the Java language's primitive types (except for char)

























