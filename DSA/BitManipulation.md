26.06.2023

### Bit manipulation
---
For unsigned integers range is 2^32-1;
For signed integers one bit is saved for sign hence range is 2^31-1

```c
(For any number n if we want to do operation on bit at position i)
1.Get Bit=>(n&(1<<i))
2.Set Bit=>(n|(1<<i))
3.Clear Bit=>(n&~(1<<i))
4.Update Bit=>((n&~(1<<i))|(value)<<i)
5.Toggle Bit=>(n^(1<<i))
6.Power of 2=>(n!=0 && n&(n-1)==0)?return true:return false;
7.Check even or odd=>if(n&1==1)return odd:return even;
8.Multiply by 2=>n<<1;
9.Divide by 2=>n>>1;
10.Uppercase to lowercase=>('C'|' ')
11.Lowercase to uppercase=>('c' & '_')
12.Clear all LSB till ith position starting from 0th positon=>a&(~(1<<(i+1)-1))
13.Clear all MSB till ith position (0 based indexing)=>a&((1<<(i+1)-1))
14.Power of 4=>if a no is power of 2 and n%3==1 then it is power of 4
15.Maximum xor sum of all elements in array can be obtained by doing | of all elements
16.If in an array of n intgers all element are present even no of times except one element then to find that element we do xor of all elements 
since x^y^x=y
17.Swapping  a and b using xor=>a=a^b;b=a^b;a=a^b;
```
To count no of set bits=>
```c
int count=0;
for(int i=31;i>=0;i--)
{
if(a&(1<<i)!=0)
count++;
}
return count;

Alternatively you can use __builtin_popcount(a) for int and __builtin_popcountlll(a) for long
```
```c
To find all subsets of an array in O((2^n)*n) where n is the size of the array;
vector<vector<int>>subsets;
int subsetcount=1<<n;
for(int mask=0;mask<subsetcount;mask++)
  {
  vector<int>subset;
  for(int i=0;i<n;i++)
    {
    if(mask &(1<<i)!=0){
    subset.push_back(v[i]);
    }
    }
    subsets.push_back(subset);
  }
















