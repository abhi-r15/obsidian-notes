The **Mersenne Twister** is a pseudorandom number generator (PRNG) algorithm used to produce sequences of numbers that approximate true randomness. It is the default random number generator in Python's `random` module.

### **Modules**

- A **module** is a single file containing Python code (e.g., functions, classes, or variables) that can be imported and used in other Python programs.
    
- Modules are used to organize code into reusable components.
    
- Example: `math.py` is a module that provides mathematical functions.
		modules can be made inside a program for it to be handled by different people to reduce complexity 
		eg. in making of a car , chassy module , tyer module etc 

### making modules 
###### create a new file inside the project (or anywhere) and then you can import it as 
		 import my_module

inside the project
![[Pasted image 20250304192734.png]]

![[Pasted image 20250304192747.png]]
![[Pasted image 20250304192801.png]]

if the module is not in the same directory you can use *sys path append*
### **Libraries**

- A **library** is a collection of related modules or packages that provide a specific set of functionality.
    
- Libraries are typically larger in scope and may include multiple modules or sub-packages.
    
- Example: The `math` module is part of Python's **standard library**, which is a collection of modules that come pre-installed with Python.

![[Pasted image 20250304190830.png]]

##### import random

`random.randint(a,b)`

![[Pasted image 20250304191000.png]]

`random.random()`

Each call to `random.random()` returns a new random number in the range `[0.0, 1.0)`
		 0.0 <= X < 1.0 

![[Pasted image 20250304193749.png]]

![[Pasted image 20250304193801.png]]

for float number there is a function - 

`random.uniform(a,b)`
###### here both a and b are inclusive.

# Lists

###### a **list** is a built-in data structure used to store an ordered collection of items

LIST = [ITEM 1 , ITEM 2,..........]

![[Pasted image 20250304194515.png]]

![[Pasted image 20250304194530.png]]

extend function - *adds a list to the end of a list* --- append only adds one item at the end

![[Pasted image 20250304202927.png]]

##### getting a random item from the list like this
![[Pasted image 20250307225711.png]]

it can also be done through a built in function of random module 

			random.choice(sequence)

*the sequence can be any sequence and list is on of them*

![[Pasted image 20250307230252.png]]

![[Pasted image 20250307230304.png]]

this can also be achieved when the list have variable names - list1 = [ list 2, list 3 ]
and the *list 2 and list 3* contain items inside them

### **double indexing clarification

the double indexing for nested lists can be interpreted through the following code below.
![[Pasted image 20250307231006.png]]
###### here the output is 
![[Pasted image 20250307231025.png]]

thus the 2 lists inside is for the first index 0 and 1 
and then the next index is for the item inside that particular list

## for ascii arts and different stuff to print use
![[Pasted image 20250307231812.png]]


