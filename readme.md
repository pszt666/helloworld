#外部排序作业

该程序目前的主要流程分为：
读取test.txt文件，里面存放一些待排序的数据。
生成归并段
1.首先从初始文件中输入MAX_NUM个记录到内存工作区中；


2.从内存工作区中选出关键字最小的记录，将其记为 MINIMAX 记录


3.将 MINIMAX 记录输出到归并段文件中
4.此时内存工作区中还剩余MAX_NUM-1个记录，若初始文件不为空，则从初始文件中输入下一个记录到内存工作区中


5.从内存工作区中的所有比 MINIMAX 值大的记录中选出值最小的关键字的记录，作为新的 MINIMAX 记录

6.
重复过程 3—5，直至在内存工作区中选不出新的 MINIMAX 记录为止，由此就得到了一个初始归并段；


7.重复 2—6，直至内存工作为空，由此就可以得到全部的初始归并段。
8.生成归并段信息输出到duan.txt文件中。


生成哈弗曼树进行归并段合并操作
1.将所有归并段按照从小到大的顺序排序
2.每次取出前MERGE_NUM小的归并段进行合并操作
3.当哈夫曼树只有一个节点时说明该哈夫曼树已经完成，数据排序完毕，然后存储到out.txt


归并段合并
依旧采用败者树来进行归并段的归并。



function.h存储所有函数声明和变量和类声明
function.cpp存储函数定义和变量和类定义
main.cpp包含程序调用

