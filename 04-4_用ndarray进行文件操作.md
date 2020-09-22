一般采用Pandas来进行此类操作，NumPy也有相关功能，读写npy格式文件或压缩的npz文件
# 文件操作
## 写入
    arr = np.arrange(10)
    np.save(path,arr)
## 读取
    np.load(path)
## 将多个数组文件压缩在一个文件中
    np.savez(path_name,a=arr1,b=arr2)
## 对已保存的压缩文件追加数据
    np.savez_comparessed(path_name,a=arr1,b=arr2)
    #a、b为自己定义的标志变量
