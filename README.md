## GFG Problem Of The Day

### Today - 17 January 2024
### Que - All Unique Permutations of an array
The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/all-unique-permutations-of-an-array/1)

![](https://badgen.net/badge/Level/Medium/yellow)

### My Approach
- Sort the array in ascending order.
- Generate all unique permutations using `std::next_permutation`.
- Return the vector of unique permutations.

### Time and Auxiliary Space Complexity

- **Time Complexity:** `O(N! * N)`, where N is the length of the array. This is because there are N! permutations, and for each permutation, it takes O(N) time to copy it.
- **Auxiliary Space Complexity:** `O(N!)`, where N is the length of the array. This is the space needed to store all unique permutations.

### Code (C++)

```cpp
class Solution {
  public:
    vector<vector<int>> uniquePerms(vector<int> &arr, int n) {
        sort(arr.begin(), arr.end());

        vector<vector<int>> out;
        do {
            out.push_back(arr);
        } while (next_permutation(arr.begin(), arr.end()));

        return out;
    }
};
```

### Contribution and Support

I always encourage contributors to participate in the discussion forum for this repository.

If you have a better solution or any queries / discussions related to the `Problem of the Day` solution, please visit our [discussion section](https://github.com/getlost01/gfg-potd/discussions). We welcome your input and aim to foster a collaborative learning environment.

If you find this solution helpful, consider supporting us by giving a `⭐ star` to the [getlost01/gfg-potd](https://github.com/getlost01/gfg-potd) repository.

![Total number of repository visitors](https://komarev.com/ghpvc/?username=gl01potdgfg&color=blue&&label=Visitors)
![](https://hit.yhype.me/github/profile?user_id=79409258)

