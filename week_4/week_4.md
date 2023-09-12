# ARTS Week 4

## Algorithm

```Python
#1123. 最深叶节点的最近公共祖先
# Definition for a binary tree node.
# class TreeNode:
#     def __init__(self, val=0, left=None, right=None):
#         self.val = val
#         self.left = left
#         self.right = right

class Solution:
    def lcaDeepestLeaves(self, root: Optional[TreeNode]) -> Optional[TreeNode]:
        def dfs(root):
            if root is None:
                return None, 0
            l, d1 = dfs(root.left)
            r, d2 = dfs(root.right)
            if d1 > d2:
                return l, d1 + 1
            if d1 < d2:
                return r, d2 + 1
            return root, d1 + 1

        return dfs(root)[0]
```



## Review
```
How 9/11 Taught Me To Stop Saying ‘Everything Will Be Okay’
https://medium.com/@JaySillings/how-9-11-taught-me-to-stop-saying-everything-will-be-okay-90195fb52c86
```

## Technique/Tips
### 关于AWS/Ceph的坑
```
如果aws s3 ls 后查看不到对应的bucket或报错，可以先在后面加上--debug，确保读取的ak/sk和对应的集群地址（ip地址）无误
```

## Share
#### 最近在读《人件》，以下是一些零碎的读书笔记
如何毁掉团队
	防御式管理
		一直有backup
		不信任手下
		错误地使用不信任
		常见方法
			程式化的方法论
			管理者的技术干涉
	官僚主义
		无需思考的文案工作
	物理分隔
		交互不影响，交流会受影响
	时间碎片
		一人兼顾多个任务，时间花在角色互换
	牺牲产品质量
		意为牺牲团队的自我认知
	伪造截止日期
		如ASAP 必须xxx完成，说了等于没说
	团伙控制
	！！！
		贬低工作或做工作的人
			励志小附件
		加班
			目的：避免指责
	内部竞争
		年度薪酬评审
		目标管理法MBO
		表彰个别员工的突出成就
		跟绩效相关的证书、奖励、现金
		任何形式的考核
	团队对工作产品的集体所有权（五）
		团队中取得的任务成就仅出自于团队中的一员，而不是整体的成就
		管理者之间竞争，有利可图就抢，抢不过就破坏

如何形成团队的化学反应
	建立对质量的追求
	提供诸多满意的闭环
	建立精英意识
		大家会在不受管理的团队中展现独特性
	允许和鼓励差异性
	维护和保护成功团队
	提供技术策略而不是技术方向

方法学
	疯狂的方法学
		没完没了的文案
		少得可怜的可行的方法
		从来没有责任心
		消磨殆尽的热情
	方法收敛：是个好事情，但并非唯一
		副作用
			维法者强力推进
			脑力劳动者强烈的自主意识
		途径
			培训
			工具
			同行评审

风险
	虚假的风险
		不允许发生风险
		将期望获得的结果说成是挑战，让给团队尽可能廉价地完成项目
		边际收益，但忽略时间安排上的管理
	真正的风险
		确保风险发生时有相应的应对措施

人生短暂，如果你需要知道所有才能的工作，你可能走不了多远

组织型学习
	将新技能传授给员工
		会直接带来人力成本的增加，如果接受培训的员工离开，投资就会泡汤
	以另一种方式运作
		会临时性的存储在相关人员的大脑，最终会变成整个组织的知识储备
	何处开展？
		组织的顶层？
			他们并不会关心日常事务
		组织的底层？
			受限于他们所在的边界，有些时机会视而不见
		中间管理层？
			√，成功的学习型组织会有一支非常强大的中间管理层
		中间管理层需要相互交流，并在一起高效融洽地工作（rARE
