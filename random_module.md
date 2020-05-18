# Random module 
* allows you to generate random numbers
## some useful functions 
### **Randint** 
* accepts 2 parameters a lowest and a highest number 
* generates integers between numx between numy (1st val lower than the second)
#### example:
## import random 
## print random.randint(0,5)
#### output will either be 1,2,3,4 or 5 
### **random**
* if you want a larger number you can also multiply it for example if you want nums 0 - 100
#### example:
## import random
## random.random() * 100
### **Choice** 
* The choice function can often be used for choosing a random element from a list.
#### example:
### import random
### myList = [2, 109, False, 10, "Lorem", 482, "Ipsum"]
### random.choice(myList)
### **shuffle** 
* The shuffle function, shuffles the elements in list in place, so they are in a random order.
### from random import shuffle
### x = [[i] for i in range(10)]
### shuffle(x)