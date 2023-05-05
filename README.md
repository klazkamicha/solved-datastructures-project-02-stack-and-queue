Download Link: https://assignmentchef.com/product/solved-datastructures-project-02-stack-and-queue
<br>
You are required to implement two data structures: a dynamic stack and a dynamic queue. You are also required to create UML diagrams for each of the classes that you implement. Finally, you have to provide the means to test your system by developing a menu program that allows the user to manipulate your structures.

<h1>Deliverables</h1>

<ul>

 <li>A 1 page pdf report with your UML diagrams and a brief explanation. Please include what each teammate did and approximate hours spent on the project.</li>

 <li>An implementation of a dynamic stack.</li>

 <li>An implementation of a dynamic queue.</li>

 <li>A menu program to test the implemented data structures.</li>

</ul>

<h1>1           Stack</h1>

In this part of the project, you need to implement one class, and create its respective UML diagram. Your functions must meet the required running times or no points will be granted.

<h2>1.1         Description</h2>

A stack stores elements in an ordered list and allows insertions and deletions at one end of the list in O(1) time.

The elements in this stack are stored in an array. The size of the array may be changed depending on the number of elements currently stored in the array, according to the following two rules:

If an element is being inserted into a stack where the array is already full, the size of the array is doubled. If, after removing an element from a stack

<em>1.2      Data Members</em>

where the number of elements is 1/4 the size of the array, then the size of the array is halved. The size of the array may not be reduced below the initially specified size.

<h2>1.2         Data Members</h2>

<ol>

 <li>A pointer to an instance of type, Type *array, to be used as an array.</li>

 <li>A counter, int count.</li>

 <li>The initial size of the array, int initialSize.</li>

 <li>The current size of the array, int arraySize.</li>

</ol>

<h2>1.3             Member Functions Constructors</h2>

<strong>DynStack( int n = 15 ) </strong>The constructor takes as an argument the initial size of the array and allocates memory for that array. The default number of entries is 15. If the argument is either 0 or a negative integer, set the initial capacity of the array to 1. Other class members are assigned as appropriate.

<strong>Destructor</strong>

∼<strong>DynStack() </strong>The destructor deletes the memory allocated for the array.

<h2>Accessors</h2>

<strong>Type top() const </strong>Returns the object at the top of the stack. It may throw a underflow exception. (O(1))

<strong>int size() const          </strong>Returns the number of elements currently stored in the

stack. (O(1))

<strong>bool empty() const           </strong>Returns true if the stack is empty, false otherwise.

(O(1)) <strong>int capacity() const </strong>Returns the current size of the array. (O(1)) <strong>void display() </strong>Prints the content of the stack. (O(n))

<h2>Mutators</h2>

<strong>void push( Type const &amp; data) </strong>Inserts the new element at the top of the stack. If the array is full, the size of the array is doubled. (O(1) on average)

<em>1.3      Member Functions</em>

<strong>Type pop() </strong>Removes the element at the top of the stack. If, after the element is removed, the array is 1/4 full and the array size is greater than the initial size, the size of the array is halved. This may throw a underflow exception. (O(1) on average)

<strong>void clear()           </strong>Removes all the elements in the stack. The array is resized

to the initial size. (O(1))

<strong>Friends</strong>

This class has no friends.

<h1>2           Queue</h1>

In this part of the project, you need to implement one class, and create its respective UML diagram. Your functions must meet the required running times or no points will be granted.

<h2>2.1         Description</h2>

A queue stores objects in an ordered list and allows insertions at one end and deletions from the other end of the list in O(1) time.

The objects in this queue are stored in an array. The capacity of the array may be changed depending on the number of objects currently stored in the array, according to the following two rules:

If an object is being inserted into a queue where the array is already full, the capacity of the array is doubled. If, after removing an object from a queue where the number of objects is one-quarter (1/4) the capacity of the array, then the capacity of the array is halved. The capacity of the array may not be reduced below the initially specified capacity.

<h2>2.2         Data Members</h2>

<ol>

 <li>A pointer to an instance of type, Type *array, to be used as an array.</li>

 <li>A head index, int iHead.</li>

 <li>A tail index, int iTail.</li>

 <li>A counter, int count.</li>

 <li>The initial size of the array, int initialSize.</li>

 <li>The current size of the array, int arraySize.</li>

</ol>

<h2>2.3             Member Functions Constructors</h2>

<strong>DynQueue( int n = 15 ) </strong>The constructor takes as an argument the initial capacity of the array and allocates memory for that array. If the argument is either 0 or a negative integer, set the initial capacity of the array to 1. The default initial capacity of the array is 15. Other member variables are assigned as appropriate.

<h2>Destructor</h2>

∼<strong>DynQueue() </strong>The destructor deletes the memory allocated for the array.

<em>2.3      Member Functions</em>

<h2>Accessors</h2>

<strong>Type front() const </strong>Returns the object at the front of the queue. It may throw a underflow exception. (O(1))

<strong>Type back() const </strong>Returns the object at the back of the queue. It may throw a underflow exception. (O(1))

<strong>int size() const          </strong>Returns the number of elements currently stored in the

queue. (O(1))

<strong>bool empty() const          </strong>Returns true if the queue is empty, false otherwise.

(O(1)) <strong>int capacity() const </strong>Returns the current size of the array. (O(1)) <strong>void display() </strong>Prints the content of the Queue. (O(n))

<h2>Mutators</h2>

<strong>void enqueue( Type const &amp; data) </strong>Insert the new element at the back of the queue. If the array is full, the size of the array is first doubled. (O(1) on average)

<strong>Type dequeue() </strong>Removes the element at the front of the queue. If, after the element is removed, the array is 1/4 full and the array size is greater than the initial size, the size of the array is halved. This may throw a underflow exception. (O(1) on average)

<strong>void clear()          </strong>Removes all the elements in the queue. The array is resized

to the initial size. (O(1))

<strong>Friends</strong>

This class has no friends.

<h1>3           The Menu Program</h1>

In order to test your program, you are required to implement a menu program that provides the means to run each of the functions in your classes. Please choose the <em>string </em>data type to create your Queue and Stack. So, when asked to create a Queue or a Stack, its array cells should hold string elements. The TA will choose one group to demo the project.

<h2>Format for the Menu Program</h2>

First, take a character, ’s’ or ’q’ (lowercase) that specifies whether we will be working with a stack or queue. Next, give the options (please have them in this <strong>EXACT </strong>order for grading purposes):

<ol>

 <li>Return Capacity (items actually in the data structure)</li>

 <li>Return Size of the data structure</li>

 <li>View first item (”top” for Stack, ”front” for Queue)</li>

 <li>Insert item (”push” for Stack, ”enqueue” for Queue)</li>

 <li>Delete item (”pop” for Stack, ”dequeue” for Queue)</li>

 <li>Display</li>

 <li>Clear</li>

 <li>Exit</li>

</ol>