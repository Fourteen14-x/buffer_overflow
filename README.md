# 环境声明

Ubuntu 16.04-64位

**基本环境安装**

•sudo apt-get install prelink



•Vulnerables 文件夹编译、安装说明  

​	/home/user/proj1/vulnerables（漏洞程序）

​	1.make

​	2.sudo make install



•exploits 文件夹编译说明  

​	/home/user/proj1/exploits（攻击程序）

​	make



**本任务所以实验均在关闭ASLR、NX等保护机制的情况下进行：**

1.关闭地址随机化功能：

echo 0 > /proc/sys/kernel/randomize_va_space2. 

2.gcc编译器默认开启了NX选项，如果需要关闭NX(DEP)选项，可以给gcc编译器添加-z execstack参数。

gcc -z execstack -o test test.c

3.关闭堆栈溢出保护，编译时禁用SSP机制( Stack Smashing Protector )

-fno-stack-protector

 buffer overflow 漏洞利用实践

2.实验内容： 编写exploits攻击漏洞程序

3.实验结果： 获取具有root权限的shell