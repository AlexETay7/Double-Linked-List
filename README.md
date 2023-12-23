# Double-Linked-List
****************
* Double Linked List
* University Assignment
* Date 11/1/2023
* Alex Taylor
**************** 

### ***OVERVIEW:***

In this program, I created a doubly-linked node-based implementation
of the IndexedUnsortedList interface. The created double-linked list
contains a fully functional Iterator that implements the 
ListIterator interface. A test suite is used to ensure the correct
functionality of the double-linked list. The test suite was given to 
me partially, but I wrote over 1500 lines of code in it by the end.


### ***INCLUDED FILES:***

 * IUDoubleLinkedList.java - A node-based doubly-linked implementation of the IndexedUnsortedList interface.
 * IndexedUnsortedList.java - Interface for an Iterable, Indexed, Unsorted List ADT. Implemented in IUDoubleLinkedList.java.
 * Node.java - A doubly-linked node class for linear data structures.
 * ListTester.java - A unit test class of black box tests for lists that implement IndexedUnsortedList.
 * README - A brief overview of the program, how to run and compile it, related concepts, and testing information.


### ***COMPILING AND RUNNING:***

 From the directory containing all source files, compile all
 java files with the command:
 <pre>
 $ javac *.java
 </pre>

 Run the compiled ListTester class file with the command:
 <pre>
 $ java ListTester.java
 </pre>

 The console output will give the results after the program finishes.


### ***PROGRAM DESIGN AND IMPORTANT CONCEPTS:***

 This program relies on the key concept of doubly-linked node-based lists.
 Essentially, each element in this list has a node reference. Each
 node has a pointer to the node behind it and in front of it.
 Each node also has a reference to an element in the list, and the
 element can be accessed through the node's methods, such as 
 a "getElement()" method. All logic for the doubly-linked 
 node-based list is done in the IUDoubleLinkedList.java file.

 We can update the elements in a list more efficiently 
 using a double-linked list by not having to shift elements in 
 the list each time we add or remove an element. This is done 
 by updating an elements corresponding node's "next node" and 
 "previous node" reference to the desired element's node.

 The pros behind a double-linked list is that four of its methods are O(n), and
 four methods are O(1). In contrast, a single linked list has 5 O(n) methods and
 3 O(1) methods. An array list has the same number of linear and constant time methods as a 
 single linked list. However, an arraylist's worst case is infinitely bad whilst an SLL and DLL 
 worst case remain under O(3n). With a single linked list, you can remove from the
 front in constant time, but not the end in constant time. With a double-linked list, 
 you can do both in constant time. Whilst a double-linked list may take (on average) 
 more memory than an ArrayList or single linked list, it makes up for it in the 
 efficiency of its removeLast() method.

 The IndexedUnsortedList interface is implemented in IUDoubleLinkedList.java
 because IUDoubleLinkedList.java is intended to provide a concrete implementation of 
 an indexed, unsorted list using a node-based double-linked list structure. 
 Node.java is the doubly-linked node data structure used in the double-linked list 
 to access elements via their nodes, set elements via their nodes, as well as to 
 allow elements to be inserted into a list without the list having to shift.


### ***TESTING:***

 I was able to test my implementation of a double-linked list by using 
 ListTester.java. ListTester is a series of black-box tests that work on any
 list that implements the IndexedUnsortedList interface. 
 I wrote 56 high-priority change scenarios where each method in IUDoubleLinkedList.java 
 is tested for an empty list, and a list with one, two, and three elements. It 
 should be noted that there are 82 possible scenarios for all methods and lists of 
 varying sizes (0-3 elements). However, I chose to only implement 56 because some 
 scenarios I realized were repetitive and did not need to be tested.

 *AS FAR AS I KNOW THERE ARE NO EXISTING BUGS*


### ***DISCUSSION:***
 
 During the method-writing phase of this project, the most frequent
 issue I had was probably when testing empty lists. At the beginning of
 my method writing, I did not handle empty lists correctly. However, I
 learned quickly and wrote out with pencil and paper the nodes and how the
 methods interacted with them. This helped me a lot and I really did not have 
 any issues after that when writing my methods for the double-linked list.

 The only other issue I came across was when implementing change scenarios, a couple of times I
 forgot to update the list in a change scenario, so I would be testing a 3-element
 change scenario with a 2-element list. I was able to recognize this quickly though
 and fix it. Other than that, I really did not have much trouble with this project. That
 may sound cocky, but Dr. Vails's (my professor) lectures were extremely helpful and I paid 
 really close attention, started early, and asked questions when I needed to. 

 I would say that what finally clicked for me at the end of the project was the test class.
 I was very intimidated and confused as to what was going on with a lot of the testers when
 I first saw it. Now though, I understand a lot more of what is going on inside the test class
 and how certain things interact with one another. I was excited to learn about test-driven development
 at the beginning of this class (even though it can be boring) and even though I am 
 still no where near an expert, I feel more confident in the idea of test-driven development.
