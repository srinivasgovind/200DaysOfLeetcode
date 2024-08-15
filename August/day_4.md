
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

### 🧩 Problem 2: Rotate the Array Left
- **Approach:**
  - *[Briefly describe your approach, e.g., Two-pointer technique, Dynamic programming with memoization, etc.]*
- **⏳ Time Complexity:** `O(m*n)`
- **💾 Space Complexity:** `O(m*n)`

```java
// Code implementation for Problem 2
public int[][] solve(int[] A, int[] B)
{


  int resultMatrix[][]= new int[B.length][A.length];



  for(int i = 0 ; i < B.length ; i++){
    int k = B[i] % A.length;
    int[] temp  = Arrays.copyOf(A, A.length);
    int[] reversed = reverseArray(temp, 0, A.length-1);
    int[] reverse1 = reverseArray(reversed, 0, A.length - k -1);
    int[] reversed2 = reverseArray(reverse1, A.length-k, A.length -1);

    for(int j = 0; j < A.length; j++){
      resultMatrix[i][j] = reversed2[j];
    }
  }
  return resultMatrix;
}
public int[] reverseArray(int[] arr, int startptr, int endptr){

  while(startptr < endptr){
    int temp = arr[startptr];
    arr[startptr] = arr[endptr];
    arr[endptr] = temp;
    startptr++;
    endptr--;
  }
  return arr;
}

```

---

