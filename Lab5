# Debugging Report: `noTriples` Method Issue

## Issue Description

### Original Post on EdStem

#### Title: `ArrayIndexOutOfBoundsException` in `noTriples` Method

**Body:**

Hi, I'm getting an `ArrayIndexOutOfBoundsException` when running my `noTriples` method with certain arrays. It happens with longer arrays, but not with shorter ones. Here's an example where it fails:

(insert screenshot)

### TA's Response

**Body:**

It looks like you're trying to access an array index that doesn't exist. Can you check the loop condition in your `noTriples` method? Make sure you're not going beyond the array's length. Maybe try adjusting the loop's range and see if that resolves the issue.

### Student's Follow-up Post

**Body:**

After modifying the loop condition as suggested, here's what I got:

(insert screenshot)

I changed the loop condition to stop before the last two elements, and it seems to be working now. Thanks for the hint!

## Setup Information

### File & Directory Structure

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
