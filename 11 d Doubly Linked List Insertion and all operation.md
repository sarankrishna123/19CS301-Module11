### EX: 11.d Doubly Linked List (Insertion and all operation)


### Aim: To Type a python function to insert elements at the beginning of the doubly linked list.
### Algorithm:
STEP 1: Start.

STEP 2: Create a node class and object of the node.

STEP 3: Create another class to use the node object.

STEP 4: The new node is always added before the head of the given Linked List. And newly added node becomes the new head of the Linked List.

STEP 5: Print the data.

STEP 6: Stop.

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
    
    def insert_at_beginning(self, data):
        new_node = Node(data)
        if not self.head:
            self.head = new_node
            return
        new_node.next = self.head
        self.head.prev = new_node
        self.head = new_node
    
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
    
    print("Original list:")
    dll.display_forward()
    
    new_val = int(input("Enter value to insert at the beginning: "))
    dll.insert_at_beginning(new_val)
    
    print("List after inserting at the beginning:")
    dll.display_forward()

```
### Output:
 
![image](https://github.com/user-attachments/assets/ca5e14bd-e347-434a-a239-dd4a967ad6bf)

 

### Result: Thus, the given program is implemented and executed successfully.
