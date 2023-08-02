# Whiteboarding Techniques

1. **One Pass/Iterative Approach**: The One Pass Approach is a common technique used in many array-related problems where the goal is to find the best possible result by processing the elements in one go without the need for multiple iterations. Initialize necessary variables to keep track of required information.

2. **Frequency Counting/Counting Occurrences**: Frequency counting, also known as counting occurrences, is a technique to efficiently count the number of occurrences of elements or items in a data set, typically in an array, list, or collection and only requires a single pass through the data. The goal is to determine the frequency of each distinct element and store this information for further analysis or processing. (e.g. most common elements, detecting duplicates, identifying patterns in data)

1. **Two Pointers Technique**: This technique involves using two pointers to traverse an array or a linked list simultaneously. It is commonly used for problems that involve searching, partitioning, or comparing elements in a collection.

2. **Sliding Window Technique**: The sliding window technique involves maintaining a dynamic window (a subarray or subsequence) within an array or string and sliding it to perform computations or find optimal solutions. It is often used for problems that involve finding subarrays with a specific property or optimizing a solution over a range of elements.

3. **Binary Search**: Binary search is an efficient algorithm for finding a specific element or determining an insertion position in a sorted array. It repeatedly halves the search space by comparing the target element with the middle element of the array.

4. **Backtracking**: Backtracking is a technique for solving problems by recursively exploring all possible solutions. It involves trying out different choices and undoing or backtracking when a choice leads to an invalid solution.

5. **Divide and Conquer**: Divide and conquer is a technique that involves breaking down a problem into smaller subproblems, solving them independently, and combining the solutions to solve the original problem. It often relies on recursion and can be used for problems like sorting, searching, and optimization.

6. **Memoization**: Memoization is a technique used in programming to optimize the execution of functions by caching and reusing the results of expensive function calls. It involves storing the results of function calls in a cache or lookup table (such as a dictionary or array), so that subsequent calls with the same inputs can retrieve the cached result instead of re-computing it.

7. **Greedy Algorithms**: Greedy algorithms make locally optimal choices at each step with the hope of finding a global optimum. They iteratively make the best choice at each stage without considering the overall future consequences.

8. **Kadane's Algorithm**: Kadane's algorithm is an efficient algorithm for finding the maximum sum of a contiguous subarray within an array of integers. The algorithm works by iterating through the array and maintaining two variables: `currentSum` and `maxSum`. 
	
```
func maxSubSum(_ numberArray: [Int]) -> Int {
    var currentSum = 0
    var maxSum = 0    
    for number in numberArray {
        currentSum = max(number, currentSum + number)
        maxSum = max(maxSum, currentSum)
    }
    return maxSum
}
```
Kadane's algorithm avoids the need for nested loops and achieves a time complexity of O(n).

### Kadane's Algorithm vs Sliding Window
Kadane's algorithm - a specialized form of the sliding window technique tailored for finding the maximum subarray sum

sliding window algorithm - a more general approach used for a broader set of problems involving windows or subsets of fixed size


## Notes

**Difference between [Int][Int] and [[Int]]**

`[Int][Int]`: Represents a two-dimensional array or matrix where both the outer and inner arrays contain elements of type `Int`.

`[[Int]]`: Represents an array of arrays, where the inner arrays can contain elements of any type, including `Int` or other types.

The distinction is important because `[Int][Int]` enforces that all elements in the array structure are of type `Int`, whereas `[[Int]]` allows for flexibility in the types of elements within the inner arrays.

**XOR (exclusive OR) bitwise operation**<br>
*Seen in Single Numbers, Unique Numbers*

The XOR bitwise operation (represented by `^` in Swift) returns 1 if two bits are different and 0 if they are the same. The key property of XOR is that it is both commutative and associative. This means that if we XOR all the elements in an array together, all elements that appear twice will cancel each other out, leaving only the XOR result of the elements that appear only once.
