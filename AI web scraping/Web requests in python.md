## using urllib library 
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
this behaves like a dictionary as you can see all the headers info is contained inside a dictionary.


### we will be using another lightweight lib with great features next , but the process is effectively the same 
###### the first step in scraping always involves a request going out and info in the form of HTML coming in.

## works as a dictionary and is non case sensitive
###### collection of key value pairs that provides info on headers.

![[Pasted image 20250219020508.png]]

#### so when requesting we can also set the request headers (as we have already learned) , these headers makes the server believe that request is coming from a browser or sm.

so the thing is many servers block out the requests of bots and scripts and browser gives alot of info to servers to make it know that it is a true client asking for a response and the most imp one is 

###### User-agent : Mozzila/5.0  (any browser)
![[Pasted image 20250219021108.png]]

now adding this on the quotes scrape site doesnt make any difference as that site doenst care about user agent (its a practice site for scraping so yeah).

## from httpbin site the list of headers a browser (mozilla in this case) sents to the server.

![[Pasted image 20250219021220.png]]

#### so basically here he did a response and then got one (of the above url of httpbin) , the requests header can be seen in json format (new attribute)
and throught .request.headers we can see the dictionary of headers that is sent by request library while approaching a server

hmmm interesting 
no. of headers are half of what the browser sends to a server (seen in above image).

![[Pasted image 20250219021504.png]]

# query parameter 
![[Pasted image 20250219215134.png]]

###### links having these "?" sign and everything after it is query paramtere.
the "&" signs comes in it aswell
the parameters in the above link are

1. author 
2. title
3. price 
these parameters are used in request making to add more info or to add filters to get what we really need 
we can get the parameter response by using the dictionary key thingy.

![[Pasted image 20250219215611.png]]

as in this url there are the comparison of prices of currencies with bitcoin.

![[Pasted image 20250219215707.png]]

![[Pasted image 20250219215730.png]]

as everything is inside the data key we can use it then to find what we need in terms of parameters by simply adding them in [' square brackets like this '].
![[Pasted image 20250219215907.png]]

#### so this is only one parameter so doing it this way is working
even in the link there is only one query parameter but the general and more effective way out of this is 

###### making the url of the base type (contains no query).
![[Pasted image 20250219220105.png]]

#### this has advantage as you can handle many parameters and encoding is done by library so yes (didn't get this one make sure to comeback here)

## interesting 
so then we use a different site or api the sunset sunrise where we have give out more than one parameters.
![[Pasted image 20250219220726.png]]

![[Pasted image 20250219220930.png]]

### the request wasnt successful.
and the problem was basically the request headers here the api discriminated us because we are using a script and it concluded that we are a bot.

##### then we see the url that was request through this and paste it in browser to see that it is indeed working on the browser
![[Pasted image 20250219221126.png]]

![[Pasted image 20250219221234.png]]

##### we get the request headers through the browser and see the user agent type
![[Pasted image 20250219221353.png]]

![[Pasted image 20250219221441.png]]

we create a headers dictionary and give that to the r which was imported as requests lib
![[Pasted image 20250219221540.png]]

##### and it worked , we tricked the api to think that we are true user client.

# authentication  and authorization 
**Authentication** and **Authorization** are two critical concepts in API security. They ensure that only legitimate users or systems can access an API

so basically we have to authenticate with the server before making any request of sorts.

![[Pasted image 20250219221903.png]]

ways through which we can authenticate with a server
**API Keys:**

- A unique string (key) is assigned to each client. This key is identified by the server.
    
- The client includes this key in the API request

###### the general structure of using an api key is like this 
![[Pasted image 20250219223638.png]]

![[Pasted image 20250219224331.png]]

###### the bearer part is just a convention that is used to indicate that the api key belongs to the bearer or is of bearer token
### another popular authentication scheme - basic auth 
![[Pasted image 20250219224509.png]]

a very simple authentication procedure in which the sever recognizes us through 2 inputs that are  - username and the password
in requests we use auth parameter to use this in the form of a tuple.

# other than GET method (we have been only using this one)
###### requests lib also supports other methods like POST DELETE PWD etc
so you just need to replace the method in the alias of imported lib

`import requests as r`
`r.delete(url)`

# POSTing data 



