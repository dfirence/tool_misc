# 反汇编

反汇编(Disassembly)：把目标代码转为[汇编](https://baike.baidu.com/item/汇编/627224)代码的过程，也可以说是把机器语言转换为汇编语言代码、低级转高级的意思，常用于软件破解（例如找到它是如何注册的，从而解出它的注册码或者编写注册机）、外挂技术、病毒分析、逆向工程、软件汉化等领域。学习和理解反汇编语言对软件调试、漏洞分析、OS的内核原理及理解高级语言代码都有相当大的帮助，在此过程中我们可以领悟到软件作者的编程思想。总之一句话：软件一切神秘的运行机制全在反汇编代码里面。



用的静态分析工具是[W32DASM](https://baike.baidu.com/item/W32DASM)、[PEiD](https://baike.baidu.com/item/PEiD)、FileInfo、 [Hex Rays Ida](https://baike.baidu.com/item/Hex Rays Ida)和HIEW等。

反汇编工具如：[OD](https://baike.baidu.com/item/OD)、[IDA Pro](https://baike.baidu.com/item/IDA Pro)、radare2、[DEBUG](https://baike.baidu.com/item/DEBUG)、C32等。

反汇编可以通过反汇编的一些软件实现，比如DEBUG就能实现反汇编，当DEBUG文件位置设置为-u时，即可实现反汇编。 而使用OD实现反汇编时，杀毒软件可能会报告有病毒与木马产生，此时排除即可，且使用OD需要有扎实的基础才能看懂。



基础工具：file， pe tools，peID，nm，ldd，objdump，otool，dumpbin， cfilt，strings，




## misc
可执行文件分析工具，比如PEID啥的，可以分析出EXE文件的内部情况，入口点，数据段，是否加壳等等。
去壳工具。简单的壳官方会提供去壳工具，复杂一点的要手动跟踪去除。
静态反编译工具。从EXE反编译出汇编代码，先大体上看看内部逻辑请款，函数调用，数据等等。
动态跟踪调试工具，比如Ollydog，简称OD。用来跟踪程序的执行过程，下断点，跟踪，找到并且分析软件加密算法，或者通过更改汇编指令改变程序逻辑。
注册机制作工具、补丁制作辅助工具。找到算法并且逆向分析出来了的用注册机制作工具写个注册机出来；通过改汇编代码的写个补丁。比如JE改成JNE之类。
以上是基本要用到的，大一点的软件破解还要用到「文件系统监视工具」「注册表监测工具」「虚拟机」等等，如果你要直接做个破解版应该还要用到「EXE资源修改替换工具」。
然后一定要的知识有：PE原理，汇编语言，算法分析，编程语言。


W32Dasm，它是一个静态反汇编工具，也是破解人常用的工具之一。
Dcwa
