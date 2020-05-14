# Algorithmic Complexity

## Big O Notation

linear time O(n)
constant time O(1)
quadric time O(n2)

![Big O Notation Graph](https://upload.wikimedia.org/wikipedia/commons/thumb/7/7e/Comparison_computational_complexity.svg/1024px-Comparison_computational_complexity.svg.png)

|Notation|Name|Description|
|--------|----|-----------|
|O(1)|Constant|Always takes the same time.|
|O(log n)|Logarithmic|Amount of work is divided by 2 after every loop iteration (binary search).|
|O(n)|Linear|Time to complete the work grows in a 1 to 1 relation to input size.|
|O(n log n)|Linearithmic|This is a nested loop, where the inner loop runs in ```log n``` time. Examples include quicksort, mergesort & heapsort.|
|O(n^2)|Quadratic|Time to complete the work grows in a ```input size ^ 2``` relation. You can recognise this whenever you have a loop that goes over all the elements & every iteration of the loop also goes over every element. You have a nested loop.|
|O(n^3)|Cubic|Same as ```n^2```, but time grows in a ```n^3``` relation to input size. Look for a triple nested loop to recognise this one.|
|O(2^n)|Exponential|Time to complete the work grows in a ```2 ^ input size``` relation. This is a lot slower than ```n^2```, so don't confuse them! One example is the recursive fibonacci algorithm.|

## Timing Framework

Benchmark

##


