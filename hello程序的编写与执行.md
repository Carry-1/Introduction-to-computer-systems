# 1. 编写源文件  
&emsp;&emsp;用程序编辑器编写好源文件hello.c,源文件在计算机中以ASII形式存放，属于文本文件，可显示可读。
# 2. 对源文件进行编译链接生成可执行文件
&emsp;&emsp;在Unix系统中可用GCC编译器对源文件进行编译。命令如下：
unix >gcc -o hello.c
unix>为shell命令行解释器的命令提示符，shell命令行解释器会根据我们输入的命令调用对应的程序，因此输入gcc之后就是调用编译器对源文件进行编译链接并生成可执行文件，保存在磁盘上。
# 3.程序执行
&emsp;&emsp;1、2两步中以及生成了可执行文件，此时可再次使用shell命令行解释器来运行可执行文件hello，即在命令行提示符之后输入./hello
格式如下：
unix>./hello
其中，“./hello”就是可执行文件在磁盘上的路径名，其中"./"表示当前目录。按下[Enter]键表示命令输入结束。
shell程序会将用户从键盘输入的每一个字符逐一读到CPU的寄存器中，然后再保存到主存中，直到**接收到[Enter]按键时，shell程序将调出操作系统内核服务程序**（所以shell程序中有系统调用，从而让CPU陷入内核态）来加载磁盘上的可执行文件hello到主存，内核加载完可执行文件中的代码和所要处理的数据之后，将hello程序第一条指令地址送到PC，CPU永远都是根据PC的内容去取指并执行。因此，随后CPU开始执行hello程序，它将“hello，world！”字符串从主存送到CPU寄存器，再送到显示器中显示。
