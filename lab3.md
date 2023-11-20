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
