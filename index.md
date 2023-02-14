
Lab Report 2 - Servers and Bugs
=========

Lab Report 2 - Servers and Bugs
=========

Part 1: StringServer
---------
Here is how I implemented StringServer.java:

<img width="894" alt="Screen Shot 2023-01-30 at 11 00 53 PM" src="https://user-images.githubusercontent.com/97763875/215689381-5dbadb29-d66b-453e-b964-e75e8e41433c.png">

Here are the screenshots of using /add-message:
the method I used here is the else if statement. param[0] is the text I've entered, which is 'hello'

<img width="428" alt="Screen Shot 2023-02-07 at 6 38 29 PM" src="https://user-images.githubusercontent.com/97763875/217414642-5d5b47bf-e155-46d1-8971-3a3c1afc9021.png">

Here is the second message I added. I used the else if statement again. And this time, it created a new line, adding my second message to the new line. 

<img width="355" alt="Screen Shot 2023-02-07 at 6 39 40 PM" src="https://user-images.githubusercontent.com/97763875/217414803-31185e50-00f5-48a8-83d9-598427149a2d.png">


Part 2: Debug
---------
The code for tests:


     @Test 
     public void testReverseInPlace() {
     int[] input1 = { 3 };
     ArrayExamples.reverseInPlace(input1);
     assertArrayEquals(new int[]{ 3 }, input1);
     }
     
     @Test 
     public void testReverseInPlace1() {
     int[] input2 = { 1,2,3 };
     ArrayExamples.reverseInPlace(input2);
     assertArrayEquals(new int[]{ 3,2,1 }, input2);
     }


The first one did not cause an error, but the second one is a failure inducing input
The corresponding output:

<img width="568" alt="Screen Shot 2023-01-30 at 11 05 18 PM" src="https://user-images.githubusercontent.com/97763875/215690075-d1b278a8-0907-4ff2-83b5-f8607e741e7f.png">

Here is the buggy code:


    static void reverseInPlace(int[] arr) {
      for(int i = 0; i < arr.length; i += 1) {
        arr[i] = arr[arr.length - i - 1];
      }
    }
  
It contains bug because it did not save the number being reversed to a temp variable. I have fixed it in the new version

Here is how I fixed it:


    static void reverseInPlace(int[] arr) {
      for(int i = 0; i < arr.length/2; i += 1) {
        int temp = arr[arr.length - 1 - i];
        arr[arr.length - i - 1] = arr[i];
        arr[i] = temp;
      }
    }
    

Part 3: Feedbacks
---------
I have learned a lot from this course. I did not know how to publish a page on github and edit it using .md. I found it a very useful skills to have. I also learned several terminal commands that I didi not know before. I also learned each component of an URL. In addition, I am more clear of how to connect to a remote server. Overall, this class is very rewarding.  
