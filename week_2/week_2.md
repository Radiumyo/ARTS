# ARTS Week 2

## Algorithm

```Python
# Definition for singly-linked list.
# class ListNode:
#     def __init__(self, val=0, next=None):
#         self.val = val
#         self.next = next

# for if 执行

class Solution:
    def reverse(self, a, b):
        pre, cur, nxt = None, a, a
        while cur != b:
            nxt = cur.next
            cur.next = pre
            pre = cur
            cur = nxt
        return pre
    
    def reverseKGroup(self, head: Optional[ListNode], k: int) -> Optional[ListNode]:
        if not head:
            return head
        a, b = head, head
        for i in range(k):
            if not b:
                return head
            b = b.next

        newhead = self.reverse(a,b)
        a.next = self.reverseKGroup(b,k)
        return newhead

        return pre
```



## Review
```
Coordinate Frames
https://w3.cs.jmu.edu/spragunr/CS354_F22/readings/frames.pdf
```
-主要介绍了三种坐标系：世界坐标系、相机坐标系、图像坐标系


## Technique/Tips

### 分享一个找数据集的网站-超神经


```
https://hyper.ai/datasets
```


## Share

最近在业务工作和生活中，会有意识地查阅“一手资料”

#### 为何“一手资料“如此重要？
- 有时高度提炼的信息并未包含你所要获取的信息，这就意味着要花更多的时间去查阅你所要的信息
- 在上下游沟通中，每级的传递都可能带来信息丢失，甚至会有错误的信息干扰，这使得找到”源头信息“”数据来源“十分重要

#### 如何养成查阅“一手资料”的习惯？
- 珍爱生命，远离百度（可换成Google/ecosia等国外搜索引擎）
- 养成翻阅论文/官网/技术文档/GitHub的习惯，CSDN/知乎/简书等知识交流网站仅作为补充
