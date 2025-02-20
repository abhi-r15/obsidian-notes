#### beautiful soup is a library of python that is used to pull out data from html and xml content
so we got the requests lib and got content in the form of html a messy string that is often in bytecode which we have to parse out in utf-8 unicode
BS4 or beautiful soup 4 solves this problem by easily traversing the html doc and extract the data we need specifically.

![[Pasted image 20250220131830.png]]

## importing beautifulsoup constructor
![[Pasted image 20250220132610.png]]
![[Pasted image 20250220132634.png]]

##### so BS4 is the library through which we are getting one class here beautifulsoup
![[Pasted image 20250220134537.png]]

### we use the html parser for the second argument in soup 
![[Pasted image 20250220134611.png]]
and then we can use the many attributes that beautiful soup provides to easily parse and fetch the html data
![[Pasted image 20250220134652.png]]

# tags
tags are the most common attributes that are parsed through the soup functions. 
tags - the html element tags that we already know about.
