# C++高频面试题
[English](https://github.com/0voice/awesome-modern-cpp-2025/blob/main/interview_questions/README.en.md)
## 目录
[语言基础](#语言基础)  
[面向对象](#面向对象)  
[内存管理](#内存管理)  
[STL与容器](#stl与容器)   
[现代C++特性](#现代c特性)  
[多线程与并发](#多线程与并发)  
[网络编程](#网络编程)  
[手撕代码](#手撕代码)  

## 语言基础

### static 关键字的作用
- 修饰普通变量：延长生命周期至程序结束，存储在静态存储区，仅初始化一次
- 修饰普通函数/全局变量：限制符号为内部链接，仅限本翻译单元可见
- 修饰类的数据成员：所有对象共享一份，属于类而非对象
- 修饰类的成员函数：无this指针，只能访问静态成员

### const 关键字的作用
- 修饰变量为只读
- 修饰指针可构成顶层const（指针本身不可改）和底层const（所指对象不可改）
- 修饰成员函数：承诺不修改成员变量，可被const对象调用
- 修饰引用：常用于函数参数避免拷贝并防止修改
- constexpr（C++11起）：表示编译期常量

### inline 内联函数和宏定义的区别
- inline函数具有类型检查、作用域控制、可调试
- 宏是预处理器文本替换，无类型检查、易产生副作用、不可调试
- inline函数可取地址，宏不能
- 现代C++推荐用inline函数或constexpr函数替代宏

### explicit 关键字的作用
- 修饰单参数构造函数，禁止隐式类型转换
- 仅允许显式构造，防止意外的类型转换错误

### nullptr 和 NULL 的区别
- NULL是宏，通常定义为0或(void*)0
- nullptr是C++11引入的std::nullptr_t类型专用空指针常量
- nullptr类型安全，不会与整数重载产生歧义

### sizeof 和 strlen 的区别
- sizeof是编译期运算符，返回类型或对象占用的字节数
- strlen是运行期函数，返回C风格字符串中\0之前的字符个数
- sizeof对数组不退化，strlen参数必须是char*

### new 和 malloc 的区别
- new是C++运算符，malloc是C库函数
- new自动计算大小并调用构造函数，malloc需手动计算字节数
- new返回正确类型指针，malloc返回void*
- new可被重载，malloc不可
- new抛出std::bad_alloc，malloc返回NULL

### delete 和 delete[] 的区别
- delete用于new分配的单个对象
- delete[]用于new[]分配的数组，会按逆序调用每个元素的析构函数
- 混用会导致未定义行为（尤其是含非平凡析构函数的类）

### 四种 cast 转换
- static_cast：基本类型转换、类层次上下转型（无运行时检查）、void*转换
- const_cast：去除或添加const/volatile属性
- reinterpret_cast：任意指针类型间转换、指针与整数转换，最危险
- dynamic_cast：类层次多态类型安全向下转型，失败返回nullptr或抛异常

### C++ 程序编译链接全过程
- 预处理：宏展开、#include展开、条件编译 → .i文件
- 编译：生成汇编代码 → .s文件
- 汇编：汇编代码 → 目标文件 .o/.obj
- 链接：符号解析、地址重定位，合并多个目标文件和库 → 可执行文件

### struct 和 class 的区别
- 唯一区别是默认访问权限：struct默认public，class默认private
- 继承默认权限也不同：struct默认public继承，class默认private继承

### C 和 C++ 的区别
- C是过程式语言，C++是支持面向对象和泛型编程的多范式语言
- C++有类、继承、多态、模板、异常处理、标准库STL等
- C++支持void*隐式转换，C++更严格的类型检查
- C++有函数重载、引用、new/delete、命名空间等特性

### extern "C" 的作用
- 禁止C++的名称修饰(name mangling)
- 使函数按C语言方式进行编译和链接
- 主要用于C++与C语言的混合编程

### volatile 关键字的作用
- 阻止编译器优化对变量的读写操作
- 保证每次访问都直接从内存读取
- 用于：多线程共享变量、内存映射IO、信号处理

### C++程序从源代码到可执行文件的详细过程
1. **预处理**：处理宏定义、头文件包含、条件编译等
2. **编译**：将预处理后的源代码转换为汇编代码
3. **汇编**：将汇编代码转换为机器码(.obj文件)
4. **链接**：将多个目标文件和库文件链接成可执行文件

## 面向对象

### 多态是怎么实现的？虚函数表了解吗
- 运行时多态通过虚函数表（vtable）实现
- 每个有虚函数的类有一个唯一的虚函数表
- 对象内部（通常首部）含有一个vptr指针指向本类的vtable
- 调用虚函数时通过vptr→vtable查找函数地址实现动态绑定

### 基类析构函数为什么必须是虚函数
- 通过基类指针/引用删除派生类对象时，若基类析构非虚，只调用基类析构
- 导致派生类部分未析构，产生资源泄漏
- 只要存在通过基类指针删除的可能性，基类析构就必须声明为virtual

### 构造函数能否是虚函数？析构函数可以是纯虚函数吗
- 构造函数不能是虚函数：vptr在构造函数体内才初始化，调用时无法动态绑定
- 析构函数可以是纯虚函数，但必须提供定义（因为基类析构仍会被调用）

### 重载、重写、重定义的区别
- 重载（overload）：同一作用域内，函数名相同参数列表不同
- 重写（override）：派生类虚函数与基类虚函数签名完全一致（C++11可显式override）
- 重定义（redefinition/hiding）：派生类定义同名函数（非虚），隐藏基类所有同名函数

### 拷贝构造函数和赋值运算符重载的区别
- 拷贝构造：从无到有，用已有对象初始化新对象
- 赋值运算符：对象已存在，用另一对象覆盖当前对象
- 拷贝构造参数必须是引用，赋值运算符返回*this引用以支持链式赋值

### 深拷贝和浅拷贝的区别
- 浅拷贝：只拷贝指针值，多个对象指向同一块内存
- 深拷贝：拷贝指针指向的内容，为每个对象分配独立内存
- 浅拷贝易导致重复释放，深拷贝安全但开销大

### Rule of Three / Rule of Five
- Rule of Three：若类需要自定义析构、拷贝构造、拷贝赋值，则三者都要自定义
- Rule of Five：C++11后加上移动构造、移动赋值，若需自定义任一则通常五者都要考虑

### final 和 override 关键字
- override：显式表明函数意在重写基类虚函数，编译器检查
- final：修饰虚函数表示不可再被重写；修饰类表示不可被继承

### 为什么构造函数不能是虚函数
- 虚函数靠vptr和vtable实现，而vptr在构造函数执行过程中才完成初始化
- 若构造函数是虚函数，则调用时vtable尚未建立，无法动态分发

### 纯虚函数和虚函数的区别
- 虚函数有实现，默认提供实现，可被重写
- 纯虚函数无实现（=0），含纯虚函数的类为抽象类，不能实例化
- 纯虚函数强制派生类必须实现

### 抽象类和接口的区别
- 抽象类：含纯虚函数的类，可含有数据成员和非纯虚函数
- 接口（C++中通常指只含纯虚函数的抽象类）：通常无数据成员、无实现，表达“能力”

### friend 关键字的作用
- 破坏封装，允许指定函数或类访问本类的private/protected成员
- 常用于运算符重载、全局函数、相关类之间使用

### C++ 中如何防止一个类被继承
- C++11：将类标记为final
- C++03：将析构函数声明为private，或用虚继承“友元+虚继承”技巧

### 虚函数表指针在对象内存布局中的位置
- 位于对象内存布局的最开始位置
- 每个有虚函数的类都有自己的虚函数表
- 通过该指针实现动态绑定

### 多重继承下派生类对象有几个虚函数表
- 有几个带虚函数的基类就有几个虚函数表
- 派生类的新虚函数放入第一个基类的虚函数表中

### 什么是菱形继承
```cpp
class A {};
class B : public A {};
class C : public A {};
class D : public B, public C {}; // 菱形继承
```
问题：D中包含两份A的实例，造成数据冗余和二义性

解决：使用虚继承(virtual inheritance)

## 内存管理

### C++ 内存分区
- 代码段（text）、常量区、静态/全局区、BSS段、堆（heap）、栈（stack）

### 堆和栈的区别
- 栈：自动管理，连续空间，速度快，大小受限
- 堆：手动管理（new/delete）管理，动态分配，易碎片，理论上受虚拟内存限制

### 内存泄漏怎么检测和定位
- Linux：valgrind、AddressSanitizer（-fsanitize=address）、mtrace
- Windows：Visual Studio诊断工具、CRT调试堆
- 通用：智能指针 + RAII、定期代码审查

### 什么是野指针、悬空指针？如何避免
- 野指针：指向非法内存的指针（未初始化或已delete）
- 悬空指针：指向已被释放的内存
- 避免方法：初始化为nullptr，delete后立即置nullptr，使用智能指针

### RAII 原理
- Resource Acquisition Is Initialization
- 资源管理与对象生命周期绑定，构造函数获取资源，析构函数释放资源
- 利用栈上对象的自动析构保证异常安全

### 智能指针了解哪些
- unique_ptr：独占所有权，不可拷贝，可移动
- shared_ptr：共享所有权，引用计数
- weak_ptr：解决shared_ptr循环引用，非拥有型

### shared_ptr 实现原理？循环引用怎么解决
- 控制块包含强引用计数、弱引用计数、deleter等
- 拷贝时强引用计数+1，析构时-1，为0时释放资源
- 循环引用：A含`shared_ptr<B>`，B含`shared_ptr<A>`，导致计数无法归零
- 解决：循环的一方改为weak_ptr

### unique_ptr 可以拷贝吗
- 默认不可拷贝（删除拷贝构造和赋值）
- 可通过std::move转移所有权，转移后原指针变为nullptr

### weak_ptr 解决循环引用原理
- weak_ptr不增加强引用计数
- lock()可尝试提升为shared_ptr，若资源已释放则得到空shared_ptr

### 内存对齐规则
- 编译器按成员最大对齐规则填充，使每个成员地址是其对齐值的整数倍
- 结构体总大小是最大对齐值的整数倍
- 目的是提升CPU读取效率（避免跨缓存行）

### placement new 是什么
在已分配的内存上构造对象

不分配内存，只调用构造函数

```cpp
void* memory = malloc(sizeof(MyClass));
MyClass* obj = new(memory) MyClass();
```
### 除了智能指针还有哪些避免内存泄漏的方法
- RAII原则(Resource Acquisition Is Initialization)

- 使用容器类代替手动内存管理

- 遵循谁申请谁释放原则

- 使用内存检测工具(Valgrind, AddressSanitizer)

## STL与容器

### vector 底层实现和扩容机制
- 连续内存，动态数组
- 容量不足时通常扩容为当前容量的1.5倍或2倍（不同实现）
- 扩容会重新分配内存、搬迁元素，原迭代器全部失效

### iterator 失效场景有哪些
- vector/deque：插入导致扩容、删除导致元素搬迁
- string扩容
- 关联容器删除节点后该节点迭代器失效，其他仍有效

### map 和 unordered_map 的区别？什么时候用哪个
- map：红黑树，有序，O(log n)，支持范围查询
- unordered_map：哈希表，平均O(1)，无序
- 有序要求或需要lower_bound用map；追求极致性能且无序要求用unordered_map

### unordered_map 哈希冲突怎么解决
- 主流实现采用链地址法（每个桶一个链表）
- 负载因子过高时会rehash扩容

### set 和 map 的底层实现
- 均为红黑树
- set的key即value，map的value是pair<const Key, T>

### emplace_back 和 push_back 区别
- push_back：接受已构造对象，发生至少一次拷贝或移动
- emplace_back：原地构造，参数直接转发给构造函数，理论上更高效

### 常用 STL 算法
- 非变算法：find、count、for_each、transform
- 变算法：sort、remove、unique、partition
- 数值算法：accumulate、inner_product

### list 和 vector 的区别
- list：双向链表，非连续，插入删除O(1)，随机访问O(n)
- vector：连续数组，随机访问O(1)，尾部插入快，中部插入慢

### STL 六大组件
- 容器（Containers）
- 分配器（Allocators）
- 算法（Algorithms）
- 迭代器（Iterators）
- 仿函数（Functors）
- 适配器（Adapters）

### 红黑树和 AVL 树的区别
- AVL：严格平衡，高度差≤1，查找更快，插入删除旋转多
- 红黑树：近似平衡，放松平衡条件，插入删除效率更高，STL广泛使用

### vector 的 resize 和 reserve 有什么区别
resize(n): 改变容器中元素的数量为n，可能构造新元素或销毁多余元素
reserve(n): 预分配至少能容纳n个元素的内存空间，不改变元素数量

### unordered_map 的负载因子是什么意思
元素数量与桶(bucket)数量的比值
负载因子过大会导致哈希冲突增加，性能下降
默认阈值约为0.75，超过会触发rehash(重新哈希)

### STL 容器的 allocator 有什么作用
将内存分配与对象构造分离开来
提供统一的内存管理接口
允许自定义内存分配策略(如内存池)


## 现代C++特性

### C++11 最重要的几个新特性
- auto、decltype、右值引用、移动语义、智能指针、lambda、nullptr、override/final、constexpr、uniform initialization、variadic templates

### 移动语义和完美转发
- 移动语义：将资源“窃取”而非拷贝，适用于临时对象
- 完美转发：保持参数的左值/右值属性原样传递给另一函数

### std::move 的作用
- 无条件将左值转换为右值引用
- 本身不移动任何东西，只是强制触发移动语义

### std::forward 的作用
- 仅在参数是右值引用时才转为右值（完美转发核心）

### lambda 表达式底层实现
- 编译器生成匿名类类型，重载operator()
- 捕获列表生成对应成员变量，构造函数初始化这些变量

### noexcept 的作用
- 声明函数不会抛异常
- 编译器可进行更激进优化（如移动构造函数若noexcept则强异常保证）
- 异常传播时若违背noexcept直接std::terminate()

### auto 和 decltype 的区别
- auto：根据初始化表达式自动推导变量类型，忽略顶层const和引用
- decltype：推导表达式的类型，保留const和引用

### 右值引用和左值引用的区别
- 左值引用：绑定到左值（有名字的实体）
- 右值引用：绑定到右值（临时对象、将亡值）
- 右值引用可延长临时对象生命周期，用于实现移动语义

### std::function 和 std::bind 有什么作用
std::function: 通用的函数包装器，可以存储任何可调用对象(函数指针、lambda、函数对象等)
std::bind: 函数参数绑定，可以创建新的可调用对象，支持参数绑定和重排

### 什么是移动语义
通过右值引用转移资源所有权，避免不必要的深拷贝
使用std::move将左值转换为右值引用
显著提升性能，特别是在容器操作中

### C++11 的 enum class 相比传统的 enum 有什么优点
强类型，不会隐式转换为整数
作用域限定，避免命名污染
可以指定底层数据类型
前向声明支持更好

### 什么是 std::initializer_list
用于初始化容器和自定义类型的轻量级类模板
支持列表初始化语法
编译器会自动从花括号初始化列表构造initializer_list对象

## 多线程与并发

### std::atomic 原理？a++ 是原子操作吗
- std::atomic使用CPU原子指令（lock prefix、cmpxchg等）或编译器内置实现
- a++不是原子操作，包含读-改-写三步
- 必须用a.fetch_add(1)或a++的atomic版本

### 死锁产生的四个条件？如何避免
- 互斥、持有并等待、非抢占、循环等待
- 避免方法：按固定顺序加锁、尽量短时间持锁、使用std::lock、超时机制

### 线程安全单例怎么写
- C++11后静态局部变量方式最简：static Singleton instance; 线程安全
- 双检查锁模式（double-checked locking）+ volatile（C++11前）
- std::call_once + std::once_flag

### mutex、condition_variable 怎么配合使用
- mutex保护共享数据
- condition_variable用于线程间等待/通知
- 典型模式：while(条件不满足) wait(lock);  notify_one/notify_all唤醒

### 线程同步方式有哪些
- mutex、condition_variable、atomic、semaphore（C++20）、barrier（C++20）、latch（C++20）、futex（底层）

### 进程和线程的区别
- 进程有独立地址空间，线程共享进程地址空间
- 进程切换开销大，线程切换快
- 进程崩溃不影响其他进程，线程崩溃可能导致整个进程退出

### std::unique_lock 和 std::lock_guard 有什么区别
lock_guard: 简单的RAII锁包装器，构造时加锁，析构时解锁，不支持手动操作
unique_lock: 更灵活，支持延迟加锁、手动解锁、所有权转移、条件变量配合使用

### C++ 内存模型中的 std::memory_order 有哪几种
memory_order_relaxed: 最宽松，只保证原子性
memory_order_consume: 数据依赖顺序
memory_order_acquire: 获取操作，建立同步关系
memory_order_release: 释放操作，建立同步关系
memory_order_acq_rel: 获取-释放操作
memory_order_seq_cst: 顺序一致性(默认最严格)

### 什么是虚假唤醒
等待状态的线程被意外唤醒，但等待的条件并未真正满足
常见于条件变量的使用中
解决方法：使用while循环检查条件变量

### 简述无锁编程的优缺点
优点：
- 避免死锁和优先级反转
- 性能更高，无上下文切换开销
- 可扩展性更好
缺点：
- 实现复杂，容易出错
- 需要处理ABA问题
- 调试和测试困难
- 对算法设计要求高


## 网络编程

### TCP 和 UDP 的区别？适用场景？
#### 核心区别
1. TCP：面向连接、可靠传输（无丢失/重复/乱序）、有流量/拥塞控制、头部开销大、字节流。
2. UDP：无连接、尽力交付（可能丢包/乱序）、无控制机制、头部开销小、数据报（保留边界）。

#### 适用场景
1. TCP：文件传输、网页访问、支付交易、数据库连接等需可靠性的场景。
2. UDP：直播/视频通话、游戏、DNS 解析等需实时性/低开销的场景。

### select、poll、epoll 的区别与原理
- select：fd_set位图，O(n)扫描，fd数量受限（通常1024）
- poll：pollfd数组，O(n)扫描，突破fd数量限制
- epoll：事件驱动，内核维护红黑树+就绪链表，O(1)返回就绪事件，支持水平/边沿触发

### 什么是粘包/拆包？如何解决？
- TCP是字节流协议，多次send可能被合并（粘包），一次send可能被拆开（拆包）
- 解决：应用层自定义协议（如消息长度前缀、定长消息、分隔符）

### TCP 三次握手、四次挥手
#### 三次握手
1. 客户端向服务端发送同步报文（SYN 包），表明客户端想要建立连接，随后客户端进入 SYN_SENT 状态。
2. 服务端收到同步请求后，向客户端回复同步+确认报文（SYN+ACK 包），既确认客户端的连接请求，也同步自身的序列号，服务端进入 SYN_RCVD 状态。
3. 客户端收到服务端的回复后，向服务端发送确认报文（ACK 包），确认已接收服务端的同步信息，此时客户端和服务端均进入 ESTABLISHED 状态，连接正式建立。
核心目的：验证双方的收发能力均正常，避免因网络延迟导致的无效连接占用资源。

#### 四次挥手
1. 主动关闭连接的一方（可能是客户端或服务端）向另一方发送结束报文（FIN 包），表明自身不再发送数据，请求断开连接，主动方进入 FIN_WAIT_1 状态。
2. 被动关闭的一方收到结束报文后，向主动方发送确认报文（ACK 包），告知已收到断开请求，此时被动方进入 CLOSE_WAIT 状态，主动方收到确认后进入 FIN_WAIT_2 状态。
3. 被动方完成自身剩余数据的发送后，向主动方发送结束报文（FIN 包），表明自身也已无数据可发，请求断开连接，被动方进入 LAST_ACK 状态。
4. 主动方收到被动方的结束报文后，向被动方发送确认报文（ACK 包），确认断开请求，主动方进入 TIME_WAIT 状态（等待 2MSL 时长，确保被动方收到确认），双方最终完成连接关闭。
核心目的：确保双方均已完成所有数据的发送和接收，避免断开连接时丢失数据。

### TIME_WAIT 状态是什么
TCP连接主动关闭方在发送最后一个ACK后进入的状态
持续时间：2MSL(最大报文段生存时间)，通常为1-4分钟
作用：确保最后一个ACK可靠到达；让旧连接的报文在网络中完全消失

### 什么是 Reactor 和 Proactor 网络模型
Reactor模式：
同步IO模型，应用程序监听事件就绪
事件就绪后应用程序同步处理IO操作
模式：read -> decode -> compute -> encode -> send

Proactor模式：
异步IO模型，应用程序发起异步IO操作
操作系统完成IO操作后回调应用程序处理
模式：发起异步IO -> 操作系统完成IO -> 回调处理函数

## 手撕代码

### 手撕线程安全单例
核心：C++11 局部静态变量初始化天然线程安全，禁止拷贝赋值确保唯一实例
```cpp
class Singleton {
public:
    static Singleton& getInstance() {
        static Singleton instance;
        return instance;
    }
    Singleton(const Singleton&) = delete;
    Singleton& operator=(const Singleton&) = delete;
private:
    Singleton() = default;
};
```
### 手撕 LRU Cache
核心：哈希表（O (1) 查找）+ 双向链表（O (1) 插入删除），表头存最近使用，表尾存最久未用
```cpp
#include <unordered_map>
#include <list>
using namespace std;

class LRUCache {
    int cap;
    list<pair<int, int>> cacheList; // (key, val)，维护访问顺序
    unordered_map<int, list<pair<int, int>>::iterator> cacheMap; // 键→迭代器
public:
    LRUCache(int capacity) : cap(capacity) {}
    int get(int key) {
        if (!cacheMap.count(key)) return -1;
        // 命中移至表头（最近使用）
        cacheList.splice(cacheList.begin(), cacheList, cacheMap[key]);
        return cacheMap[key]->second;
    }
    void put(int key, int value) {
        if (cacheMap.count(key)) {
            // 已存在：更新值+移表头
            cacheMap[key]->second = value;
            cacheList.splice(cacheList.begin(), cacheList, cacheMap[key]);
            return;
        }
        // 新增至表头
        cacheList.emplace_front(key, value);
        cacheMap[key] = cacheList.begin();
        // 超容删除表尾（最久未用）
        if (cacheList.size() > cap) {
            cacheMap.erase(cacheList.back().first);
            cacheList.pop_back();
        }
    }
};
```
### 手撕快速排序
核心：分治思想，选基准值分区（小于基准放左，大于放右），递归排序左右区间
```cpp
#include <vector>
#include <algorithm>
using namespace std;

int partition(vector<int>& nums, int l, int r) {
    int pivot = nums[l];
    int i = l, j = r;
    while (i < j) {
        while (i < j && nums[j] >= pivot) j--;
        while (i < j && nums[i] <= pivot) i++;
        if (i < j) swap(nums[i], nums[j]);
    }
    swap(nums[l], nums[i]); // 基准归位
    return i;
}
void quickSort(vector<int>& nums, int l, int r) {
    if (l >= r) return;
    int pivotIdx = partition(nums, l, r);
    quickSort(nums, l, pivotIdx - 1);
    quickSort(nums, pivotIdx + 1, r);
}
```
### 手撕归并排序
核心：分治 + 合并，拆分数组为子数组，递归排序后合并两个有序子数组（稳定排序）
```cpp
#include <vector>
using namespace std;

void merge(vector<int>& nums, int l, int mid, int r) {
    vector<int> temp(r - l + 1);
    int i = l, j = mid + 1, k = 0;
    // 合并有序子数组
    while (i <= mid && j <= r) {
        temp[k++] = nums[i] <= nums[j] ? nums[i++] : nums[j++];
    }
    // 拷贝剩余元素
    while (i <= mid) temp[k++] = nums[i++];
    while (j <= r) temp[k++] = nums[j++];
    // 回写原数组
    for (int p = 0; p < temp.size(); p++) nums[l + p] = temp[p];
}
void mergeSort(vector<int>& nums, int l, int r) {
    if (l >= r) return;
    int mid = l + (r - l) / 2; // 避免溢出
    mergeSort(nums, l, mid);
    mergeSort(nums, mid + 1, r);
    merge(nums, l, mid, r);
}
```
### 手撕字符串反转
核心：双指针相向移动，原地交换字符（O (n) 时间，O (1) 空间）
```cpp
#include <string>
#include <algorithm>
using namespace std;

void reverseString(string& s) {
    int l = 0, r = s.size() - 1;
    while (l < r) swap(s[l++], s[r--]);
}
```

### 手撕两数之和
核心：哈希表存已遍历数值的索引，O (n) 时间查找补数（target - 当前值）
```cpp
#include <vector>
#include <unordered_map>
using namespace std;

vector<int> twoSum(vector<int>& nums, int target) {
    unordered_map<int, int> numMap; // key: 数值，value: 索引
    for (int i = 0; i < nums.size(); i++) {
        int complement = target - nums[i];
        if (numMap.count(complement)) return {numMap[complement], i};
        numMap[nums[i]] = i;
    }
    return {}; // 题目保证有解，可省略
}
```
