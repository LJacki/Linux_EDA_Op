# Linux_EDA_Op

Record the EDA tool operation.

记录方式还是先在README中记录，然后在整理分档；

查看发行版本：https://blog.csdn.net/szr4630/article/details/79613267

```shell
lsb_release -a
```

centos 7.8;

gedit 显示行号：https://www.cnblogs.com/wq242424/p/6151461.html

快捷键：

Super+R ：打开终端；

Super+J：打开计算器；



Verdi：

https://blog.csdn.net/kevindas/article/details/79008106

需要指定 -P

```bash
vcs	-full64 *.v \
	-debug_all \
	-R \
	-timescale=1ns/1ps \
	-P	/home/eda/synopsys/verdi/Verdi_O-2018.09-SP2/share/PLI/VCS/linux64/novas.tab \
		/home/eda/synopsys/verdi/Verdi_O-2018.09-SP2/share/PLI/VCS/linux64/pli.a 
	-l compile.log
```



