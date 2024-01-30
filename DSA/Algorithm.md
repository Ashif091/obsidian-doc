#### What is an Algorithms ?
`input -> algorithms -> output `

#### ﻿Characteristics
1. ﻿Well defined inputs and outputs
﻿2.  Each step should be clear and unambiguous
﻿3. Language independent

#### Why algorithms?
1. ﻿As a developer, you're going to come across problems that you need to solve
2. ﻿Learning algorithms translates to learning different techniques to efficiently solve those problems
﻿3. One problem can be solved in many ways using different algorithms
﻿4. Every algorithm comes with its own tradeoffs when it comes to performance
#### Algorithm analysis

﻿ 1. There are multiple ways to solve one problem Ex:
﻿ 2. There are multiple algorithms to sort a list of numbers
﻿ 3. How do we analyse which one of them is the most efficient algorithm?
﻿ 4. Generally, when we talk about performance, we use an absolute measure
﻿ 5. If I can run 100 meters in 12 seconds, I'm faster than someone who takes 15 seconds


#### Algorithm analysis contd.
﻿1. The absolute running time of an algorithm cannot be predicted, since it depends on a number of factors
	﻿- Programming language used to implement the algorithm-
	﻿- The computer the program runs on
	﻿- Other programs running at the same time
	﻿- Quality of the operating system


2. ﻿We evaluate the performance of an algorithm in terms of its input size
﻿- Time complexity : 
﻿     Amount of time taken by an algorithm to run, as a function of input size
﻿- Space complexity :
	﻿ Amount of memory taken by an algorithm to run, as a function of input size
﻿
﻿3. By evaluating against the input size, the analysis is not only machine independent but the comparison is also more appropriate.
	﻿- There is no one solution that works every single time. It is always good to know multiple ways to solve the problem and use the best solution, given your constraints
	﻿- If your app needs to be very quick and has plenty of memory to work with, you don't have to worry about space complexity
	﻿- If you have very little memory to work with, you should pick a solution that is relatively slower but needs less space


### ﻿How to represent complexity?
##### Asymptotic notations
- Mathematical tools to represent time and space complexity 
	1. [[Big O notation]] (O-notation) - Worst case complexity 
	2. Omega Notation (Q-notation) - Best case complexity 
	3. Theta Notation (O-notation) - Average case complexity


