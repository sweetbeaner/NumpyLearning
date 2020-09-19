# 数据结构和序列
python数据结构简单强大
## 元组
固定长度，不可变，可嵌套，可拆包（赋值给多个变量）

tup = 4,5,6
即为(4,5,6)

元组.count(变量)函数，统计变量出现的次数
## 列表
可变长度，可变内容

list = [1,2,3,4]

list[index]取值

+ append(元素)增加元素
+ insert(index,元素)插入元素
+ pop(index)删除元素
+ remove(元素)移除第一个出现的元素
+ extend(列表)，list联合其他列表，for循环效率更好
+ sort()排序
+ bisect.bisect(list,'元素')二分搜索
+ bisect.insort(list,'元素')已排序列表的维护
+ list[sta:end] 切片，取列表[sta,end)中间的值

## 内置序列函数
python内置的操作序列的函数，可以直接调动的函数
+ enumerate(集合) 遍历序列同时获得当前元素的索引，可用于构建字典
+ sorted(集合) 对列表进行排序
+ zip(集合,集合2) 对列表或元组的元素进行配对，形成一个新的元组列表，也可以用于已配对的元组的拆分
+ reversed(集合) 对集合中的元素进行倒序排列
## 字典
最重要的内置数据结构，键值对，值可嵌套
dict = {'name':'chen','age':18}
+ pop、del删除键值
+ dict['键']=值 插入或设置元素
+ keys、values 输出键或者值，list()转化为列表
+ update 合并字典
+ 序列生成字典dict(序列1,序列2)，序列1为键，2为值
+ 字典默认值defaultdict(list)
+ 可哈希化的字典键才有效
## 集合
