[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/9YUeXH71)
# Theoretical Sorting

A Computer Science researcher claims to have come up with a sorting algorithm
that can sort arbitrary elements in $O(n)$ time based on comparisons of two
elements at a time. This would be asymptotically faster than any known general
sorting algorithm. The algorithm itself is proprietary and will be sold by a
company.

How would you verify this claim? You may assume that you have access to a
black-box implementation of the sorting algorithm, i.e. you cannot examine the
source code, but you can use it to sort any list you like. Explain in detail
your method for investigating whether X is correct, including any expected
results you would get.

Also give a theoretical argument for why X could or could not be correct, based
on the complexity of the general sorting problem we covered in class.

Add your answers to this markdown file.

## Answer

To verify this claim using the black-box, I would execute the algorithm on data sets of various sizes and see how they compare. We would expect a data set of size $2n$ to take about twice as long to sort than a list of size $n$. Generalizing this, we can say that a list of size $x*n$ will take $x$ times longer to sort than an $n$ sized list. For further insight on how it works, we could try different patterns to see what is the best case and worst case input for this algorithm. Running enough of these tests, we could plot the results and hope to see some type of linear relationship, adjusting the axes and scaling as necessary. 

However, theoretically, this algorithm cannot have a runtime of $O(n)$ because it would defy the complexity of the sorting problem itself. We could try to develop a decision tree with height $n$ instead of $n\log n$ and we would find that there wouldn't be enough leaves; some possible permutations of the array would be missing, therefore some lists will not be able to get sorted. 
