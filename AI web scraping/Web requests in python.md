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

#### request module of urllib
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

