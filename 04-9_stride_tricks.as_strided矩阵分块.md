## 高效分块函数as_strided
    def as_strided(x, shape=None, strides=None, subok=False, writeable=True):
    
numpy中的高效矩阵分块方法：根据给定的shape和strides给ndarray创建一个视图

**重点在于shape（形状）和strides（步长）参数的构造**

## 参数
### x:ndarray

创建一个新的ndarray

### shape

新ndarray的形状，默认为x.shape

shape是一个元组，描述数据的维数

### strides

元组或者ndarray

步长，默认为x.strides.

步长（步幅）的单位是元素数量*itemsize

### subok

bool型，可选。如果为True，则保留子类。

### writeable

bool型，可选。如果设置为False，则返回的数组将始终为只读。

## 返回值
view:ndarray

## 说明

给定确切的步幅，ʻas_strided``创建一个数组视图和形状。 

这意味着它将操纵内部数据结构ndarray，如果操作不正确，则数组元素可以指向无效的内存，可能会破坏结果或使程序崩溃。

建议在以下情况下始终使用原始的x.strides计算新的步伐以避免依赖连续内存布局。

此外，使用此函数创建的数组通常包含self内存重叠，因此两个元素相同。

在这种阵列上的向量化写操作通常是不可预测的。

对于小型，大型，或转置数组。

由于写入这些数组必须经过测试并非常出色注意，您可能要使用``writeable = False''以避免意外写入操作。
