# Lab Report 5

## Part 1: Debugging Scenario
### 1. Original post
**Title:** <br>
Help with reversing lists

**What environment are you using (computer, operating system, web browser, terminal/editor, and so on)?** <br>
I am currently running my code on a MacBook Pro which means I am using my Mac's operating system. I am using the VSCode terminal and editor in order to compile and run my code. <br>

**Detail the symptom you're seeing. Be specific; include both what you're seeing and what you expected to see instead. Screenshots are great, copy-pasted terminal output is also great. Avoid saying “it doesn't work”.** <br>


**Detail the failure-inducing input and context. That might mean any or all of the command you're running, a test case, command-line arguments, working directory, even the last few commands you ran. Do your best to provide as much context as you can.** <br>


## 2. TA Response
For your `reverseInPlace` method, consider how many times you want your loop to iterate and think about what happens if you aren't creating a new array to store the reversed elements. <br>
For your `reversed` method, consider what values you want to be stored in your `newArray` and your original array `arr`.

## 3. Updated code after TA Response

I realized that in my `reverseInPlace` method, I had to change `i < arr.length` to `i < arr.length/2` since the original array rather than a reversed array was returning due to my incorrect bound. I also created a new variable `temp` to store the value of `arr[i]` so that when I changed the value at `arr[i]`, the old value wouldn't be forgotten. <br>
For my `reversed` method, I realized that I was incorrectly assigning values to `arr` instead of `newArray` so I had to switch the two and return `newArray` instead of `arr`.

## 4. All of the necessary setup information
**The file and directory structure:** <br>


**Contents of file before fixing the bug:** <br>
```
public class ArrayExamples {

  // Changes the input array to be in reversed order
  static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    } 
  }

  // Returns a *new* array with all the elements of the input array in
  // reversed order
  static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
  }
}
```

**Command(s) used to trigger the bug:**


**What to edit to fix the bug:** <br>
**reverseInPlace:** For this method, you had to change how many times the loop would iterate to `i < arr.length/2` compared to the original `i < arr.length` because if you don't, the original list will be returned if you iterate through the whole array and reverse elements. You also had to create a new variable `temp` to store `arr[i]` to save the value at `arr[i]` before it got changed. <br>

**reversed:** For this method, you had to change the value assignment to `newArray[i] = arr[arr.length-i-1]` compared to the original `arr[i] = newArray[arr.length - i - 1]` so that you assign the reversed elements to newArray rather than the original one. Also, you have to return `newArray` and not `arr` at the end.


## Part 2: Reflection
Something I learned this quarter is that if I ever need help with something, I need to be the one to take intitiative to ask. I realized that a lot of the people in my lab were quick to understand what was going on and worked at their own fast-pace (something that was difficult for me to do), so if I ever needed assistance I had to go ask them for help rather than have them check up on everybody else. Not only that, but learning how to write a grading script was also very interesting because it let me take a peek into what TA's usually do for us that I had never seen before. 
