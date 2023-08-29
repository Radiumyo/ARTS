# ARTS Week 2

## Algorithm

```Python
# 206. Reverse Linked List
# class ListNode:
#     def __init__(self, val=0, next=None):
#         self.val = val
#         self.next = next
class Solution:
    def reverseList(self, head: Optional[ListNode]) -> Optional[ListNode]:
        cur =  head
        pre = None
        while cur:
            tmp = cur.next
            cur.next = pre
            pre = cur
            cur = tmp
        return pre
```



## Review

Coordinate Frames
-link https://w3.cs.jmu.edu/spragunr/CS354_F22/readings/frames.pdf


## Technique/Tips

### 分享一个十分好用的划词软件——沙拉查词


```
https://saladict.crimx.com/
```


## Share

最近在业务工作和生活中，会有意识地查阅“一手资料”

#### 为何“一手资料“如此重要？
- 有时高度提炼的信息并未包含你所要获取的信息，这就意味着要花更多的时间去查阅你所要的信息
- 在上下游沟通中，每级的传递都可能带来信息丢失，甚至会有错误的信息干扰，这使得找到”源头信息“”数据来源“十分重要

#### 如何养成查阅“一手资料”的习惯？
- 珍爱生命，远离百度（可换成Google/ecosia等国外搜索引擎）
- 养成翻阅论文/官网/技术文档/GitHub的习惯，CSDN/知乎/简书等知识交流网站仅作为补充
