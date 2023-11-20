# Part 1 - Bugs

## Failure-inducing input
  static void reverseInPlace(int[] arr) {
    int hold = arr[0];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
- The two methods that are called when this is executed is the 'main' method from 'StringServer' and 'handleRequest' from 'StringHandler.' 'main' allows it to start with a specific port number while 'handleRequest' gets executed when the server recieves the "add" request.
- 'StringBuilder messages' is initially empty since nothing has been appended, 'int messagesCount' is 0 for the same reason as before, and 'URL url' contains the request: '/add-message?s=Hello' as that is the current request. 
- 'messages' changes from an empty string to "1. Hello\n" and 'messageCount' changes from 0 to 1 because the request has been executed.

## "/add-message?s=How are you"
<img width="634" alt="pic one" src="https://github.com/vssb4214/cse15l-lab-reports/assets/147002913/5b361262-6e4a-42b9-a206-c058593334f9">

- Only one method is called since the server already started. 'handleRequest' from 'StringHandler' is called to deal with the new "add" request. 
- 'StringBuilder messages' now contains "1. Hello\n", 'int messagesCount' is 1, and 'URL url' contains the request: '/add-message?s=How are you'.
- 'messages' changes from "1. Hello\n" to "1. Hello\n2. How are you\n" and 'messageCount' changes from 1 to 2.

# Part 2
## The path to the private key for your SSH key for logging into ieng6
<img width="319" alt="Screenshot 2023-11-05 at 8 23 06 PM" src="https://github.com/vssb4214/cse15l-lab-reports/assets/147002913/eeb83f95-da1f-4cdc-8c21-fe625b70a82d">

## The path to the public key for your SSH key for logging into ieng6
<img width="392" alt="Screenshot 2023-11-05 at 8 27 32 PM" src="https://github.com/vssb4214/cse15l-lab-reports/assets/147002913/a21523b2-b7e7-4c70-bc2d-9344431a6190">

## A terminal interaction where you log into ieng6 with your course-specific account without being asked for a password.
<img width="567" alt="Screenshot 2023-11-05 at 8 29 41 PM" src="https://github.com/vssb4214/cse15l-lab-reports/assets/147002913/229f6b4d-cf3a-47c8-bbad-bfe61836b313">

## Something I learned
- My parents are both in the computer science field, so I've heard the term "ssh" in their work conversations. I finally learned what that meant, and I even learned how to execute it. It's pretty cool how I can just log in to computer across the world with one simple command in my terminal. 



