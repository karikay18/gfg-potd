# GFG Problem Of The Day

## Today - 22 June 2023
### Que - Lemonade Change

[Question Link](https://practice.geeksforgeeks.org/problems/lemonade-change/1)


### My approach
- Iterate through each customer in the queue and greedily process their request. 
- Firstly store the value of the note in our collection box. If needed, provide a 10-dollar bill as change then check and provide the necessary number of 5-dollar bills. If you fail in providing change bills return `false`;


### Code (c++) 
```
class Solution {
  public:
    bool lemonadeChange(int n, vector<int> &bills) {
        map<int,int> mp;
        for(auto bill: bills){
            ++mp[bill];                      // add bill note to cash box.
            
            int change = bill - 5;           // cut the price of lemonade and provide remaining change.
            
            if(change == 15 && mp[10] > 0){  // provide one 10 bill note if change value is 15.
                --mp[10];
                change -= 10;
            }
            
            if(change>=5){                   // last option, provide 5 bill notes as many as needed.
                if(change/5 <= mp[5]){  
                    mp[5] -= change/5;
                    change = 0;
                }else
                    return false;            // if we cannot provide 5 bill notes in change return false. 
            }
        }
        
        return true;
    }
};
```

#### If you like my solutions, please consider a ⭐ `star` to this repo.

![GFG](https://komarev.com/ghpvc/?username=gl01potdgfg&color=blue&&label=Visitors)