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
18.To count total no of bits in a binary rep of a no. n=log2(n)+1 if n>0;
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

To find all subsets of an array in O((2^n)*n) where n is the size of the array;
```c
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

```
To add two binary numbers=>make cases
```c
 string addBinary(string a, string b) {
        string ans;
        reverse(a.begin(),a.end());
        reverse(b.begin(),b.end());
        char c='0';
        char ip;
        int i;
        for(i=0;i<min(a.length(),b.length());i++)
        {
            if(a[i]=='1' && b[i]=='1')
            {
                if(c=='1')
                {
                    ip='1';
                    c='1';    
                }
                else
                {
                    ip='0';
                    c='1';
                }
            }
            else if((a[i]=='1' && b[i]=='0') || (b[i]=='1' && a[i]=='0'))
            {
                if(c=='1')
                {
                    ip='0';
                    c='1';
                }
                else
                {
                    ip='1';
                    c='0';
                }
            }
            else
            {
                if(c=='1')
                {
                    ip='1';
                    c='0';
                }
                else
                {
                    ip='0';
                    c='0';
                }
            }
            ans+=ip;
        }
for (; i < a.length(); i++)
        {
            if (a[i] == '1')
            {
                if (c == '1')
                    ans.push_back('0');
                else
                    ans.push_back('1');
                    
            }
            else
            {
                if (c == '1')
                {
                    ans.push_back('1');
                    c = '0';
                }
                else
                    ans.push_back('0');
            }
        }
        for (; i < b.length(); i++)
        {
            if (b[i] == '1')
            {
                if (c == '1')
                    ans.push_back('0');
                else
                    ans.push_back('1');
                    
            }
            else
            {
                if (c == '1')
                {
                    ans.push_back('1');
                    c = '0';
                }
                else
                    ans.push_back('0');
            }
        }
        if(c=='1')
        ans+='1';
        reverse(ans.begin(),ans.end());
        return ans;
    }
```













