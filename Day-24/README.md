The provided sources cover two primary topics: mathematical methods for comparing functions and algorithmic strategies for solving the Array Partition problem.
1. Comparison of Mathematical Functions
The sources outline methods to determine which of two functions is larger, which is essential for understanding upper and lower bounds in computer science.
• Sampling Values: One simple method is to plug in various values for n. For example, comparing n 
2
  and n 
3
  by sampling values like 2, 3, and 4 shows that n 
3
  grows significantly faster.
• Logarithmic Comparison: For more complex functions, applying a logarithm to both sides simplifies the comparison. Using log properties, one can break down functions like n 
2
 logn and n(logn) 
10
  to see which terms dominate. In this specific case, the n 
2
  term (which becomes 2logn after applying log) outweighs the (logn) 
10
  term.
• Asymptotic Equality: Functions may be "value-wise" different but asymptotically equal. For instance, 3⋅n 
n

​
 
  and n 
n

​
 
  have the same growth rate (Big O), even though the first function has a larger coefficient.
2. Array Partition Problem (LeetCode 561)
This problem asks to group 2n integers into n pairs such that the sum of the minimums of each pair is maximized.
Approach 1: Sorting
• Logic: To maximize the sum, you want to avoid "wasting" large numbers by pairing them with very small numbers. By sorting the array, you can pair the smallest number with the next smallest number, the third smallest with the fourth, and so on.
• Implementation: Once the array is sorted, the maximum sum is simply the sum of all elements at even indices (index 0, 2, 4, etc.).
• Complexity: This approach has a time complexity of O(nlogn) due to the sorting step.
Approach 2: Count Sort
• Logic: When the range of numbers is small (in this case, between −10,000 and 10,000), Count Sort can be more efficient.
• Implementation:
    ◦ Create a frequency array to store the count of each number. Since indices must be positive, map the range by adding an offset (e.g., adding 10,000 to each number).
    ◦ Iterate through the frequency array. Use a boolean flag (like isEvenIndex) to track whether the current element should be added to the sum.
    ◦ If a number appears multiple times, the flag toggles for each occurrence to ensure only the "minimums" of the theoretical pairs are summed.
• Complexity: This approach achieves a linear time complexity of O(n+k), where k is the range of the numbers, and a space complexity of O(k).
