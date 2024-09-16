
# 📅 Day 35: 2024-09-14

## 🚀 Problems Solved

---

### 🧩 Problem 1: 
You are given an integer array A of length N comprising of 0's & 1's, and an integer B.

You have to tell all the indices of array A that can act as a center of 2 * B + 1 length 0-1 alternating subarray.

A 0-1 alternating array is an array containing only 0's & 1's, and having no adjacent 0's or 1's. For e.g. arrays [0, 1, 0, 1], [1, 0] and [1] are 0-1 alternating, while [1, 1] and [0, 1, 0, 0, 1] are not.
- **Approach 1: Bruteforce**
  - *[Briefly describe your approach]*
- **⏳ Time Complexity:** `O((n-window+1)*(window))`
- **💾 Space Complexity:** `O(1)`

```java
// Code implementation for Problem 1
public int[] solve(int[] A, int B) {

  int window = 2 * B + 1;
  List<Integer> ans = new ArrayList<>();
  for(int i = 0; i < A.length - window+1; i++){
    boolean flag = true;
    int prev = -1;

    for(int j = i; j < i+window; j++){
      if(A[j] == prev){
        flag = false;
        break;
      }
      prev = A[j];
    }
    if(flag){
      ans.add(i+B);
    }
  }

  int result[] = new int[ans.size()];
  for(int i=0; i<ans.size(); i++){
    result[i] = ans.get(i);
  }
  return result;
}
```

---

### 🧩 Problem 2: [Problem Title or Description]
- **Approach 1: Bruteforce**
  - *[Briefly describe your approach]*
- **⏳ Time Complexity:** `O(n^2)`
- **💾 Space Complexity:** `O(n)`

```java
// Code implementation for Problem 2
[Write your Java code here]
```

- **Approach 2: Optimized**
  - *[Briefly describe your approach]*
- **⏳ Time Complexity:** `O(n^2)`
- **💾 Space Complexity:** `O(n)`

```java
// Code implementation for Problem 2
[Write your Java code here]
```

---

### 🧩 Problem 3: [Problem Title or Description]
- **Approach 1: Bruteforce**
  - *[Briefly describe your approach]*
- **⏳ Time Complexity:** `O(n^2)`
- **💾 Space Complexity:** `O(n)`

```java
// Code implementation for Problem 3
[Write your Java code here]
```

- **Approach 2: Optimized**
  - *[Briefly describe your approach]*
- **⏳ Time Complexity:** `O(n^2)`
- **💾 Space Complexity:** `O(n)`

```java
// Code implementation for Problem 3
[Write your Java code here]
```

---

