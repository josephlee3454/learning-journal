# what is a stack?
* a stack is a data structure that consists of Nodes. but in a stack it only holds reference to the next node

# terminology 
* Push : nodes and items that put in the stack are pushed 
* Pop : nodes and items that are removed are considered pop
* Top : this is the top of the stack.
* Peek : when you peek you will veiw the value of the top Node in the stack. But if you attempt to peek an empty stackj an exception will be raised 
* IsEmpty : returns true when stack is empty otherwise returns false 

# First In Last Out (FILO)
* This means that the first item that is added to yoiur stack will be the last item popped out of the stack 

# Last In First Out (LIFO)
* basically like FILO except instead of being the last item popped off the stack it will be the first item popped out of the stack

# Push O(1)
* pushing a node onto a stack will always be an O(1) operation this is because it takes the same amount of time no matter how any Nodes(n) you have in the stack. 
* When you add something to the stack you push it by assign it as the new top whit the next property eqaul to the the original top. 

# Pop O(1)
* when popping off a stack is the action of removing a Node from the top. When Popping the top Node will be reassigned to the Node that lives below and the top Node is returned to the user
* one side note that might seem obvious but typiucally you will check isEmpty before performing a pop to avoid rasing an exception 

# Peek O(1)
* when performing a peek you will only be inspecting the top node of the stack
* also check isEmpty

# Queue 
* Enqueue : Nodes or items that are added to the queue
* Dequeue : Nodes or items that are removed from the queue. if called when queue is empty an exception will be raised 
* front : this is the front/ first Node of the queue  
* Rear : This is the rear/last Node of thequeue 
* peek : when you peek you will view the value of the front Node in the queue. if called when the queue id empty an exception will be raised 
* isEmpty : returns true when queue is empty otherwise returns false

# FIFO  queue
* this means that the first item in the queue will be the first item out of the queue 
# LILO (Last In Last Out)
* this means that the last item in the queue will be the last item out of the queue 
# enqueue O(1)
* when you add a item to a queue you use the enqueue action. 
# Dequeue o(1)
* when you remove an item from a queue you use the dequeue action. check isEmpty to avoid an exception being raised 
# Peek O(1)
* when using the peek you will only be inspecting the front node of the queue 

