### Duckett JS book
#### Chapter 10, Error Handling & Debugging
##### there are two things you can do with the errors:
* 1:DEBUG THE SCRIPT TO FIX ERRORS 
* 2: HANDLE ERRORS GRACEFULLY 
##### Debugging is about deduction: eliminating potential causes of an error.
##### The JavaScript console will tell you when there is a problem with a script,
##### where to look for the problem, and what kind of issue it seems to be. 
##### If you know your code might fail, use try, catch, and finally.
##### Each one is given its own code block. 
##### If you know something might cause a problem for your script, you can
##### generate your own errors before the interpreter creates them. 
##### To create your own error, you use the following line:
```
throw new Error( ' message ') ;
```
##### If you understand execution contexts (which have two
##### stages) and stacks, you are more likely to find the error
##### in your code. 

