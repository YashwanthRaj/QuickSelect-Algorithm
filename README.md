# Quickselect-Algorithm
CSCI 6212 [Project 2] - Median of Medians version of QuickSelect algorithm to find the kth smallest element in an array. 

Traditional way is to sort the array and find the kth element, but even the best sorting algorithm will give us a time complexity of O(nlog(n))
Instead we use QuickSelect Algorithm, which takes time complexity of O(n).

# Theoretical Analysis  
Traditional way of solving the problem is to sort the array and select the kth element from the start. But the                        sorting algorithm will take O(nlog(n)) time to complete the sorting. We use Quickselect algorithm where we can find the kth smallest element without sorting, and Time complexity of this algorithm in O(n).
In this algorithm, we select a pivot element and use it to create smaller subarrays. The arrays are broken into smaller arrays of length 5, and the median of each smaller array is calculated. Then we analyze the medians of all the smaller arrays and recursively use it to find the median of medians, which we use as pivot element. This way we can effectively ensure that the pivot is close to true median of given array. 

# Algorithm Analysis 
•	The algorithm starts by checking the size of the array. If less than 5, then it sorts the array and returns the kth element. 
•	If size of arrays is larger than 5, then the algorithm divides the array into groups of 5 elements. Then it calculates the median of all the groups.
•	After processing all the groups, it calculates the median of all the medians from smaller groups. 
•	Now, the median of medians is used as the pivot element to partition the array into three parts, Ones that are less than pivot, Ones that are equal to pivot, and Ones that are greater than pivot. 
•	Now depending on the given element k, the program makes recursive calls to select one of the 3 divisions created by pivot element. 
•	After division selection and processing, the algorithm returns the result.

# Experimental Analysis 
We have formulated and run the code for different values of n ranging from 10 to 10^7, and noted down the time taken for each n value. We also substitute the values of n in time complexity expression that we have derived and tabulate all the results. 
Now we notice that the experimental time is in milliseconds, but the theoretical time are constants, hence, to plot graphs, we need to multiply all the theoretical values by scaling constant.

Scaling Constant=(Average of Experimental Results in ms)/(Average of Theoretical Results@)

The average of experimental values is 652.4185714 and the average of theoretical values is 1587301.43. Hence dividing them, we get the scaling constant as 0.000411, which we multiply with theoretical values to get the adjusted values that we can plot.

# Comparing Experimental and Theoretical values

<img width="314" alt="image" src="https://github.com/YashwanthRaj/QuickSelect-Algorithm/assets/99544533/2b95c2e5-7039-450a-8b87-336585a8d93c">

# Graph Observation:
From the graph we can observe that the theoretical calculation and the experimental calculations are very close to each other. Both the graphs are increasing in linear time O(n).

# Conclusion
We have analyzed Quickselect algorithm Median of Medians method to find the kth smallest element in any given array. We have formulated the code and compared experimental and theoretical values. 
