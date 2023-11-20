### Lab Report 3 - Bugs and Commands

#### Part 1: Bugs

##### Bug in ArrayExamples.java

###### Failure-Inducing Input:
```java
@Test
public void testReversed2() {
    int[] input1 = {1, 2, 3};
    assertArrayEquals(new int[]{ }, ArrayExamples.reversed(input1));
  }
```
###### Non-Failure-Inducing Input :
```java
@Test
public void testReversedEven() {
    int[] input = {1, 2, 3, 4};
    int[] expected = {4, 3, 2, 1};
    assertArrayEquals(expected, ArrayExamples.reversed(input));
}
```
###### Symptom:
<img width="779" alt="Screenshot 2023-11-19 at 11 24 49 PM" src="https://github.com/vssb4214/cse15l-lab-reports/assets/147002913/03a11735-e12a-4fbc-944e-bf3555e798b7">

###### After fixes made to ArrayExample.java and to testReversed2:
<img width="778" alt="Screenshot 2023-11-19 at 11 28 57 PM" src="https://github.com/vssb4214/cse15l-lab-reports/assets/147002913/9664113a-8773-4c95-8a6b-f8974d68c424">
###### Explanation:
An inaccurate expectation of an empty array {} from an input array {1, 2, 3} and a problem in the reversed function of ArrayExamples.java caused the testReversed2 method of ArrayTests.java to fail. Rather than creating a new array that was appropriately reversed, the reversed method inadvertently modified the existing array. The reversed function was adjusted to correctly generate and return a new array with the members of the input array in reverse order. The test was then fixed by updating its expected result to the correctly reversed array {3, 2, 1}. This adjustment made sure the procedure produced the desired results, matching the requirements of the updated test.

###### testReversed2 Before & After:
```java
@Test
public void testReversed2() {
  int[] input1 = {1, 2, 3};
  assertArrayEquals(new int[]{ }, ArrayExamples.reversed(input1));
}
```
```java
@Test
public void testReversed2() {
  int[] input1 = {1, 2, 3};
  assertArrayEquals(new int[]{3, 2, 1}, ArrayExamples.reversed(input1));
}
```

###### reversed Before & After:
```java
static int[] reversed(int[] arr) {
  int[] newArray = new int[arr.length];
  for(int i = 0; i < arr.length; i += 1) {
    arr[i] = newArray[arr.length - i - 1];
  }
  return newArray;
}
```
```java
static int[] reversed(int[] arr) {
  int[] newArray = new int[arr.length];
  for(int i = 0; i < arr.length; i += 1) {
    newArray[i] = arr[arr.length - i - 1];
  }
  return newArray;
}
```









