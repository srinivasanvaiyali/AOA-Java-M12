# EX 2A Assign Cookies using Greedy Algorithm.
# DATE:
# AIM:
To Write a Java program for the following Constraints. Assume you are an awesome parent and want to give your children some cookies. But, you should give each child at most one cookie.

Each child i has a greed factor g[i], which is the minimum size of a cookie that the child will be content with; and each cookie j has a size s[j]. If s[j] >= g[i], we can assign the cookie j to the child i, and the child i will be content. Your goal is to maximise the number of your content children and output the maximum number.

# Algorithm
1.Start the program and read: Number of children n and their greed factors g[]. Number of cookies m and their sizes s[].

2.Sort both arrays g[] (children’s greed) and s[] (cookie sizes) in ascending order to distribute the smallest cookie that satisfies each child.

3.Initialize two pointers: i = 0 → to track children. j = 0 → to track cookies.

4.Use a loop to iterate through cookies: If the current cookie s[j] satisfies the child g[i] (i.e., s[j] >= g[i]), increment i (child is satisfied). Always increment j to check the next cookie.

5.After the loop, the variable i represents the total number of content (satisfied) children. Print i and stop the program.
# Program:
```
Program to implement Reverse a String
Developed by: SRINIVASAN V
Register Number:212222043008
```
```
import java.util.*;

public class AssignCookies {
    
    public static int findContentChildren(int[] g, int[] s) {
        // Type Your Logic Here.
        Arrays.sort(g);
        Arrays.sort(s);
        int i=0,j=0;
        while(i<g.length && j<s.length){
            if(s[j]>=g[i])i++;
            j++;
        }
        return i;
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] g = new int[n];
        for (int i = 0; i < n; i++) g[i] = sc.nextInt();
        int m = sc.nextInt();
        int[] s = new int[m];
        for (int i = 0; i < m; i++) s[i] = sc.nextInt();
        System.out.println(findContentChildren(g, s));
    }
}
```
# OUTPUT :
<img width="363" height="348" alt="512169064-e9443079-3efd-4a14-94f6-c45cd9e4dd06" src="https://github.com/user-attachments/assets/9aee2fb2-8cde-47ac-9adb-2101aff31cb2" />

# Result:
The program successfully print all the numbers from 1 to N.
