# Einsum()爱因斯坦标记法

    Einsum:Einstein summation convention
  
爱因斯坦求和约定，爱因斯坦标记法，省去求和符号。
可以替代但不限于以下函数：

+ 矩阵求迹：trace
+ 求矩阵对角线：diag
+ 张量（沿轴）求和：sum
+ 张量转置：transopose
+ 矩阵乘法：dot
+ 张量乘法：tensordot
+ 向量内积：inner

使用爱因斯坦求和约定，可以以简单的方式表示许多常见的多维线性代数数组运算。

## 张量

+ 零维张量：标量 1
+ 一维张量：矢量 [1,2,3,4]^T
+ 二维张量：矩阵 [[1,2,3],[4,5,6],[7,8,9]]
+ 三维张量：矩阵数组 P
+ 四维张量：矩阵数组的矢量(?) [P1,P2,P3]^T
+ ......


## 函数的定义

    einsum(equation, *operands)
    
equation:字符串表达式
operands:操作数

**是一个元组参数，并不是只能有两个，所以只要是能够通过einsum标记法表示的乘法求和公式，都可以用一个einsum解决**
