## task 3

### 题目
支持syzkaller for linux工具

### 描述
目前内核赛道参赛队实现的OS能够支持Linux应用，所以需要在参赛队自己写的内核上支持运行[syzkaller for linux](https://github.com/google/syzkalle)这个内核测试工具。

### 对内核的具体要求
参考[syzkaller的工作流程](https://github.com/google/syzkaller/blob/master/docs/internals.md)。硬件环境是qemu for riscv64。总分100分。
1. 【10分】支持sshd for linux运行
2. 【15分】支持syz-fuzzer for linux运行
3. 【15分】支持syz-executor for linux运行
4. 【10分】参考/sys/kernel/debug/kcov的输出，直接给出类似格式的输出(不需要实现kcov功能)
5. 【15分】实现linux的kcov功能支持，能够产生类似/sys/kernel/debug/kcov的输出
6. 【35分】完整运行syzaller，完成设计实现与执行过程分析报告

### 参考
- [kcov](https://www.kernel.org/doc/html/latest/dev-tools/kcov.html)
- [How syzkaller works](https://github.com/google/syzkaller/blob/master/docs/internals.md)
- [Adding new OS support for syzkaller](https://github.com/google/syzkaller/blob/master/docs/adding_new_os_support.md)
- Syzkaller 源码分析(1)-(5)：[1](https://xz.aliyun.com/t/5079)、[2](https://xz.aliyun.com/t/5098)、[3](https://xz.aliyun.com/t/5154)、[4](https://xz.aliyun.com/t/5223)、[5](https://xz.aliyun.com/t/5401)
- [syzkaller on freebsd](https://freebsdfoundation.org/wp-content/uploads/2021/01/Kernel-Fuzzing.pdf)
- [从0到1开始使用syzkaller进行Linux内核漏洞挖掘](https://bbs.kanxue.com/thread-265405.htm)
- [fuzzing-tutorial经典论文/书籍/博客等](https://github.com/liyansong2018/fuzzing-tutorial)
