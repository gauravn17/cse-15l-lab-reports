# Lab Report 2 - Servers and Bugs

## Part 1

**Writing a StringServer**

The following is the code for StringServer, a web server that keeps track of a single string that gets added to by incoming requests through the add/s=string operation.

    import java.io.IOException;
    import java.net.URI;

    class Handler implements URLHandler {
        String message="";

        public String handleRequest(URI url) {
            if (url.getPath().equals("/")) {
                return message;
            } else {
                System.out.println("Path :"+url.getPath());
                if(url.getPath().contains("/add-message")){
                    String[] parameters= url.getQuery().split("=");
                    if(parameters[0].equals("s")){
                        message+=parameters[1]+"\n";
                    }
                    return message;
                }
                return "404 Not Found!";
            } 
    }
    }

    class StringServer {
        public static void main(String[] args) throws IOException {
            if(args.length == 0){
                System.out.println("Missing port number! Try any number between 1024 and 49151");
                return;
            }

            int port = Integer.parseInt(args[0]);

            Server.start(port, new Handler());
        }
    }
    
 The following are the screenshots taken after running the StringServer and using /add?s=Hello and /add?s=How are you, respectively:

 ![Add1](https://user-images.githubusercontent.com/93863977/236639925-5b73f28f-4e58-44f7-8910-f84afd90255a.png)


 ![Add2](https://user-images.githubusercontent.com/93863977/236639930-cb0b238e-e9f6-4b4f-8a99-f3f4dbda1d83.png)

For each of the screenshots the methods used are:

- the getPath() method, which returns the path of a URL.
- the contains() method, which checks if the path of the url contains a given string, and returns a boolean value.
- the getQuery() method, which returns the query of the URL( the portion of the URL after '?q=')
- the split() method, which in this case helps create an array of strings split by the character '='.
- the equals() method, which checks if the first element of the string array equals "s".

- For the first screenshot,the value of String parameters[] is {"s","Hello"} (due to the url.getQuery.split("=") method), and thus, since message+=parameters[1], the value of String message is "Hello", which is returned to the page.
- For the second screenshot,the value of String parameters[] is {"s","How are you"} (due to the url.getQuery.split("=") method), and thus, since message+=parameters[1], the value of String message is "How are you", which is returned to the page.
- For both screenshots, the value of int port is args[0], which is 4001.
- For both screenshots, the value of URI url is the url of the local server.
- For both screenshots, url.getPath() returns "/add-message", and the condition url.getPath.contains("/add-message") returns true.

Below is the screenshot of the bash terminal used to run the server:

![Screenshot 2023-05-06 at 11 10 48 AM](https://user-images.githubusercontent.com/93863977/236640299-ab542ff4-9f43-43e1-8930-135aac1e9a94.png)

## Part 2

**Using jUnit to identify bugs and fix them**

I will be addressing the bug in the reversed() method from the ArrayExamples.java code.

- A failure inducing input for the reversed() method is the following:

        public void testReversed(){
        int input [] = {2,3,4,5,6};
        assertArrayEquals(new int[]{6,5,4,3,2},ArrayExamples.reversed(input));
        }

- An input that does not produce a failure is the following:

        public void testReversed(){
        int input []={};
        assertArrayEquals(new int[]{}, ArrayExamples.reversed(input));
        }

- The image below is the screenshot taken after the jUnit tests are run on Eclipse IDE, showing the symptom of the problem:

![Screenshot 2023-05-06 at 8 17 03 PM](https://user-images.githubusercontent.com/93863977/236655816-bb4cc98b-2646-4023-989b-72871b58d0d7.png)

This image shows 2 test runs, 1 error and 1 failure on the left hand side

- The buggy code for the reversed() method:

      static int[] reversed(int[] arr) {
        int[] newArray = new int[arr.length];
        for(int i = 0; i < arr.length; i += 1) {
          arr[i] = newArray[arr.length - i - 1];
        }
        return arr;
      }
  
- The correct code for the reversed method is the following:

      static int[] reversed(int[] arr) {
        int[] newArray = new int[arr.length];
        for(int i = 0; i < arr.length; i += 1) {
          newArray[i] = arr[arr.length - i - 1];
        }
        return newArray;
      }
  
  The difference between the buggy and correct code, is that the buggy code assigns values from 'newArray', which has no elements, to the original array, 'arr' when it should be the other way around. 
  The buggy code also returns the original array, 'arr' instead of the new reversed array, 'newArray'.
  These problems are fixed with changes inside and after the for loop, where the line 'arr[i] = newArray[arr.length - i - 1]' is replaced with 'newArray[i] = arr[arr.length - i - 1]', and newArray is returned outside the for loop instead of 'arr'.

## Part 3- Reflection

- In lab 2, I learned about the different parts of a URL, how to use methods such as getPath() and getQuery() and also how to build and host web servers from the command line. I had a lot of trouble running the server at first due to the file not being in the right directory, and finally troubleshooting that and getting it to work was a great learning experience for me.
- In lab 3, I gained more practice in reading through buggy code and using jUnit tests to debug.

