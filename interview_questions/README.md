# C++高频面试题
## 语言基础
### C 和 C++ 的区别
### struct 和 class 的区别
### static 关键字的作用
### const 关键字的作用
### volatile 关键字的作用
### inline 内联函数和宏定义的区别
### explicit 关键字的作用
### sizeof 和 strlen 的区别
### nullptr 和 NULL 的区别
### typedef 和 using 的区别
### union 了解吗
### placement new 是什么

## OOP 核心
### C++ 的三大特性是什么
### 多态是怎么实现的？虚函数表了解吗
### 虚函数表在什么时候构造？多继承下虚表怎么排列
### 基类析构函数为什么必须是虚函数
### 构造函数能否是虚函数？析构函数可以是纯虚函数吗
### 纯虚函数和虚函数的区别
### 抽象类和接口的区别
### 重载、重写、重定义的区别
### 拷贝构造函数和赋值运算符重载的区别
### 深拷贝和浅拷贝的区别
### Rule of Three / Rule of Five
### 为什么构造函数不能是虚函数
### final 和 override 关键字
### friend 关键字的作用
### C++ 中如何防止一个类被继承

## 内存管理
### C++ 内存分区（五段内存模型）
### 堆和栈的区别
### new 和 malloc 的区别
### delete 和 delete[] 的区别
### 内存泄漏怎么检测和定位
### 什么是野指针、悬空指针？如何避免
### RAII 原理
### 智能指针了解哪些
### shared_ptr 实现原理？循环引用怎么解决
### unique_ptr 可以拷贝吗
### weak_ptr 解决循环引用原理
### make_shared 和 new 的区别
### operator new 和 operator delete 可以重载吗
### 内存对齐规则
### alignas 和 alignof 的区别

## STL 与容器
### STL 六大组件
### vector 底层实现和扩容机制
### vector<bool> 为什么特化
### list 和 vector 的区别
### map 和 unordered_map 的区别？什么时候用哪个
### unordered_map 哈希冲突怎么解决
### set 和 map 的底层实现
### 红黑树和 AVL 树的区别
### iterator 失效场景有哪些
### 常用 STL 算法（sort、find、lower_bound、accumulate 等）

## 现代 C++（11/14/17/20）
### C++11 最重要的几个新特性
### auto 和 decltype 的区别
### 移动语义和完美转发
### std::move 的作用
### 右值引用和左值引用的区别
### std::forward 的作用
### lambda 表达式底层实现
### std::function 和 std::bind 原理
### 智能指针（unique_ptr/shared_ptr/weak_ptr）
### nullptr
### noexcept 的作用
### thread_local
### C++20 协程了解吗

## 多线程与并发
### 进程和线程的区别
### 线程同步方式有哪些
### mutex、condition_variable 怎么配合使用
### std::atomic 原理？a++ 是原子操作吗
### 死锁产生的四个条件？如何避免
### 线程安全单例怎么写
### 实现一个线程池

## 编译链接与底层
### C++ 程序编译链接全过程（预处理→编译→汇编→链接）
### 静态链接和动态链接的区别
### 四种 cast 转换
### 模板实例化发生在什么时候
### 函数模板和类模板的区别
### SFINAE 和 std::enable_if

## 设计模式与手撕代码
### 常见设计模式（单例、工厂、观察者、策略）
### 手撕线程安全单例
### 手撕简易 shared_ptr
### 手撕 LRU Cache
### 手撕线程池
### 手撕生产者消费者
### 手撕简易 vector/string

## 网络编程（C++后台必问）
### TCP 三次握手、四次挥手
### TIME_WAIT 和 CLOSE_WAIT 的区别
### select、poll、epoll 的区别与原理
### Reactor 和 Proactor 模型
