NumPy的核心————多维数组对象ndarray
# 一、基本操作
## 1.导入NumPy

    import numpy as np
    
## 2.建立ndarray

    data = np.random.randn(2,3) 
    
## 3.维度数量、维度与类型

    data.shape
    data.dtype
    data.ndim
    
# 二、生成ndarray
## 1.使用array函数，以序列性对象为参数，进行传值
    list=[1,2,3,4,5]
    arr1 = np.array(list)
    print(arr1)
## 2.支持列表嵌套模式
    list=[[1,2,3,4,5],[6,7,8,9,10]]
    arr1 = np.array(list)
    print(arr1)
## 3.数组生成函数
+ np.array(容器)：根据输入数据生成一个ndarray
+ np.asarray()：将输入转换为ndarray
+ arange()：内建函数range返回一个数组（一维）
+ ones()：给定形状和数据类型生成一个全1的ndarray
+ ones_like()：根据数组生成一个形状一样的1的ndarray
+ zeros()：给定形状和数据类型生成0的ndarray
+ zeros_like()：给定数据生成同样形状全0的ndarray
+ empty()：给定形状和数据类型生成空的ndarray
+ enpty_like()：给定数据生成同样形状空的ndarray
+ empty()：给定形状和数据类型生成指定数值的ndarray
+ enpty_like()：给定数据生成同样形状指定数值的ndarray

# 三、ndarray的数据类型
dtype：特殊的对象，表示一个ndarray的某一种类型。

dtype是NumPy能够与其他数据交互的原因
## 1.ndarray的数据类型转换
转换后生成一个新的ndarray
    data.astype(np.float654)
# 四、ndarray的数组算数
+ ndarray的算数运算是按位运算，并非线性代数中的矩阵运算。
+ ndarray的运算需要尺寸相同，否则会设计广播特性。

# 五、基础索引与切片
## 切片的性质
+ 用于选择某个数据子集或者某个元素，返回视图
+ 对ndarray的索引进行操作，也会作用在原ndarray上
+ NumPy是对数据的管理，不产生过多复制，想复制数据也用arr[切片].copy()
+ 高维ndarray可以通过arr[i,j]来选择第i行、j列个元素，也可以按arr[x:y,m,n]来进行行、列的切片

# 六、布尔索引
用布尔结果对ndarray进行切片，保留True的元素
+ 返回结果为切片的拷贝，编辑对原ndarray的值没有影响

# 七、神奇索引
用于使用整数数组对ndarray进行数据索引
+ 神奇索引可以选出包含指定顺序的结果，使用列表或数组
+ 用负的值索引，从尾部进行选择
arr[[列表]]
+ 对于多维矩阵，如二维矩阵，则按多个列表进行索引，每个列表的每列为一个定位坐标，定位到ndarray的元素

# 八、数组转换和换轴
转置是数组的特殊重组形式，不复制任何内容，仅仅是建立一个索引

arr.T是transpose的一个特例，transpose可以对矩阵的轴进行转置

    arr.T
    arr.transpose()
    
对矩阵进行转置，如转置后做点乘，求矩阵的内积

   arr.swapaxes()
可对轴进行转置
