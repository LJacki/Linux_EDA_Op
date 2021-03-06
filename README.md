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

这个VCS使用写的很详细：

https://zhuanlan.zhihu.com/p/127335447



PrimeTime

https://wenku.baidu.com/view/676a1337d5bbfd0a785673a4.html

https://www.jianshu.com/p/30769ce8925a

在文档中找到一个文件：PrimeTime_PX_Tutorials

PT使用中文教程：https://wenku.baidu.com/view/b33455d4360cba1aa811da43.html

所以，需要整理一个Project，做完Sim，DC，和primetime；

## 2021-03-06

linux sed 命令 https://www.runoob.com/linux/linux-comm-sed.html

Linux sed 命令是利用脚本来处理文本文件。

sed 可依照脚本的指令来处理、编辑文本文件。

Sed 主要用来自动编辑一个或多个文件、简化对文件的反复操作、编写转换程序等。

VCS命令行中的-f,-F以及-file参数区别 https://blog.csdn.net/immeatea_aun/article/details/89155349

命令行使用 vcs -full64 -h获得manual可知，三者区别不大，详情如下：

-f <filename>

指定包含源文件和编译时选项的路径名列表的文件。
-F <filename>

与-f选项相同，但允许您指定文件的路径，文件中列出的源文件不必是绝对路径名。
-file filename

此选项适用于使用-f或-F选项指定的文件中的条目可能遇到的问题。 此文件可以包含更多编译时选项和不同类型的文件。 它可以包含用于控制编译和PLI选项和目标文件的选项。 您还可以在此文件中使用转义字符和元字符，例如$，`和！ 等

VCS 常用命令 https://blog.csdn.net/immeatea_aun/article/details/79789838

**需要严格指定file_list中的文件路径以及文件名称，\*.v在verdi命令行操作时候，会无法加载source文件；**

## 压缩

2、tar 命令
tar可以用来打包文件，还可以把特定目录下的全部文件打包成一个总的文件，打包的同时还可以同时使用gzip的功能进行压缩。如果只执行tar命令则压缩后

的文件后缀名是.tar,如果执行gzip命令则压缩后的文件名后缀名是.gz。如果同时执行两个命令则压缩后的文件名是.tar.gz或者简写为.tgz。

比如：tar -zcvf boot.tgz /boot #将/boot目录整合压缩成boot.tgz

参数说明：-z:使用gzip压缩；-c 创建压缩文件；-v 是显式当前被压缩的文件，-f 指使用文件名即boot.tgz。

解压命令：tar -zxvf boot.tgz 

参数说明：-x 是解压的意思

如果解压的同时指定解压目录可以执行以下命令：

tar -zxvf boot.tgz -C /home/dir #需要使用-C参数，后面跟上文件路径。

Linux cp 命令
Linux 命令大全 Linux 命令大全

Linux cp（英文全拼：copy file）命令主要用于复制文件或目录。

语法
cp [options] source dest
或

cp [options] source... directory
参数说明：

-a：此选项通常在复制目录时使用，它保留链接、文件属性，并复制目录下的所有内容。其作用等于dpR参数组合。
-d：复制时保留链接。这里所说的链接相当于Windows系统中的快捷方式。
-f：覆盖已经存在的目标文件而不给出提示。
-i：与-f选项相反，在覆盖目标文件之前给出提示，要求用户确认是否覆盖，回答"y"时目标文件将被覆盖。
-p：除复制文件的内容外，还把修改时间和访问权限也复制到新文件中。
-r：若给出的源文件是一个目录文件，此时将复制该目录下所有的子目录和文件。
-l：不复制文件，只是生成链接文件。
实例
使用指令 cp 将当前目录 test/ 下的所有文件复制到新目录 newtest 下，输入如下命令：

$ cp –r test/ newtest          
注意：用户使用该指令复制目录时，必须使用参数 -r 或者 -R 。

DC的gatecount = total area / the area of NAND2;

把2个PMOS和2个NMOS看成一个面积单元，也就是一个2输入与非门为一个单元，所以DC report_area，并找到对应元件库中的2输入与非门的面积大小（我找不到）；
https://blog.csdn.net/chevroletss/article/details/6082960


