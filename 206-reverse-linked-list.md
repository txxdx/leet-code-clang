```c
/**
 * Definition for singly-linked list.
 * struct ListNode {
 *     int val;
 *     struct ListNode *next;
 * };
 */


struct ListNode* reverseList(struct ListNode* head){    
    struct ListNode* cur = head, *prev = NULL;
    
    while (cur) {
        struct ListNode* next = cur->next;
        if (next == NULL) head = cur;
        cur->next = prev;
        prev = cur;
        cur = next;
    }
    
    return head;
}

```

