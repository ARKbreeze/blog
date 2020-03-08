# Collection

- 作为体系的根接口，提供整体的约定

- java.util 工具包

## List

- list.contains(list1)  ; 取交集 list{1，2，3} list1{2，3 }   -> {2,3};
- 本质是数组
- 扩容 >>1 即扩容扩当前的一半



## Set

- 不重复，根据equal()方法判断
- hashset 无序
- treeset 用定义的顺序自动排序
- linkedset 链表实现有序
- treeset 红黑树  平衡二叉树(AVL)



# Map

- hashmap 是线程不安全的 ，在多线程时扩容是可能会导致死循环， 推荐使用concourrenthashmap 线程安全的



## HashCode 

- 目的为了提高效率
- 同一个对象始终返回相同的hashcode
- 两个对象equal返回true，则必须返回相同的hashcode
- 两个对象不等，也可能返回相同的hashcode
- hash单项映射

# 数据结构

- 队列/双端队列(栈) queue/deque
- 链表   linkedlist
- 优先级队列 

# Guava

- goole guava 尽量少造轮子，多用经过大众检验的
- Lists/Sets/Maps   工具类
- ImmutableSet/ImmutableMap   不可变
- MultiSet/MutisetMap     set可以统计重复元素次数/map可以一键对应多值
- BiMap 双向map   可以用值找键



# 偷群友的体系图

![image-20200307224236989](img\image-20200307224236989.png)