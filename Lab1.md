# "cat"
> <img width="209" alt="Screenshot 2023-10-04 at 3 18 21 PM" src="https://github.com/vssb4214/cse15l-lab-reports/assets/147002913/b40a7983-5e18-4a97-b047-24160c327d81">  

When the cat command is used without any arguments, it waits for user input. In this case, the working directory was set to /home/user/documents/. The system is ready to accept input from the user, indicated by the > symbol. This is not an error; the computer is waiting for the user to provide input.
> <img width="510" alt="Screenshot 2023-10-04 at 3 21 40 PM" src="https://github.com/vssb4214/cse15l-lab-reports/assets/147002913/fa9826b4-1e55-4eaf-822a-449c060d862a">


Using the "cat" command with a path to a directory is not valid because "cat" is specifically designed to read the contents of files, not directories. Therefore, attempting to use "cat" with a directory path results in an error. The working directory was /home/user/. The error message indicates that the specified path is a directory and not a file, so the cat command cannot proceed. When the cat command is used with a valid file path, the contents of the file.txt are displayed. 

# "cd" 

> <img width="344" alt="Screenshot 2023-10-04 at 3 33 39 PM" src="https://github.com/vssb4214/cse15l-lab-reports/assets/147002913/22f65f9e-a88e-48e3-8f9b-0c5ad0f51597">

Running "cd" without a specific directory just shows where you are in the computer. It's like checking your current location. If you don't provide a destination, "cd" takes you back to your starting point.

> <img width="583" alt="Screenshot 2023-10-04 at 3 21 01 PM" src="https://github.com/vssb4214/cse15l-lab-reports/assets/147002913/3e341786-ccc8-4fb3-a424-7d3b66da7c36">


Using "cd lecture1" moves you to the "lecture1" directory. This operation doesn’t cause any errors; it simply changes your location within the computer. Attempting "cd" with a file, like "cd file.txt," results in an error. "cd" is meant for navigating directories, not handling individual files. "cd" is designed for folders, not files.

# "ls"
> <img width="197" alt="Screenshot 2023-10-04 at 3 38 14 PM" src="https://github.com/vssb4214/cse15l-lab-reports/assets/147002913/5b7b9f80-64bb-45c3-acc8-df8bd95e8b00">


When you use the "ls" command alone, it displays the files and folders in your current location. This doesn't generate errors; it simply shows the contents of your present working directory. The working directory signifies your exact position in the computer's file system. For example, if you are in /home/user/documents/, running "ls" shows the files/directories within that specific location.

> <img width="533" alt="Screenshot 2023-10-04 at 3 38 07 PM" src="https://github.com/vssb4214/cse15l-lab-reports/assets/147002913/87ae7fb7-096e-4f4a-a18e-fb6d99d142a1">

When you use "ls" with a directory path, like "ls /home/user/documents/", it shows the files inside that specific directory. This command doesn't create errors; it just shows the contents of the selected folder. For example, if you're in /home/user/, running "ls /home/user/documents/" reveals the files in the "documents" folder at your current location. However, running "ls" with a file path, like "ls /home/user/documents/file.txt," results in an error because "ls" works with directories, not files.
