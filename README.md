# Median Filter
An embedded friendly, fast one-dimensional median filter algorithm implementation in C and C++

Useful for spike and noise removal from analog signals or other DSP

Also known as "salt-and-pepper noise" or "impulse noise" filter

这个仓库名为 MedianFilter，提供了一个用 C 和 C++ 实现的嵌入式友好、快速的一维中值滤波算法。 该算法可用于从模拟信号或其他数字信号处理（DSP）中去除尖峰和噪声，也被称为 “椒盐噪声” 或 “脉冲噪声” 滤波器。

仓库文件结构：

LICENSE

MedianFilter.c

MedianFilter.h

MedianFilter.hpp

README.md

example.c

文件说明：

LICENSE：该项目采用 MIT 许可证，允许用户自由使用、复制、修改和分发软件，但需包含版权声明和许可声明，且软件按 “原样” 提供，不提供任何形式的保证。

MedianFilter.c：C 语言实现的中值滤波算法核心代码，包含 MEDIANFILTER_Insert 函数，用于向滤波器中插入新样本并返回中值。

MedianFilter.h：C 语言头文件，可能包含 MedianFilter.c 中使用的结构体和函数声明。

MedianFilter.hpp：C++ 实现的中值滤波算法，使用模板类 MedianFilter 实现，支持不同数据类型和元素数量的滤波器。

README.md：项目说明文件，介绍了项目的基本信息和用途。

example.c：C 语言示例代码，演示了如何使用中值滤波器。通过随机生成新值并插入滤波器，每秒打印一次新值和中值。

代码实现要点：

C++ 实现 (MedianFilter.hpp)： 使用模板类 MedianFilter，支持不同数据类型和元素数量的滤波器。 
要求数据类型为算术类型，元素数量为奇数且至少为 3。 使用链表结构管理滤波器中的元素，通过 Insert 函数插入新值并返回中值。 
C 实现 (MedianFilter.c)： 定义了 MEDIANFILTER_Insert 函数，用于向滤波器中插入新样本并返回中值。 
同样使用链表结构管理滤波器中的元素，通过指针操作实现元素的插入和排序。

示例代码：

以下是 example.c 中的示例代码，演示了如何使用中值滤波器：
