# CSE15L Lab Report 4

### Step 4: Log into ieng6
```markdown
- **Command Entered:**
  `<up> <enter>`
- **Description:**
  Used the up arrow to access the last command (SSH login command) from the bash history and executed it by pressing enter.
```
<img width="578" alt="Screenshot 2023-12-03 at 5 32 03 PM" src="https://github.com/vssb4214/cse15l-lab-reports/assets/147002913/8f7a359f-8da2-451d-846b-1278e9b81cef">

### Step 5: Clone the Repository
```markdown
- **Command Entered: "git clone git@github.com:vssb4214/lab7.git" **
  `<Command-C> (from notes) <Command-V>` 
- **Description:**
  Cloned the lab7 repository using the SSH URL copied from the notes.
```
<img width="518" alt="Screenshot 2023-12-03 at 5 40 00 PM" src="https://github.com/vssb4214/cse15l-lab-reports/assets/147002913/06bed701-6c83-4f5d-ab73-130a73e6a465">

### Step 6: Run Tests to Verify Failure
```markdown
- **Commands Entered:**
  `ls + <enter>`
  `cd lab7 + <enter>`
  `ls`
  `bash ./test.sh`
- **Description:**
  Listed the contents of the current directory, changed directory to lab7, listed its contents, and ran the provided test script to verify the failing tests.
```
<img width="596" alt="Screenshot 2023-12-03 at 5 41 03 PM" src="https://github.com/vssb4214/cse15l-lab-reports/assets/147002913/4f8bc5e6-0c4d-4b78-86c6-7fb2ca392e05">

### Step 7: Edit the File to Fix the Failing Test
```markdown
- **Commands Entered:**
  `ls`
  `vim ListExamples.java`
  `i`
  `<right> <delete> 2 <esc> :x`
- **Description:**
  Opened `ListExamples.java` with vim, navigated to the line with the bug, made the necessary correction from `index1` to `index2`, saved, and exited the editor.
```
<img width="519" alt="Screenshot 2023-12-03 at 5 42 00 PM" src="https://github.com/vssb4214/cse15l-lab-reports/assets/147002913/7a45da0e-da4d-4434-a992-dd28c4d573ef">
<img width="617" alt="Screenshot 2023-12-03 at 5 42 52 PM" src="https://github.com/vssb4214/cse15l-lab-reports/assets/147002913/c1ddc5c6-e086-48f6-b07c-ef65f912f809">

### Step 8: Run Tests to Confirm Fix
```markdown
- **Command Entered:**
  `bash ./test.sh`
- **Description:**
  Executed the test script again to confirm that the previously failing test now passes.
```
<img width="344" alt="Screenshot 2023-12-03 at 5 43 12 PM" src="https://github.com/vssb4214/cse15l-lab-reports/assets/147002913/d68b3760-2207-4e70-a50b-022ab01796a6">

### Step 9: Commit and Push Changes to GitHub
```markdown
- **Commands Entered:**
  `git add ListExamples.java + <enter>`
  `git commit -m "Fixed" + <enter>`
  `git push origin main + <enter>`
- **Description:**
  Made the changes made to `ListExamples.java`, committed these changes with a message, and pushed the commit to the `main` branch of the GitHub repository.
```
<img width="713" alt="Screenshot 2023-12-03 at 5 44 33 PM" src="https://github.com/vssb4214/cse15l-lab-reports/assets/147002913/a9c22cf8-20ae-4026-990d-079211739933">

