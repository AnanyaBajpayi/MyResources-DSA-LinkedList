19/6/2023

### LINKED LIST

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

7.Delete the middle element
```c
Use 3 pointers fast,slow and prev initialised to head,head and null respectively and move them in a way that when fast reaches the end ,slow reaches the middle and prev reaches one before middle. Now,change the links of prev and delete slow.
```

8.Remove duplicate elements
```c
Use prev and curr and loop until curr becomes null
if(prev->data==curr->data)
     {
         Node* temp=curr;
         prev->next=curr->next;
         curr=curr->next;
         delete(temp);
     }
     else{
         prev=curr;
         curr=curr->next;
     }
```

9.Nth node from end
```c
Two approaches
1.Traverse and find the length l of the linked list and get n-l+1 th element from start
2.Use fast and slow pointer and move fast ahead by n nodes.Now when fast reaches the last element or goes out slow will point at the required element
Code:
           if(n==getlen(head))return head->data;
           if(head==NULL || head->next==NULL)return -1;
           Node *fast=head;
           Node *slow=head;
           int count=1;
           while(count<n)
           {
               if(fast->next==NULL)return -1;
               fast=fast->next;
               count++;
           }
           while(fast!=NULL && fast->next!=NULL)#both are being checked in order to include even and odd cases
           {
               count++;
               slow=slow->next;
               fast=fast->next;
           }
           if(n<count)
           return(slow->data);
           else
           return -1;

           Here getlen(head)gives length of the linked list 

```

10.To rotate an linkedlist right by k positions=>We take a pointer at tail and tailprev,loop till k after every rotation make the tail as head,tailprev->next=NULL
and make the tail new head
```c
int getlength(ListNode* head1)
    {
        int count=1;
        while(head1->next!=NULL)
        {
            count++;
            head1=head1->next;
        }
        return count;
    }
    ListNode* rotateRight(ListNode* head, int k) {
        if(head==NULL || head->next==NULL)return head;
        int l=getlength(head);
        k=k%l;
    for(int i=1;i<=k;i++)
    { 
        ListNode* tail=head;
        ListNode* tailprev=NULL;
        while(tail->next!=NULL)
        {
            tailprev=tail;
            tail=tail->next;

        }
        tail->next=head;
        tailprev->next=NULL;
        head=tail;
    }
    return head;
    }
```
