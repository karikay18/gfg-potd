# GFG Problem Of The Day

## Today - 4 June 2023
### Que - Reversing the equation

[Question Link](https://practice.geeksforgeeks.org/problems/reversing-the-equation2205/1)

### My approach
- Use two stacks to store the numbers and operators.
- Update the stacks as new numbers and operators are encountered.
- Implement a top-to-bottom traversal of the stacks to print the numbers and operators alternatively.

### Code (c++)
```
class Solution
{
  public:
    string reverseEqn (string str)
        {
            stack<string> num;
            stack<char> op;
            string s = "";
            for(auto i: str){
                if(i<'0' || i>'9'){
                    num.push(s);
                    op.push(i);
                    s = "";
                }
                else
                s += i;
            }
            num.push(s);
            s = "";
            while(!op.empty()){
                s += num.top();
                s += op.top();
                num.pop();
                op.pop();
            }
            s += num.top();
            return s;
        }
};
```