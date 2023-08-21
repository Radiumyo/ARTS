# ARTS Week 1

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

The Inner Game of Tennis - The Discovery of the Two Selves

- 提高网球或任何办事效率的关键是：发现self1(有显著意识的以语言思维为主要特征的自我) 和 self2(无意识的本能的自我) 之间的关系
- 一般来说self1为命令发出者，self2为操作者
- 要想self1和self2合二为一，需要掌握以下技能(the art of concentration)：
  1. 对于想要得到的结果，必须要有一个清晰的画像
  2. 学会相信self2，相信它能做出最好的表现，并有从失败中获取经验的能力
  3. 要学会不要“偏心”地观察一件事情(单纯观察发生了什么，不带任何评价)

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
