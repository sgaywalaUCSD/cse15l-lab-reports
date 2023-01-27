# CSE15L Lab Report 2
***
## Part 1
Code for String Server:

![image](https://user-images.githubusercontent.com/122569404/215223764-2649a682-93a1-481f-9e28-ed7b936c2ebc.png)

Screenshot adding 1st Message:

![image](https://user-images.githubusercontent.com/122569404/215223891-c3e038ac-94a1-49e0-8490-9ec83646296e.png)

* The methods in the code called are: the main method, parseInt method to get the port from args, Server's start method, StringServer's handleRequest Method, and URI's getPath method.
* relevant arguments to those methods values of relevant fields: The argument for the port is 3221 (randomely chosen), the path is "/add-message", and the query is "?s=Testing Message 1". 
* how values of relevant fields change: The value of the message field changes from the empty String to "Testing Message 1\n". 

Screenshot adding another Message:

![image](https://user-images.githubusercontent.com/122569404/215223995-6844f2a4-a07a-4413-beb1-734c4428ac57.png)

* The methods in the code called are: the main method, parseInt method to get the port from args, Server's start method, StringServer's handleRequest Method, URI's getPath method, etc.
* relevant arguments to those methods values of relevant fields: The argument for the port is 3221 (randomely chosen), the path is "/add-message", and the query is "?s=Testing adding another message". 
* how values of relevant fields change: The value of the message field changes from "Testing Message 1\n" to "Testing Message 1\nTesting adding another message\n". 

## Part 2


## Part 3
Something from this lab I learned was, ironically, not so much about bugs and testing. I learned more about how array references work, especially when it comes to references being passed to methods. For example, this code (though it appears like it may work), does not actually reverse the Array in place because of how Array References work:

![image](https://user-images.githubusercontent.com/122569404/215225184-f938dbbc-b283-48ff-8d04-424362e87a50.png)

Instead, a for loop has to be used to change each element of the original array for the code to work, like this:

![image](https://user-images.githubusercontent.com/122569404/215225234-fa38b52b-8f46-4435-aba2-6e8f5a3dca40.png)

Ultimately, I learned more about how pass by reference works in java.
