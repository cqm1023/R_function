### 1. 语法

nchar()函数的基本语法是：

```shell
nchar(x)
```
功能：返回位置上字符的长度

### 2.解释
```R
对象：x或者向量
```

### 3. 示例

```R
nchar(c(1,2,3,4,5))
[1] 1 1 1 1 1
> tmp <- data.frame(a=c(1,10,20),b=c("a","b","c"))
> tmp
   a b
1  1 a
2 10 b
3 20 c
> nchar(tmp$a)
[1] 1 2 2
```
### 4. 与length区别
```R
> length(c(1,2,3,4,5))
[1] 5
> length(tmp$a)
[1] 3
```
