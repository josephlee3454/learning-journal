# list comprehensions 
* is a quick effective way to make a list
* list comprehension always returns a result list 

### what it used to look like 
###### new_list = []
###### for i in old_list:
######   if filter(i):
######     new_list.append(expressions(i))


### what it looks like now
###### new_list = [expression(i) for i in old_loidt if filter()]


### The list comprehension starts with a '[' and ']', to help you remember that the result is going to be a list.

```sqaures = []
    for i in range (1,101)
      sqaures.append(i**2)
    print(sqaures)``



## out put for both: [1,4,9,16,25,36 ...]


sqaures2 = [i**2 for i in range (1,101)]