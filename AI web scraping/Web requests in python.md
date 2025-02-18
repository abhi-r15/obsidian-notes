## done through using urllib library 
###### it is the part of standard library and ships with python itself
this library of python gives us a large number of modules , we'll use urllib request module for now.
### **1. Module**

A **module** is a single Python file (`.py`) that contains **functions, classes, and variables** that can be used in other programs.

### **2. Library**

A **library** is a **collection of modules** that provide specific functionality. A library can contain **multiple modules** and even dependencies.  
✅ **Example of a library:**

- **NumPy** (has multiple modules for array operations, linear algebra, etc.)
- **Pandas** (contains modules for data handling)
- **Requests** (modules for making HTTP requests)

#### request module of urllib (below example is from datalore site)
![[Pasted image 20250216154206.png]]

then took a site example from where to scrape quotes for practice
![[Pasted image 20250216154337.png]]

![[Pasted image 20250216154405.png]]

###### used the read function/method to get the response , notice b' at the start which means it is in bytecode format to change it to unicode(which we read) we do
![[Pasted image 20250216154529.png]]

###### it is in one line so for indentation we print it
![[Pasted image 20250216154617.png]] 

### we did alot of steps tho , a more direct way is using urlopen function as a context manager(?)

#### context manager - 
### **Context Manager in Python**

A **context manager** in Python is a construct that allows you to manage resources efficiently using the `with` statement. It ensures that resources (like files, database connections, network sockets) are properly **acquired and released**.

---

## **Why Use a Context Manager?**

- **Automatic Cleanup** → Ensures resources are properly closed.
- **Exception Safety** → Handles errors gracefully.
- **Cleaner Code** → No need for explicit `try-finally` blocks.

![[Pasted image 20250216154926.png]]

## cohesive manner

![[Pasted image 20250216162900.png]]

### using urllib in most of the cases is not suitable or convenient, module offers an api that is too low level.

# request lib : http for humans

#### not an inbuilt lib that is included in python natively so you need to install the lib.
`pip install requests`

###### now doing the same thing we did in the above example through importing requests library we get some additional useful methods.
![[Pasted image 20250216164309.png]]

![[Pasted image 20250216164452.png]]

###### same as the previous one (urllib) can also be done in a concise manner through context manager "with" command.

![[Pasted image 20250216164607.png]]

using text attribute we can straight get the string without the need of decoding to utf-8.
![[Pasted image 20250216164716.png]]

we can get the response headers through the headers attribute.

