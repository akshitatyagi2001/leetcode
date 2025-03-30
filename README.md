# LEETCODE 125. Valid Palindrome

## Description
A phrase is a palindrome if, after converting all uppercase letters into lowercase letters and removing all non-alphanumeric characters, it reads the same forward and backward. Alphanumeric characters include letters and numbers.

Given a string s, return true if it is a palindrome, or false otherwise.

### Example 1:

Input: s = "A man, a plan, a canal: Panama"
Output: true
Explanation: "amanaplanacanalpanama" is a palindrome.


### Solution:

#### JAVA

```java
public static boolean isPalindrome(String s) {
    s = s.toLowerCase();
    s = s.replaceAll("[^a-zA-Z0-9]", "");
// reverse string
    String reversed = "";
    for (int i = s.length() - 1; i >= 0; i--) {
        reversed += s.charAt(i);
    }
    if (reversed.equals(s)) {
        return true;
    }
    return false;
}
```