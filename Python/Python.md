####  *theres a different notes section for web scraping with python , these notes will only include stuff that is about python in general.
### some very very basic stuff if 

### data types
yada yada blah blah

#### 1. **concatenation done in the same way as js
`print("123" + "456")`
`123456`

*note - it will be added and the output will be 576 if double quotes aren't used
there is also another way which is by using 
* formatted string literals - f-strings
`print(f"My favorite fruit is {favorite_fruit}")`
(`print("my favorite fruit is" + favorite_fruit)`
![[Pasted image 20250226015830.png]]

![[Pasted image 20250226015857.png]]
![[Pasted image 20250226015917.png]]
###### writing `print(123_234_345)` will get you the output `123234345`
**underscores are neglected by the interpreter 
##### 2.  subscripting
![[Pasted image 20250225004155.png]]

getting the index and printing out the value , in this case its "u" , we can also get the index vales as negative integers starting from -1 ---> *this indicates the last value ("h" in this case)*
#### 3. **typecasting

done through using functions that can typecast different data type to other type
as concatenation cant be done of the different data types

![[Pasted image 20250225011701.png]]
*helpful in this scenario 
eg.
`int("23")`

#### 4. **floor division
using // will give out an integer type 
as the normal division changes the data type to float 

	print(6 / 3) --> 2.0
	print(6 // 3) --> 2

#### 5. **power notation(just two asterisk)**
power notation no function call or sm just two asterisks 

	 print(2**3) ---> 8

#### 6. **rounding off (the round( ) function)**
![[Pasted image 20250226235441.png]]

printing these values are both quite inconvenient
seeing as using int(num) we get the whole part and without it we get whole lots of decimals

*round( ) ---> this just rounds the number to the possible nearest int value 
30.85422393 --> 31

![[Pasted image 20250226235759.png]]

takes two parameters , one is the number and other is the number of digits it will to round off to.
![[Pasted image 20250226235843.png]]


