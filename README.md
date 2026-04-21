# 📅 Day 01 - Chessboard Cell Color

---

## 🧩 Problem Statement

Given a coordinate in the form of a string (like "a1", "b2"), determine whether the cell is **Black** or **White** on a chessboard.

---

## 📥 Input Format

* A string `s` of length 2
* First character: column (a–h)
* Second character: row (1–8)

---

## 📤 Output Format

* Print `"Black"` or `"White"`

---

## 🔍 Sample Testcases

### Example 1

Input: a1
Output: Black

### Example 2

Input: b2
Output: Black

### Example 3

Input: a2
Output: White

---

## 🧠 Logic / Approach

* Convert column letter → number (a=1, b=2, ...)
* Convert row character → integer
* Add row + column
* If sum is even → Black
* If sum is odd → White

---

## 💻 Code (Java)

```java
import java.util.Scanner;

public class Main {
    public static String determineColor(String s) {
        char colChar = s.charAt(0);
        char rowChar = s.charAt(1);

        int col = colChar - 'a' + 1;
        int row = rowChar - '0';

        int sum = col + row;

        if (sum % 2 == 0)
            return "Black";
        else
            return "White";
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String s = scanner.nextLine().trim();
        System.out.println(determineColor(s));
    }
}
```

---

## ⏱️ Time & Space Complexity

* Time: O(1)
* Space: O(1)

---

## 📌 Key Takeaway

This problem is based on an even-odd pattern (parity), similar to chessboard coloring.
