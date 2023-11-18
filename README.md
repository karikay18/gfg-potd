## GFG Problem Of The Day

### Today - 18 November 2023
### Que - Reverse a Doubly Linked List
The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/reverse-a-doubly-linked-list/1)

![](https://badgen.net/badge/Level/Basic/green)

### My Approach
To reverse a doubly linked list, I go through the list, swapping the `prev` and `next` pointers for each node while updating the head during each iteration.

### Time and Auxiliary Space Complexity

- **Time Complexity**: `O(N)`, where `N` is the number of nodes in the doubly linked list.
- **Auxiliary Space Complexity**: `O(1)`, as the reversal is done in-place without using additional space.

### Code (C++)
```cpp
class Solution {
public:
    Node* reverseDLL(Node* head) {
        Node* curr = head;

        while (curr) {
            head = curr;
            Node* prev = curr->prev;
            curr->prev = curr->next;
            curr->next = prev;
            curr = curr->prev;
        }

        return head;
    }
};
```
### Contribution and Support

I always encourage contributors to participate in the discussion forum for this repository.

If you have a better solution or any queries / discussions related to the `Problem of the Day` solution, please visit our [discussion section](https://github.com/getlost01/gfg-potd/discussions). We welcome your input and aim to foster a collaborative learning environment.

If you find this solution helpful, consider supporting us by giving a `⭐ star` to the [getlost01/gfg-potd](https://github.com/getlost01/gfg-potd) repository.


![Total number of repository visitors](https://komarev.com/ghpvc/?username=gl01potdgfg&color=blue&&label=Visitors)
![](https://hit.yhype.me/github/profile?user_id=79409258)
