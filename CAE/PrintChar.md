###用机器码显示字符

这是本章的第一个任务，我们先来了解一下背景信息，并且学习一下基础知识。

####背景信息

#####Intel 8086与IBM PC

8086处理器是Intel在1970年代推出的16位通用处理器。学习本节的过程中，你需要思考一下“16位”的含义。8086奠定了Intel的x86系列的辉煌。

IBM PC机是IBM公司推出的计算机系统。最早的型号在1981年推出，围绕Intel 8088处理器（8086的廉价版）建造。IBM PC一直延续到现在，现在的绝大多数台式和笔记本电脑都是PC机（IBM PC兼容机）。

{一直保持的兼容性(即使x86、x86_64系统)，最易获得的实验平台}

{虚拟机软件对PC的模拟很成熟，比如VMWare虚拟机也能满足实验需求}

######阅读资料

通用处理器：[https://www.zhihu.com/question/20647938](https://www.zhihu.com/question/20647938)

IBM PC：[https://zh.wikipedia.org/wiki/IBM_PC](https://zh.wikipedia.org/wiki/IBM_PC)

#####PC引导过程与MBR

{MBR被原样复制到内存某处执行；必要的55AA标志}

######阅读资料

MBR维基百科页面：[https://zh.wikipedia.org/wiki/%E4%B8%BB%E5%BC%95%E5%AF%BC%E8%AE%B0%E5%BD%95](https://zh.wikipedia.org/wiki/%E4%B8%BB%E5%BC%95%E5%AF%BC%E8%AE%B0%E5%BD%95)

####本节需要的基础知识

#####二进制及十六进制表示无符号数

{知道怎么转换，熟练使用Windows计算器“程序员”模式}

{一个十六进制位能表示4个二进制位；字节，字，双字，四字，分别对应多少二进制位，多少十六进制位}

{记住65536以内的2的整数次幂，记住2^32的数量级}

#####存储程序原理与冯·诺伊曼结构

{简化的计算机宏观结构（CPU、内存、IO设备的三角关系）}

{图灵完全：存储程序式结构不是必然的——元胞自动机}

#####8086的寄存器与指令集

{网上有大量的介绍}

{最权威最精确最全面的信息来源，Intel手册，8086手册很难找，一般人我不告诉他}

######参考资料

[The 8086 Family User‘s Manual](https://archive.org/details/bitsavers_intel80869lyUsersManualOct79_62967963)

#####进行下一步的两种方式

{两种指令，顺序与跳转}

#####结构化程序

{局部跳转与调用跳转，子程序}

#####中断调用

{PC引导环境，其中的子程序调用方案：中断调用}

######参考资料

[Ralf Brown's Interrupt List](http://www.ctyme.com/rbrown.htm)

####目标

用机器码写一个PC引导程序并运行，在屏幕上显示一个字符“A”。

{三步：填充参数、执行调用、无限循环}

{最少可仅用三种指令：mov、int、jmp}

{int 10h/AH=0Ah}

#####8086指令的编码格式

{Intel 8086手册}

{Intel x86最新手册}

[X86指令编码的那些事儿](http://ytliu.info/blog/2016/12/10/x86zhi-ling-bian-ma-de-na-xie-shi-er/)

[http://www.ee.hacettepe.edu.tr/~alkar/ELE414/](http://www.ee.hacettepe.edu.tr/~alkar/ELE414/)第三个附件（8088/8086 Instruction Set, Machine Codes, Addressing Modes）

#####实验用虚拟机文件

[VMWare虚拟机存档](./CAE.VMWare.7z)

#####十六进制编辑器WinHex

{}

####答案

{}
