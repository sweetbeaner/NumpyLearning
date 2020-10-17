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

## 定义
    numpy.einsum(subscripts, *operands, out=None, dtype=None, order='K', casting='safe', optimize=False)
    
## 参数

+ subscripts : str，指定求和的操作，可以是多个，用逗号分开。除非包含显式指示符“->”以及精确输出形式的下标标签，否则将执行隐式（经典的爱因斯坦求和）计算。
+ operands : list of array_like，输入。
+ out : ndarray, optional，指定输出。
+ dtype : {data-type, None}， optional，可以指定运算的数据类型，可能需要用户提供类型转换接口。默认为None。
+ order : {‘C’, ‘F’, ‘A’, ‘K’}， optional，控制输出的内存布局。'C'=contiguous；'F'=Fortran contiguous；'A'表示输入为'F'时输出为'F'，否则输出为'C'；'K'表示输出的layout应该尽可能和输入一致。
+ casting : {‘no’, ‘equiv’, ‘safe’, ‘same_kind’, ‘unsafe’}， optional，指定可能发生的数据类型转换，不推荐使用'unsafe'。
+ ‘no’ 表示不做数据类型转换。
+ ‘equiv’ 表示仅允许字节顺序更改。
+ + ‘safe’ 表示只允许保留值的强制类型转换。
+ ‘same_kind’ 表示仅允许安全类型转换或同一类型（例如float64到float32）内的类型转换。
+ ‘unsafe’ 表示可以进行任何数据转换。
+ optimize : {False, True, ‘greedy’, ‘optimal’}, optional，控制是否进行中间优化。默认False，不做优化；设为True则使用greedy算法。还接受np.einsum_path函数的提供的列表。


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
