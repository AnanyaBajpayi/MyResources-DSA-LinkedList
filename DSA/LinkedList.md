19/6/2023

###LINKED LIST

---
1. Middle element
```c
2 approaches
1. Naive approach - Find n and then return n/2 and n/2+1
2. Fast and slow pointer(return slow pointer when fast==NULL or fast->next==NULL)
```

2. Deleting a node
```c
Traverse till the pointer before the element to be deleted and change the links.....diff condition for deletion at head
```

3. Binary to Decimal
```c
Traverse the linked list and concatenate the binary string.
```

4. Delete multiple nodes in a linked list
```c
Used stack implementation or a reverse based approach, (MARKED)
```

5. Swap Nodes in Pair
```c
Use recursive approach, 
class Solution {
public:
    ListNode* swapPairs(ListNode* head) {
        if(head==NULL||head->next==NULL){
            return head;
        }
        ListNode* temp=head->next;
        head->next=swapPairs(head->next->next);
        temp->next=head;
        return temp;
    }
```

6.Reverse a Linked List
```c
Use 3 pointers prev,curr,next and change links accordingly.
```
