# CSE15L Lab Report 4

## Task: Improving Efficiency with Vim and Command Line Operations

### Step 4: Log into ieng6
```markdown
- **Command Entered:**
  `<up> <enter>`
- **Description:**
  Used the up arrow to access the last command (SSH login command) from the bash history and executed it by pressing enter.
```

### Step 5: Clone the Repository
```markdown
- **Command Entered:**
  `<Command-C> (from notes) <Command-V>` 
- **Description:**
  Cloned the lab7 repository using the SSH URL copied from the notes.
```

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
### Step 7: Edit the File to Fix the Failing Test
```markdown
- **Commands Entered:**
  `ls`
  `vim ListExamples.java`
  `<right> <delete> 2 <esc> :x`
- **Description:**
  Opened `ListExamples.java` with vim, navigated to the line with the bug, made the necessary correction from `index1` to `index2`, saved, and exited the editor.
```

### Step 8: Run Tests to Confirm Fix
```markdown
- **Command Entered:**
  `bash ./test.sh`
- **Description:**
  Executed the test script again to confirm that the previously failing test now passes.
```


### Step 9: Commit and Push Changes to GitHub
```markdown
- **Commands Entered:**
  `git add ListExamples.java + <enter>`
  `git commit -m "Fixed" + <enter>`
  `git push origin main + <enter>`
- **Description:**
  Staged the changes made to `ListExamples.java`, committed these changes with a descriptive message, and pushed the commit to the `main` branch of the GitHub repository.

