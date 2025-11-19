
# EX 2A Assign Cookies using Greedy Algorithm. 
## DATE: 30/08/2025
## AIM:
To Write a Java program for the following Constraints.
Assume you are an awesome parent and want to give your children some cookies. But, you should give each child at most one cookie.

Each child i has a greed factor g[i], which is the minimum size of a cookie that the child will be content with; and each cookie j has a size s[j]. If s[j] >= g[i], we can assign the cookie j to the child i, and the child i will be content. Your goal is to maximise the number of your content children and output the maximum number.

## Algorithm
1. Read the sizes of the greed array g and cookie array s, and input their elements.
2. Sort both arrays in non-decreasing order.
3. Initialize two pointers i = 0 for children and j = 0 for cookies.
4. Traverse both arrays; if the current cookie s[j] satisfies the child g[i], increase i. Always increase j.
5. When traversal ends, i represents the number of content children; print i.


## Program:
```
/*
Program to implement Reverse a String
Developed by: Mohammed Muzammil A
Register Number:  212222040103
*/

import java.util.*;

public class AssignCookies {
    
    public static int findContentChildren(int[] g, int[] s) {
        Arrays.sort(g);
        Arrays.sort(s);
        int i = 0, j = 0;
        while (i < g.length && j < s.length) {
            if (s[j] >= g[i]) i++;
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

## Output:
<img width="829" height="295" alt="2a" src="https://github.com/user-attachments/assets/840724cf-c175-41c7-aeda-32842042f0a5" />




## Result:
The program successfully print all the numbers from 1 to N. 
