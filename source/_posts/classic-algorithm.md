---
title: classic algorithm
date: 2023-03-05 15:52:41
tags: ['algorithm'] 
---



# 经典算法

## 链表

### 反转链表

```cpp
class Solution{
public:
	ListNode * reveserList(ListNode* head){
		ListNode *pre = nullptr,next;
		while(head){
			next = head->next;
			head->next = pre;
			pre = head;
			head = next;
		}
		return pre;
	}
}
```

