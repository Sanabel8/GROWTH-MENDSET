SOLID principles intro
SOLID stands for:
. S - Single-responsiblity Principle
. O - Open-closed Principle
. L - Liskov Substitution Principle
. I - Interface Segregation Principle
. D - Dependency Inversion Principle

* Single-Responsibility Principle :A class should have one and only one reason to change, meaning that a class should have only one job.
* Open-Closed Principle :Objects or entities should be open for extension but closed for modification.
- Coding to an interface is an integral part of SOLID.
* Liskov Substitution Principle: Let q(x) be a property provable about objects of x of type T. Then q(y) should be provable for objects y of type S where S is a subtype of T.
- This means that every subclass or derived class should be substitutable for their base or parent class.
* Interface Segregation Principle :A client should never be forced to implement an interface that it doesn’t use, or clients shouldn’t be forced to depend on methods they do not use.
* Dependency Inversion Principle : Entities must depend on abstractions, not on concretions. It states that the high-level module must not depend on the low-level module, but they should depend on abstractions.
- This principle allows for decoupling.
example for connects to a MySQL database:
```class MySQLConnection
{
    public function connect()
    {
        // handle the database connection
        return 'Database connection';
    }
}

class PasswordReminder
{
    private $dbConnection;

    public function __construct(MySQLConnection $dbConnection)
    {
        $this->dbConnection = $dbConnection;
    }
}
```
OO SOLID principles in real life
solid: a mnemonic acronym for five principles of object oriented programming or, as i hinted, really just programming in general 
* the benefite from following solid : code that's a lot more likely to be 1. maintainable. 2. these design guidelines,3.  properly followed, 4. will tend to steer you toward writing clean code.
## s is for single responsibility principle
* the single responsibility principle (srp) : asserts that a class or module should do one thing only.
*  the class or module should have only one reason to change.
* if we have class opnes coonections to DB it multiple reasons to change: 
1. adoption of a new database 
2. modified file output format
3. deciding to use an orm, etc.
* so in terms of the srp, we'd say that this class is doing too much.
*  ducks are fun, but they're also a great example of the pitfalls that the srp can help you avoid.

## o is for open/closed principle
* open/closed principle :  code entities should be open for extension, but closed for modification.
* for instance, inheriting from it and overriding or extending certain behaviors
* an example : a switch statement somewhere that you needed to go in and add to every time you wanted to add a menu option to your application.
* the mechanism that allows you to do this is purely one of extension
* pple, google, and microsoft make the core phone functionality closed for modification and they open it to an extension .

## l is for liskov substitution principle
* the liskov substitution principle (lsp): is most unique to object-oriented programming
* lsp :basically, that any child type of a parent type should be able to stand in for that parent without things blowing up.
* for example :if you have a class, animal, with a makenoise() method, then any subclass of animal should reasonably implement makenoise()

## i is for interface segregation principle
* the interface segregation principle (isp) :you should favor many, smaller, client-specific interfaces over one larger, more monolithic interface.

## d is for dependency inversion
* the dependency inversion principle (dip): to write code that depends upon abstractions rather than upon concrete details.
* this gives the code in question a lot more flexibility -- you can swap in anything that conforms to the stream abstraction and it will still work.










