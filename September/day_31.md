
# 📅 Day 31: 2024-09-10

## 🚀 Problems Solved

---

### 🧩 Problem 1: A wire connects N light bulbs.

Each bulb has a switch associated with it; however, due to faulty wiring, a switch also changes the state of all the bulbs to the right of the current bulb.

Given an initial state of all bulbs, find the minimum number of switches you have to press to turn on all the bulbs.

You can press the same switch multiple times.

Note: 0 represents the bulb is off and 1 represents the bulb is on.
- **Approach:Bruteforce**
  - *Bruteforce way of thinking*
- **⏳ Time Complexity:** `O(n^2)`
- **💾 Space Complexity:** `O(1)`

```java
public int bulbs(int[] A) {

  int count = 0;

  for(int i = 0 ; i < A.length; i++){
    if(A[i] == 0){
      count++;
      for(int j = i+1; j < A.length; j++){
        A[j] = 1 - A[j];
      }
    }
  }
  return count;
}
```

- **Approach: Optimized**
  - *Tricky by observation of input toggling figured out event count have orginal array , while odd count toggles the array*
- **⏳ Time Complexity:** `O(n)`
- **💾 Space Complexity:** `O(1)`

```java
public int bulbs(int[] A) {

  int count = 0;

  for(int i = 0 ; i < A.length; i++){
    int state = A[i];

    if(count % 2 == 0){
      state = A[i];
    }else{
      state = 1 - A[i];
    }

    if(state == 0){
      count++;
    }
  }
  return count;
}
```

---

### 🧩 Problem 2: [Problem Title or Description]
- **Approach:**
  - *[Briefly describe your approach, e.g., Two-pointer technique, Dynamic programming with memoization, etc.]*
- **⏳ Time Complexity:** `[e.g., O(n), O(log n)]`
- **💾 Space Complexity:** `[e.g., O(1), O(n)]`

```java
// Code implementation for Problem 2
[Write your Java code here]
```

---

### 🧩 Problem 3: [Problem Title or Description]
- **Approach:**
  - *[Briefly describe your approach, e.g., Two-pointer technique, Dynamic programming with memoization, etc.]*
- **⏳ Time Complexity:** `[e.g., O(n), O(log n)]`
- **💾 Space Complexity:** `[e.g., O(1), O(n)]`

```java
// Code implementation for Problem 3
[Write your Java code here]
```

---

