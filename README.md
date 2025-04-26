# 19CS301-Module11
### EX: 11.1 Singly Linked List (Traversal, Search and Delete)

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
class Node:
      def     init (self, data=None):
            self.data = data
            self.next = None


class SLinkedList:
       def      init (self):
             self.head = None

       def listprint(self):
             printval = self.head
             while printval is not None:
                    print(printval.data)
                    printval = printval.next

 list = SLinkedList()
list.head = Node("Mon")
e2 = Node("Tue")
e3 = Node("Wed")

# Link first Node to second node list.head.next = e2

# Link second Node to third node e2.next = e3

list.listprint()

```
### Output:
![image](https://github.com/user-attachments/assets/f7547c51-0a61-45c2-93da-48fbb60de473)


### Result: Thus, the given program is implemented and executed successfully .
 


### EX: 11.b Singly Linked List (Insertion and all operation)


### Aim: To Write a python program to add new element at the start of the list.


### Algorithm:

STEP 1: Start.

STEP 2: Create a node class and object of the node.

STEP 3: Create another class to use the node object.

STEP 4 : The new node is always added before the head of the given Linked List. And newly added node becomes the new head of the Linked List.

STEP 5 : Print the result.

STEP 6 : Stop.

### Program:
```
class Node:
            def     __init__ (self, data):
                  self.data = data
                  self.next = None

class LinkedList:
            def      __init__ (self):
                      self.head = None

            def push_front(self, newElement):
                    newnode = Node(newElement)
                    newnode.next=self.head
                    self.head = newnode
 
              def PrintList(self):
                     temp = self.head
                     if(temp != None):
           
                           print("The list contains:", end=" ")
                           while (temp != None):
                                print(temp.data, end=" ")
                                temp = temp.next
                                print()
                            else:
                                print("The list is empty.")


MyList = LinkedList()
MyList.push_front(10)
MyList.push_front(20)
MyList.push_front(30)
MyList.PrintList()
```
### Output:
![image](https://github.com/user-attachments/assets/4dae3c02-c85a-4294-9c03-294102d7fd9c)



### Result: Thus, the given program is implemented and executed successfully .
 


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
class Node:
          def    __ init__ (self, data):
               self.item = data
               self.nref = None
               self.pref = None

class DoublyLinkedList:
         def    __ init__ (self):
               self.start_node = None

          def insert_in_emptylist(self, data):
                 if self.start_node is None:
                    new_node = Node(data)
                    self.start_node = new_node
                  else:
                     print("list is not empty")


           def insert_at_start(self, data):
                   if self.start_node is None:
                           new_node = Node(data)
                           self.start_node = new_node
                            print("node inserted")
                            return
new_node = Node(data)
new_node.nref = self.start_node
self.start_node.pref = new_node
self.start_node = new_node

def insert_at_end(self, data):
          if self.start_node is None:
                new_node = Node(data)
                self.start_node = new_node return
           n = self.start_node
         while n.nref is not None:
                 n = n.nref
                 new_node = Node(data)
                 n.nref = new_node
                new_node.pref = n

def traverse_list(self):
         if self.start_node is None:
              print("List has no element")
              return
          else:
              n = self.start_node
         while n is not None:
                   print(n.item, " ")
                   n = n.nref
new_linked_list = DoublyLinkedList()
new_linked_list.insert_in_emptylist(50)
new_linked_list.insert_at_start(10)
new_linked_list.insert_at_start(5)
new_linked_list.insert_at_start(18)
new_linked_list.insert_at_end(29)
new_linked_list.insert_at_end(39)
new_linked_list.insert_at_end(49)
new_linked_list.traverse_list()
```
### Output:
![image](https://github.com/user-attachments/assets/151c84f1-3971-46a7-a040-bed7bde5df09)

### Result: Thus, the given program is implemented and executed successfully.
 


### EX: 11.4 Doubly Linked List (Insertion and all operation)


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
class Node:
         def     __init__(self, data):
                self.item = data
                self.nref = None
                 self.pref = None

class DoublyLinkedList:
                def      init (self):
                     self.start_node = None

                def insert_in_emptylist(self, data):
                    if self.start_node is None:
                             new_node = Node(data)
                             self.start_node = new_node
                    else:
 
                         print ("list is not empty")


                def insert_at_start(self, data):
                   if self.start_node is None:
                          new_node = Node(data)
                          self.start_node = new_node
                          print ("node inserted")
                          return
                    new_node = Node(data)
                    new_node.nref = self.start_node
                    self.start_node.pref = new_node
                   self.start_node = new_node

              def traverse_list(self):
                  if self.start_node is None:
                            print ("List has no element")
                            return
                   else:
                            n = self.start_node
                   while n is not None:
                              print (n.item , " ")
                              n = n.nref
 new_linked_list = DoublyLinkedList()
 new_linked_list.insert_in_emptylist(40)
new_linked_list.insert_at_start(30)
new_linked_list.insert_at_start(20)
new_linked_list.insert_at_start(10)
new_linked_list.traverse_list()
```
### Output:
 
![image](https://github.com/user-attachments/assets/c9883d28-638d-4f70-bc2d-f269a1606a45)

 

### Result: Thus, the given program is implemented and executed successfully.
