# 19CS301-Module11
### EX: 11 a Singly Linked List (Traversal, Search and Delete)

### Aim: Write a function to traverse the linked list and display it in the following format.

### Algorithm:

STEP 1: Start.

STEP 2: Create a node class and object of the node.

STEP 3: Create another class to use the node object.

STEP 4 : Using data traversing traverse from first to last data element .

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

class LinkedList:
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
    
    def display(self):
        current = self.head
        if not current:
            print("List is empty")
            return
        while current:
            if current.next:
                print(f"{current.data} ->", end=" ")
            else:
                print(f"{current.data} -> None", end="")
            current = current.next
        print()

if __name__ == "__main__":
    linked_list = LinkedList()
    
    for i in range(4):
        val = int(input(f"Enter value {i+1}: "))
        linked_list.append(val)
    
    linked_list.display()

       

```
### Output:
![image](https://github.com/user-attachments/assets/6981d2f7-cda7-47d2-b9e2-e1efbde7dc2c)


### Result: Thus, the given program is implemented and executed successfully .
 


