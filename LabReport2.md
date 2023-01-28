# Part 1

## Screenshot of StringServer.java

![StringServer_implementation_screenshot](https://user-images.githubusercontent.com/110694499/215291425-b5b759cd-86b4-49e8-bd02-eadeae2456c2.jpg)

## Using /add-message >> Example 1

![add-message_image1](https://user-images.githubusercontent.com/110694499/215292014-239aacab-3759-487d-910e-fee9b10175e5.jpg)

In the StringServer.java file, there are many methods being called, such as:
1. java.net.URI.getPath() - No arguments; Returns the decoded path component of this URI, or null if the path is undefined
2. equals() - Takes an argument called anObject: The object to compare the String in getPath() against
3. format() - Takes a string argument and outputs a formatted string
4. handleRequest() - Takes any URI
5. println() - Takes a string argument, prints it, then terminates the line
6. contains() - Takes a sequence of char values to search for in a string, and outputs true/false
7. java.net.URI.getQuery() - Returns the decoded query component of this URI.
8. java.lang.String.split() - Takes a string argument, then splits this string around matches of the given regular expression.
9. java.util.ArrayList.add() - Takes a String argument and appends the string to the end of the ArrayList
10. java.util.ArrayList.get() - Takes an integer index and returns the element at the specified index of the ArrayList
11. java.util.ArrayList.size() - No arguments; returns the number of valid elements in the ArrayList

# Using /add-message >> Example 2

![add-message_image2](https://user-images.githubusercontent.com/110694499/215292016-c12680a5-a4d6-4b83-abf9-759b3a018abb.jpg)

# Part 2: Bug Analysis

## We will be focusing on fixing the reversed() method found in ArrayExamples.java
...
static int[] reversed(int[] arr) {
  int[] newArray = new int[arr.length];
  for(int i = 0; i < arr.length; i += 1) {
    arr[i] = newArray[arr.length - i - 1];
  }
  return arr;
}
...

A failure-inducing input:
...
@Test
public void testReversed2() {
  int[]input2 = {1, 2, 3};
  assertArrayEquals(new int[]{3, 2, 1}, ArrayExamples.reversed(input2));
}
...

A *non* failure-inducing input:
...
@Test
public void testReversed() {
  int[] input1 = { };
  assertArrayEquals(new int[]{ }, ArrayExamples.reversed(input1));
}
...


