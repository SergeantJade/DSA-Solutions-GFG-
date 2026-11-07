## 01. Second Largest

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/second-largest3735/1)

### Problem Description

**Task:** Given an array of positive integers arr[], return the second largest element from the array. If the second largest element doesn't exist then return -1.Note: The second largest element should not be equal to the largest element.Examples:Input: arr[] = [12, 35, 1, 10, 34, 1]

#### Examples

##### Example 1

- **Output:**
```text
-1
```
- **Explanation:** The largest element of the array is 10 and the second largest element does not exist.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (C++)

- **Submitted:** 2026-11-07 17:39:57
- **Status:** Correct
- **Marks:** 2

```cpp
class Solution {
  public:
    int getSecondLargest(vector<int> &arr) {
        // code here
        int largest=INT_MIN;
    int second=INT_MIN;
    for(int i=0;i<arr.size();i++){
        if(arr[i]>largest){
            second=largest;
            largest=arr[i];
        }
        else if(arr[i]<largest && arr[i]>second){
            second=arr[i];
        }
    }
    if(second==INT_MIN){
        return -1;
    }
    return second;
    }
};
```

*Generated on: 11/7/2026, 5:56:52 PM*