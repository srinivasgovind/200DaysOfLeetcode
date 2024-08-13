
# 📅 Day 3: 2024-08-13

## 🚀 Problems Solved

---

### 🧩 Problem 1: Group Anagram
- **Approach:**
  - *Sort the Strings and maintain map of List to group them.*
- **⏳ Time Complexity:** `O(n * klogk)`
- **💾 Space Complexity:** `O(n * k)`

```java
// Code implementation for Problem 1
public List<List<String>> groupAnagrams(String[] strs) {
  Map<String, List<String>>  hm = new HashMap<>();
  List<List<String>> result = new ArrayList<>();
  for(String str: strs){
    char[] chars = str.toCharArray();
    Arrays.sort(chars);
    String sorted = new String(chars);

    if(!hm.containsKey(sorted)){
      hm.put(sorted, new ArrayList<>());
    }
    hm.get(sorted).add(str);
  }
  for(String key : hm.keySet()){
    result.add(hm.get(key));
  }
  return result;
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

