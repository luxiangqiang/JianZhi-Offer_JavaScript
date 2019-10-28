---
Time：2019/10/28
Title: 包含 main 函数的栈
Author: 小鹿
---



### 面试题 30：包含 min 函数的栈

定义栈的数据结构，请在该类型中实现一个能够得到栈的最小元素的 min 函数。在该栈中，调用 min、push及 pop 的时间复杂度为 O(1)。



#### 一、思路

创建两个栈，一个是数据栈，一个是辅助栈。

- **入栈：当元素压入数据栈的时候。**
  - 应先判断数据栈是否为空，为空时，将新元素压入数据栈和辅助栈，因为此时元素为最小元素。
  - 如果数据栈不为空，就拿出栈中最小的元素进行比较（辅助栈中顶部元素），小于则该元素同时入两个栈，否则只进入数据栈。

  

- **出栈：当元素出栈的时候。**

  - 如果取出的元素正好是栈中的最小元素，则数据栈和辅助栈同时出栈。
  - 否则，只出栈数据栈。





- **栈中最小元素:**
  - 直接在辅助栈中取出最小元素。



#### 二、测试用例

- 新压入栈的数据比之前大、新压入栈的数据比之前小 —— 普通测试。

- 弹出栈的数字是最小元素、弹出栈的不是最小元素 —— 特殊测试。
- 输入的元素不能为 null —— 输入测试。



#### 三、代码实现

```javascript
// 数据栈
let temp = [];
// 辅助栈
let temp1 = [];

// 出栈
function top1(){
    if(temp.length > 0){
        return temp[temp.length - 1];
    }else{
        return null;
    }
}

// 入栈
function push(value){
    let popValue = top1();
    // 判断是否为第一个数据栈是否有已经存在元素
    // 如果存在，则与栈最小元素进行比较
    // 无数据第一个元素就是最小元素、与辅助栈最小元素比较最小
    if(!popValue || value < temp1[temp1.length - 1]){
        temp.push(value)
        temp1.push(value)
    }else if(value >= temp1[temp1.length - 1]){
        // 如果入栈元素比辅助栈元素大，则只进入数据栈
        temp.push(value)
        temp1.push(temp1[temp1.length - 1])
    }
}

// 出栈
function pop(){
    let popValue = top1();
    // 如果出栈的是最小元素，则两个栈的长度都减一
    if(popValue === temp1[temp1.length - 1]){
        result = temp[temp.length - 1];
        temp.length--;
        temp1.length--;
    }else{
        // 只减数据栈的大小
        temp.length--;
    }
    return popValue;
}

// 取出最小值
function min(){
    return temp1[temp.length - 1];
}

// 测试用例
push(5)
push(1)
push(6)
push(8)
pop()
pop()
console.log(min());
pop();
console.log(min());
console.log(temp)
console.log(temp1)
```













