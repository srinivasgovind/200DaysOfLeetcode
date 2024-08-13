
# 📅 Day 2: 2024-08-12

## 🚀 Problems Solved

---

### 🧩 Problem 1: TWO SUM
- **Approach1:**
  - * Iterate through inner loop and compare all the cases*
- **⏳ Time Complexity:** `O(n^2)`
- **💾 Space Complexity:** `O(1)`

```java
// Code implementation for Problem 1
public int[] twoSum(int[] nums, int target) {

  int[]  result = new int[2];
  for(int i = 0 ; i < nums.length -1; i++){
      for(int j = i + 1; j < nums.length; j++){
          if(nums[i] + nums[j] == target){
              result[0] = i;
              result[j] = j;
          }
      }

  }

  return result;
}

```

- **Approach2:**
  - *Using HashMap store prev inputs and their ith location*
- **⏳ Time Complexity:** `O(n)`
- **💾 Space Complexity:** `O(n)`

```java
// Code implementation for Problem 1
public int[] twoSum(int[] nums, int target) {

  Map<Integer,Integer> hm = new HashMap<>();

  int[]  result = new int[2];
  for(int i = 0 ; i < nums.length; i++){

    if(hm.containsKey(target-nums[i])){
      result[0] = i;
      result[1] = hm.get(target-nums[i]);
    }
    else{
      hm.put(nums[i],i);
    }

  }

  return result;
}
```

---

### 🧩 Problem 2: Contains Duplicate
- **Approach1:**
  - * Sort the array and compare prev element with current( 2 pointers)*
- **⏳ Time Complexity:** `O(nlogn)`
- **💾 Space Complexity:** `O(1)`

```java
// Code implementation for Problem 2
public boolean containsDuplicate(int[] nums) {
  Arrays.sort(nums);
  int prev = 0;
  for(int i = 1; i < nums.length ; i++){
    if(nums[i] == nums[prev]){
      return true;
    }
    prev++;
  }
  return false;
}
```

- **Approach2:**
  - * Set to store the elements and find duplicates with Set*
- **⏳ Time Complexity:** `O(n)`
- **💾 Space Complexity:** `O(n)`

```java
// Code implementation for Problem 2
public boolean containsDuplicate(int[] nums) {
  Set<Integer> hs = new HashSet<>();

  for(int num : nums){
    if(hs.contains(num)){
      return true;
    }
    hs.add(num);
  }
  return false;
}
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

