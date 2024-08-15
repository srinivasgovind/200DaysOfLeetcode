
# 📅 Day 4: 2024-08-14

## 🚀 Problems Solved

---

### 🧩 Problem 1: Rotate the Array
- **Approach:**
  - * This problem can be solved if we get intution of reversing the array*
- **⏳ Time Complexity:** `O(n)`
- **💾 Space Complexity:** `O(1)`

```java
// Code implementation for Problem 1
public static void main(String[] args) {
  // YOUR CODE GOES HERE
  // Please take input and print output to standard input/output (stdin/stdout)
  // DO NOT USE ARGUMENTS FOR INPUTS

  Scanner sc = new Scanner(System.in);

  int n = sc.nextInt();
  int arr[]  = new int[n];
  for(int i = 0 ; i < n ; i++){
    arr[i] = sc.nextInt();
  }
  int k = sc.nextInt();
  if( k > n){
    k = k % n;
  }
  reverseArray(arr, 0, n -1);
  reverseArray(arr, 0, k-1);
  reverseArray(arr, k, n-1);

  for(int i = 0 ; i < arr.length; i++){
    System.out.print(arr[i] + " ");
  }

}

public static void reverseArray(int[] arr, int start, int end){

  int startptr = start;
  int endptr = end;

  while(startptr < endptr){
    int temp = arr[startptr];
    arr[startptr] = arr[endptr];
    arr[endptr] = temp;
    startptr++;
    endptr--;
  }
}
```

---

