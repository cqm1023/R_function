### 1.查看目录与文件

```R
  getwd()  # 查看当前工作目录
  list.dirs() # 查看当前目录的子目录
  dir() #查看当前目录的子目录和文件
  list.files()# 同上
  dir(path = ".") #查看子目录和文件
  file.info(".") #查看当前目录的信息
  
eg：
> dir(path = ".", pattern = "*R")
[1] "0.Rproj"     "1.downloa.R"
> dir(path = ".", pattern = "*R$")
[1] "1.downloa.R"
eg:
list.files(path = ".", pattern = NULL, all.files = FALSE,
           full.names = FALSE, recursive = FALSE,...)
```

### 2.检查目录和文件

```R
> file.exists("./other") #检查目录/文本是否存在
[1] FALSE

eg:
if(!file.exists("./raw_data")) dir.create("raw_data")
```

用`file_test()`可以判断是一个目录还是文件。。。。。

### 3.创建目录和文件

创建目录使用`dir.create()`；当创建多级目录时，设置参数recursive = TRUE。
创建空文件使用`file.create()`

其他

```	R
Usage

file.create(..., showWarnings = TRUE)
file.exists(...)
file.remove(...) # 删除目录，or unlink
file.rename(from, to) # file.rename("T1", "T2")
file.append(file1, file2)
file.copy(from, to, overwrite = recursive, recursive = FALSE,
          copy.mode = TRUE, copy.date = FALSE)
file.symlink(from, to)
file.link(from, to)
Sys.junction(from, to)
system("tree") # 查看目录结构,== linux的tree
```