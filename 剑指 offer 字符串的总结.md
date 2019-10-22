## 剑指 offer 字符串的总结

### 一、解题思路总结

#### 1、最低级思路 —— 暴力破解

通过对字符串题的总结，使用暴力破解法是最低级的方法，也是效率最低的方法，按照正常的思路遍历字符串的字符进行解决问题。

- 基本所有题型都会有一个暴力破解法



#### 2、哈希表法

很多字符串题目涉及到次数的，我们一听到次数，就立马想到用哈希表统计次数，然后进行下一步的处理，哈希表这种数据结构，一般键用来存储字符，值用来统计次数，而且操作数据的时间复杂度为 n(1)。所以借助哈希表能让你快速的解决问题的关键，而且效率也会得到大幅度提升。

- [第一次只出现一次的字符串]([https://github.com/luxiangqiang/JianZhi-Offer_JavaScript/blob/master/%E7%AC%AC%E4%B8%80%E4%B8%AA%E5%8F%AA%E5%87%BA%E7%8E%B0%E4%B8%80%E6%AC%A1%E7%9A%84%E5%AD%97%E7%AC%A6%E4%B8%B2.md](https://github.com/luxiangqiang/JianZhi-Offer_JavaScript/blob/master/第一个只出现一次的字符串.md))



#### 3、字符串转化数组更易解决

字符串的一些提醒，我们可以将字符串转化为数组操作，为什么呢？虽然字符串的自带的操作方法很多，但是有些不如数组方便，通常可以使用 `split` 方法将字符串转化为数组再操作，因为这样可以使用一些数组的方法，比如反转数组等。

- [翻转字符串]([https://github.com/luxiangqiang/JianZhi-Offer_JavaScript/blob/master/%E5%8F%8D%E8%BD%AC%E5%AD%97%E7%AC%A6%E4%B8%B2.md](https://github.com/luxiangqiang/JianZhi-Offer_JavaScript/blob/master/反转字符串.md))



#### 4、递归

通常字符串题型用到递归，递归的使用条件，将大问题分解为小问题，而且大问题的解决方式和小问题的解决方法相同，这样使用递归更加的方便。

- [字符串的排列]([https://github.com/luxiangqiang/JianZhi-Offer_JavaScript/blob/master/%E5%AD%97%E7%AC%A6%E4%B8%B2%E7%9A%84%E6%8E%92%E5%88%97.md#%E4%BA%8C%E6%B5%8B%E8%AF%95%E7%94%A8%E4%BE%8B](https://github.com/luxiangqiang/JianZhi-Offer_JavaScript/blob/master/字符串的排列.md#二测试用例))



### 二、测试用例

通过以上题目中，我将测试用例分为三大种，测试代码的时候，在这三大种进行想就可以了。

- **普通测试**
- **特殊测试**
- **输入测试**



#### 1、普通测试

> 根据题目的要求，进行简单测试，比如输入多个字符、带空格的字符等。



#### 2、特殊测试

> 进行特殊情况的处理，比如输入一个字符，所有字符都是唯一的字符、所有字符相同的字符串等特殊情况。



#### 3、输入测试

> 一般为输入空指针 null 和空字符串进行测试。

