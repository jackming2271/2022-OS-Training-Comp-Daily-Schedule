# 2022-OS-Training-Comp-Daily-Schedule
此文档为个人参加[2022年开源操作系统训练营](https://github.com/LearningOS/rust-based-os-comp2022/blob/main/scheduling.md)的工作记录  

因对于操作系统/基础软件的兴趣而来, 希望能够在本次活动中和大家一起努力, 争取有所收获

活动目标: 探索把现代系统语言Rust和灵活开放的系统结构RISC-V带入到操作系统的架构与设计的创新中来，思考未来的操作系统应该是什么样。

## 目录
07/07开始学习, 每周四至下周三为一个循环, 每周三完成周报 / 每天晚上完成当日总结

**第一阶段 (7月1日～7月31日)**  

|  | 周四 | 周五 | 周六 | 周天 | 周一 | 周二 | 周三 | 周报 |
| ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- |
| 07/07 ~ 07/13 | [Day1](#Day1) | [Day2](#Day2)  |  [Day3](#Day3)  | [Day4](#Day4) | [Day5](#Day5) | [Day6](#Day6) | [Day7](#Day7) | [第 1 周](#Week1) | 
| 07/14 ~ 07/20 | Day8 | Day9 | Day10 | Day11 | Day12 | Day13 | Day14 | 第 2 周 |
 

## Day1
今天投入的全部时间都在做 rustlings , 目前进度 50/84 , 明天争取搞定 rustlings  
在完成 rustlings 的过程中, 发现对于 ?操作符 / 枚举类型 / 错误处理的部分有点遗忘, 有几个题有卡壳的情况  
明天先快速过一遍 [Rust圣经](https://course.rs/basic/compound-type/enum.html) 然后再继续做
  
## Day2
今天进度: rustlings 64/84 , 发现rustlings后面的内容很多不熟悉 (模板 / 共享指针 等) 
还是和昨天一样, 配合着rust圣经一边看一边做题, 最后20道加油
  
## Day3
**各方向进展**
Rust
- 学习 [关联类型 / 宏 / 线程] 等部分
- 完成 rustlings 84/84

## Day4
配置实验环境, 了解github classroom, 了解实验开发流程, 今日提交通过lab0-0 ， lab0-1

## Day5
工作太忙，今天暂时没搞，o(╥﹏╥)o

## Day6
学习指导书第三章及之前的部分，完成实验一 o(*￣︶￣*)o， 总结见[实验报告1](https://github.com/LearningOS/lab1-os3-zhaiqiming/blob/main/reports/lab1.md)

## Day7
今天学习lab2指导书, 完成了 sys_get_task_info & sys_get_time , 主要是在内核中通过Page_table的虚实地址转换,查询系统调用传入地址的真实物理地址, 然后写入相关信息的过程

## Week1
**第 1 周 总结 👨🏼‍🍳**  
本周主要完成了以下内容:  
**Rust:**
- 学习Rust圣经, 完成rustling(84/84) 


**自学risc-v系统结构:**  
- 复习CS61C部分内容, 之前做得CS61C实验: [repo](https://github.com/zhaiqiming/CS61C) 


**基于Rust语言进行操作系统内核实验**:  
- 学习 Open-Source-OS-Training-Camp-2022 文档 , 完成lab0-0, lab0-1, lab1, lab2(除实验报告), lab3 正在开发中...  
- 提出PR两个, 一个[文档语法问题](https://github.com/LearningOS/rCore-Tutorial-Guide-2022S/pull/14) , 一个 [os4-ref的bug](https://github.com/LearningOS/rust-based-os-comp2022/pull/77)  


经验总结🐝:
1. Rust不同于C++, 遇到不懂的Rust概念时, 可以结合操作系统或者编译的知识去理解, 最好不要借鉴C++ 
2. 我写的Rust代码大概率首次是不会通过编译的😈, 可以先使用 cargo build --release 检查编译问题, 这样比make run速度会快很多
3. 代码需要高内聚, 这一点在lab2做得不好(在task模块做了很多mm模块的操作), 之后一定严格要求, 尽量在模块内部实现并以接口的方式提供给调用方
  
**下周目标🐯:**  
**Rust:**
- (32 Rust Quizes) -> (exercisms.io 快速练习)  
  
**自学risc-v系统结构:**
- 自学PPT for RISC-V特权指令级架构  
- 自学RISC-V手册：一本开源指令集的指南 重点是第10章  

**基于Rust语言进行操作系统内核实验**:  
- 完成lab2, 3 ,4 ,5全部实验(代码 & 报告) 

## Day8
学习lab3的代码

## Day9
在lab3-os5中完成了向前兼容, 通过了usertests的全部内容

## Day10
完成lab3-os5的全部代码, 通过所有测试(感觉stride测试样例的误差比较大, 最好把测试用例的时长都加大一点,这样就将不同进程的误差比降到了2以下), 同样还没写report😭, 最后一起写吧

## Day11
学习lab4-os6的代码, 主要涉及文件系统