# classes and objects
* Objects are an encapsulation of variables and functions into a single entity. Objects get their variables and functions from classes. Classes are essentially a template to create your objects. i copied this straight from the article: https://www.learnpython.org/en/Classes_and_Objects because it is the perfect defintion
# recursive functions
## A recursive function is a function defined in terms of itself via self-referential expressions.
* which means that the specified function will continue to call itself and repeat its behavior until some condition is met to return a result
### all recursive functions have a common structure made up by 2 parts such as base & recursive
## maintaining state
### when you are working with recursive functions keep in mind that each recursive call has its own execution context so in order to maintain state during recursion you have to either 
* Thread the state through each recursive call so that the current state is part of the current call’s execution context
* keep the state in global scope 
