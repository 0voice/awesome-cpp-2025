# C++高频面试题

## 目录
[语言基础](#语言基础)  
[面向对象](#面向对象)  
[内存管理](#内存管理)  
[STL与容器](#stl与容器)   
[现代C++特性](#现代c特性)  
[多线程与并发](#多线程与并发)  
[网络编程](#网络编程)  
[设计模式与架构](#设计模式与架构)  
[手撕代码](#手撕代码)  

## 语言基础
### C 和 C++ 的区别
C 是过程式语言，C++ 是多范式（过程式 + 面向对象 + 泛型）。C++ 增加了 class、继承、多态、模板、STL、异常处理、RAII 等，天然支持面向对象和泛型编程，同时兼容全部 C 代码。

### struct 和 class 的区别
唯一区别是默认访问权限：struct 默认 public，class 默认 private。其他完全一样（都可以有成员函数、继承、模板等）。

### static 关键字的作用
1. 静态局部变量：生命周期延长到程序结束，只初始化一次  
2. 静态全局变量/函数：限制作用域在本编译单元（内部链接）  
3. 静态成员变量：属于类，所有对象共享一份  
4. 静态成员函数：无 this 指针，只能访问静态成员

### const 关键字的作用
1. 修饰变量：不可修改  
2. 修饰指针：可区分“指针本身const”和“指向内容const”  
3. 修饰成员函数：承诺不修改成员变量，可用于 const 对象  
4. 修饰返回值：防止误修改（如返回引用/指针）
### volatile 关键字的作用
告诉编译器该变量可能被意外修改（如硬件寄存器、多线程共享），禁止优化（如寄存器缓存、指令重排）。注意：volatile ≠ 线程安全。

### inline 内联函数和宏定义的区别
- inline 有类型检查、作用域、调试支持  
- 宏是纯文本替换，无类型安全，易出错  
- 现代 C++ 推荐用 constexpr 或 inline 替代宏

### explicit 关键字的作用
禁止单参数构造函数的隐式转换，避免意外类型转换（如 `MyString s = 'a';`）。

### sizeof 和 strlen 的区别
- sizeof 是编译期运算符，返回类型/对象占字节数  
- strlen 是运行期函数，计算 \0 之前的字符数  
- sizeof(char[10]) = 10，strlen("hello") = 5

### nullptr 和 NULL 的区别
NULL 实际上是 0，nullptr 是 std::nullptr_t 类型，只能隐式转换为指针类型，避免重载歧义。

### typedef 和 using 的区别
using 是 C++11 引入，更强大：支持模板别名（typedef 不行）。推荐用 using。

### union 了解吗
所有成员共享同一块内存，可节省空间，常用于类型惩罚（type punning）或节省内存（如网络协议包）。注意严格别名规则（C++17 后更严格）。

### placement new 是什么
在已分配的内存上构造对象：`new (ptr) Class()`，常用于内存池、自定义分配器。

## 面向对象
### C++ 的三大特性是什么
封装、继承、多态。

### 多态是怎么实现的？虚函数表了解吗
运行时多态通过虚函数表（vtable）实现。每个有虚函数的类有一个隐藏的 vptr 指向 vtable，vtable 存储虚函数地址。调用时通过 vptr → vtable 查找实际函数。

### 虚函数表在什么时候构造？多继承下虚表怎么排列
vtable 在编译期生成，对象构造时初始化 vptr。多继承下每个有虚函数的基类会有一个 vptr，排列顺序与继承顺序一致。

### 基类析构函数为什么必须是虚函数
否则通过基类指针 delete 子类对象时，只调用基类析构，导致子类资源泄漏。

### 构造函数能否是虚函数？析构函数可以是纯虚函数吗
构造函数不能是虚函数（vptr 在构造函数中才初始化）。析构函数可以是纯虚函数，但必须提供定义（常用于接口类）。

### 纯虚函数和虚函数的区别
纯虚函数无实现，类成为抽象类不能实例化；虚函数有默认实现，可被重写。

### 抽象类和接口的区别
抽象类可以有成员变量和非纯虚函数；“接口”通常指只有纯虚函数 + 无成员变量的抽象类（C++ 无原生接口）。

### 重载、重写、重定义的区别
- 重载（overload）：同一作用域，函数名同参数不同  
- 重写（override）：子类重新实现父类虚函数  
- 重定义（hiding）：子类定义同名函数，隐藏父类版本（非虚函数）

### 拷贝构造函数和赋值运算符重载的区别
拷贝构造：创建新对象；赋值运算符：已存在对象赋值。常一起实现（copy-and-swap 惯用法）。

### 深拷贝和浅拷贝的区别
浅拷贝只复制指针，深拷贝复制指向的资源。内置类型默认浅拷贝，自定义类型需手动实现深拷贝。

### Rule of Three / Rule of Five
有以下任一需实现另两个（三法则）：析构、拷贝构造、拷贝赋值。C++11 后加移动构造和移动赋值（五法则）。

### 为什么构造函数不能是虚函数
构造函数执行时 vptr 尚未初始化，无法实现动态绑定。

### final 和 override 关键字
override：显式声明重写虚函数，编译器检查；final：禁止虚函数被重写或类被继承。

### friend 关键字的作用
打破封装，允许指定函数/类访问 private/protected 成员。慎用。

### C++ 中如何防止一个类被继承
C++11 后用 `final` 关键字：`class A final {}`

## 内存管理
### C++ 内存分区（五段内存模型）
栈、堆、全局/静态存储区、常量存储区、代码区。

### 堆和栈的区别
栈：自动管理，连续，快速；堆：手动管理，动态分配，易碎片。

### new 和 malloc 的区别
new 调用构造函数、类型安全、抛异常；malloc 纯内存分配、返回 void*、返回 NULL。

### delete 和 delete[] 的区别
delete 调用一个析构；delete[] 调用数组每个元素的析构。

### 内存泄漏怎么检测和定位
工具：Valgrind、AddressSanitizer、Visual Studio 诊断工具。

### 什么是野指针、悬空指针？如何避免
野指针：未初始化指针；悬空指针：指向已释放内存。避免：初始化为 nullptr，delete 后置 nullptr，使用智能指针。

### RAII 原理
Resource Acquisition Is Initialization：资源获取即初始化，析构函数释放资源。智能指针、锁、文件句柄都基于 RAII。

### 智能指针了解哪些
unique_ptr（独占）、shared_ptr（共享）、weak_ptr（破环循环引用）。

### shared_ptr 实现原理？循环引用怎么解决
内部双计数：强引用（use_count）、弱引用（weak_count）。循环引用用 weak_ptr 打破。

### unique_ptr 可以拷贝吗
默认不可拷贝（删除拷贝构造），支持移动语义。

### weak_ptr 解决循环引用原理
weak_ptr 不增加强引用计数，lock() 可升级为 shared_ptr（若对象已销毁返回空）。

### make_shared 和 new 的区别
make_shared 一次分配（控制块+对象），效率更高，异常安全。

### operator new 和 operator delete 可以重载吗
可以重载（全局或类级别），用于自定义内存分配（如内存池）。

### 内存对齐规则
结构体按最大成员对齐方式填充。pragma pack 可修改。

### alignas 和 alignof 的区别
alignas 指定对齐，alignof 查询类型对齐要求。

## STL与容器
### STL 六大组件
容器、算法、迭代器、仿函数、适配器、分配器。

### vector 底层实现和扩容机制
连续内存，动态数组。扩容通常 1.5x 或 2x（实现定义），旧数据搬迁，迭代器失效。

### vector<bool> 为什么特化
节省空间，用 1 bit 表示 bool（位压缩），但牺牲了部分性能和 & 操作。

### list 和 vector 的区别
list 是双向链表，插入删除 O(1)，随机访问 O(n)；vector 是动态数组，随机访问 O(1)。

### map 和 unordered_map 的区别？什么时候用哪个
map：红黑树，有序，O(log n)；unordered_map：哈希表，平均 O(1)，无序。需排序用 map，否则优先 unordered_map。

### unordered_map 哈希冲突怎么解决
开放寻址或拉链法（主流实现用拉链法）。

### set 和 map 的底层实现
都是红黑树，set = map<key, T> 的特化（值忽略）。

### 红黑树和 AVL 树的区别
AVL 更严格平衡（高度差 ≤1），查找更快；红黑树放松平衡（通过颜色），插入删除更快。

### iterator 失效场景有哪些
vector：插入可能扩容，所有迭代器失效；删除后迭代器失效  
map/set：删除不影响其他迭代器  
list：删除仅影响当前迭代器

### 常用 STL 算法
sort、stable_sort、lower_bound、upper_bound、find、accumulate、transform、for_each（配合 lambda）

## 现代C++特性
### C++11 最重要的几个新特性
auto、lambda、智能指针、move 语义、nullptr、右值引用、decltype、constexpr、线程支持

### auto 和 decltype 的区别
auto 根据初始化表达式推导类型；decltype 根据表达式本身推导类型（不求值）。

### 移动语义和完美转发
移动：转移资源所有权（std::move）；完美转发：保持值类别（std::forward）。

### std::move 的作用
将左值强制转为右值引用，允许移动构造/赋值。

### 右值引用和左值引用的区别
左值引用绑定左值，右值引用绑定右值（临时对象），用于移动语义。

### std::forward 的作用
完美转发：在模板函数中保持参数的左值/右值属性。

### lambda 表达式底层实现
编译器生成匿名类，重载 operator()，捕获列表变成成员变量。

### std::function 和 std::bind 原理
std::function 是类型擦除的函数包装器；std::bind 预绑定参数，返回可调用对象（C++11 已不推荐，优先 lambda）。

### noexcept 的作用
声明函数不抛异常，优化性能（move 若 noexcept 才启用），异常传播时若违背直接 terminate。

### thread_local
每个线程拥有独立副本，常用于线程局部存储（如日志 ID）。

### C++20 协程了解吗
引入 co_await、co_yield、co_return，generator、task 等，支持异步编程（需编译器+库支持）。

## 多线程与并发
### 进程和线程的区别
进程有独立地址空间，线程共享进程资源。线程切换更快，开销更小。

### 线程同步方式有哪些
互斥锁、条件变量、原子操作、信号量、读写锁、屏障。

### mutex、condition_variable 怎么配合使用
生产者消费者模型：mutex 保护队列，condition_variable 通知唤醒。

### std::atomic 原理？a++ 是原子操作吗
基于 CPU 原子指令（lock cmpxchg 等）。a++ 不是原子（读-改-写三步），需用 atomic<int>::fetch_add。

### 死锁产生的四个条件？如何避免
互斥、持有并等待、不剥夺、循环等待。避免：固定加锁顺序、超时放弃、使用 std::lock。

### 线程安全单例怎么写
双检查锁 + volatile（C++11 前）或 Meyers' Singleton（C++11 后推荐，静态局部变量线程安全）。

### 实现一个线程池
任务队列 + 固定数量线程 + 条件变量（等待任务）+ 优雅退出机制。

## 编译链接与底层
### C++ 程序编译链接全过程
预处理（.i）→ 编译（.s）→ 汇编（.o/.obj）→ 链接（可执行文件）

### 静态链接和动态链接的区别
静态链接：库打包进可执行文件，体积大，独立运行  
动态链接：运行时加载 .so/.dll，体积小，可共享更新

### 四种 cast 转换
static_cast（基本类型、上下转型）、dynamic_cast（运行时类型检查，RTTI）、const_cast（去 const）、reinterpret_cast（强制转换，如指针转整数）

### 模板实例化发生在什么时候
编译期（显式实例化除外），导致代码膨胀。

### 函数模板和类模板的区别
函数模板可自动推导，类模板必须显式指定类型（C++17 后类模板参数可推导）。

### SFINAE 和 std::enable_if
Substitution Failure Is Not An Error：模板重载失败不报错，常用于条件启用模板（enable_if）。

## 网络编程
### TCP 三次握手、四次挥手
**三次握手**
- 目的：建立双向可靠连接，同步双方初始序列号（ISN）
- 流程：
  1. 主动方（CLOSED→SYN_SENT）：发 SYN + 自身 ISN
  2. 被动方（LISTEN→SYN_RCVD）：回 SYN+ACK + 自身 ISN + 确认号=主动方 ISN+1
  3. 主动方（SYN_SENT→ESTABLISHED）：回 ACK + 确认号=被动方 ISN+1 → 被动方→ESTABLISHED

 **四次挥手**
- 目的：关闭双向连接，确保数据完全传输（以主动方先关闭为例）
- 流程：
  1. 主动方（ESTABLISHED→FIN_WAIT_1）：发 FIN（不再发数据，可收数据）
  2. 被动方（ESTABLISHED→CLOSE_WAIT）：回 ACK → 主动方→FIN_WAIT_2
  3. 被动方（CLOSE_WAIT→LAST_ACK）：处理完数据后发 FIN
  4. 主动方（FIN_WAIT_2→TIME_WAIT）：回 ACK → 被动方→CLOSED；主动方等 2MSL 后关闭

### TIME_WAIT 和 CLOSE_WAIT 的区别
- TIME_WAIT：
  - 所属方：主动关闭方
  - 触发：发送最后一个 ACK 后
  - 时长：2MSL（避免旧报文干扰）
  - 问题：短连接场景易端口耗尽
- CLOSE_WAIT：
  - 所属方：被动关闭方
  - 触发：收到对方 FIN 并回复 ACK 后
  - 时长：无固定值（需应用层调用 close()）
  - 问题：应用层未关连接会导致资源泄漏

### select、poll、epoll 的区别与原理
- select：
  - 底层：位图（fd_set）
  - 连接上限：FD_SETSIZE（默认 1024）
  - 效率：O(n)（遍历所有 fd）
  - 特性：水平触发、每次拷贝 fd 集合、跨平台
  - 场景：少量连接
- poll：
  - 底层：动态数组（pollfd[]）
  - 连接上限：无（依赖内存）
  - 效率：O(n)（遍历所有 fd）
  - 特性：水平触发、每次拷贝数组、跨平台
  - 场景：中量连接
- epoll（Linux 特有）：
  - 底层：红黑树+就绪链表
  - 连接上限：无（依赖内存）
  - 效率：O(1)（仅处理就绪 fd）
  - 特性：水平/边缘触发、仅初始化拷贝、共享 fd
  - 场景：高并发（万级+）

### Reactor 和 Proactor 模型
- Reactor（反应堆）：
  - 核心：被动等事件就绪（I/O 可读/可写）
  - 操作：事件就绪后应用层主动读写
  - 依赖：非阻塞 I/O + 事件通知
  - 特点：易实现、复杂度低
  - 示例：Nginx（epoll+Reactor）
- Proactor（前摄器）：
  - 核心：主动发起 I/O 操作，等完成通知
  - 操作：内核完成读写后通知应用层
  - 依赖：异步 I/O + 完成通知
  - 特点：复杂度高、依赖内核支持
  - 示例：Windows IOCP

## 设计模式与架构

## 手撕代码
### 手撕线程安全单例
```cpp
class Singleton {
public:
    static Singleton& getInstance() {
        static Singleton instance;   // C++11 魔法静态，线程安全
        return instance;
    }
private:
    Singleton() = default;
    Singleton(const Singleton&) = delete;
    Singleton& operator=(const Singleton&) = delete;
};
```
一句话：C++11 之后局部静态变量初始化是线程安全的，直接写就行
### 手撕简易 shared_ptr
```cpp
template<typename T>
class shared_ptr {
    T* ptr;
    int* count;                     // 引用计数

public:
    explicit shared_ptr(T* p = nullptr) : ptr(p) {
        if (p) count = new int(1);
        else   count = nullptr;
    }

    // 拷贝构造
    shared_ptr(const shared_ptr& other) : ptr(other.ptr), count(other.count) {
        if (count) ++(*count);
    }

    // 拷贝赋值
    shared_ptr& operator=(const shared_ptr& other) {
        if (this != &other) {
            if (count && --(*count) == 0) {  // 先释放旧资源
                delete ptr; delete count;
            }
            ptr = other.ptr;
            count = other.count;
            if (count) ++(*count);
        }
        return *this;
    }

    // 移动构造（C++11 加分）
    shared_ptr(shared_ptr&& other) noexcept : ptr(other.ptr), count(other.count) {
        other.ptr = nullptr;
        other.count = nullptr;
    }

    ~shared_ptr() {
        if (count && --(*count) == 0) {
            delete ptr;
            delete count;
        }
    }

    T* get() const { return ptr; }
    T& operator*() const { return *ptr; }
    T* operator->() const { return ptr; }
    int use_count() const { return count ? *count : 0; }
};
```
核心三件套：指针 + 计数指针 + 拷贝时计数++，析构时计数--

### 手撕 LRU Cache
```cpp
class LRUCache {
    int cap;
    list<pair<int,int>> cache;                    // key-value + 访问顺序
    unordered_map<int, list<pair<int,int>>::iterator> mp;

public:
    LRUCache(int capacity) : cap(capacity) {}

    int get(int key) {
        if (mp.find(key) == mp.end()) return -1;
        cache.splice(cache.begin(), cache, mp[key]);  // 移到最前
        return mp[key]->second;
    }

    void put(int key, int value) {
        if (get(key) != -1) {                         // 已存在就更新
            mp[key]->second = value;
            return;
        }
        if (cache.size() == cap) {                    // 淘汰最久未使用
            int del_key = cache.back().first;
            cache.pop_back();
            mp.erase(del_key);
        }
        cache.emplace_front(key, value);
        mp[key] = cache.begin();
    }
};
```
核心：哈希表 + 双向链表，splice O(1) 移动节点
### 手撕线程池
```cpp
class ThreadPool {
    vector<thread> workers;
    queue<function<void()>> tasks;
    mutex mtx;
    condition_variable cv;
    bool stop = false;

public:
    ThreadPool(int n) {
        for (int i = 0; i < n; ++i) {
            workers.emplace_back([this] {
                while (true) {
                    function<void()> task;
                    {
                        unique_lock<mutex> lock(mtx);
                        cv.wait(lock, [this] { return stop || !tasks.empty(); });
                        if (stop && tasks.empty()) return;
                        task = move(tasks.front());
                        tasks.pop();
                    }
                    task();
                }
            });
        }
    }

    template<typename F>
    void add(F&& f) {
        {
            unique_lock<mutex> lock(mtx);
            tasks.emplace(forward<F>(f));
        }
        cv.notify_one();
    }

    ~ThreadPool() {
        {
            unique_lock<mutex> lock(mtx);
            stop = true;
        }
        cv.notify_all();
        for (auto& t : workers) t.join();
    }
};
```
核心：任务队列 + 条件变量唤醒 + RAII 析构优雅退出

### 手撕生产者消费者
```cpp
queue<int> q;
mutex mtx;
condition_variable cv;

void producer() {
    for (int i = 0; i < 100; ++i) {
        {
            unique_lock<mutex> lock(mtx);
            q.push(i);
        }
        cv.notify_one();
    }
}

void consumer() {
    while (true) {
        unique_lock<mutex> lock(mtx);
        cv.wait(lock, [&] { return !q.empty(); });
        int data = q.front(); q.pop();
        lock.unlock();
        cout << data << endl;
    }
}
```
核心：wait 必须配合谓词，防止虚假唤醒

### 手撕简易 vector
```cpp
template<typename T>
class Vector {
    T* data;
    size_t size_, capacity_;

    void reallocate() {
        capacity_ = capacity_ ? capacity_ * 2 : 1;
        T* new_data = new T[capacity_];
        for (size_t i = 0; i < size_; ++i)
            new_data[i] = move(data[i]);
        delete[] data;
        data = new_data;
    }

public:
    void push_back(const T& val) {
        if (size_ == capacity_) reallocate();
        data[size_++] = val;
    }
    // ... 其他接口
};
```
核心：三指针 + 2倍扩容 + move 优化
