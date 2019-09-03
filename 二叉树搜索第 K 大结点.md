---
Time：2019/9、3
Title: 二叉树搜索第 K 大节点
Author: 小鹿
---



## 面试题五十四：

给定一棵二叉搜索树，请找出其中的第 K 大节点。



#### 一、思路

要想找到第 K 大结点必要要知道排序，二叉树的前、中、后遍历中的中序遍历就是从小到大排序。然后遍历的同时计数找到第 K 大节点。



#### 二、测试用例

- 完全二叉树、非完全二叉树 —— 普通测试
- 只有左子节点的二叉树、只有右子节点的二叉树、只有一个节点的二叉树 —— 特殊测试
- K 的范围、空树 —— 输入测试



#### 三、代码编写

```javascript
// 求二叉树中第 K 大节点
var kthTallest = function(root, k) {
  let res = []
  // 遍历
  const inorder = (root) => {
    if (root) {
      inorder(root.left);
      res.push(root.val);
      inorder(root.right);
    }
  }
  // 调用
  inorder(root);
  return res[res.length - k]
};

```

