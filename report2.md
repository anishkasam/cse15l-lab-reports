# Week 2 Lab Report

## Part 1

Code for StringServer:
![Image](images/StringServer.png)

Screenshot #1 of StringServer:
![Image](images/StringServerDemo1.png)

Which methods in your code are called?
What are the relevant arguments to those methods, and the values of any relevant fields of the class?
How do the values of any relevant fields of the class change from this specific request? If no values got changed, explain why.

Screenshot #2 of StringServer:
![Image](iages/StringServerDemo2.png)

## Part 2

Failure-inducing input for the buggy program
`@Test
 public void testReverseInPlaceTwo() {
 int[] input1 = {1, 2, 3, 4};
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{4, 3, 2, 1}, input1);
  }`
