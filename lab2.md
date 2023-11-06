# "/add-message?s=Hello"
<img width="454" alt="pic 2" src="https://github.com/vssb4214/cse15l-lab-reports/assets/147002913/e7496a78-4c3a-4ded-a1b8-20086f82d85c">

- The two methods that are called when this is executed is the 'main' method from 'StringServer' and 'handleRequest' from 'StringHandler.' 'main' allows it to start with a specific port number while 'handleRequest' gets executed when the server recieves the "add" request.
- 'StringBuilder messages' is initially empty, 'int messagesCount' is 0, and 'URL url' contains the request: '/add-message?s=Hello'
- 'messages' changes from an empty string to "1. Hello\n" and 'messageCount' changes from 0 to 1

# "/add-message?s=How are you"
<img width="634" alt="pic one" src="https://github.com/vssb4214/cse15l-lab-reports/assets/147002913/5b361262-6e4a-42b9-a206-c058593334f9">

- Only one method is called since the server already started. 'handleRequest' from 'StringHandler' is called to deal with the new "add" request. 
- 'StringBuilder messages' now contains "1. Hello\n", 'int messagesCount' is 1, and 'URL url' contains the request: '/add-message?s=How are you'
- 'messages' changes from "1. Hello\n" to "1. Hello\n2. How are you\n" and 'messageCount' changes from 1 to 2  
