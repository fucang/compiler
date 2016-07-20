                                       编译器的构建流程
编译器编写的三个步骤：
1、词法分析器：用于将字符串转化成内部的表示结构
2、语法分析器：将词法分析得到的标记流（token）生成一颗语法树
3、目标代码的生成：将语法树转化成目标代码

自己实现的过程：
1、构建自己的虚拟机以及指令集，之后生成的目标代码便是我们的指令集
2、构建我们的词法分析器
3、构建语法分析器

编译器的框架
编译器主要包括4个函数：
1、next()用于词法分析，获取下一个标记，它将自动忽略空白字符
2、program()语法分析的入口，分析整个C语言程序
3、expression(level)用于解析一个表达式
4、eval()虚拟机的入口，用于解释目标代码
因为表达式在语法分析中相对独立并且比较复杂，所以我将它单独作为一个函数。

实现一个简单的编译器，什么都不做。
main()函数就是读取一个源代码文件，逐个读取每个字符，并输出每个字符。然后调用以上四个函数。见代码comp1.c


