Download Link: https://assignmentchef.com/product/solved-cesc328-programming-assignment-7
<br>
Write a recursive function to calculate the <em>minimum positive subsequence sum</em> (MPSS). In other words, of all subsequences whose sum adds to a positive number, you want to determine the minimum of such sums.

<strong><u>Hint</u></strong>:

<ol>

 <li>Use the same divide and conquer algorithm for MSS, but now it is not so easy to compute</li>

</ol>

MPSS<sub>middle</sub>, <strong>Explain why</strong>? (You could make a counter example on a piece of paper)

<ol start="2">

 <li>For each subarray there are <strong>n/2</strong> such subsequence sums. (Find them and save them in 2 different arrays called S<sub>L</sub> and S<sub>R</sub>) (<strong>g.</strong> Let’s say that the left subarray is: a<sub>L</sub> = [ 2, -3, 1, 4, -6] ➔ S<sub>L</sub> = [2, -1, 0, 4, -2])</li>

 <li>Using quicksort, sort S<sub>L</sub> in <em>ascending</em> order and S<sub>R</sub> in <em>descending</em></li>

 <li>Define two markers: i and j: Let i be the index marker of S<sub>L</sub>, and j for S<sub>R</sub>.</li>

 <li>Set s<sub>min</sub> = <em>inf</em>. Now start iterating through S<sub>L</sub> and S<sub>R</sub>:

  <ol>

   <li>If s = S<sub>L</sub>(i) + S<sub>R</sub>(j) ≤ 0, then increment i.</li>

   <li>Else if s &lt; s<sub>min</sub>, then set s<sub>min</sub> = s, and increment j,</li>

   <li>Otherwise, we have s &gt; s<sub>min</sub>, in which case we increment j.</li>

   <li>Set MPSS<sub>middle</sub> = s<sub>min</sub> when either the elements of S<sub>L</sub> or S<sub>R</sub> have been exhausted.</li>

  </ol></li>

 <li><u>Calculate</u> the time complexity of your algorithm for finding MPSS on paper and show your answer to me. Running time should satisfies <em>T(n) = Θ(nlog<sup>2</sup> n).</em></li>

 <li>Explain how/why the algorithm for MPSS<sub>middle</sub> (You may write your answer on paper)</li>

</ol>




<strong><em><u>Example</u></em></strong>:  Ask the user to give you the size of the array (<em>n</em>) and generate <em>n</em> random <em>numbers</em> between -20 to 20.

A = [2, -3, 1, 4, -6, 10, -12, 5.2, 3.6, -8],  <strong><em><u>Output</u></em></strong>:

MPSS = 0.8


