Download Link: https://assignmentchef.com/product/solved-fit2004-assignment-2
<br>
This assignment achieves the Learning Outcomes of:

<ul>

 <li>1) Analyse general problem solving strategies and algorithmic paradigms, and apply them to solving new problems;</li>

 <li>2) Prove correctness of programs, analyse their space and time complexities;</li>

 <li>4) Develop and implement algorithms to solve computational problems.</li>

</ul>

In addition, you will develop the following employability skills:

<ul>

 <li>Text comprehension</li>

 <li>Designing test cases</li>

 <li>Ability to follow specifications precisely</li>

</ul>

<h1>Assignment timeline</h1>

In order to be successful in this assessment, the following steps are provided as a suggestion. This is an approach which will be useful to you both in future units, and in industry.

<h2>Planning</h2>

<ol>

 <li>Read the assignment specification as soon as possible and write out a list of questions you have about it.</li>

 <li>Clarify these questions. You can go to a consultation, talk to your tutor, discuss the tasks with friends or ask in the forums.</li>

 <li>As soon as possible, start thinking about the problems in the assignment.

  <ul>

   <li>It is strongly recommended that you do not write code until you have a solid feeling for how the problem works and how you will solve it.</li>

  </ul></li>

 <li>Writing down small examples and solving them by hand is an excellent tool for coming to a better understanding of the problem.

  <ul>

   <li>As you are doing this, you may see patterns which allow you to deduce the correct algorithm to solve the problem.</li>

   <li>You will also get a feel for the kinds of edge cases you will need to handle.</li>

  </ul></li>

 <li>Write down a high level description of the algorithm you will use.</li>

 <li>Determine the complexity of your algorithm idea, ensuring it meets the requirements.</li>

</ol>

<h2>Implementing</h2>

<ol>

 <li>Think of test cases that you can use to check if your algorithm works.

  <ul>

   <li>Use the edge cases you found during the previous phase to inspire your test cases.</li>

   <li>It is also a good idea to generate large random test cases.</li>

   <li>Sharing test cases is allowed, as it is not helping solve the assignment. Check the forums for test cases!</li>

  </ul></li>

 <li>Code up your algorithm, (remember decomposition and comments) and test it on the tests you have thought of.</li>

 <li>Try to break your code. Think of what kinds of inputs you could be presented with which your code might not be able to handle.

  <ul>

   <li>Large inputs</li>

   <li>Small inputs</li>

   <li>Inputs with strange properties</li>

   <li>What if everything is the same?</li>

   <li>What if everything is different?</li>

   <li>..</li>

  </ul></li>

</ol>

<h2>Before submission</h2>

<ul>

 <li>Make sure that the input/output format of your code matches the specification.</li>

 <li>Make sure your filenames match the specification.</li>

 <li>Make sure your functions are named correctly and take the correct inputs.</li>

</ul>

<h1>Special requirements</h1>

For this assignment, there are two tasks to complete. As usual, there are required complexities, but for each of these two task, there are two different complexities listed. One complexity we will refer to as the optimal complexity, and the other complexity we will refer to as the sub-optimal complexity.

In order to receive full marks for the assignment, you must submit an algorithm with the optimal complexity for at least one of the two tasks. If you complete both tasks within the sub-optimal complexity, but not the optimal complexity, then the maximum mark you can receive for the whole assignment is 80% (24/30).

If one or both of your tasks has a complexity worse than the sub-optimal complexity listed in the task description, your mark will be significantly lower (as usual).

For each of the two functions, please clearly state in the function documentation whether the function has been implemented optimally or sub-optimally. Note that you are allowed to submit two sub-optimal tasks! This choice is so that if you cannot see how to solve the problems optimally, you still have a chance to get most of the marks.

<h2>Documentation</h2>

For this assignment (and all assignments in this unit) you are required to document and comment your code appropriately. This documentation/commenting must consist of (but is not limited to)

<ul>

 <li>For each function, high level description of that function. This should be a one or two sentence explanation of what this function does. One good way of presenting this information is by specifying what the input to the function is, and what output the function produces (if appropriate)</li>

 <li>For each function, the Big-O complexity of that function, in terms of the input. Make sure you specify what the variables involved in your complexity refer to. Remember that the complexity of a function includes the complexity of any function calls it makes.</li>

 <li>Within functions, comments where appropriate. Generally speaking, you would comment complicated lines of code (which you should try to minimise) or a large block of code which performs a clear and distinct task (often blocks like this are good candidates to be their own functions!).</li>

</ul>

<h2>1          Oscillations</h2>

In this task, you will find the longest oscillation in a given list. To do this you will write a function longest_oscillation(L).

1.1        Input

A list of integers, L. The list can contain duplicates or be empty.

<h3>1.2        Output</h3>

Given a list L of length m, we define an oscillation as a (possibly empty) sequence of increasing indices of L <em>a</em><sub>1</sub><em>,a</em><sub>2</sub><em>,…a<sub>n </sub></em>such that

<ul>

 <li>L[<em>a<sub>j</sub></em>]6= L[<em>a<sub>j</sub></em><sub>+1</sub>]</li>

 <li>if L[<em>a<sub>j</sub></em>] &lt; L[<em>a<sub>j</sub></em><sub>+1</sub>], then L[<em>a<sub>j</sub></em><sub>+1</sub>] &gt; L[<em>a<sub>j</sub></em><sub>+2</sub>]</li>

 <li>if L[<em>a<sub>j</sub></em>] &gt; L[<em>a<sub>j</sub></em><sub>+1</sub>], then L[<em>a<sub>j</sub></em><sub>+1</sub>] &lt; L[<em>a<sub>j</sub></em><sub>+2</sub>]</li>

</ul>

Your function should return the length of the longest oscillation in L, and the indices in L at which it occurs. It should do this by returning a tuple, where the first element of the tuple is a number, which represents the length of the oscillation. The second element is a list which contains the indices of the elements in L which make up the oscillation.

The values in this list should be in ascending order (i.e. the indices should be in the same order that they are in L).

Example:

longest_oscillation([1,5,7,4,6,8,6,7,1]) returns (7, [0,2,3,5,6,7,8]). This corresponds to the red values from L: ([1,5,7,4,6,8,6,7,1])

longest_oscillation([1,1,1,1,1]) returns (1, [0]) This corresponds to the red values from L: ([1,1,1,1,1])

longest_oscillation([1,2,3]) returns (2, [0,1]) This corresponds to the red values from L: ([1,2,3])

Note: Some lists may have multiple longest oscillations, you may return any one of them. Do not return more than one.

As an example, valid return values for longest_oscillation([1,2,3]) are (2, [0,1]), (2, [0,2]) and (2, [1,2]).

<h3>1.3         Complexity</h3>

Given an input list of length <em>N</em>:

<h4>1.3.1        Sub-optimal</h4>

<ul>

 <li>longest_oscillation must run in <em>O</em>(<em>N</em><sup>2</sup>) time</li>

 <li>longest_oscillation must use <em>O</em>(<em>N</em>) auxiliary space</li>

</ul>

<h4>1.3.2       Optimal</h4>

<ul>

 <li>longest_oscillation must run in <em>O</em>(<em>N</em>) time</li>

 <li>longest_oscillation must use <em>O</em>(<em>N</em>) auxiliary space</li>

</ul>

<h2>2          Increasing walk</h2>

Given a two-dimensional matrix of numbers, you will find the longest increasing walk in the matrix. To do this, you will write a function longest_walk(M).

<h3>2.1        Input</h3>

The input, M, is a list of <em>n </em>lists, with each inner list being length <em>m</em>, and containing only integers. M can be thought of as an <em>n </em>× <em>m </em>matrix, with row <em>i </em>of the matrix being represented by M[i]. Thus M[i][j] represents the value in row <em>i</em>, column <em>j </em>of the matrix. We will refer to M as a matrix from this point onward.

M can contain duplicates, and can be empty.

<h3>2.2        Output</h3>

An increasing walk in a matrix M is a sequence of values of M which are

<ul>

 <li>sequentially adjacent (this can be horizontally, vertically or diagonally)</li>

 <li>each value in the sequence is greater than the previous value</li>

</ul>

Your function should return the length of the longest increasing walk in M, and the co-ordinates of the elements in that walk, in order. It should do this by returning a tuple, where the first element of the tuple is a number representing the length of the longest walk in M. The second element in the tuple is a list of 2-element tuples. These tuples are the (row, column) co-ordinates of the elements of M which make up the longest increasing walk, in the same order as they would be traversed during the walk.

Example:

<table width="642">

 <tbody>

  <tr>

   <td width="642">M = [[1,2,3], [4,5,6],[7,8,9]] longest_walk(M) = (7, [(0,0), (0,1), (0,2), (1,1), (1,2), (2,1), (2,2)])</td>

  </tr>

  <tr>

   <td width="642">M = [[1,2,3], [1,2,1],[2,1,3]] longest_walk(M) = (3, [(0,0), (1,1), (2,2)])</td>

  </tr>

 </tbody>

</table>

M = [[4,6],

[7,2]] longest_walk(M) = (4, [(1,1), (0,0), (0,1), (1,0)])

Note: As in task 1, there may be multiple valid return values for a given input. You may return any one of them. Do not return more than one.

<h3>2.3         Complexity</h3>

Given an input matrix of <em>n </em>rows and <em>m </em>columns.

<h4>2.3.1        Sub-optimal</h4>

<ul>

 <li>longest_walk must run in <em>O</em>(<em>nm</em>log(<em>nm</em>)) time</li>

 <li>longest_walk must use <em>O</em>(<em>nm</em>) auxiliary space</li>

</ul>

<h4>2.3.2       Optimal</h4>

<ul>

 <li>longest_walk must run in <em>O</em>(<em>nm</em>) time</li>

 <li>longest_walk must use <em>O</em>(<em>nm</em>) auxiliary space</li>

</ul>