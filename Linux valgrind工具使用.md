#### valgrind安装

```shell
apt install valgrind
```

out为编译文件，编译选项有-g

#### memcheck

内存泄漏等内存问题

```shell
valgrind --tool=memcheck --log-file=memcheck.log --leak-check=yes  ./out
```

#### cachegrind

缓存分析器

```shell
valgrind --tool=cachegrind ./out
callgrind_annotate cachegrind.out.pid | grep -v “???” > cachegrind.log
```

cachegrind.out.pid为cachegrind工具的输出文件，pid替换为真实值。

#### callgrind

函数分析器

```shell
valgrind --tool=callgrind ./out
#线程分离
valgrind --tool=callgrind --separate-threads=yes ./out
callgrind_annotate callgrind.out.pid | grep -v “???” > callgrind.log
```

callgrind.out.pid为callgrind工具的输出文件，pid替换为真实值。

#### massif

内存分析器

```shell
valgrind --tool=massif ./out
```

可视化查看工具

```shell
sudo apt install massif-visualizer
massif-visualizer massif.out.pid
```

massif.out.pid为massif工具的输出文件，pid替换为真实值。

#### Helgrind

多线程分析器（暂时未使用）

```shell
valgrind --tool=helgrind ./out
```





