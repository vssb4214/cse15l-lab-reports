### EdStem Post:

#### Title: `ArrayIndexOutOfBoundsException` in `noTriples` Method

**Body:**

Hi, I'm getting an `ArrayIndexOutOfBoundsException` when running my `noTriples` method with certain arrays. It happens with longer arrays, but not with shorter ones. The objective of this method is: "Given an array of ints, we'll say that a triple is a value appearing 3 times in a row in the array. Return true if the array does not contain any triples."

Here's an example where it fails:

![Screenshot 2023-12-02 at 3 24 44 PM](https://github.com/vssb4214/cse15l-lab-reports/assets/147002913/e1dd3e40-5f9f-4967-9164-70bd1d80adb3)

### TA's Response

**Body:**

It looks like you're trying to access an array index that doesn't exist. Can you check the loop condition in your `noTriples` method? Make sure you're not going beyond the array's length. Maybe try adjusting the loop's range and see if that resolves the issue.

### Student's Response

**Body:**

After modifying the loop condition as suggested, here's what I got:

![Screenshot 2023-12-02 at 3 21 34 PM](https://github.com/vssb4214/cse15l-lab-reports/assets/147002913/dbec8570-169b-4343-b942-4deb23eb310c)

![Screenshot 2023-12-02 at 3 22 10 PM](https://github.com/vssb4214/cse15l-lab-reports/assets/147002913/7b45d8da-e8ea-4c78-b2f5-7016de719357)

I changed the loop condition to stop before the last two elements, and it seems to be working now. Thanks you!

## Setup Information

### File involved

- `Main.java` - contains the main Java code and `noTriples` method
- `run.sh` - bash script to compile and run the Java program

### Contents of Each File Before Fixing the Bug

**Main.java:**

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.println("Enter the number of elements in the array:");
        int n = scanner.nextInt();
        int[] nums = new int[n];

        System.out.println("Enter the elements of the array:");
        for (int i = 0; i < n; i++) {
            nums[i] = scanner.nextInt();
        }

        System.out.println("Checking for triples...");
        boolean result = noTriples(nums);
        System.out.println("No triples found: " + result);
    }

    public static boolean noTriples(int[] nums) {
        for (int i = 0; i < nums.length; i++) { // Bug here
            if ((nums[i] == nums[i + 1]) && (nums[i] == nums[i + 2])) {
                return false;
            }
        }
        return true;
    }
}
```
```bash
#!/bin/bash

javac Main.java

if [ $? -eq 0 ]; then
    # Run the Java program
    java Main
else
    echo "Compilation failed."
fi
```
### Java File After Fixing the Bug
```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.println("Enter the number of elements in the array:");
        int n = scanner.nextInt();
        int[] nums = new int[n];

        System.out.println("Enter the elements of the array:");
        for (int i = 0; i < n; i++) {
            nums[i] = scanner.nextInt();
        }

        System.out.println("Checking for triples...");
        boolean result = noTriples(nums);
        System.out.println("No triples found: " + result);
    }

    public static boolean noTriples(int[] nums) {
        for (int i = 0; i < nums.length - 2; i++) {
            System.out.println("Iteration " + i + ": nums[" + i + "] = " + nums[i] + ", nums[" + (i + 1) + "] = " + nums[i + 1] + ", nums[" + (i + 2) + "] = " + nums[i + 2]);
            if ((nums[i] == nums[i + 1]) && (nums[i] == nums[i + 2])) {
                return false;
            }
        }
        return true;
    }
}
```
### Reflection:
I learned a whole lot of commands throughout this course. I would always see these commands in my previous CS classes, but I'd never knew what they actually did; I was just told to use them. I appreciate that we were introduced to GitHub, I feel like it is an industry standard and that it is a super useful skill to have. 

### Credit:
I used my code from a 3rd party Java Course called CodingBat (Specific problem: https://codingbat.com/prob/p170221) 
