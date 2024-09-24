
# 📅 Day 41: 2024-09-20

## 🚀 Problems Solved

---

### 🧩 Problem 1: Length of longest consecutive ones
Given a binary string A. It is allowed to do at most one swap between any 0 and 1. Find and return the length of the longest consecutive 1’s that can be achieved.
- **Approach 1: Bruteforce**
  - *[Briefly describe your approach]*
- **⏳ Time Complexity:** `O(n)`
- **💾 Space Complexity:** `O(1)`

```java
// Code implementation for Problem 1
public int solve(String A) {

  int n = A.length();

  int left[] = new int[n];
  int right[] = new int[n];

  if(A.charAt(0)=='1'){
    left[0] = 1;

  }else{
    left[0] = 0;
  }

  if(A.charAt(n-1)== '1'){
    right[n-1] = 1;
  }else{
    right[n-1] = 0;
  }

  for(int i=1; i<n; i++){
    if(A.charAt(i) == '1'){
      left[i] = left[i-1]+1;
    }
    else{
      left[i] = 0;
    }
  }
  for(int i = n-2; i>=0; i--){
    if(A.charAt(i) == '1'){
      right[i] = right[i+1]+1;
    }else{
      right[i] = 0;
    }
  }
  int max_count = 0;
  int sum = 0;
  int total_ones = 0;
  for(int i = 0; i < n; i++){
    max_count = Math.max(max_count, left[i]);
    if(A.charAt(i) == '1'){
      total_ones++;
    }
  }

  for(int j = 1; j < n-1; j++){
    if(A.charAt(j)=='0'){
      sum = left[j-1]+right[j+1];
      if(sum<total_ones){
        sum+=1;
      }
      max_count = Math.max(max_count, sum);
    }
  }
  return max_count;

}
```

- **Approach 2: Optimized**
  - *[Briefly describe your approach]*
- **⏳ Time Complexity:** `O(n^2)`
- **💾 Space Complexity:** `O(n)`

```java
// Code implementation for Problem 1
[Write your Java code here]
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

