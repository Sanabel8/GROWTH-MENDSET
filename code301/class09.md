FUNCTIONAL PROGRAMMING

What is functional programming?  
is a programming paradigm — a style of building the structure and elements of computer programs — that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data 

What is a pure function and how do we know if something is a pure function?
Pure functions are stable, consistent, and predictable. Given the same parameters, pure functions will always return the same result.
* It returns the same result if given the same arguments (it is also referred as deterministic)
* It does not cause any observable side effects

What are the benefits of a pure function?
The code’s definitely easier to test. We don’t need to mock anything. So we can unit test pure functions with different contexts:
Given a parameter A → expect the function to return value B
Given a parameter C → expect the function to return value D

What is immutability?
unchanging over time or unable to be changed.

What is Referential transparency?
pure functions + immutable data = referential transparency
