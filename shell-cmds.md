## 常用shell命令

### cat
#### 查看文件
```
cat file
```
### 将std输出重定向到文件
```
cat file*.txt > concated.txt
```

### 合并输出+控制先后顺序
```
printf输出在cat前
printf "A\tB\tC\t\n" | cat - file
printf输出在cat后
printf "A\tB\tC\t\n" | cat file -
```

### 挤压连续空行
```
n行空行变为1行空行
printf "A\t\n\n\n\nB\t\n\nC\t" | cat -s
```

### 显示行数
```
cat -n file
仅显示非空行函数，空行不计入行数
printf "A\t\n\n\n\nB\t\n\nC\t" | cat -sb
```
### 查看特殊字符
```
行尾用$标识
cat -E file
tab用^I标识
cat -T file
```