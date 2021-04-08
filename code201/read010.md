j.s
chapter10
* ORDER OF EXECUTION: To find the source of an error, it helps to know how scripts are processed. 
* The JavaScript interpreter uses the concept of execution contexts. 
There is one global execution context; plus, each function creates a new new execution context. They correspond to variable scope. 

* EXECUTION CONTEXT:1.GLOBAL CONTEXT
                    2.FUNCTION CONTEXT 
                    3.EVAL CONTEXT (NOT SHOWN)


* Each time a script enters a new execution context, there are two phases of activity: 
1: PREPARE 
2: EXECUTE
* In the interpreter, each execution context has its own va ri ables object.

* ERROR OBJECTS contain appear in the console:
1.name :type of executing
2.message : description
3.file Number :Name of the JavaScript file 
4.lineNumber Line: number of error 

* TYPES OF RERROR:
1.Error 
2.Syntax Error:
. MISMATCHING OR UNCLOSED QUOTES 
 
. MISSING CLOSING BRACKET 

. MISSING COMMA IN ARRAY 

. MALFORMED PROPERTY NAME  

3.ReferenceError 
. VARIABLE IS UNDECLARED 
. NAMED FUNCTION IS UNDEFINED 

4.TypeError
. NCORRECT CASE FOR document OBJECT 

. INCORRECT CASE FOR write() METHOD 

. METHOD DOES NOT EXIST 

. DOM NODE DOES NOT EXIST 

5.RangeError
. CANNOT CREATE ARRAY WITH -1 ITEMS 

.NUMBER OF DIGITS AFTER DECIMAL IN tofixed() CAN ONLY BE 0-20
 
.NUMBER OF DIGITS IN toPrecision() CAN ONLY BE 1-21 

6.URI Error:CHARACTERS ARE NOT ESCAPED
7.EvalError 

* HOW TO DEAL WITH ERRORS :
1.HOW TO DEAL WITH ERRORS 
2. HANDLE ERRORS GRACEFULLY 

WHERE IS THE PROBLEM? 
1. Look at the error message.
2. Check how far the script is running
3. Use breakpoints where things are going wrong. 


The JavaScript console in chrome :
On a PC, press the F12 key or: 
1. Go to the options menu (or three line menu icon) 
2. Select Toots or More tools. 
3. Select JavaScript Console or Developer Tools On a Mac press Alt + Cmd + J. Or: 
4. Go to the View menu. 
5. Select Developer. 
6. Open the JavaScript Console or Developer Tools option and select Console. 

INTERNET EXPLORER 
Press the F12 key or: 
1. Go to the settings menu in the top-right. 
2. Select developer tools.

SAFARI 
Press Alt + Cmd + C or: 
1. Go to the Develop menu. 
2. Select Show Error Console. If the Develop menu is not shown: 
1. Go to the Safari menu. 
2. Select Preferences. 
3. Select Advanced. 
4. Check the box that says "Show Develop menu in menu bar." 

* If you know your code might fail, use try, catch, and finally. 
Each one is given its own code block. 

```try { 
II Try to execute this code 
catch (exception) { 
II If there is an exception, run this code 
}finally { 
II This always gets executed
}
```

DEBUGGING TIPS 
1. ANOTHER BROWSER 
2. ADD NUMBERS 
3. STRIP IT BACK 
4. EXPLAINING THE CODE 
5. CODE PLAYGROUNDSSEARCH
6. VALIDATION TOOLS 




















