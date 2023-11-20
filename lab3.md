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

##### Explanation:

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

#### Part 1: Researching Commands

###### ChatGPT Explanation of Grep:
<img width="610" alt="Screenshot 2023-11-19 at 11 40 10 PM" src="https://github.com/vssb4214/cse15l-lab-reports/assets/147002913/16d6a551-8009-4ea3-b541-e2050596e963">

##### grep -r:
<img width="718" alt="Screenshot 2023-11-19 at 11 42 51 PM" src="https://github.com/vssb4214/cse15l-lab-reports/assets/147002913/12b000b0-fe5d-4936-af6d-650b306424b8">

##### This command searched all the files that contained the word "reversed" and printed each line that does


##### grep -c:
<img width="621" alt="Screenshot 2023-11-19 at 11 47 40 PM" src="https://github.com/vssb4214/cse15l-lab-reports/assets/147002913/592cb981-b892-4151-a66a-0ecf82df6533">

##### The command counts all the lines that contain the word "input" and returns the numerical value

##### grep -v:
<img width="632" alt="Screenshot 2023-11-19 at 11 49 32 PM" src="https://github.com/vssb4214/cse15l-lab-reports/assets/147002913/1e38724e-5bfa-4ebe-b7e2-ff6113592f3d">

##### This command returns every line that does not contain "input"

##### Pattern with grep:
<img width="661" alt="Screenshot 2023-11-19 at 11 52 08 PM" src="https://github.com/vssb4214/cse15l-lab-reports/assets/147002913/e014e665-7309-42a8-977a-afe79eef853c">

I was able to find the occurances of "void" and "input" in ArrayTests.java using grep standalone. 





