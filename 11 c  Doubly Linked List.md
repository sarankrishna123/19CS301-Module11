### EX: 11.C Doubly Linked List (Traversal, Search and Delete)

### Aim: To Write a python program to traverse the elements in doubly linked list.

### Algorithm:

STEP 1: Start.

STEP 2: Create a node class and object of the node.

STEP 3: Create another class to use the node object.
STEP 4 : Traverse the list from start to last data element.

STEP 5 : Print the data.

STEP 6 : Stop.

### Program:
```
reg no:212223070023
name:saran krishna P S
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None
        self.prev = None

class DoublyLinkedList:
    def __init__(self):
        self.head = None
    
    def append(self, data):
        new_node = Node(data)
        if not self.head:
            self.head = new_node
            return
        last = self.head
        while last.next:
            last = last.next
        last.next = new_node
        new_node.prev = last
    
    def display_forward(self):
        current = self.head
        if not current:
            print("List is empty")
            return
        while current:
            print(current.data, end=" <-> ")
            current = current.next
        print("None")
    
    def display_backward(self):
        current = self.head
        if not current:
            print("List is empty")
            return
        while current.next:
            current = current.next
        while current:
            print(current.data, end=" <-> ")
            current = current.prev
        print("None")

if __name__ == "__main__":
    dll = DoublyLinkedList()
    
    for i in range(4):
        val = int(input(f"Enter value {i+1}: "))
        dll.append(val)
    
    print("Traversal in forward direction:")
    dll.display_forward()
    
    print("Traversal in backward direction:")
    dll.display_backward()


```
### Output:
![image](https://github.com/user-attachments/assets/5f5f7b16-b7fc-45fb-a98b-9c141cb89922)

### Result: Thus, the given program is implemented and executed successfully.
 


