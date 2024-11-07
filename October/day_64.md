
# 📅 Day 64: 2024-10-13

## 🚀 Problems Solved

---

### 🧩 Problem 1: 
Design and implement a Linked List data structure.
A node in a linked list should have the following attributes - an integer value and a pointer to the next node.

Insert_node(position, value) - To insert the input value at the given position in the linked list.
delete_node(position) - Delete the value at the given position from the linked list.
print_ll() - Print the entire linked list, such that each element is followed by a single space (no trailing spaces).
- **Approach 1: **
  - *LinkedList Impl*
- **⏳ Time Complexity:** `Individual FN`
- **💾 Space Complexity:** `O(1)`

```java
// Code implementation for Problem 1
static Node head;

static class Node{
  int value;
  Node next;
  Node(int value){
    this.value = value;
    next = null;
  }
}

public static void insert_node(int position, int value) {
  // @params position, integer
  // @params value, integer
  if(position == 1){
    Node newNode = new Node(value);
    newNode.next = head;
    head = newNode;
    return;
  }


  Node current = head;

  for(int i = 1; i < position-1; i++){
    if(current != null){
      current = current.next;
    }

  }

  if(current != null){
    Node newnode = new Node(value);
    newnode.next = current.next;
    current.next = newnode;
  }

}

public static void delete_node(int position) {
  // @params position, integer

  if(head == null){
    return;
  }
  if(position == 1){
    head = head.next;
    return;
  }

  Node current = head;
  for(int i = 1; i < position-1 && current!=null; i++){
    current = current.next;

  }
  if(current != null && current.next != null){
    current.next = current.next.next;
  }


}

public static void print_ll() {
  // Output each element followed by a space
  Node current = head;
  while(current != null){
    System.out.print(current.value);
    if(current.next != null){
      System.out.print(" ");
    }

    current = current.next;
  }
}


```
---

### 🧩 Problem 2: 
Given a matrix A of size Nx3 representing operations. Your task is to design the linked list based on these operations.

There are four types of operations:

0 x -1: Add a node of value x before the first element of the linked list. After the insertion, the new node will be the first node of the linked list.
1 x -1: Append a node of value x to the last element of the linked list.
2 x index: Add a node of value x before the indexth node in the linked list. If index equals to the length of linked list, the node will be appended to the end of linked list. If index is greater than the length, the node will not be inserted.
3 index -1: Delete the indexth node in the linked list, if the index is valid.
A[i][0] represents the type of operation.

A[i][1], A[i][2] represents the corresponding elements with respect to type of operation.

Note: Indexing is 0 based.
- **Approach 1:**
  - *LinkedList Impl Logic*
- **⏳ Time Complexity:** `Individual case`
- **💾 Space Complexity:** `O(1)`

```java
// Code implementation for Problem 2
public ListNode head;
public ListNode solve(int[][] A) {

  for(int i =0; i < A.length; i++){
    int operation = A[i][0];

    if(operation == 0){
      int value = A[i][1];
      ListNode newnode = new ListNode(value);
      newnode.next = head;
      head = newnode;
    }

    else if(operation == 1){
      int value = A[i][1];
      ListNode newnode = new ListNode(value);
      ListNode current  = head;

      if(current == null){
        head = newnode;
        continue;
      }
      while(current.next != null){
        current = current.next;
      }

      current.next = newnode;
    }
    else if(operation == 2){
      int value = A[i][1];
      ListNode newnode = new ListNode(value);
      int index = A[i][2];
      if(index == 0){
        newnode.next = head;
        head = newnode;
        continue;
      }
      ListNode current = head;

      for(int k = 0; k < index-1;  k++){
        if(current == null){
          continue;
        }
        current = current.next;
      }
      if(current != null){
        newnode.next = current.next;
        current.next = newnode;
      }
    }
    else if (operation == 3){
      int index = A[i][1];
      ListNode current = head;
      if(current == null){
        continue;
      }
      if(index == 0){
        head = head.next;
      }

      for(int k = 0; k < index-1 && current!= null; k++){
        current = current.next;
      }

      if(current != null && current.next != null){
        current.next = current.next.next;
        continue;
      }




    }

  }

  return head;
}
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

