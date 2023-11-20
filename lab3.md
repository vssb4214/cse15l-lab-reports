### Lab Report 3 - Bugs and Commands

#### Part 1: Bugs

##### Bug in ArrayExamples.java

###### Failure-Inducing Input:
```java
@Test
public void testReversedOdd() {
    int[] input = {1, 2, 3};
    int[] expected = {3, 2, 1};
    assertArrayEquals(expected, ArrayExamples.reversed(input));
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
<img width="691" alt="Screenshot 2023-11-19 at 7 00 32 PM" src="https://github.com/vssb4214/cse15l-lab-reports/assets/147002913/11a21612-0b80-429e-8fbe-d66433b7096a">

