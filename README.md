## GFG Problem Of The Day

### Today - 09 November 2023
### Que - Predict the Column
The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/predict-the-column/1)

![](https://badgen.net/badge/Level/Easy/green)

### My Approach
I'll find and return the column index with the maximum number of zeros. 
- To do this, I'll iterate through each column, counting the number of zeros in each column, and keeping track of the column with the maximum zeros. 

### Time and Auxiliary Space Complexity

- **Time Complexity**: `O(n^2)` because we iterate through all elements in the `n x n` matrix.
- **Auxiliary Space Complexity**: `O(1)` as we use a constant amount of additional space.

### Code (C++)
```cpp
class Solution {
public:
    int columnWithMaxZeros(vector<vector<int>> &arr, int n) {
        int maxZeros = 0;
        int columnIdx = -1;
        
        for (int j = 0; j < n; j++) {
            int zerosCount = 0;
            for (int i = 0; i < n; i++) {
                if (arr[i][j] == 0) {
                    zerosCount++;
                }
            }
            
            if (zerosCount > maxZeros) {
                maxZeros = zerosCount;
                columnIdx = j;
            }
        }
        
        return columnIdx;
    }
};
```
### Contribution and Support

I always encourage contributors to participate in the discussion forum for this repository.

If you have a better solution or any queries / discussions related to the `Problem of the Day` solution, please visit our [discussion section](https://github.com/getlost01/gfg-potd/discussions). We welcome your input and aim to foster a collaborative learning environment.

If you find this solution helpful, consider supporting us by giving a `⭐ star` to the [getlost01/gfg-potd](https://github.com/getlost01/gfg-potd) repository.


![Total number of repository visitors](https://komarev.com/ghpvc/?username=gl01potdgfg&color=blue&&label=Visitors)
![](https://hit.yhype.me/github/profile?user_id=79409258)