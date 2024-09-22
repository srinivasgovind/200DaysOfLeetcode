
# 📅 Day 40: 2024-09-19

## 🚀 Problems Solved

---

### 🧩 Problem 1: 
You are given an array A consisting of heights of Christmas trees and an array B of the same size consisting of the cost of each of the trees (Bi is the cost of tree Ai, where 1 ≤ i ≤ size(A)), and you are supposed to choose 3 trees (let's say, indices p, q, and r), such that Ap < Aq < Ar, where p < q < r.
The cost of these trees is Bp + Bq + Br.

You are to choose 3 trees such that their total cost is minimum. Return that cost.

If it is not possible to choose 3 such trees return -1.
- **Approach 1: Bruteforce**
  - *[Briefly describe your approach]*
- **⏳ Time Complexity:** `O(n^3)`
- **💾 Space Complexity:** `O(1)`

```java
// Code implementation for Problem 1
public int solve(int[] A, int[] B) {

  int sum = Integer.MAX_VALUE;

  for(int i = 0; i < A.length; i++){
    for(int j = i+1; j < A.length; j++){
      for(int k = j+1; k < A.length; k++){
        if(A[i] < A[j] && A[j] < A[k]){
          sum = Math.min(sum, B[i]+B[j]+B[k]);
        }
      }
    }
  }
  if(sum == Integer.MAX_VALUE){
    return -1;
  }
  return sum;
}

```

- **Approach 2: Optimized**
  - *take j as middle value iterate left to find i and iterate right to find k*
- **⏳ Time Complexity:** `O(n^2)`
- **💾 Space Complexity:** `O(1)`

```java
// Code implementation for Problem 1
public int solve(int[] A, int[] B) {

  int min_cost = (int)(1e9 + 10);

  for(int j = 1; j < A.length - 1; j++){

    int min_i = (int)(1e9 + 10);
    int min_k = (int)(1e9 + 10);
    for(int i = j-1;  i>=0; i--){
      if(A[i]<A[j] && B[i]<min_i){
        min_i = B[i];

      }
    }

    for(int k = j+1; k < A.length; k++){
      if(A[j] < A[k] && B[k] < min_k){
        min_k = B[k];
      }
    }
    min_cost = Math.min(min_cost, B[j]+min_i+min_k);
  }
  if(min_cost == (int)(1e9 + 10)){
    return -1;
  }

  return min_cost;

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

