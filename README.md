<h1 id="cpp-like-js">CPP-LIKE-JS</h1>
<p>A versatile npm package designed for JavaScript developers familiar with C++.</p>
<p>Offering a STL-equivalent collection of data structures and utilities. </p>
<p>Simplify your development process by leveraging C++ like functionalities with C++&#39;s Syntactical Synonymosity directly in JavaScript, including vector, linked list, stack, queue, priority queues, deque, and more. </p>
<h2 id="installation">Installation</h2>
<p>Install cpp-like-js with npm</p>
<pre><code class="lang-bash">  npm <span class="hljs-selector-tag">i</span> cpp-like-js
</code></pre>
<h2 id="highlights">Highlights</h2>
<p>1.) Uses Exact Same C++ functions in JavaScript, easing the transition for C++ developers.</p>
<p>2.) Comprehensive Data Structures: V.1.0.0 includes rigorous implementations of vector, linked list, stack, queue, priority queues, deques and trees.</p>
<p>3.) Intuitive Input/Output: Utilize &#39;cin&#39; and &#39;cout&#39; for user input and output in JS.</p>
<p>4.) Enhanced Functionality: Supports advanced operations like emplace, insert, and swap across various data structures.</p>
<p>5.) Deep Copy Support: Easily clone data structures without reference issues using methods like clone_without_reference and copy_without_reference.</p>
<p>6.) Balanced and Optimized Trees: Provides tree structures with features like balanced check, height calculation, LCA (Lowest Common Ancestor) finding, diameter calculation and more.</p>
<p>7.) Robust Error Handling: Implements comprehensive error checking to ensure reliability and stability.</p>
<p>8.) Simple Integration: Designed for easy integration into existing JavaScript projects with minimal setup.</p>
<h2 id="usage-1-console-utilities">Usage 1.) CONSOLE UTILITIES</h2>
<pre><code><span class="hljs-keyword">REQUIRE</span>:-

<span class="hljs-keyword">const</span> cout = <span class="hljs-keyword">require</span>(<span class="hljs-string">'cpp-like-js'</span>).cout;

cout(<span class="hljs-number">6</span>+<span class="hljs-number">7</span>+<span class="hljs-number">8</span>); <span class="hljs-comment">//21</span>
</code></pre><p>Using &#39;cout&#39; instead of &#39;console.log&#39; for user output.</p>
<pre><code><span class="hljs-keyword">const</span> cout = <span class="hljs-built_in">require</span>(<span class="hljs-string">'cpp-like-js'</span>).cout;
<span class="hljs-keyword">const</span> cin = <span class="hljs-built_in">require</span>(<span class="hljs-string">'cpp-like-js'</span>).cin;

cout(<span class="hljs-string">"Enter the value of num: "</span>);
<span class="hljs-keyword">const</span> num = cin ();
</code></pre><p>Using just &#39;cin&#39; instead of 
&#39;readLine(prompt): Reads a string value from a user
readInt(prompt): Reads an integer value from a user
readFloat(prompt): Reads a float value from a user&#39; for user input.</p>
<h2 id="usage-2-vector">Usage 2.) Vector</h2>
<p>The Vector class provides a dynamic array implementation, similar to the std::vector in C++. It supports a wide range of operations for managing elements.</p>
<pre><code>   <span class="hljs-keyword">REQUIRE</span>:-

   <span class="hljs-keyword">const</span> <span class="hljs-comment">{Vector}</span> = <span class="hljs-keyword">require</span>(<span class="hljs-string">'cpp-like-js'</span>);

   <span class="hljs-keyword">const</span> vec = <span class="hljs-keyword">new</span> Vector(); <span class="hljs-comment">//instance of Vector class</span>
</code></pre><p>Constructor</p>
<p>Vector(): Initializes an empty vector.</p>
<p>Methods:-</p>
<p>size(): Returns the number of elements in the vector.</p>
<pre><code><span class="hljs-keyword">let</span> v = <span class="hljs-keyword">new</span> Vector();
v.push_back(<span class="hljs-number">10</span>);
cout(v.size()); <span class="hljs-comment">// Output: 1</span>
<span class="hljs-keyword">empty</span>(): Returns <span class="hljs-keyword">true</span>,
<span class="hljs-keyword">if</span> the vector is <span class="hljs-keyword">empty</span>, otherwise <span class="hljs-keyword">false</span>.
<span class="hljs-keyword">let</span> v = <span class="hljs-keyword">new</span> Vector();
cout(v.<span class="hljs-keyword">empty</span>()); <span class="hljs-comment">// Output: true</span>
</code></pre><p>push_back(val): Adds an element to the end of the vector.</p>
<pre><code><span class="hljs-keyword">let</span> v = <span class="hljs-function"><span class="hljs-keyword">new</span> <span class="hljs-title">Vector</span>();
<span class="hljs-title">v</span>.<span class="hljs-title">push_back</span>(<span class="hljs-number">10</span>);</span>
</code></pre><p>pop_back(): Removes the last element from the vector. Throws an error if the vector is empty.</p>
<pre><code><span class="hljs-keyword">let</span> v = <span class="hljs-function"><span class="hljs-keyword">new</span> <span class="hljs-title">Vector</span>();
<span class="hljs-title">v</span>.<span class="hljs-title">push_back</span>(<span class="hljs-number">10</span>);
<span class="hljs-title">v</span>.<span class="hljs-title">pop_back</span>();</span>
</code></pre><p>insert(index, val): Inserts an element at the specified index. Throws an error if the index is out of range.</p>
<pre><code><span class="hljs-keyword">let</span> v = <span class="hljs-function"><span class="hljs-keyword">new</span> <span class="hljs-title">Vector</span>();
<span class="hljs-title">v</span>.<span class="hljs-title">push_back</span>(<span class="hljs-number">10</span>);
<span class="hljs-title">v</span>.<span class="hljs-title">insert</span>(<span class="hljs-number">0</span>, <span class="hljs-number">5</span>);</span>
</code></pre><p>erase(index): Removes the element at the specified index. Throws an error if the index is out of range.</p>
<pre><code><span class="hljs-keyword">let</span> v = <span class="hljs-function"><span class="hljs-keyword">new</span> <span class="hljs-title">Vector</span>();
<span class="hljs-title">v</span>.<span class="hljs-title">push_back</span>(<span class="hljs-number">10</span>);
<span class="hljs-title">v</span>.<span class="hljs-title">erase</span>(<span class="hljs-number">0</span>);</span>
</code></pre><p>clear(): Removes all elements from the vector.</p>
<pre><code><span class="hljs-keyword">let</span> v = <span class="hljs-function"><span class="hljs-keyword">new</span> <span class="hljs-title">Vector</span>();
<span class="hljs-title">v</span>.<span class="hljs-title">push_back</span>(<span class="hljs-number">10</span>);
<span class="hljs-title">v</span>.<span class="hljs-title">clear</span>();</span>
</code></pre><p>resize(n, val = undefined): Resizes the vector to contain n elements. If n is greater than the current size, the vector is expanded with val.</p>
<pre><code><span class="hljs-keyword">let</span> v = <span class="hljs-function"><span class="hljs-keyword">new</span> <span class="hljs-title">Vector</span>();
<span class="hljs-title">v</span>.<span class="hljs-title">push_back</span>(<span class="hljs-number">10</span>);
<span class="hljs-title">v</span>.<span class="hljs-title">resize</span>(<span class="hljs-number">5</span>, <span class="hljs-number">0</span>);</span>
</code></pre><p>front(): Returns the first element of the vector. Throws an error if the vector is empty.</p>
<pre><code><span class="hljs-keyword">let</span> v = <span class="hljs-function"><span class="hljs-keyword">new</span> <span class="hljs-title">Vector</span>();
<span class="hljs-title">v</span>.<span class="hljs-title">push_back</span>(<span class="hljs-number">10</span>);
<span class="hljs-title">cout</span>(v.front()); <span class="hljs-comment">// Output: 10</span></span>
</code></pre><p>back(): Returns the last element of the vector. Throws an error if the vector is empty.</p>
<pre><code><span class="hljs-keyword">let</span> v = <span class="hljs-function"><span class="hljs-keyword">new</span> <span class="hljs-title">Vector</span>();
<span class="hljs-title">v</span>.<span class="hljs-title">push_back</span>(<span class="hljs-number">10</span>);
<span class="hljs-title">cout</span>(v.back()); <span class="hljs-comment">// Output: 10</span></span>
</code></pre><p>at(index): Returns the element at the specified index. Throws an error if the index is out of range.</p>
<pre><code><span class="hljs-keyword">let</span> v = <span class="hljs-function"><span class="hljs-keyword">new</span> <span class="hljs-title">Vector</span>();
<span class="hljs-title">v</span>.<span class="hljs-title">push_back</span>(<span class="hljs-number">10</span>);
<span class="hljs-title">cout</span>(v.at(<span class="hljs-number">0</span>)); <span class="hljs-comment">// Output: 10</span></span>
</code></pre><p>swap(other): Swaps the contents of the vector with another vector. Throws an error if the argument is not a vector.</p>
<pre><code>let v1 =<span class="hljs-built_in"> new </span>Vector();
let v2 =<span class="hljs-built_in"> new </span>Vector();
v1.push_back(10);
v2.push_back(20);
v1.swap(v2);
</code></pre><p>assign(n, val): Assigns n elements with the specified value to the vector. Throws an error if n is negative.</p>
<pre><code><span class="hljs-keyword">let</span> v = <span class="hljs-function"><span class="hljs-keyword">new</span> <span class="hljs-title">Vector</span>();
<span class="hljs-title">v</span>.<span class="hljs-title">assign</span>(<span class="hljs-number">5</span>, <span class="hljs-number">10</span>);</span>
</code></pre><p>assign_range(arr): Assigns elements from an array to the vector. Throws an error if the argument is not an array.</p>
<pre><code><span class="hljs-keyword">let</span> v = <span class="hljs-function"><span class="hljs-keyword">new</span> <span class="hljs-title">Vector</span>();
<span class="hljs-title">v</span>.<span class="hljs-title">assign_range</span>([<span class="hljs-number">1</span>, <span class="hljs-number">2</span>, <span class="hljs-number">3</span>]);</span>
</code></pre><p>sort(): Sorts the elements of the vector in ascending order.</p>
<pre><code><span class="hljs-keyword">let</span> v = <span class="hljs-function"><span class="hljs-keyword">new</span> <span class="hljs-title">Vector</span>(); 
<span class="hljs-title">v</span>.<span class="hljs-title">sort</span>();</span>
</code></pre><p>reverse(): Reverses the order of the elements in the vector.</p>
<pre><code><span class="hljs-keyword">let</span> v = <span class="hljs-function"><span class="hljs-keyword">new</span> <span class="hljs-title">Vector</span>();
<span class="hljs-title">v</span>.<span class="hljs-title">reverse</span>();</span>
</code></pre><p>copy_without_reference(): Returns a copy of the vector without reference to the original.</p>
<pre><code>let <span class="hljs-built_in">v1</span> = new Vector()<span class="hljs-comment">;</span>
<span class="hljs-built_in">v1</span>.push_back(<span class="hljs-number">10</span>)<span class="hljs-comment">;</span>
let v2 = <span class="hljs-built_in">v1</span>.copy_without_reference()<span class="hljs-comment">;</span>
</code></pre><p>##IMPORTANT NOTE:</p>
<p>In C++, assigning one vector to another results in a copy of the elements from one vector to the other.</p>
<p>In JavaScript, objects are typically assigned by reference. </p>
<p>When you assign one vector (or any object) to another using &#39;=&#39; or by passing references, both variables will reference the same underlying object. </p>
<p>This means changes made to one variable will affect the other because they share the same reference. </p>
<p>So, copy_without_reference() function helps to copy by data which is very helpful.</p>
<p>equals(other): Returns true if the vector is equal to another vector. Throws an error if the argument is not a vector.</p>
<pre><code>let <span class="hljs-built_in">v1</span> = new Vector()<span class="hljs-comment">;</span>
let v2 = new Vector()<span class="hljs-comment">;</span>
<span class="hljs-built_in">v1</span>.push_back(<span class="hljs-number">10</span>)<span class="hljs-comment">;</span>
v2.push_back(<span class="hljs-number">10</span>)<span class="hljs-comment">;</span>
cout(<span class="hljs-built_in">v1</span>.equals(v2))<span class="hljs-comment">; // Output: true</span>
</code></pre><p>print(): Prints the elements of the vector.</p>
<pre><code><span class="hljs-keyword">let</span> v = <span class="hljs-function"><span class="hljs-keyword">new</span> <span class="hljs-title">Vector</span>();
<span class="hljs-title">v</span>.<span class="hljs-title">push_back</span>(<span class="hljs-number">10</span>);
<span class="hljs-title">v</span>.<span class="hljs-title">print</span>(); <span class="hljs-comment">// Output: 10</span></span>
</code></pre><h2 id="usage-3-linked-lists">Usage 3.) Linked Lists</h2>
<p>The LinkedList class provides a singly linked list implementation with various utility methods for managing elements.</p>
<pre><code>   <span class="hljs-keyword">REQUIRE</span>:-

   <span class="hljs-keyword">const</span> <span class="hljs-comment">{LinkedList}</span> = <span class="hljs-keyword">require</span>(<span class="hljs-string">'cpp-like-js'</span>);

   <span class="hljs-keyword">const</span> ll = <span class="hljs-keyword">new</span> LinkedList(); <span class="hljs-comment">//instance of LinkedList class</span>
</code></pre><p>Constructor:-</p>
<p>LinkedList(): Initializes an empty linked list.</p>
<p>Methods:-</p>
<p>push_back(data): Adds an element to the end of the linked list.</p>
<pre><code><span class="hljs-keyword">let</span> <span class="hljs-built_in">list</span> = <span class="hljs-literal">new</span> LinkedList();
<span class="hljs-built_in">list</span>.push_back(<span class="hljs-number">10</span>);
</code></pre><p>push_front(data): Adds an element to the front of the linked list.</p>
<pre><code><span class="hljs-keyword">let</span> <span class="hljs-built_in">list</span> = <span class="hljs-literal">new</span> LinkedList();
<span class="hljs-built_in">list</span>.push_front(<span class="hljs-number">10</span>);
</code></pre><p>pop_front(): Removes the first element from the linked list.</p>
<pre><code><span class="hljs-keyword">let</span> <span class="hljs-built_in">list</span> = <span class="hljs-literal">new</span> LinkedList();
<span class="hljs-built_in">list</span>.push_back(<span class="hljs-number">10</span>);
<span class="hljs-built_in">list</span>.pop_front();
</code></pre><p>pop_back(): Removes the last element from the linked list.</p>
<pre><code><span class="hljs-keyword">let</span> <span class="hljs-built_in">list</span> = <span class="hljs-literal">new</span> LinkedList();
<span class="hljs-built_in">list</span>.push_back(<span class="hljs-number">10</span>);
<span class="hljs-built_in">list</span>.pop_back();
</code></pre><p>front(): Returns the first element of the linked list.</p>
<pre><code>let <span class="hljs-built_in">list</span> = <span class="hljs-keyword">new</span> LinkedList();
<span class="hljs-built_in">list</span>.push_back(<span class="hljs-number">10</span>);
<span class="hljs-built_in">cout</span>(<span class="hljs-built_in">list</span>.front()); <span class="hljs-comment">// Output: 10</span>
</code></pre><p>back(): Returns the last element of the linked list.</p>
<pre><code>let <span class="hljs-built_in">list</span> = <span class="hljs-keyword">new</span> LinkedList();
<span class="hljs-built_in">list</span>.push_back(<span class="hljs-number">10</span>);
<span class="hljs-built_in">cout</span>(<span class="hljs-built_in">list</span>.back()); <span class="hljs-comment">// Output: 10</span>
</code></pre><p>empty(): Returns true if the linked list is empty, otherwise false.</p>
<pre><code><span class="hljs-keyword">let</span> <span class="hljs-keyword">list</span> = <span class="hljs-keyword">new</span> LinkedList();
cout(<span class="hljs-keyword">list</span>.<span class="hljs-keyword">empty</span>()); <span class="hljs-comment">// Output: true</span>
</code></pre><p>size(): Returns the number of elements in the linked list.</p>
<pre><code>let <span class="hljs-built_in">list</span> = <span class="hljs-keyword">new</span> LinkedList();
<span class="hljs-built_in">list</span>.push_back(<span class="hljs-number">10</span>);
<span class="hljs-built_in">cout</span>(<span class="hljs-built_in">list</span>.size()); <span class="hljs-comment">// Output: 1</span>
</code></pre><p>clear(): Removes all elements from the linked list.</p>
<pre><code><span class="hljs-keyword">let</span> <span class="hljs-built_in">list</span> = <span class="hljs-literal">new</span> LinkedList();
<span class="hljs-built_in">list</span>.push_back(<span class="hljs-number">10</span>);
<span class="hljs-built_in">list</span>.clear();
</code></pre><p>print(): Prints all elements of the linked list.</p>
<pre><code><span class="hljs-keyword">let</span> <span class="hljs-keyword">list</span> = <span class="hljs-keyword">new</span> LinkedList();
<span class="hljs-keyword">list</span>.push_back(<span class="hljs-number">10</span>);
<span class="hljs-keyword">list</span>.<span class="hljs-keyword">print</span>(); <span class="hljs-comment">// Output: 10</span>
</code></pre><p>insertAt(position, data): Inserts an element at the specified position. Throws an error if the position is invalid.</p>
<pre><code>let <span class="hljs-type">list</span> = new LinkedList();
<span class="hljs-type">list</span>.push_back(<span class="hljs-number">10</span>);
<span class="hljs-type">list</span>.insertAt(<span class="hljs-number">0</span>, <span class="hljs-number">5</span>);
</code></pre><p>deleteAt(position): Removes the element at the specified position. Throws an error if the position is invalid.</p>
<pre><code><span class="hljs-keyword">let</span> <span class="hljs-built_in">list</span> = <span class="hljs-literal">new</span> LinkedList();
<span class="hljs-built_in">list</span>.push_back(<span class="hljs-number">10</span>);
<span class="hljs-built_in">list</span>.deleteAt(<span class="hljs-number">0</span>);
</code></pre><p>reverse(): Reverses the linked list.</p>
<pre><code><span class="hljs-keyword">let</span> <span class="hljs-built_in">list</span> = <span class="hljs-literal">new</span> LinkedList();
<span class="hljs-built_in">list</span>.push_back(<span class="hljs-number">10</span>);
<span class="hljs-built_in">list</span>.reverse();
</code></pre><p>findMiddle(): Returns the middle element of the linked list.</p>
<pre><code>let <span class="hljs-built_in">list</span> = <span class="hljs-keyword">new</span> LinkedList();
<span class="hljs-built_in">list</span>.push_back(<span class="hljs-number">10</span>);
<span class="hljs-built_in">cout</span>(<span class="hljs-built_in">list</span>.findMiddle()); <span class="hljs-comment">// Output: 10</span>
</code></pre><p>merge(otherList): Merges the linked list with another sorted linked list.</p>
<pre><code><span class="hljs-keyword">let</span> list1 = <span class="hljs-function"><span class="hljs-keyword">new</span> <span class="hljs-title">LinkedList</span>();
<span class="hljs-title">let</span> <span class="hljs-title">list2</span> = <span class="hljs-title">new</span> <span class="hljs-title">LinkedList</span>();
<span class="hljs-title">list1</span>.<span class="hljs-title">push_back</span>(<span class="hljs-number">1</span>);
<span class="hljs-title">list2</span>.<span class="hljs-title">push_back</span>(<span class="hljs-number">2</span>);
<span class="hljs-title">let</span> <span class="hljs-title">mergedList</span> = <span class="hljs-title">list1</span>.<span class="hljs-title">merge</span>(list2);</span>
</code></pre><p>detectCycle(): Returns true if the linked list contains a cycle, otherwise false.</p>
<pre><code>let <span class="hljs-built_in">list</span> = <span class="hljs-keyword">new</span> LinkedList();
<span class="hljs-built_in">cout</span>(<span class="hljs-built_in">list</span>.detectCycle()); <span class="hljs-comment">// Output: false</span>
</code></pre><p>removeDuplicates(): Removes duplicate elements from the linked list.</p>
<pre><code><span class="hljs-keyword">let</span> <span class="hljs-built_in">list</span> = <span class="hljs-literal">new</span> LinkedList();
<span class="hljs-built_in">list</span>.push_back(<span class="hljs-number">10</span>);
<span class="hljs-built_in">list</span>.push_back(<span class="hljs-number">10</span>);
<span class="hljs-built_in">list</span>.removeDuplicates();
</code></pre><p>sort(): Sorts the elements of the linked list.</p>
<pre><code><span class="hljs-keyword">let</span> <span class="hljs-built_in">list</span> = <span class="hljs-literal">new</span> LinkedList();
<span class="hljs-built_in">list</span>.push_back(<span class="hljs-number">2</span>);
<span class="hljs-built_in">list</span>.push_back(<span class="hljs-number">1</span>);
<span class="hljs-built_in">list</span>.sort();
</code></pre><p>split(): Splits the linked list into two halves and returns them as an array.</p>
<pre><code><span class="hljs-keyword">let</span> <span class="hljs-built_in">list</span> = <span class="hljs-keyword">new</span> <span class="hljs-type">LinkedList</span><span class="hljs-literal">()</span>;
<span class="hljs-built_in">list</span>.push_back(<span class="hljs-number">10</span>);
<span class="hljs-keyword">let</span> [firstHalf, secondHalf] = <span class="hljs-built_in">list</span>.split<span class="hljs-literal">()</span>;
</code></pre><p>findIntersection(otherList): Finds the intersection node of two linked lists.</p>
<pre><code><span class="hljs-keyword">let</span> list1 = <span class="hljs-function"><span class="hljs-keyword">new</span> <span class="hljs-title">LinkedList</span>();
<span class="hljs-title">let</span> <span class="hljs-title">list2</span> = <span class="hljs-title">new</span> <span class="hljs-title">LinkedList</span>();
<span class="hljs-title">list1</span>.<span class="hljs-title">push_back</span>(<span class="hljs-number">10</span>);
<span class="hljs-title">list2</span>.<span class="hljs-title">push_back</span>(<span class="hljs-number">10</span>);
<span class="hljs-title">cout</span>(list1.findIntersection(list2)); <span class="hljs-comment">// Output: 10</span></span>
</code></pre><p>toArray(): Converts the linked list to an array.</p>
<pre><code>let <span class="hljs-built_in">list</span> = <span class="hljs-keyword">new</span> LinkedList();
<span class="hljs-built_in">list</span>.push_back(<span class="hljs-number">10</span>);
<span class="hljs-built_in">cout</span>(<span class="hljs-built_in">list</span>.toArray()); <span class="hljs-comment">// Output: [10]</span>
</code></pre><p>copy_without_reference(): Returns a copy of the linked list without reference to the original.</p>
<pre><code><span class="hljs-keyword">let</span> list1 = <span class="hljs-function"><span class="hljs-keyword">new</span> <span class="hljs-title">LinkedList</span>();
<span class="hljs-title">list1</span>.<span class="hljs-title">push_back</span>(<span class="hljs-number">10</span>);
<span class="hljs-title">let</span> <span class="hljs-title">list2</span> = <span class="hljs-title">list1</span>.<span class="hljs-title">copy_without_reference</span>();</span>
</code></pre><h2 id="usage-4-stacks">Usage 4.) Stacks</h2>
<p>The Stack class provides a stack implementation with various utility methods for managing elements.</p>
<pre><code>    <span class="hljs-keyword">REQUIRE</span>:-

    const {<span class="hljs-built_in">Stack</span>} = <span class="hljs-keyword">require</span>(<span class="hljs-string">'cpp-like-js'</span>);

    const st = <span class="hljs-literal">new</span> <span class="hljs-built_in">Stack</span>(); <span class="hljs-comment">//instance of Stack</span>
</code></pre><p>Constructor:-</p>
<p>Stack(): Initializes an empty stack.</p>
<p>Methods:-</p>
<p>push(element): Adds an element to the top of the stack.</p>
<pre><code><span class="hljs-keyword">let</span> <span class="hljs-built_in">stack</span> = <span class="hljs-literal">new</span> <span class="hljs-built_in">Stack</span>();
<span class="hljs-built_in">stack</span>.push(<span class="hljs-number">10</span>);
</code></pre><p>pop(): Removes and returns the top element of the stack. Throws an error if the stack is empty.</p>
<pre><code><span class="hljs-keyword">let</span> <span class="hljs-built_in">stack</span> = <span class="hljs-literal">new</span> <span class="hljs-built_in">Stack</span>();
<span class="hljs-built_in">stack</span>.push(<span class="hljs-number">10</span>);
cout(<span class="hljs-built_in">stack</span>.pop()); <span class="hljs-comment">// Output: 10</span>
</code></pre><p>top(): Returns the top element of the stack without removing it. Throws an error if the stack is empty.</p>
<pre><code><span class="hljs-keyword">let</span> <span class="hljs-built_in">stack</span> = <span class="hljs-literal">new</span> <span class="hljs-built_in">Stack</span>();
<span class="hljs-built_in">stack</span>.push(<span class="hljs-number">10</span>);
cout(<span class="hljs-built_in">stack</span>.top()); <span class="hljs-comment">// Output: 10</span>
</code></pre><p>isEmpty(): Returns true if the stack is empty, otherwise false.</p>
<pre><code><span class="hljs-keyword">let</span> <span class="hljs-built_in">stack</span> = <span class="hljs-literal">new</span> <span class="hljs-built_in">Stack</span>();
cout(<span class="hljs-built_in">stack</span>.isEmpty()); <span class="hljs-comment">// Output: true</span>
</code></pre><p>size(): Returns the number of elements in the stack.</p>
<pre><code><span class="hljs-keyword">let</span> <span class="hljs-built_in">stack</span> = <span class="hljs-literal">new</span> <span class="hljs-built_in">Stack</span>();
<span class="hljs-built_in">stack</span>.push(<span class="hljs-number">10</span>);
cout(<span class="hljs-built_in">stack</span>.size()); <span class="hljs-comment">// Output: 1</span>
</code></pre><p>clear(): Removes all elements from the stack.</p>
<pre><code><span class="hljs-keyword">let</span> <span class="hljs-built_in">stack</span> = <span class="hljs-literal">new</span> <span class="hljs-built_in">Stack</span>();
<span class="hljs-built_in">stack</span>.push(<span class="hljs-number">10</span>);
<span class="hljs-built_in">stack</span>.clear();
</code></pre><p>get(index): Returns the element at the specified index. Throws an error if the index is out of bounds.</p>
<pre><code><span class="hljs-keyword">let</span> <span class="hljs-built_in">stack</span> = <span class="hljs-literal">new</span> <span class="hljs-built_in">Stack</span>();
<span class="hljs-built_in">stack</span>.push(<span class="hljs-number">10</span>);
cout(<span class="hljs-built_in">stack</span>.get(<span class="hljs-number">0</span>)); <span class="hljs-comment">// Output: 10</span>
</code></pre><p>contains(element): Returns true if the stack contains the specified element, otherwise false.</p>
<pre><code><span class="hljs-keyword">let</span> <span class="hljs-built_in">stack</span> = <span class="hljs-literal">new</span> <span class="hljs-built_in">Stack</span>();
<span class="hljs-built_in">stack</span>.push(<span class="hljs-number">10</span>);
cout(<span class="hljs-built_in">stack</span>.contains(<span class="hljs-number">10</span>)); <span class="hljs-comment">// Output: true</span>
</code></pre><p>toArray(): Converts the stack to an array.</p>
<pre><code><span class="hljs-keyword">let</span> <span class="hljs-built_in">stack</span> = <span class="hljs-literal">new</span> <span class="hljs-built_in">Stack</span>();
<span class="hljs-built_in">stack</span>.push(<span class="hljs-number">10</span>);
cout.<span class="hljs-keyword">log</span>(<span class="hljs-built_in">stack</span>.toArray()); <span class="hljs-comment">// Output: [10]</span>
</code></pre><p>swap(stack): Swaps the elements of the current stack with another stack.</p>
<pre><code><span class="hljs-keyword">let</span> stack1 = <span class="hljs-function"><span class="hljs-keyword">new</span> <span class="hljs-title">Stack</span>();
<span class="hljs-title">let</span> <span class="hljs-title">stack2</span> = <span class="hljs-title">new</span> <span class="hljs-title">Stack</span>();
<span class="hljs-title">stack1</span>.<span class="hljs-title">push</span>(<span class="hljs-number">10</span>);
<span class="hljs-title">stack2</span>.<span class="hljs-title">push</span>(<span class="hljs-number">20</span>);
<span class="hljs-title">stack1</span>.<span class="hljs-title">swap</span>(stack2);</span>
</code></pre><p>emplace(element): Adds an element to the top of the stack.</p>
<pre><code><span class="hljs-keyword">let</span> <span class="hljs-built_in">stack</span> = <span class="hljs-literal">new</span> <span class="hljs-built_in">Stack</span>();
<span class="hljs-built_in">stack</span>.emplace(<span class="hljs-number">10</span>);
</code></pre><p>emplace_back(...args): Adds multiple elements to the top of the stack.</p>
<pre><code><span class="hljs-keyword">let</span> <span class="hljs-built_in">stack</span> = <span class="hljs-literal">new</span> <span class="hljs-built_in">Stack</span>();
<span class="hljs-built_in">stack</span>.emplace_back(<span class="hljs-number">10</span>, <span class="hljs-number">20</span>, <span class="hljs-number">30</span>);
</code></pre><p>reserve(capacity): Sets the length of the stack to the specified capacity.</p>
<pre><code><span class="hljs-keyword">let</span> <span class="hljs-built_in">stack</span> = <span class="hljs-literal">new</span> <span class="hljs-built_in">Stack</span>();
<span class="hljs-built_in">stack</span>.reserve(<span class="hljs-number">10</span>);
</code></pre><p>erase(position): Removes the element at the specified position. Throws an error if the position is out of bounds.</p>
<pre><code><span class="hljs-keyword">let</span> <span class="hljs-built_in">stack</span> = <span class="hljs-literal">new</span> <span class="hljs-built_in">Stack</span>();
<span class="hljs-built_in">stack</span>.push(<span class="hljs-number">10</span>);
<span class="hljs-built_in">stack</span>.erase(<span class="hljs-number">0</span>);
</code></pre><p>copy_without_reference(): Returns a copy of the stack without reference to the original.</p>
<pre><code><span class="hljs-keyword">let</span> stack1 = <span class="hljs-literal">new</span> <span class="hljs-built_in">Stack</span>();
stack1.push(<span class="hljs-number">10</span>);

<span class="hljs-keyword">let</span> stack2 = stack1.copy_without_reference();
print(): Prints <span class="hljs-literal">all</span> elements of the <span class="hljs-built_in">stack</span>.

<span class="hljs-keyword">let</span> <span class="hljs-built_in">stack</span> = <span class="hljs-literal">new</span> <span class="hljs-built_in">Stack</span>();
<span class="hljs-built_in">stack</span>.push(<span class="hljs-number">10</span>);

<span class="hljs-built_in">stack</span>.print(); <span class="hljs-comment">// Output: 10</span>
</code></pre><h2 id="usage-5-queue">Usage 5.) Queue</h2>
<p>The Queue class provides a queue implementation with various utility methods for managing elements.</p>
<pre><code>    <span class="hljs-keyword">REQUIRE</span>:-

    const {<span class="hljs-built_in">Queue</span>} = <span class="hljs-keyword">require</span>(<span class="hljs-string">'cpp-like-js'</span>);

    const q = <span class="hljs-literal">new</span> <span class="hljs-built_in">Queue</span>(); <span class="hljs-comment">//instance of Queue</span>
</code></pre><p>Constructor:-</p>
<p>Queue(): Initializes an empty queue.</p>
<p>Methods:-</p>
<p>push(element): Adds an element to the back of the queue.</p>
<pre><code><span class="hljs-keyword">let</span> <span class="hljs-built_in">queue</span> = <span class="hljs-literal">new</span> <span class="hljs-built_in">Queue</span>();
<span class="hljs-built_in">queue</span>.push(<span class="hljs-number">10</span>);
</code></pre><p>pop(): Removes and returns the front element of the queue. Throws an error if the queue is empty.</p>
<pre><code><span class="hljs-keyword">let</span> <span class="hljs-built_in">queue</span> = <span class="hljs-literal">new</span> <span class="hljs-built_in">Queue</span>();
<span class="hljs-built_in">queue</span>.push(<span class="hljs-number">10</span>);
cout(<span class="hljs-built_in">queue</span>.pop()); <span class="hljs-comment">// Output: 10</span>
</code></pre><p>front(): Returns the front element of the queue without removing it. Throws an error if the queue is empty.</p>
<pre><code><span class="hljs-keyword">let</span> <span class="hljs-built_in">queue</span> = <span class="hljs-literal">new</span> <span class="hljs-built_in">Queue</span>();
<span class="hljs-built_in">queue</span>.push(<span class="hljs-number">10</span>);
cout(<span class="hljs-built_in">queue</span>.front()); <span class="hljs-comment">// Output: 10</span>
</code></pre><p>back(): Returns the back element of the queue without removing it. Throws an error if the queue is empty.</p>
<pre><code><span class="hljs-keyword">let</span> <span class="hljs-built_in">queue</span> = <span class="hljs-literal">new</span> <span class="hljs-built_in">Queue</span>();
<span class="hljs-built_in">queue</span>.push(<span class="hljs-number">10</span>);
cout(<span class="hljs-built_in">queue</span>.back()); <span class="hljs-comment">// Output: 10</span>
</code></pre><p>size(): Returns the number of elements in the queue.</p>
<pre><code><span class="hljs-keyword">let</span> <span class="hljs-built_in">queue</span> = <span class="hljs-literal">new</span> <span class="hljs-built_in">Queue</span>();
<span class="hljs-built_in">queue</span>.push(<span class="hljs-number">10</span>);
cout(<span class="hljs-built_in">queue</span>.size()); <span class="hljs-comment">// Output: 1</span>
</code></pre><p>empty(): Returns true if the queue is empty, otherwise false.</p>
<pre><code><span class="hljs-keyword">let</span> <span class="hljs-built_in">queue</span> = <span class="hljs-literal">new</span> <span class="hljs-built_in">Queue</span>();
cout(<span class="hljs-built_in">queue</span>.empty()); <span class="hljs-comment">// Output: true</span>
</code></pre><p>clear(): Removes all elements from the queue.</p>
<pre><code><span class="hljs-keyword">let</span> <span class="hljs-built_in">queue</span> = <span class="hljs-literal">new</span> <span class="hljs-built_in">Queue</span>();
<span class="hljs-built_in">queue</span>.push(<span class="hljs-number">10</span>);
<span class="hljs-built_in">queue</span>.clear();
</code></pre><p>emplace(...args): Adds multiple elements to the back of the queue.</p>
<pre><code><span class="hljs-keyword">let</span> <span class="hljs-built_in">queue</span> = <span class="hljs-literal">new</span> <span class="hljs-built_in">Queue</span>();
<span class="hljs-built_in">queue</span>.emplace(<span class="hljs-number">10</span>, <span class="hljs-number">20</span>, <span class="hljs-number">30</span>);
</code></pre><p>swap(otherQueue): Swaps the elements of the current queue with another queue.</p>
<pre><code><span class="hljs-keyword">let</span> queue1 = <span class="hljs-function"><span class="hljs-keyword">new</span> <span class="hljs-title">Queue</span>();
<span class="hljs-title">let</span> <span class="hljs-title">queue2</span> = <span class="hljs-title">new</span> <span class="hljs-title">Queue</span>();
<span class="hljs-title">queue1</span>.<span class="hljs-title">push</span>(<span class="hljs-number">10</span>);
<span class="hljs-title">queue2</span>.<span class="hljs-title">push</span>(<span class="hljs-number">20</span>);
<span class="hljs-title">queue1</span>.<span class="hljs-title">swap</span>(queue2);</span>
</code></pre><p>copy_without_reference(otherQueue): Copies the elements of another queue to the current queue without reference.</p>
<pre><code><span class="hljs-keyword">let</span> queue1 = <span class="hljs-literal">new</span> <span class="hljs-built_in">Queue</span>();
queue1.push(<span class="hljs-number">10</span>);
<span class="hljs-keyword">let</span> queue2 = <span class="hljs-literal">new</span> <span class="hljs-built_in">Queue</span>();
queue2.copy_without_reference(queue1);
</code></pre><p>print(): Prints all elements of the queue.</p>
<pre><code><span class="hljs-keyword">let</span> <span class="hljs-built_in">queue</span> = <span class="hljs-literal">new</span> <span class="hljs-built_in">Queue</span>();
<span class="hljs-built_in">queue</span>.push(<span class="hljs-number">10</span>);
<span class="hljs-built_in">queue</span>.print(); <span class="hljs-comment">// Output: 10</span>
</code></pre><h2 id="usage-6-heaps-priority-queues-min-max-heap-">Usage 6.) Heaps (Priority Queues) [MIN/MAX Heap]</h2>
<pre><code>    REQUIRE:-

const {PriorityQueueMaxOnTop , PriorityQueueMinOnTop} = <span class="hljs-built_in">require</span>(<span class="hljs-string">'cpp-like-js'</span>);

const max_heap = <span class="hljs-keyword">new</span> PriorityQueueMaxOnTop(); <span class="hljs-regexp">//i</span>nstance <span class="hljs-keyword">of</span> PriorityQueueMaxOnTop <span class="hljs-class"><span class="hljs-keyword">class</span>.</span>
const min_heap = <span class="hljs-keyword">new</span> PriorityQueueMinOnTop(); <span class="hljs-regexp">//i</span>nstance <span class="hljs-keyword">of</span> PriorityQueueMinOnTop <span class="hljs-class"><span class="hljs-keyword">class</span>.</span>
</code></pre><p>The PriorityQueue module provides two priority queue implementations: </p>
<p>PriorityQueueMinOnTop and PriorityQueueMaxOnTop. </p>
<p>These classes manage elements with associated priorities, supporting various utility methods for managing the queue.</p>
<p>PriorityQueueMinOnTop means MinHeap.
PriorityQueueMaxOnTop means MaxHeap.</p>
<p>MinHeap: A priority queue where the element with the smallest priority is on top.</p>
<p>MaxHeap: A priority queue where the element with the highest priority is on top.</p>
<p>Constructor:-</p>
<p>PriorityQueueMinOnTop(): Initializes an empty priority queue.</p>
<p>Methods:-</p>
<p>isEmpty(): Returns true if the queue is empty, otherwise false.</p>
<pre><code><span class="hljs-keyword">let</span> pq = <span class="hljs-function"><span class="hljs-keyword">new</span> <span class="hljs-title">PriorityQueueMinOnTop</span>();
<span class="hljs-title">cout</span>(pq.isEmpty()); <span class="hljs-comment">// Output: true</span></span>
</code></pre><p>size(): Returns the number of elements in the queue.</p>
<pre><code><span class="hljs-keyword">let</span> pq = <span class="hljs-function"><span class="hljs-keyword">new</span> <span class="hljs-title">PriorityQueueMinOnTop</span>();
<span class="hljs-title">cout</span>(pq.size()); <span class="hljs-comment">// Output: 0</span></span>
</code></pre><p>push(value, priority): Adds an element with the given priority to the queue.</p>
<pre><code><span class="hljs-keyword">let</span> pq = <span class="hljs-function"><span class="hljs-keyword">new</span> <span class="hljs-title">PriorityQueueMinOnTop</span>();
<span class="hljs-title">pq</span>.<span class="hljs-title">push</span>('task1', <span class="hljs-number">1</span>);</span>
</code></pre><p>top(): Returns the value of the top element without removing it. Throws an error if the queue is empty.</p>
<pre><code><span class="hljs-keyword">let</span> pq = <span class="hljs-function"><span class="hljs-keyword">new</span> <span class="hljs-title">PriorityQueueMinOnTop</span>();
<span class="hljs-title">pq</span>.<span class="hljs-title">push</span>('task1', <span class="hljs-number">1</span>);
<span class="hljs-title">cout</span>(pq.top()); <span class="hljs-comment">// Output: 'task1'</span></span>
</code></pre><p>pop(): Removes and returns the top element. Throws an error if the queue is empty.</p>
<pre><code><span class="hljs-keyword">let</span> pq = <span class="hljs-function"><span class="hljs-keyword">new</span> <span class="hljs-title">PriorityQueueMinOnTop</span>();
<span class="hljs-title">pq</span>.<span class="hljs-title">push</span>('task1', <span class="hljs-number">1</span>);
<span class="hljs-title">cout</span>(pq.pop()); <span class="hljs-comment">// Output: 'task1'</span></span>
</code></pre><p>clear(): Removes all elements from the queue.</p>
<pre><code><span class="hljs-keyword">let</span> pq = <span class="hljs-function"><span class="hljs-keyword">new</span> <span class="hljs-title">PriorityQueueMinOnTop</span>();
<span class="hljs-title">pq</span>.<span class="hljs-title">push</span>('task1', <span class="hljs-number">1</span>);
<span class="hljs-title">pq</span>.<span class="hljs-title">clear</span>();</span>
</code></pre><p>get(index): Returns the value of the element at the specified index. Throws an error if the index is out of bounds.</p>
<pre><code><span class="hljs-keyword">let</span> pq = <span class="hljs-function"><span class="hljs-keyword">new</span> <span class="hljs-title">PriorityQueueMinOnTop</span>();
<span class="hljs-title">pq</span>.<span class="hljs-title">push</span>('task1', <span class="hljs-number">1</span>);
<span class="hljs-title">cout</span>(pq.get(<span class="hljs-number">0</span>)); <span class="hljs-comment">// Output: 'task1'</span></span>
</code></pre><p>contains(value): Returns true if the queue contains the specified value, otherwise false.</p>
<pre><code><span class="hljs-keyword">let</span> pq = <span class="hljs-function"><span class="hljs-keyword">new</span> <span class="hljs-title">PriorityQueueMinOnTop</span>();
<span class="hljs-title">pq</span>.<span class="hljs-title">push</span>('task1', <span class="hljs-number">1</span>);
<span class="hljs-title">cout</span>(pq.contains('task1')); <span class="hljs-comment">// Output: true</span></span>
</code></pre><p>toArray(): Returns an array of all values in the queue.</p>
<pre><code><span class="hljs-keyword">let</span> pq = <span class="hljs-function"><span class="hljs-keyword">new</span> <span class="hljs-title">PriorityQueueMinOnTop</span>();
<span class="hljs-title">pq</span>.<span class="hljs-title">push</span>('task1', <span class="hljs-number">1</span>);
<span class="hljs-title">cout</span>(pq.toArray()); <span class="hljs-comment">// Output: ['task1']</span></span>
</code></pre><p>copy_without_reference(): Returns a new priority queue with the same elements, but without reference to the original queue.</p>
<pre><code>let pq1 = new PriorityQueueMinOnTop()<span class="hljs-comment">;</span>
pq1.push(<span class="hljs-string">'task1'</span>, <span class="hljs-number">1</span>)<span class="hljs-comment">;</span>
let pq2 = pq1.copy_without_reference()<span class="hljs-comment">;</span>
<span class="hljs-keyword">swap(i, </span><span class="hljs-keyword">j): </span><span class="hljs-keyword">Swaps </span>the elements <span class="hljs-built_in">at</span> indices i <span class="hljs-keyword">and </span><span class="hljs-keyword">j.
</span>
let pq = new PriorityQueueMinOnTop()<span class="hljs-comment">;</span>
pq.push(<span class="hljs-string">'task1'</span>, <span class="hljs-number">1</span>)<span class="hljs-comment">;</span>
pq.push(<span class="hljs-string">'task2'</span>, <span class="hljs-number">2</span>)<span class="hljs-comment">;</span>
pq.<span class="hljs-keyword">swap(0, </span><span class="hljs-number">1</span>)<span class="hljs-comment">;</span>
</code></pre><p>reserve(n): Sets the internal array length to n.</p>
<pre><code><span class="hljs-keyword">let</span> pq = <span class="hljs-function"><span class="hljs-keyword">new</span> <span class="hljs-title">PriorityQueueMinOnTop</span>();
<span class="hljs-title">pq</span>.<span class="hljs-title">reserve</span>(<span class="hljs-number">10</span>);</span>
</code></pre><p>erase(value): Removes all elements with the specified value from the queue.</p>
<pre><code><span class="hljs-keyword">let</span> pq = <span class="hljs-function"><span class="hljs-keyword">new</span> <span class="hljs-title">PriorityQueueMinOnTop</span>();
<span class="hljs-title">pq</span>.<span class="hljs-title">push</span>('task1', <span class="hljs-number">1</span>);
<span class="hljs-title">pq</span>.<span class="hljs-title">erase</span>('task1');</span>
</code></pre><p>print(): Prints all elements of the queue.</p>
<pre><code><span class="hljs-keyword">let</span> pq = <span class="hljs-function"><span class="hljs-keyword">new</span> <span class="hljs-title">PriorityQueueMinOnTop</span>();
<span class="hljs-title">pq</span>.<span class="hljs-title">push</span>('task1', <span class="hljs-number">1</span>);
<span class="hljs-title">pq</span>.<span class="hljs-title">print</span>(); <span class="hljs-comment">// Output: (task1, 1)</span></span>
</code></pre><h2 id="usage-7-deque">Usage 7.) Deque</h2>
<p>The Deque class provides a double-ended queue (deque) implementation with various utility methods for managing the elements.</p>
<pre><code><span class="hljs-keyword">REQUIRE</span>:-

<span class="hljs-keyword">const</span> <span class="hljs-comment">{ Deque }</span> = <span class="hljs-keyword">require</span>(<span class="hljs-string">'cpp-like-js'</span>);

<span class="hljs-keyword">const</span> dq = <span class="hljs-keyword">new</span> Deque(); <span class="hljs-comment">//instance of Deque</span>
</code></pre><p>Constructor:-</p>
<p>Deque(): Initializes an empty deque.</p>
<pre><code><span class="hljs-keyword">let</span> deque = <span class="hljs-function"><span class="hljs-keyword">new</span> <span class="hljs-title">Deque</span>(); <span class="hljs-comment">//instance of Deque </span></span>
</code></pre><p>Methods:-</p>
<p>empty(): Returns true if the deque is empty, otherwise false.</p>
<p>  let deque = new Deque();
  console.log(deque.empty()); // Output: true</p>
<p>size(): Returns the number of elements in the deque.</p>
<pre><code>let <span class="hljs-built_in">deque</span> = <span class="hljs-keyword">new</span> Deque();
console.<span class="hljs-built_in">log</span>(<span class="hljs-built_in">deque</span>.size()); <span class="hljs-comment">// Output: 0</span>
</code></pre><p>clear(): Removes all elements from the deque.</p>
<pre><code><span class="hljs-keyword">let</span> deque = <span class="hljs-function"><span class="hljs-keyword">new</span> <span class="hljs-title">Deque</span>();
<span class="hljs-title">deque</span>.<span class="hljs-title">clear</span>();</span>
</code></pre><p>push_back(value): Adds an element to the back of the deque.</p>
<pre><code><span class="hljs-keyword">let</span> deque = <span class="hljs-function"><span class="hljs-keyword">new</span> <span class="hljs-title">Deque</span>();
<span class="hljs-title">deque</span>.<span class="hljs-title">push_back</span>('element');</span>
</code></pre><p>push_front(value): Adds an element to the front of the deque.</p>
<pre><code><span class="hljs-keyword">let</span> deque = <span class="hljs-function"><span class="hljs-keyword">new</span> <span class="hljs-title">Deque</span>();
<span class="hljs-title">deque</span>.<span class="hljs-title">push_front</span>('element');</span>
</code></pre><p>emplace_back(...args): Adds multiple elements to the back of the deque.</p>
<pre><code><span class="hljs-keyword">let</span> deque = <span class="hljs-keyword">new</span> Deque();
deque.emplace<span class="hljs-number">_</span>back(<span class="hljs-string">'element1'</span>, <span class="hljs-string">'element2'</span>);
</code></pre><p>emplace_front(...args): Adds multiple elements to the front of the deque.</p>
<pre><code><span class="hljs-keyword">let</span> deque = <span class="hljs-keyword">new</span> Deque();
deque.emplace<span class="hljs-number">_f</span>ront(<span class="hljs-string">'element1'</span>, <span class="hljs-string">'element2'</span>);
</code></pre><p>pop_back(): Removes and returns the element from the back of the deque. Throws an error if the deque is empty.</p>
<pre><code><span class="hljs-keyword">let</span> deque = <span class="hljs-function"><span class="hljs-keyword">new</span> <span class="hljs-title">Deque</span>();
<span class="hljs-title">deque</span>.<span class="hljs-title">push_back</span>('element');
<span class="hljs-title">cout</span>(deque.pop_back()); <span class="hljs-comment">// Output: 'element'</span></span>
</code></pre><p>pop_front(): Removes and returns the element from the front of the deque. Throws an error if the deque is empty.</p>
<pre><code><span class="hljs-keyword">let</span> deque = <span class="hljs-function"><span class="hljs-keyword">new</span> <span class="hljs-title">Deque</span>();
<span class="hljs-title">deque</span>.<span class="hljs-title">push_front</span>('element');
<span class="hljs-title">cout</span>(deque.pop_front()); <span class="hljs-comment">// Output: 'element'</span></span>
</code></pre><p>front(): Returns the element at the front of the deque without removing it. Throws an error if the deque is empty.</p>
<pre><code><span class="hljs-keyword">let</span> deque = <span class="hljs-function"><span class="hljs-keyword">new</span> <span class="hljs-title">Deque</span>();
<span class="hljs-title">deque</span>.<span class="hljs-title">push_front</span>('element');
<span class="hljs-title">cout</span>(deque.front()); <span class="hljs-comment">// Output: 'element'</span></span>
</code></pre><p>back(): Returns the element at the back of the deque without removing it. Throws an error if the deque is empty.</p>
<pre><code><span class="hljs-keyword">let</span> deque = <span class="hljs-function"><span class="hljs-keyword">new</span> <span class="hljs-title">Deque</span>();
<span class="hljs-title">deque</span>.<span class="hljs-title">push_back</span>('element');
<span class="hljs-title">cout</span>(deque.back()); <span class="hljs-comment">// Output: 'element'</span></span>
</code></pre><p>at(index): Returns the element at the specified index. Throws an error if the index is out of range.</p>
<pre><code><span class="hljs-keyword">let</span> deque = <span class="hljs-function"><span class="hljs-keyword">new</span> <span class="hljs-title">Deque</span>();
<span class="hljs-title">deque</span>.<span class="hljs-title">push_back</span>('element');
<span class="hljs-title">cout</span>(deque.at(<span class="hljs-number">0</span>)); <span class="hljs-comment">// Output: 'element'</span></span>
</code></pre><p>insert(position, value): Inserts an element at the specified position. Throws an error if the position is invalid.</p>
<pre><code><span class="hljs-keyword">let</span> deque = <span class="hljs-function"><span class="hljs-keyword">new</span> <span class="hljs-title">Deque</span>();
<span class="hljs-title">deque</span>.<span class="hljs-title">push_back</span>('element1');
<span class="hljs-title">deque</span>.<span class="hljs-title">insert</span>(<span class="hljs-number">1</span>, 'element2');</span>
</code></pre><p>erase(position): Removes and returns the element at the specified position. Throws an error if the position is invalid.</p>
<pre><code><span class="hljs-keyword">let</span> deque = <span class="hljs-function"><span class="hljs-keyword">new</span> <span class="hljs-title">Deque</span>();
<span class="hljs-title">deque</span>.<span class="hljs-title">push_back</span>('element1');
<span class="hljs-title">cout</span>(deque.erase(<span class="hljs-number">0</span>)); <span class="hljs-comment">// Output: 'element1'</span></span>
</code></pre><p>swap(otherDeque): Swaps the contents of this deque with another deque. Throws an error if the argument is not an instance of Deque.</p>
<pre><code><span class="hljs-keyword">let</span> deque1 = <span class="hljs-function"><span class="hljs-keyword">new</span> <span class="hljs-title">Deque</span>();
<span class="hljs-title">let</span> <span class="hljs-title">deque2</span> = <span class="hljs-title">new</span> <span class="hljs-title">Deque</span>();
<span class="hljs-title">deque1</span>.<span class="hljs-title">push_back</span>('element1');
<span class="hljs-title">deque2</span>.<span class="hljs-title">push_back</span>('element2');
<span class="hljs-title">deque1</span>.<span class="hljs-title">swap</span>(deque2);</span>
</code></pre><p>assign(count, value): Clears the deque and assigns count elements of the specified value.</p>
<pre><code><span class="hljs-keyword">let</span> deque = <span class="hljs-keyword">new</span> Deque();
deque.<span class="hljs-keyword">assign</span>(<span class="hljs-number">3</span>, <span class="hljs-string">'element'</span>);
</code></pre><p>resize(count, value = undefined): Resizes the deque to contain count elements. If the new size is larger, the value is added; if smaller, elements are removed.</p>
<pre><code><span class="hljs-keyword">let</span> deque = <span class="hljs-function"><span class="hljs-keyword">new</span> <span class="hljs-title">Deque</span>();
<span class="hljs-title">deque</span>.<span class="hljs-title">resize</span>(<span class="hljs-number">3</span>, 'element');</span>
</code></pre><p>splice(position, count): Removes count elements starting from the specified position.</p>
<pre><code><span class="hljs-keyword">let</span> deque = <span class="hljs-function"><span class="hljs-keyword">new</span> <span class="hljs-title">Deque</span>();
<span class="hljs-title">deque</span>.<span class="hljs-title">push_back</span>('element1');
<span class="hljs-title">deque</span>.<span class="hljs-title">push_back</span>('element2');
<span class="hljs-title">deque</span>.<span class="hljs-title">splice</span>(<span class="hljs-number">0</span>, <span class="hljs-number">1</span>);</span>
</code></pre><p>find(value): Returns the index of the first occurrence of the specified value, or -1 if not found.</p>
<pre><code><span class="hljs-keyword">let</span> deque = <span class="hljs-function"><span class="hljs-keyword">new</span> <span class="hljs-title">Deque</span>();
<span class="hljs-title">deque</span>.<span class="hljs-title">push_back</span>('element');
<span class="hljs-title">cout</span>(deque.find('element')); <span class="hljs-comment">// Output: 0</span></span>
</code></pre><p>count(value): Returns the number of occurrences of the specified value in the deque.</p>
<pre><code><span class="hljs-keyword">let</span> deque = <span class="hljs-function"><span class="hljs-keyword">new</span> <span class="hljs-title">Deque</span>();
<span class="hljs-title">deque</span>.<span class="hljs-title">push_back</span>('element');
<span class="hljs-title">deque</span>.<span class="hljs-title">push_back</span>('element');
<span class="hljs-title">cout</span>(deque.count('element')); <span class="hljs-comment">// Output: 2</span></span>
</code></pre><p>begin(): Returns an iterator to the beginning of the deque.</p>
<pre><code><span class="hljs-keyword">let</span> deque = <span class="hljs-keyword">new</span> <span class="hljs-type">Deque</span><span class="hljs-literal">()</span>;
deque.push_back(<span class="hljs-symbol">'element1'</span>);
deque.push_back(<span class="hljs-symbol">'element2'</span>);
<span class="hljs-keyword">for</span> (<span class="hljs-keyword">let</span> el <span class="hljs-keyword">of</span> deque.<span class="hljs-keyword">begin</span><span class="hljs-literal">()</span>) {
cout(el);
}
</code></pre><p>end(): Returns an iterator to the end of the deque.</p>
<pre><code><span class="hljs-keyword">let</span> deque = <span class="hljs-keyword">new</span> <span class="hljs-type">Deque</span><span class="hljs-literal">()</span>;
deque.push_back(<span class="hljs-symbol">'element1'</span>);
deque.push_back(<span class="hljs-symbol">'element2'</span>);
<span class="hljs-keyword">for</span> (<span class="hljs-keyword">let</span> el <span class="hljs-keyword">of</span> deque.<span class="hljs-keyword">end</span><span class="hljs-literal">()</span>) {
cout(el);
}
</code></pre><p>copy_without_reference(): Returns a new deque with the same elements, but without reference to the original deque.</p>
<pre><code><span class="hljs-keyword">let</span> deque1 = <span class="hljs-function"><span class="hljs-keyword">new</span> <span class="hljs-title">Deque</span>();
<span class="hljs-title">deque1</span>.<span class="hljs-title">push_back</span>('element');
<span class="hljs-title">let</span> <span class="hljs-title">deque2</span> = <span class="hljs-title">deque1</span>.<span class="hljs-title">copy_without_reference</span>();</span>
</code></pre><p>toArray(): Returns an array of all elements in the deque.</p>
<pre><code><span class="hljs-keyword">let</span> deque = <span class="hljs-function"><span class="hljs-keyword">new</span> <span class="hljs-title">Deque</span>();
<span class="hljs-title">deque</span>.<span class="hljs-title">push_back</span>('element');
<span class="hljs-title">cout</span>(deque.toArray()); <span class="hljs-comment">// Output: ['element']</span></span>
</code></pre><p>print(): Prints all elements of the deque.</p>
<pre><code><span class="hljs-keyword">let</span> deque = <span class="hljs-function"><span class="hljs-keyword">new</span> <span class="hljs-title">Deque</span>();
<span class="hljs-title">deque</span>.<span class="hljs-title">push_back</span>('element');
<span class="hljs-title">deque</span>.<span class="hljs-title">print</span>(); <span class="hljs-comment">// Output: Deque contents: element</span></span>
</code></pre><h2 id="usage-8-tree">Usage 8.) Tree</h2>
<p>The Tree class represents a tree structure. It contains methods to manipulate the tree and perform various operations.</p>
<pre><code><span class="hljs-keyword">REQUIRE</span>:-

<span class="hljs-keyword">const</span> <span class="hljs-comment">{Tree}</span> = <span class="hljs-keyword">require</span>(<span class="hljs-string">'cpp-like-js'</span>);

<span class="hljs-keyword">const</span> myTree = <span class="hljs-keyword">new</span> Tree(); <span class="hljs-comment">//instance of Tree class</span>
</code></pre><p>Constructor:-</p>
<p>Tree(): Initializes a new, empty tree.</p>
<pre><code><span class="hljs-keyword">const</span> tree = <span class="hljs-keyword">new</span> Tree();
</code></pre><p>Methods:-</p>
<p>setRoot(value): Sets the root node of the tree with the specified value.</p>
<pre><code><span class="hljs-attribute">const rootNode</span> = tree.setRoot(10);
</code></pre><p>findLCA(value1, value2): Finds the lowest common ancestor (LCA) of the nodes with the specified values.</p>
<pre><code><span class="hljs-attribute">const lca</span> = tree.findLCA(5, 15);
</code></pre><p>isBST(): Checks if the tree is a binary search tree (BST).</p>
<pre><code><span class="hljs-attribute">const isBST</span> = tree.isBST();
</code></pre><p>levelOrderTraversal(): Returns an array of node values using level-order traversal.</p>
<pre><code><span class="hljs-attribute">const values</span> = tree.levelOrderTraversal();
</code></pre><p>getDiameter(): Returns the diameter (longest path) of the tree.</p>
<pre><code><span class="hljs-attribute">const diameter</span> = tree.getDiameter();
</code></pre><p>serialize(): Serializes the tree into a string representation.</p>
<pre><code><span class="hljs-attribute">const serializedTree</span> = tree.serialize();
</code></pre><p>static deserialize(data): Deserializes a string representation of a tree into a Tree object.</p>
<pre><code>const <span class="hljs-built_in">tree</span> = <span class="hljs-built_in">Tree</span>.deserialize(serializedTree);
</code></pre><p>copy_without_reference(): Creates a deep copy of the tree without reference to the original tree.</p>
<pre><code><span class="hljs-attribute">const copiedTree</span> = tree.copy_without_reference();
</code></pre><p>Example Usage:-</p>
<pre><code><span class="hljs-keyword">const</span> {Tree} = <span class="hljs-built_in">require</span>(<span class="hljs-string">'cpp-like-js'</span>);

<span class="hljs-keyword">const</span> myTree = <span class="hljs-keyword">new</span> Tree();
<span class="hljs-keyword">const</span> rootNode = myTree.setRoot(<span class="hljs-number">10</span>);

rootNode.addChild(<span class="hljs-number">5</span>);
rootNode.addChild(<span class="hljs-number">15</span>);

<span class="hljs-built_in">console</span>.log(myTree.levelOrderTraversal()); <span class="hljs-comment">// Output: [10, 5, 15]</span>

<span class="hljs-keyword">const</span> lca = myTree.findLCA(<span class="hljs-number">5</span>, <span class="hljs-number">15</span>);
<span class="hljs-built_in">console</span>.log(lca); <span class="hljs-comment">// Output: 10</span>

<span class="hljs-keyword">const</span> serializedTree = myTree.serialize();
<span class="hljs-built_in">console</span>.log(serializedTree);

<span class="hljs-keyword">const</span> deserializedTree = Tree.deserialize(serializedTree);
<span class="hljs-built_in">console</span>.log(deserializedTree.levelOrderTraversal()); <span class="hljs-comment">// Output: [10, 5, 15]</span>
</code></pre><h2 id="authors">Authors</h2>
<ul>
<li><a href="https://www.github.com/adityaslg2001">@adityaslg2001</a></li>
</ul>
<h1 id="cpp-like-js">cpp-like-js</h1>
