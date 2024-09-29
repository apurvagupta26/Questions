Given a random array arr of numbers, please return them in ascending sorted order.

Examples:

Input:
arr[] = [1 5 3 2]
Output: [1 2 3 5]
Explanation: After sorting array will be like [1, 2, 3, 5].
Input: arr[] = [3 1]
Output: [1 3]
Explanation: After sorting array will be like [1, 3].

Expected Time Complexity: O(n * log n)
Expected Auxiliary Space: O(1)

Solution:
    sortArr(arr) {
        return arr.sort((a,b)=>a-b)
    }
