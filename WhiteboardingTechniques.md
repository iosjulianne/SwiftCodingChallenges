### Whiteboarding Techniques

1. **Two Pointers Technique**: This technique involves using two pointers to traverse an array or a linked list simultaneously. It is commonly used for problems that involve searching, partitioning, or comparing elements in a collection.

2. **Sliding Window Technique**: The sliding window technique involves maintaining a dynamic window (a subarray or subsequence) within an array or string and sliding it to perform computations or find optimal solutions. It is often used for problems that involve finding subarrays with a specific property or optimizing a solution over a range of elements.

3. **Binary Search**: Binary search is an efficient algorithm for finding a specific element or determining an insertion position in a sorted array. It repeatedly halves the search space by comparing the target element with the middle element of the array.

4. **Backtracking**: Backtracking is a technique for solving problems by recursively exploring all possible solutions. It involves trying out different choices and undoing or backtracking when a choice leads to an invalid solution.

5. **Divide and Conquer**: Divide and conquer is a technique that involves breaking down a problem into smaller subproblems, solving them independently, and combining the solutions to solve the original problem. It often relies on recursion and can be used for problems like sorting, searching, and optimization.

6. **Greedy Algorithms**: Greedy algorithms make locally optimal choices at each step with the hope of finding a global optimum. They iteratively make the best choice at each stage without considering the overall future consequences.

7. **Kadane's Algorithm**: Kadane's algorithm is an efficient algorithm for finding the maximum sum of a contiguous subarray within an array of integers. The algorithm works by iterating through the array and maintaining two variables: `currentSum` and `maxSum`.

```
func maxSubarraySum(_ nums: [Int]) -> Int {
    var currentSum = nums[0]
    var maxSum = nums[0]
    
    for i in 1..<nums.count {
        currentSum = max(nums[i], currentSum + nums[i])
        maxSum = max(maxSum, currentSum)
    }
    
    return maxSum
}
```
Kadane's algorithm avoids the need for nested loops and achieves a time complexity of O(n).
