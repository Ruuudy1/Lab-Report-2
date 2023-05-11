# Part 1:
## Web server called StringServer that supports the path and behavior described below:
![image](https://github.com/Ruuudy1/Lab-Report-2/assets/130013367/e2d7a22b-bb30-4c7d-ae83-82642ecce986)
![image](https://github.com/Ruuudy1/Lab-Report-2/assets/130013367/47d38aa8-e850-4e40-a803-554dc513b689)

### Show the code for your StringServer, and two screenshots of using /add-message:
![image](https://github.com/Ruuudy1/Lab-Report-2/assets/130013367/e80efa34-7517-474c-bca1-7120ad8c30fd)

### Which methods in your code are called?:

The method handle() is called to add hello

### What are the relevant arguments to those methods, and the values of any relevant fields of the class?

HttpExchange t = localhost:1128/add-messages?s=helloo :
URI url = add-message?s
message = helloo -returned /n + keyValue[1]
String query = s = helloo
String[] KeyValue = keyValue[0] = s, keyValue[1] = hello,

### How do the values of any relevant fields of the class change from this specific request? If no values got changed, explain why.

the query "s" variable got set to "helloo"
and the keyVslue array index 1 is set to s. and array at index 2 is set to hello.

/add-message?s=How are you
![image](https://github.com/Ruuudy1/Lab-Report-2/assets/130013367/00fa8c34-8b8d-4c03-9621-4908104d3753)
### Which methods in your code are called?
The method handle() is called to add hello

### What are the relevant arguments to those methods, and the values of any relevant fields of the class?

HttpExchange t = localhost:1128/add-messages?s=how are you?
URI url = add-message?s
message = hello -/n how are you? added as well \n + keyValue[1] hello
String query = s = how are you?
String[] KeyValue = keyValue[0] = s, keyValue[1] = how are you?,

### How do the values of any relevant fields of the class change from this specific request? If no values got changed, explain why.

the query "s" variable got set to "how are you?"
and the keyVslue array index 1 is set to s. and array at index 2 is set to how are you?.

# Part 2:

the bug I will be focusing on from lab 3 is in the AverageWithoutLowest2() method.

![AverageWithoutLowest2()](https://github.com/Ruuudy1/Lab-Report-2/assets/130013367/669306a6-05e2-45a0-afdb-5ace57587673)

This one was tricky to figure out at first. yet when looking at the code for the method: 

![image](https://github.com/Ruuudy1/Lab-Report-2/assets/130013367/12a6d66e-44f0-43d6-b8f9-11c4dc8ed987)

The symptom we were testing for is an incorrect value, which we got when we tested {-1,-1,-1}. This happened because there is a bug in the second for loop. When there are multiple numbers at the lowest value, NONE of them get added to the sum, when only one of them shouldn’t. Giving us 0 as the output.

To fix this what I did is iterate through the loop and only store the lowest variable once to take into account the I subtracted this number from the sum of my array.

![image](https://github.com/Ruuudy1/Lab-Report-2/assets/130013367/3b383bcb-7c7e-408b-b13a-3757d8c252a9)


# Part 3:

One thing I learned in labs from weeks 2 and 3 is how debug my code more efficiently. I really liked the material we covered in week 3 
most notably the article we learned in which it compared the student's midnset on what is right to the teachers way of a program being right.
I found it really funny but relatable to me as I also call it a day after just running my code a few times an seeing it compile correctly. 
I think this is the most import thing we have learned so far as it has also come in really handy to me in CSE12 as we constantly work with 
junit and I often find myself stuck with bugs.
