# Part 1: Creating a Web Server Called StringServer

## Screenshot of StringServer.java

![StringServer_implementation_screenshot](https://user-images.githubusercontent.com/110694499/215291425-b5b759cd-86b4-49e8-bd02-eadeae2456c2.jpg)

## Using /add-message >> Example 1

![add-message_image1](https://user-images.githubusercontent.com/110694499/215292014-239aacab-3759-487d-910e-fee9b10175e5.jpg)

In the StringServer.java file, the method being called is: public String handleRequest(URI url);

The relevant arguments are:

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

## Using /add-message >> Example 2

![add-message_image2](https://user-images.githubusercontent.com/110694499/215292016-c12680a5-a4d6-4b83-abf9-759b3a018abb.jpg)



# Part 2: Bug Analysis

## We will be focusing on fixing the reversed() method found in ArrayExamples.java
The original code, as provided in GitHub:
```
static int[] reversed(int[] arr) {
  int[] newArray = new int[arr.length];
  for(int i = 0; i < arr.length; i += 1) {
    arr[i] = newArray[arr.length - i - 1];
  }
  return arr;
}
```

A failure-inducing input:
```
@Test
public void testReversed2() {
  int[]input2 = {1, 2, 3};
  assertArrayEquals(new int[]{3, 2, 1}, ArrayExamples.reversed(input2));
}
```
![testReversed2_FAILED_TEST](https://user-images.githubusercontent.com/110694499/215296016-50ab8535-be19-4845-b8cf-94f07bf80a17.jpg)


A *non* failure-inducing input:
```
@Test
public void testReversed() {
  int[] input1 = { };
  assertArrayEquals(new int[]{ }, ArrayExamples.reversed(input1));
}
```
![testReversed_PASSED_TEST](https://user-images.githubusercontent.com/110694499/215296021-a1021497-8a28-46d4-b86d-aaf49566fc5c.jpg)

Bug FIXED:
```
static int[] reversed(int[] arr) {
  int[] newArray = new int[arr.length];
  for(int i = 0; i < arr.length; i++) {
    newArray[arr.length-i-1] = arr[i];
  }
  
  return newArray;
}
```
The reason why there was a bug that resulted in the symptom shown above was that we were updating the *old* array, with reversed elements rather than the *new* one and were also returning the old array. 

These changes results in a passed test for the same *non* failure-inducing input as aforementioned:
![testReversed2_PASSED](https://user-images.githubusercontent.com/110694499/215296385-dc0301c1-0897-43a5-bdd5-c1827c6b8421.jpg)

# Part 3: What I Learned

In lab 2, I learned how to clone repositories using Github desktop and how to implement a program on Visual Studio Code that takes a URL string as an input and responds with the text of a web page. I then learned how to build and run the server on my local computer. 

In lab 3, I learned how to use tester java files to help me debug methods and how to write a web server that takes incoming requests in a URL and outputs a concatenated string, separated by new lines. 
