# EX 2D Pattern Matching using Naive Approach.
# DATE:
# AIM:
To write a Java program to for given constraints. Given text string with length n and a pattern with length m, the task is to prints all occurrences of pattern in text. Note: You may assume that n > m.

Examples:

Input: text = "THIS IS A TEST TEXT", pattern = "TEST" Output: Pattern found at index 10

Input: text = "AABAACAADAABAABA", pattern = "AABA" Output: Pattern found at index 0, Pattern found at index 9, Pattern found at index 12

# Algorithm
1.Input: Read the main string text. Read the substring pattern to be searched

2.Initialize variables: Let n = length of text. Let m = length of pattern.

3.Slide the pattern over the text: For each position i from 0 to n - m: Compare each character of pattern with the corresponding substring of text starting at index i.

4.Check for match: For each position i: Initialize j = 0. While j < m and text[i + j] == pattern[j], continue comparing. If j == m, then a match is found — print "Pattern found at index " + i.

5.If no match is found, no output is printed.
# Program:
```
Program to implement Reverse a String
Developed by: SRINIVASAN V
Register Number:212222043008
```
```
import java.util.Scanner;

public class NaivePatternSearch {
    //Type code here....
    static void search(String text,String pattern){
        int n=text.length();
        int m=pattern.length();
        for(int i=0;i<=n-m;i++){
            int j;
            for(j=0;j<m;j++){
                if(text.charAt(i+j)!=pattern.charAt(j))
                break;
            }
            if(j==m)
                System.out.println("Pattern found at index "+i);
        
    }
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Taking input from the user
        //.out.print("Enter the text: ");
        String text = scanner.nextLine();

        //System.out.print("Enter the pattern: ");
        String pattern = scanner.nextLine();

        // Search for pattern in the text
        search(text, pattern);

        scanner.close();
    }
}
```
# OUTPUT :
<img width="789" height="276" alt="512174740-20b4a10f-b4c9-41f2-a374-bc975ccd4cb3" src="https://github.com/user-attachments/assets/38980f85-859d-4a8a-b2ba-7e2bce9813fd" />

# RESULT :
The program successfully implemented and the expected output is verified.
