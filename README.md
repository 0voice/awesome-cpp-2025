# C++ 零基础入门到面试通关：2025 一站式学习指南

🌟 本仓库旨在为学习 C++ 的程序员们提供学习资源导航

💡 涵盖从基础知识到实战项目的资料与示例，帮助你快速入门并逐步进阶！
<p>
  <a href="https://github.com/0voice/awesome-modern-cpp-2025/stargazers">
    <img src="https://img.shields.io/github/stars/0voice/awesome-modern-cpp-2025?color=ffcb47&label=%E2%AD%90%20Stars&style=for-the-badge" alt="Stars"/>
  </a>
  <a href="https://github.com/0voice/awesome-modern-cpp-2025/fork">
    <img src="https://img.shields.io/github/forks/0voice/awesome-modern-cpp-2025?color=34d058&label=%F0%9F%8D%B4%20Forks&style=for-the-badge" alt="Forks"/>
  </a>
  <a href="https://github.com/0voice/awesome-modern-cpp-2025/watchers">
    <img src="https://img.shields.io/github/watchers/0voice/awesome-modern-cpp-2025?color=8b46ff&label=%F0%9F%94%94%20Watch&style=for-the-badge" alt="Watchers"/>
  </a>
</p>


[English README](https://github.com/0voice/awesome-modern-cpp-2025/blob/main/README.en.md)
## 适用人群
- 零基础编程小白
- 在校计算机相关专业学生
- 其他语言转 C++ 开发者
- 需巩固基础、补充面试知识点的初级 C++ 工程师

## 为什么选择 C++？
- 核心优势：性能高效、跨平台、应用场景广泛（后端 / 服务器、嵌入式、游戏开发等）
- 就业前景：互联网、金融科技、物联网、汽车电子等主流行业岗位需求稳定，稀缺性强，薪资溢价明显。
- 生态成熟：STL/Boost等库完善，C++17/20新特性降低开发门槛，经典不过时。
- 技术硬核：培养底层思维与性能优化能力，技术迁移性强（适配Go/Rust等）；

关于这个问题，请参考：
- [为什么你应该学习 C++](https://www.youtube.com/shorts/1Zku-mXDY9g)
- [C++ 的应用领域及为什么学习 C++ 编程语言](https://www.youtube.com/watch?v=brqRL_t0RmM)
- [在 AI 时代，你应该学习 C++ 吗？](https://www.youtube.com/watch?v=1POqwCxIhjo)
- [C++ 的真相（值得你花时间吗？）](https://www.youtube.com/watch?v=q1ZmFc-sqNc)
- [这才是你需要的 C 语言、C++ 学习路线](https://www.youtube.com/watch?v=gO4Jp78nM0g)

## 目录
- [学习路线](#学习路线)
- [核心知识点](#核心知识点)
- [C++现代特性进阶](#c-现代特性进阶c20--c23)
- [Linux环境下开发C++](https://github.com/0voice/awesome-modern-cpp-2025/tree/main/cpp-on-linux)
- [推荐资源](#推荐资源)
- [常用工具](#常用工具)
- [应用方向](#应用方向)
- [实战项目](#实战项目)
- [面试题](#面试题)

## 学习路线
  
  <img src="https://raw.githubusercontent.com/0voice/awesome-modern-cpp-2025/main/roadmap/cpp-roadmap.svg">        

### 阶段 0：准备工作（0.5–1 天）
**目标**：搭建开发环境，编译并运行第一个 C++ 程序  
- Windows（MinGW + VS Code）
- macOS（Xcode 命令行工具）
- Linux（GCC/Clang）

若尚未完成此步骤或遇到问题，请参考 [C++ 开发环境搭建指南](https://github.com/0voice/awesome-modern-cpp-2025/blob/main/environment_setup/README.md)。

### 阶段 1：基础入门（2–3 周）
**目标**：掌握基础语法，理解编译流程，规避常见陷阱  
**核心知识点**：
- 变量、数据类型、运算符、控制流、函数、数组、字符串
- 指针与引用基础、const/volatile/static 基础用法
- 编译与链接、头文件保护机制
- CMake 基础（多文件项目）

**实战项目**：[计算器](https://github.com/arash28134/simple-calculator)、[猜数字](https://github.com/LargeRaindrop/NumberGuess)、简易通讯录（数组版）

### 阶段 2：OOP 核心（3–4 周）
**目标**：设计规范类，理解多态机制  
**学习模块**：
1. 类与对象、构造函数/析构函数
2. 拷贝/移动语义、深拷贝 vs 浅拷贝
3. 继承、虚函数、虚函数表（vtable）
4. 静态成员、友元、模板基础

**实战项目**：[学生管理系统](https://github.com/abhiishekpanchal/STUDENT-MANAGEMENT-SYSTEM---OOPS-CONCEPTS)/[图书管理系统](https://github.com/MAbubakkar/Library-Management-System    )

### 阶段 3：现代 C++ 与 STL（2–3 周）
**目标**：编写地道、高效的代码  
**核心知识点**：
- 全量 STL 容器与算法
- 迭代器及失效场景
- Lambda 表达式、auto、范围 for、智能指针
- 异常处理、文件 IO

**实战项目**：[高性能词频统计工具](https://github.com/NimraGJay/STL)、[简易日志系统](https://github.com/Ahmed-Ibrahim-30/Logging-System)

### 阶段 4：系统编程（4–6 周）
**目标**：开发生产级核心组件  
**核心知识点**：
- RAII 与智能指针深度解析
- 多线程编程（std::thread、互斥锁、条件变量、原子操作）
- 线程池实现
- Socket 编程（TCP/UDP）
- 设计模式、调试与性能分析

**重点项目**
- [高性能线程池](https://github.com/progschj/ThreadPool)
- [带线程池的轻量 HTTP 服务器](https://github.com/yhirose/cpp-httplib)
- [高性能聊天服务器](https://github.com/chronoxor/CppServer)

### 阶段 5：面试冲刺（2–3 周）
**目标**：自信应对技术面试  
- 全知识点复盘
- 150+ 高频面试题训练
- 项目讲解与模拟面试

### 打卡表
| 周数 | 阶段 | 推荐资源 | 阶段任务 |
|------|----------|----------------|--------------|
| 第0周 | 阶段0 | [C++ 开发环境搭建指南](https://github.com/0voice/awesome-modern-cpp-2025/blob/main/environment_setup/README.md)或[清晰易懂的C+＋开发环境搭建教程](https://blog.51cto.com/u_16349720/14112761)| 完成开发环境搭建 |
| 第1-3周  | 阶段 1 | [黑马程序员](https://www.bilibili.com/video/BV1et411b73Z/?spm_id_from=333.337.search-card.all.click&vd_source=b1133efda5c53025ed35233121e57402)| 完成3个demo放GitHub |
| 第4-7周  | 阶段 2 | 《C++ Primer Plus》 | 学生/图书管理系统完整版 |
| 第7-9周  | 阶段 3 | 《Effective Modern C++》 | 词频统计工具 |
| 第10-15周 | 阶段 4 | 重点项目三选一或[实战项目](#实战项目)中选一个大项目 | 完成项目传GitHub |
| 第16-18周 | 阶段 5 | 牛客/LeetCode C++ 专区 | 高频笔面题 + 项目复盘 |

## 核心知识点
### [基础语法篇](https://github.com/0voice/awesome-modern-cpp-2025/blob/main/core_knowledge/%E5%9F%BA%E7%A1%80%E8%AF%AD%E6%B3%95%E7%AF%87.md)
  - **变量与数据类型**：整型/浮点型/字符型/布尔型、const、typedef
  - **运算符与表达式**：算术/关系/逻辑运算符、复合赋值、自增自减（前置和后置）
  - **控制流**：if-else、switch、for/while/do-while、break/continue、cin/cout+iomanip、namespace
  - **函数**：定义/声明、值/引用/指针传参、返回值、函数重载、默认参数、lambda简介
  - **数组与字符串**：一维数组、C风格字符串和std::string（常用操作）
  - **指针入门**：定义/解引用/取地址、指针与数组/函数、野指针/nullptr、指针和引用（核心区别）

### [面向对象篇](https://github.com/0voice/awesome-modern-cpp-2025/blob/main/core_knowledge/%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E7%AF%87.md)
  - **类与对象**：class/struct区别、成员变量/函数、对象创建（栈/堆）、访问控制（public/private/protected）
  - **构造与析构**：默认/带参/拷贝/移动构造与移动赋值、析构函数（虚析构必要性）、初始化列表、RAII原则、智能指针初步认识、Rule of Five
  - **继承与多态**：继承语法、基类/派生类、虚函数、纯虚函数+抽象类、vtable简介
  - **运算符重载**：赋值/算术/关系/<<运算符、深拷贝和浅拷贝
  - **模板基础**：函数模板、类模板、STL容器底层关联

### [进阶基础篇](https://github.com/0voice/awesome-modern-cpp-2025/blob/main/core_knowledge/%E8%BF%9B%E9%98%B6%E5%9F%BA%E7%A1%80%E7%AF%87.md)
  - **STL**：容器（vector/list/map/unordered_map/set）、迭代器（失效场景）、常用算法（sort/find/count/for_each）、lambda配合STL
  - **文件IO**：文本/二进制文件读写、fstream、文件指针操作、数据持久化
  - **异常处理**：try-catch/throw、自定义异常类、noexcept
  - **内存管理**：new/delete、malloc/free区别、智能指针（unique_ptr/shared_ptr/weak_ptr）、内存泄漏避免
  - **现代特性**：auto、decltype、lambda

### [实战提升篇](https://github.com/0voice/awesome-modern-cpp-2025/blob/main/core_knowledge/%E5%AE%9E%E6%88%98%E6%8F%90%E5%8D%87%E7%AF%87.md)
  - **多线程**：std::thread、mutex/lock_guard、condition_variable、atomic、线程池原理、死锁避免
  - **网络编程**：TCP/UDP基础、Socket编程流程（服务端/客户端）、TCP粘包问题、IO多路复用简介
  - **设计模式**：单例（线程安全版）、简单工厂/工厂方法、策略模式（适用场景+核心代码）



## C++ 现代特性进阶（C++20 & C++23）

### 1. Concepts 与 requires（C++20）
作用：对模板参数添加清晰、可读性高的约束，替代复杂的 SFINAE。
什么时候用：所有泛型库、自己写模板函数/类时必开。

```cpp
template<typename T>
concept Integral = std::is_integral_v<T>;

template<Integral T>
T add(T a, T b) { return a + b; }

// 自定义复杂概念
template<typename T>
concept Hashable = requires(T x) {
    { std::hash<T>{}(x) } -> std::convertible_to<std::size_t>;
};

template<Hashable T>
class Cache { /* ... */ };
```
常见坑：概念太严格会导致本来能编译的代码过不去，建议先写宽松概念，再逐步收紧。

### 2. Ranges 库（C++20）
作用：函数式风格处理序列，支持延迟计算与管道写法，代码更简洁高效。
什么时候用：任何需要 filter/map/take/drop/sort 的地方。
优势：不产生中间容器，缓存友好，代码量减半。
```cpp
std::vector<int> v = {1, 2, 3, 4, 5, 6, 7, 8, 9, 10};

auto result = v
    | std::views::filter([](int x) { return x % 2 == 0; })   // 偶数
    | std::views::transform([](int x) { return x * x; })     // 平方
    | std::views::take(4);                                   // 前 4 个

for (int x : result) std::cout << x << ' ';  // 4 16 36 64
```

### 3. std::span（C++20）
作用：轻量级、非拥有权的固定大小数组/容器视图，安全传递连续数据。
什么时候用：函数参数需要“一段连续内存”时，全部改 span。
```cpp
void process(std::span<const int> data) {
    for (int x : data) std::cout << x << ' ';
}

std::vector<int> vec{1, 2, 3};
int arr[] = {4, 5, 6};
process(vec);
process(arr);
```
常见错误：span 保存的是视图，原始数据析构了会悬空。确保生命周期比 span 长。

### 4. Coroutines 协程（C++20）
作用：编写异步/生成器代码更自然，无需回调或线程。

```cpp
#include <coroutine>
#include <iostream>

struct Generator {
    struct promise_type {
        int current_value;
        std::suspend_always yield_value(int value) {
            current_value = value;
            return {};
        }
        std::suspend_always initial_suspend() { return {}; }
        std::suspend_always final_suspend() noexcept { return {}; }
        Generator get_return_object() { return {}; }
        void return_void() {}
        void unhandled_exception() {}
    };
    bool next() { /* 实际使用需配合协程库 */ return false; }
    int value() { return 0; }
};
```

### 5. deducing this（C++23）
作用：让成员函数把 this 当作普通参数传，完美解决 CRTP 和递归 lambda 的痛点。

```cpp
struct Node {
    Node* left = nullptr;
    Node* right = nullptr;

    int height(this Node const& self) {
        if (!self.left && !self.right) return 1;
        int l = self.left ? self.left->height() : 0;
        int r = self.right ? self.right->height() : 0;
        return 1 + std::max(l, r);
    }
};
```

### 6. std::expected（C++23）
作用：携带值或错误信息的现代返回值类型，比异常和返回值对更轻量。
适用场景：所有可能失败但不值得抛异常的操作（解析、IO、计算等）。
```cpp
std::expected<int, std::string> safe_divide(int a, int b) {
    if (b == 0) return std::unexpected("division by zero");
    return a / b;
}

auto result = safe_divide(42, 7)
                .and_then([](int x) { return safe_divide(100, x); })
                .value_or(-1);
```

### 7. std::mdspan（C++23）
作用：非拥有权的多维数组视图，适合图像、矩阵、科学计算场景。

```cpp
#include <mdspan>

void print(std::mdspan<const int, std::dextents<size_t, 2>> matrix) {
    for (size_t i = 0; i < matrix.extent(0); ++i) {
        for (size_t j = 0; j < matrix.extent(1); ++j)
            std::cout << matrix(i, j) << ' ';
        std::cout << '\n';
    }
}
```

### 8. std::flat_map / std::flat_set（C++23）
作用：基于连续容器的有序映射/集合，缓存友好，查找速度更快。
什么时候用：配置表、字典、频繁查找的小数据集（< 10万条）全换 flat_map。
```cpp
std::flat_map<std::string, int> m = {
    {"apple", 5}, {"banana", 3}, {"orange", 8}
};
// 自动排序，内存连续，适合热点数据
```

### 9. 多维下标 operator[]（C++23）
作用：原生支持多维数组下标操作，语法更直观。

```cpp
int arr[3][4][5]{};
arr[1, 2, 3] = 42;        // 相当于 arr[1][2][3] = 42;
```

### 10. Lambda 增强（C++23）
作用：支持模板参数、属性标记，表达能力更强。

```cpp
auto templated_lambda = []<typename T>(T a, T b) {
    return a + b;
};

auto attributed = [] [[nodiscard]] (int x) { return x * x; };
```


## 推荐资源
### 视频推荐
| 视频名称 | 链接 |
|----------|------|
| 黑马程序员匠心之作 C++教程从0到1入门编程,学习编程不再难 | [Bilibili](https://www.bilibili.com/video/BV1et411b73Z/?spm_id_from=333.337.search-card.all.click&vd_source=b1133efda5c53025ed35233121e57402) |
| 【整整300集】这绝对是2025年B站最全最细的C++零基础全套教程 | [Bilibili](https://www.bilibili.com/video/BV1Y6oVYGE4v/?spm_id_from=333.337.search-card.all.click&vd_source=b1133efda5c53025ed35233121e57402) |
| C++ Programming Course - Beginner to Advanced | [YouTube](https://www.youtube.com/watch?v=8jLOx1hD3_o) |
| Full C++ Crash Course for Beginners (2025 Edition) | [YouTube](https://www.youtube.com/watch?v=zKddJjNc0_s) |
| C++ FULL COURSE For Beginners | [YouTube](https://www.youtube.com/watch?v=GQp1zzTwrIg) |
| The Cherno 的 C++ 系列 | [YouTube](https://www.youtube.com/playlist?list=PLlrATfBNZ98dudnM48yfGUldqGD0S4FFb) |
| Coding for Everyone: C and C++ Specialization | [Coursera](https://www.coursera.org/specializations/coding-for-everyone) |
| C++ For C Programmers, Part A & B | [Coursera](https://www.coursera.org/learn/c-plus-plus-a) |
| C++ Programming: Basic Skills | [edX](https://www.edx.org/learn/c-programming/codio-c-programming-basic-skills) |
| Programming Abstractions (CS106B) | [YouTube](https://www.youtube.com/playlist?list=PLFE6E58F856038C69) |

### 实体书推荐
| 书籍名称                                      | 作者                | 难度 | 简介                                                                 |
|-----------------------------------------------|---------------------|------|----------------------------------------------------------------------|
| 《C++ Primer Plus》（第 6 版）                 | Stephen Prata       | ★★☆☆☆ | 零基础友好，语言通俗、例子贴近生活，从语法到面向对象逐步递进，每章配套练习题。适合纯新手稳步搭建基础，唯一不足是未涵盖 C++11+ 现代写法。 |
| 《C++ Primer》（第 6 版）                      | Stanley B. Lippman 等 | ★★★☆☆ | 全面系统的 C++ 圣经，覆盖语法、STL 及 C++11+ 现代特性，强调实战实践。知识点密度高、讲解深入，比第 5 版更易入门，适合有基础后夯实体系或进阶现代写法。 |
| 《Accelerated C++》           | Andrew Koenig & Barbara E. Moo | ★★★☆☆ | 项目驱动式快速入门，跳过冗余内容，聚焦高效、规范的实战代码。适合有轻微编程基础、想快速上手项目的学习者。 |
| 《Programming: Principles and Practice Using C++》（第 2 版） | Bjarne Stroustrup（C++之父） | ★★★☆☆ | 兼顾原则与实践，不只是教语法，更侧重培养抽象思维与算法能力。适合想理解 C++ 设计哲学、打好底层逻辑的学习者。 |
| 《Effective C++》（第 3 版）                   | Scott Meyers        | ★★★★☆ | 提炼 55 条核心最佳实践，直指代码陷阱。是初学者向中级进阶的必备读物，能快速提升代码质量。 |
| 《The C++ Programming Language》（第 4 版）| Bjarne Stroustrup（C++之父） | ★★★★★ | 官方权威参考手册，详尽覆盖 C++ 标准及高级特性（含现代特性）。适合各阶段开发者查阅。 |
| 《Modern C++ Design》     | Andrei Alexandrescu | ★★★★★ | 深入讲解模板元编程与泛型设计模式，聚焦高阶开发技巧。仅针对有丰富经验的 C++ 程序员，新手慎入。 |

**难度指数：**    
★☆☆☆☆ ~ ★★☆☆☆：纯新手可直接阅读  
★★★☆☆：需具备一定基础 + 每日编码练习  
★★★★☆ ~ ★★★★★：仅限中高级水平学习者  

### 电子书推荐
| 书籍名称 | 作者 | 简介 |
|----------|-----------|------|
| [A Complete Guide to Programming in C++](https://www.idpoisson.fr/volkov/C%2B%2B.pdf) | Ulla Kirchartz & Peter Müller | 从零基础到高级，覆盖语法、OOP 和 STL，带练习和参考。 |
| [Beginning C++ Programming](https://notalentgeek.github.io/note/note/project/project-independent/pi-brp-beginning-c-programming/document/20170807-1504-cet-1-book-and-source-1.pdf) | Ivor Horton | 入门指南，逐步讲解语法、函数和类，适合初学者。 |
| [C++ Tutorial](https://cds.iisc.ac.in/wp-content/uploads/DS286.AUG2016.Lab2_.cpp_tutorial.pdf) | IISc Bangalore | 简明教程，焦点基础语法、指针和文件 IO，大学讲义风格。 |
| [CS 200: Concepts of Programming using C++ (Spring 2025)](https://rachel.likespizza.com/course-archives/202501_CS200.pdf) | Rachel Wil Singh | 2025 课程笔记，覆盖基础概念、数据结构和调试。 |
| [C++ Annotations (Version 11.0)](https://www.icce.rug.nl/documents/cplusplus/11.0/C++Annotations-11.0.pdf) | Frank B. Brokken | 全面参考书，详细 OOP、多线程和现代特性，免费开源。 |

### 网站推荐
| 网站名称 | 简介 |
|----------|------|
| [菜鸟教程](https://www.runoob.com/cplusplus/cpp-tutorial.html) | 中文在线C++教程平台，提供从基础语法到高级主题的互动学习资源，适合零基础初学者。 |
| [LearnCpp.com](https://www.learncpp.com/) | 免费的英文C++教程网站，强调最佳实践和常见错误，避免，覆盖核心概念到现代C++特性。 |
| [CPlusPlus.com](https://cplusplus.com/) | 全面的C++参考手册和教程，包括语法解释、示例代码和论坛讨论，适合自学者和开发者。 |
| [GeeksforGeeks](https://www.geeksforgeeks.org/c-plus-plus/) | 编程知识库，提供C++算法、数据结构和面试题的详细文章与代码片段，面向求职者。 |
| [Codecademy](https://www.codecademy.com/learn/learn-c-plus-plus) | 互动式C++学习路径，通过浏览器编码练习基础到中级技能，结合项目实践。 |
| [Coursera](https://www.coursera.org/courses?query=c%2B%2B) | 大学级C++在线课程集合，如加州大学和密歇根大学的专项，包含视频、测验和证书。 |
| [CppReference](https://en.cppreference.com/w/) | 权威的C++标准库在线参考文档，精确描述API、模板和语言特性，适合专业开发者查询。 |
| [LeetCode](https://leetcode.com/problemset/all/?search=C%2B%2B) | 算法和编码挑战平台，支持C++提交，提供海量题目用于刷题和面试准备。 |
| [GitHub Awesome C++](https://github.com/fffaraz/awesome-cpp) | 精选C++开源资源列表，包括框架、库、书籍和工具，助力深入探索生态系统。 |

## 常用工具

### 1. 编译器
- [GCC](https://gcc.gnu.org/)：开源、跨平台
- [Clang/LLVM](https://clang.llvm.org/)：现代编译器，诊断优秀
- [MSVC](https://learn.microsoft.com/en-us/cpp/windows/latest-supported-vc-redist)：Windows原生
- [MinGW-w64](https://www.mingw-w64.org/)：Windows上跑GCC
- [Intel oneAPI DPC++/C++ Compiler](https://www.intel.com/content/www/us/en/developer/tools/oneapi/dpc-compiler.html)：AVX-512 向量化神器
- [Emscripten](https://emscripten.org/)：C++ 编译到 WebAssembly

### 2. 集成开发环境
- [Visual Studio](https://visualstudio.microsoft.com/)：Windows 全家桶
- [CLion](https://www.jetbrains.com/clion/)：JetBrains系最强C++ IDE
- [VSCode + C++ 插件](https://code.visualstudio.com/)：轻量神器
- [Qt Creator](https://www.qt.io/product/development-tools)：Qt官方IDE
- [Visual Studio Code + CMake Tools + clangd](https://code.visualstudio.com/)：2025年最流行组合
- [Codelite](https://codelite.org/)：免费开源替代
- [Cevelop](https://www.cevelop.com/)：Eclipse CDT的现代化分支

### 3. 构建系统
- [CMake](https://cmake.org/)：事实标准
- [Meson](https://mesonbuild.com/)：比CMake 更快、更简洁（2025 增长最猛）
- [Ninja](https://ninja-build.org/)：极速构建后端
- [Bazel](https://bazel.build/)：Google出品，大型仓库神器
- [xmake](https://xmake.io/)：国产现代构建，Lua配置超爽
- [Premake](https://premake.github.io/)：轻量跨平台生成器

### 4. 调试器 & 性能分析
- [GDB](https://sourceware.org/gdb/) / [LLDB](https://lldb.llvm.org/)
- [WinDbg](https://learn.microsoft.com/en-us/windows-hardware/drivers/debugger/)：Windows 内核调试
- [Tracy Profiler](https://github.com/wolfpld/tracy)：2025最火帧级性能分析神器
- [Perfetto](https://perfetto.dev/)：Google出品系统级追踪
- [Valgrind](https://valgrind.org/) + [AddressSanitizer](https://clang.llvm.org/docs/AddressSanitizer.html)：内存错误检测
- [RenderDoc](https://renderdoc.org/)：图形调试神器（Vulkan/DX/OpenGL）

### 5. 包管理器
- [vcpkg](https://vcpkg.io/)：微软官方，VS集成最丝滑
- [Conan 2.x](https://conan.io/)：最成熟的C++包管理
- [cppan](https://cppan.org/)：老牌但仍可用
- [Hunter](https://github.com/cpp-pm/hunter)：CMake 原生集成
- [Buckaroo](https://buckaroo.pm/)：新兴选手

### 6. 代码分析与测试
- [Clang-Tidy](https://clang.llvm.org/extra/clang-tidy/)：官方静态分析
- [Cppcheck](https://cppcheck.net/)：轻量 bug 检测
- [PVS-Studio](https://pvs-studio.com/)：工业级静态分析（免费给开源）
- [Google Test](https://github.com/google/googletest) / [Catch2](https://github.com/catchorg/Catch2)
- [doctest](https://github.com/doctest/doctest)：单头文件测试框架，最轻量
- [ApprovalTests.cpp](https://github.com/approvals/ApprovalTests.cpp)：黄金输出测试法

### 7. 代码格式化 & 重构
- [clang-format](https://clang.llvm.org/docs/ClangFormat.html)：行业标准
- [uncrustify](https://github.com/uncrustify/uncrustify)：高度可配置
- [astyle](http://astyle.sourceforge.net/)：老牌格式化工具
- [Sourcery](https://sourcery.ai/)（付费）：AI 驱动重构建议

### 8. 内存与性能检测
- [Valgrind](https://valgrind.org/)
- [Address/Memory/Thread Sanitizer](https://clang.llvm.org/docs/)：Clang 自带
- [gperftools](https://github.com/gperftools/gperftools)：CPU/Memory Profiler
- [tcmalloc](https://github.com/google/tcmalloc)：高性能内存分配器

### 9. 文档生成 & 可视化
- [Doxygen](https://www.doxygen.nl/)：代码文档生成
- [Sphinx + Breathe](https://www.sphinx-doc.org/)：现代文档系统
- [Graphviz](https://graphviz.org/)：类图/调用图可视化

### 10. 开发辅助
- [Git](https://git-scm.com/) + [GitKraken](https://www.gitkraken.com/) / [Fork](https://git-fork.com/)
- [Docker](https://www.docker.com/)：环境隔离
- [CMake GUI / ccmake](https://cmake.org/cmake/gui/)：可视化配置
- [Ninja + ccache](https://ccache.dev/)：编译提速 5–10 倍
- [include-what-you-use](https://include-what-you-use.org/)：头文件依赖分析
- [cpplint](https://github.com/cpplint/cpplint)：Google 风格检查
- [GitHub Copilot / Codeium / Tabnine](https://github.com/features/copilot)：AI 补全（2025 年标配）

这样一套工具链装完，从写代码 → 编译 → 调试 → 性能分析 → 部署 → CI/CD 全流程无死角，面试被问“你的开发环境怎么搭的？”直接甩这张表，面试官当场跪了。

## 应用方向
| 应用方向 | 核心场景 | 推荐框架/库 |
|----------|----------|-------------|
| **桌面应用开发** | 办公软件、工业控制界面、桌面工具、设计类软件 | [Qt](https://www.qt.io/)：跨平台全栈框架，集成 GUI、网络、数据库、多媒体。<br>[MFC](https://learn.microsoft.com/en-us/cpp/mfc/mfc-desktop-applications)：Windows 原生框架，适合 legacy 项目。<br>[wxWidgets](https://www.wxwidgets.org/)：跨平台轻量框架，原生风格。<br>[FLTK](http://www.fltk.org/)：快速轻量跨平台GUI工具包。<grok-card data-id="d9a22e" data-type="citation_card"></grok-card><br>[ImGui](https://github.com/ocornut/imgui)：立即模式GUI，最小依赖。<grok-card data-id="bcdc99" data-type="citation_card"></grok-card><br>[JUCE](https://juce.com/)：跨平台软件开发全包类库。<grok-card data-id="cada29" data-type="citation_card"></grok-card> |
| **嵌入式开发** | 车载中控、智能家居面板、医疗设备、工业控制器、路由器固件 | [Qt Embedded](https://www.qt.io/qt-for-embedded-linux)：嵌入式 GUI，适配 ARM 等。<br>[FreeRTOS](https://www.freertos.org/)：轻量 RTOS，资源受限设备。<br>[Yocto/Buildroot](https://www.yoctoproject.org/)：Linux 嵌入式系统。<br>[ETL](https://github.com/ETLCPP/etl)：嵌入式模板库，无标准库依赖。<grok-card data-id="8a2a21" data-type="citation_card"></grok-card><br>[tbox](https://github.com/tboox/tbox)：多平台 glib-like 库。<grok-card data-id="a647e0" data-type="citation_card"></grok-card><br>[lwIP](https://savannah.nongnu.org/projects/lwip/)：轻量TCP/IP栈。<grok-card data-id="a9bbf3" data-type="citation_card"></grok-card><br>[DPDK](https://www.dpdk.org/)：快速数据包处理库。<grok-card data-id="1305db" data-type="citation_card"></grok-card> |
| **后端/服务器开发** | 分布式系统、API 网关、数据库内核、高并发服务（游戏服务器、支付系统） | [Boost.Asio](https://www.boost.org/doc/libs/1_85_0/doc/html/boost_asio.html)：异步网络库，TCP/UDP/HTTP。<br>[Muduo](https://github.com/chenshuo/muduo)：Reactor 模式高并发服务器。<br>[Brpc](https://github.com/apache/incubator-brpc)：RPC 框架，多协议支持。<br>[Drogon](https://drogon.org/)：HTTP 框架，异步 IO + ORM。<br>[Seastar](https://seastar.io/)：高性能服务器框架，无锁设计。<grok-card data-id="fa5784" data-type="citation_card"></grok-card><br>[Folly](https://github.com/facebook/folly)：Facebook高性能C++库。<grok-card data-id="bb5131" data-type="citation_card"></grok-card><br>[Crow](https://crowcpp.org/)：微型Web框架，类似Flask。<grok-card data-id="d76a5f" data-type="citation_card"></grok-card> |
| **游戏开发** | 3A 游戏客户端、游戏引擎、游戏服务器、独立游戏 | [Unreal Engine](https://www.unrealengine.com/)：开源引擎，蓝图系统 + C++。<br>[Cocos2d-x](https://www.cocos.com/en/cocos2d-x)：跨平台 2D 引擎。<br>[Unity](https://unity.com/)：C# 上层 + C++ 优化。<br>[raylib](https://www.raylib.com/)：简单易用游戏编程库。<grok-card data-id="bedc09" data-type="citation_card"></grok-card><br>[SFML](https://www.sfml-dev.org/)：简单快速多媒体库。<grok-card data-id="df0e06" data-type="citation_card"></grok-card><br>[SDL2](https://www.libsdl.org/)：多媒体访问层。<grok-card data-id="354a80" data-type="citation_card"></grok-card><br>[EnTT](https://github.com/skypjack/entt)：现代C++ ECS框架。<grok-card data-id="deaa51" data-type="citation_card"></grok-card> |
| **音视频/流媒体开发** | 播放器、直播推流/拉流、视频编辑、音视频转码、监控安防 | [FFmpeg](https://ffmpeg.org/)：音视频处理库，解码/编码/传输。<br>[GStreamer](https://gstreamer.freedesktop.org/)：流媒体管道框架。<br>[SDL](https://www.libsdl.org/)：多媒体库，音频/渲染。<br>[OpenCV](https://opencv.org/)：视频分析（如人脸识别）。<br>[PortAudio](http://www.portaudio.com/)：跨平台音频I/O。<grok-card data-id="b5c9b8" data-type="citation_card"></grok-card><br>[miniaudio](https://miniaud.io/)：单文件音频库。<grok-card data-id="dd680d" data-type="citation_card"></grok-card><br>[libav](https://libav.org/)：多媒体处理工具集。<grok-card data-id="042a7d" data-type="citation_card"></grok-card> |
| **人工智能/机器学习** | 深度学习框架底层、模型推理优化、高性能计算（HPC） | [TensorFlow C++ API](https://www.tensorflow.org/api_docs/cc)：模型部署接口。<br>[LibTorch (PyTorch C++)](https://pytorch.org/cppdocs/)：动态图推理库。<br>[OpenCV](https://opencv.org/)：图像预处理/特征提取。<br>[Eigen](http://eigen.tuxfamily.org/)：矩阵运算库。<br>[ONNX Runtime](https://onnxruntime.ai/)：跨框架推理引擎。<br>[Dlib](https://dlib.net/)：机器学习工具包。<grok-card data-id="07ef52" data-type="citation_card"></grok-card><br>[ncnn](https://github.com/Tencent/ncnn)：移动端神经网络推理。<grok-card data-id="68c7cd" data-type="citation_card"></grok-card><br>[mlpack](https://mlpack.org/)：可扩展ML库。<grok-card data-id="fc1fd6" data-type="citation_card"></grok-card> |
| **系统编程/内核开发** | 操作系统内核、驱动程序、数据库内核、文件系统 | [Linux Kernel](https://www.kernel.org/)：内核 API 开发。<br>[WDF/KMDF](https://learn.microsoft.com/en-us/windows-hardware/drivers/wdf/)：Windows 驱动框架。<br>[SQLite](https://www.sqlite.org/)：嵌入式数据库内核。<br>[Boost](https://www.boost.org/)：通用C++库集合。<grok-card data-id="c5a377" data-type="citation_card"></grok-card><br>[Abseil](https://abseil.io/)：Google C++基础库。<grok-card data-id="773214" data-type="citation_card"></grok-card><br>[jemalloc](https://jemalloc.net/)：高性能内存分配器。<grok-card data-id="087a32" data-type="citation_card"></grok-card> |
| **金融科技/高频交易** | 高频交易系统、量化交易引擎、金融风控系统（要求低延迟、高可靠） | [QuickFIX](http://www.quickfixengine.org/)：FIX 协议库。<br>[Boost.Asio](https://www.boost.org/)：低延迟网络。<br>[QuantLib](https://www.quantlib.org/)：量化金融开源库。<grok-card data-id="ffb7ea" data-type="citation_card"></grok-card> |

## 实战项目
### 桌面应用开发
| 项目名称                                                         | 难度       | 核心技能                                   |
|------------------------------------------------------------------|------------|--------------------------------------------|
| [ocornut/imgui](https://github.com/ocornut/imgui)               | ★★☆☆☆     | 立即模式 GUI、调试工具                     |
| [zhuzichu520/FluentUI](https://github.com/zhuzichu520/FluentUI) | ★★☆☆☆     | 现代 Qt + Win11 风格                       |
| [microsoft/terminal](https://github.com/microsoft/terminal)    | ★★★★☆     | 大型现代化桌面、GPU 渲染                   |
| [jurplel/qmc-decode-gui](https://github.com/jurplel/qmc-decode-gui) | ★★☆☆☆ | Qt 实用工具、跨平台打包                    |
| [flameshot-org/flameshot](https://github.com/flameshot-org/flameshot) | ★★★☆☆ | 截图工具、Qt + 图像处理                     |
| [deskflow/deskflow](https://github.com/debauchee/barrier)      | ★★★★☆     | 多设备鼠标共享、跨平台网络                 |
| [wxWidgets/wxWidgets](https://github.com/wxWidgets/wxWidgets) | ★★★☆☆ | 跨平台桌面GUI框架、原生控件适配 |
| [transmission/transmission](https://github.com/transmission/transmission) | ★★★☆☆ | 跨平台BT下载工具、多协议解析、异步IO |
| [qBittorrent/qBittorrent](https://github.com/qBittorrent/qBittorrent) | ★★★☆☆ | Qt桌面开发、P2P网络传输、客户端优化 |
| [sqlitebrowser/sqlitebrowser](https://github.com/sqlitebrowser/sqlitebrowser) | ★★★☆☆ | Qt数据库可视化工具、SQL解析、跨平台打包 |
| [mltframework/shotcut](https://github.com/mltframework/shotcut) | ★★★★☆ | Qt视频编辑器、多线程渲染、FFmpeg深度集成 |
| [Genymobile/scrcpy](https://github.com/Genymobile/scrcpy) | ★★★☆☆ | Android屏幕镜像、低延迟USB/WiFi传输、ADB协议 |

### 嵌入式开发
| 项目名称                                                         | 难度       | 核心技能                                   |
|------------------------------------------------------------------|------------|--------------------------------------------|
| [bblanchon/ArduinoJson](https://github.com/bblanchon/ArduinoJson) | ★☆☆☆☆   | 静态内存 JSON                              |
| [lvgl/lvgl](https://github.com/lvgl/lvgl)                      | ★★☆☆☆     | 嵌入式 GUI 最强库                          |
| [zephyrproject-rtos/zephyr](https://github.com/zephyrproject-rtos/zephyr) | ★★★★☆ | 现代 RTOS、BLE、驱动                       |
| [platformio/platformio-core](https://github.com/platformio/platformio-core) | ★★★☆☆ | 嵌入式构建系统                             |
| [RT-Thread/rt-thread](https://github.com/RT-Thread/rt-thread)   | ★★★★☆     | 国产RTOS、组件化                      |
| [espressif/esp-idf](https://github.com/espressif/esp-idf)      | ★★★★☆     | ESP32 官方 SDK、低功耗                     |
| [ARM-software/CMSIS_5](https://github.com/ARM-software/CMSIS_5) | ★★★☆☆ | ARM内核标准接口、嵌入式固件开发 |
| [littlevgl/lv_drivers](https://github.com/littlevgl/lv_drivers) | ★★☆☆☆ | 嵌入式显示驱动、外设适配、LVGL配套驱动 |
| [chibios/ChibiOS](https://github.com/chibios/ChibiOS) | ★★★★☆ | 轻量级RTOS、实时调度、嵌入式中断管理 |
| [project-chip/connectedhomeip](https://github.com/project-chip/connectedhomeip) | ★★★★☆ | Matter智能家居协议栈、BLE/Thread、设备认证 |
| [espressif/esp-adf](https://github.com/espressif/esp-adf)           | ★★★★☆ | ESP32音频框架、Wi-Fi音频流、DSP算法 |
| [wolfSSL/wolfSSL](https://github.com/wolfSSL/wolfSSL)               | ★★★☆☆ | 嵌入式TLS/加密库、轻量SSL、硬件加密加速 |

### 后端/服务器开发
| 项目名称                                                         | 难度       | 核心技能                                   |
|------------------------------------------------------------------|------------|--------------------------------------------|
| [yhirose/cpp-httplib](https://github.com/yhirose/cpp-httplib)   | ★☆☆☆☆     | 单头文件 Web 服务器                        |
| [drogonframework/drogon](https://github.com/drogonframework/drogon) | ★★☆☆☆ | 高性能 Web 框架、协程                      |
| [chenshuo/muduo](https://github.com/chenshuo/muduo)             | ★★★★☆     | Reactor 网络库圣经                         |
| [apache/brpc](https://github.com/apache/brpc)                   | ★★★★☆     | 百度 RPC 框架、bthread                     |
| [Tencent/libco](https://github.com/Tencent/libco)               | ★★★★☆     | 协程库（微信后台在用）                     |
| [scylladb/seastar](https://github.com/scylladb/seastar)         | ★★★★★     | 共享无锁、百万 QPS                         |
| [userver-framework/userver](https://github.com/userver-framework/userver) | ★★★★★ | C++20 协程服务框架                         |
| [grpc/grpc](https://github.com/grpc/grpc) | ★★★★☆ | 高性能RPC框架、Protocol Buffers序列化 |
| [mongocxx/mongocxx](https://github.com/mongodb/mongocxx) | ★★★☆☆ | MongoDB C++驱动、文档型数据库交互 |
| [cpp-netlib/cpp-netlib](https://github.com/cpp-netlib/cpp-netlib) | ★★★☆☆ | 跨平台网络库、HTTP客户端/服务器开发 |
| [abseil/abseil-cpp](https://github.com/abseil/abseil-cpp)   | ★★☆☆☆ | Google高性能基础库、字符串/容器/并发工具 |
| [idealvin/coost](https://github.com/idealvin/coost)         | ★★★☆☆ | 协程+日志+单元测试全家桶、陈硕最新力作 |
| [oatpp/oatpp](https://github.com/oatpp/oatpp)               | ★★☆☆☆ | 零依赖Web框架、ORM、Swagger自动生成 |

### 游戏开发
| 项目名称                                                         | 难度       | 核心技能                                   |
|------------------------------------------------------------------|------------|--------------------------------------------|
| [SFML/SFML](https://github.com/SFML/SFML)                       | ★☆☆☆☆     | 轻量 2D 游戏库                             |
| [skypjack/entt](https://github.com/skypjack/entt)               | ★★☆☆☆     | ECS 架构                                   |
| [RobLoach/raylib-cpp](https://github.com/RobLoach/raylib-cpp)   | ★★☆☆☆     | 极简游戏开发库                             |
| [TheCherno/Hazel](https://github.com/TheCherno/Hazel)           | ★★★★☆     | 从零写游戏引擎（教学级）                   |
| [godotengine/godot](https://github.com/godotengine/godot)      | ★★★★☆     | 完整开源引擎                               |
| [cocos2d/cocos-engine](https://github.com/cocos/cocos-engine)| ★★★★☆     | 国内最常用的手游引擎之一                           |
| [microsoft/Zork](https://github.com/microsoft/Zork) | ★★☆☆☆ | 经典文字冒险游戏架构、交互式逻辑设计 |
| [Ogre3D/Ogre](https://github.com/OGRECave/ogre) | ★★★★☆ | 3D渲染引擎、场景管理、材质系统 |
| [Polycode/Polycode](https://github.com/ivansafrin/Polycode) | ★★★☆☆ | 跨平台游戏开发框架、2D/3D一体化开发 |
| [bkaradzic/bgfx](https://github.com/bkaradzic/bgfx)         | ★★★★☆ | 跨平台渲染后端、Vulkan/Metal/DX12抽象 |
| [NVIDIA-Omniverse/PhysX](https://github.com/NVIDIA-Omniverse/PhysX) | ★★★★☆ | 物理引擎、刚体/布料模拟、GPU加速 |
| [Urho3D/Urho3D](https://github.com/Urho3D/Urho3D)           | ★★★★☆ | 轻量级3D引擎、脚本绑定、网络同步 |
| [educ8s/Cpp-Retro-Snake-Game-with-raylib](https://github.com/educ8s/Cpp-Retro-Snake-Game-with-raylib) | ★★☆☆☆ | raylib复古贪吃蛇、游戏循环、碰撞检测、得分系统<grok-card data-id="f3188e" data-type="citation_card"></grok-card> |
| [mmistika/SFML-SnakeGame](https://github.com/mmistika/SFML-SnakeGame) | ★★☆☆☆ | SFML贪吃蛇、图形渲染、键盘输入、边界检查<grok-card data-id="163cbc" data-type="citation_card"></grok-card> |
| [pknowledge/C-Snake-Game](https://github.com/pknowledge/C-Snake-Game) | ★☆☆☆☆ | ncurses终端贪吃蛇、控制台游戏、数组模拟蛇身<grok-card data-id="166b27" data-type="citation_card"></grok-card> |
| [radumirea/cpp-tetris](https://github.com/radumirea/cpp-tetris) | ★★★☆☆ | C++俄罗斯方块克隆、方块旋转、行消除、AI备选<grok-card data-id="58ed9d" data-type="citation_card"></grok-card> |
| [educ8s/Cpp-Tetris-Game-with-raylib](https://github.com/educ8s/Cpp-Tetris-Game-with-raylib) | ★★☆☆☆ | raylib俄罗斯方块、块生成、碰撞物理、预览系统<grok-card data-id="39a6f0" data-type="citation_card"></grok-card> |
| [Nathandelenclos/Arcade](https://github.com/Nathandelenclos/Arcade) | ★★★☆☆ | SFML吃豆人+贪吃蛇、多库支持、OOP游戏架构、AI幽灵<grok-card data-id="b7995e" data-type="citation_card"></grok-card> |
| [arseniisemenow/c-cpp-brickgame-cli-desktop-tetris-snake-1](https://github.com/arseniisemenow/c-cpp-brickgame-cli-desktop-tetris-snake-1) | ★★☆☆☆ | 终端砖块游戏（Tetris+Snake）、控制台输入、多模式支持<grok-card data-id="54c902" data-type="citation_card"></grok-card> |7.7秒

### 音视频/流媒体开发
| 项目名称                                                         | 难度       | 核心技能                                   |
|------------------------------------------------------------------|------------|--------------------------------------------|
| [obsproject/obs-studio](https://github.com/obsproject/obs-studio) | ★★★★☆   | 实时推流、插件系统                         |
| [FFmpeg/FFmpeg](https://github.com/FFmpeg/FFmpeg)               | ★★★★☆     | 音视频编解码全家桶                         |
| [bluenviron/mediamtx](https://github.com/bluenviron/mediamtx)   | ★★★☆☆     | 零依赖流媒体服务器                         |
| [Haivision/srt](https://github.com/Haivision/srt)               | ★★★★☆     | 低延迟传输协议                             |
| [isl-org/Open3D](https://github.com/isl-org/Open3D)             | ★★★★☆     | 3D 数据处理、点云                          |
| [libavif/libavif](https://github.com/AOMediaCodec/libavif) | ★★★☆☆ | AVIF图像编解码、多媒体格式处理 |
| [xiph/vorbis](https://github.com/xiph/vorbis) | ★★★☆☆ | 开源音频编码、有损压缩算法、音频流处理 |
| [GStreamer/gstreamer](https://github.com/GStreamer/gstreamer) | ★★★★☆ | 流媒体处理框架、插件化架构、音视频管线 |
| [gpac/gpac](https://github.com/gpac/gpac)                   | ★★★★☆ | MP4Box作者、多媒体容器、分片/封装处理 |
| [xiph/rav1e](https://github.com/xiph/rav1e)                 | ★★★★☆ | AV1编码器、SIMD并行优化 |
| [videolan/libbluray](https://github.com/videolan/libbluray) | ★★★☆☆ | Blu-ray解码、H.265流、导航菜单 |

### 人工智能/机器学习
| 项目名称                                                         | 难度       | 核心技能                                   |
|------------------------------------------------------------------|------------|--------------------------------------------|
| [nlohmann/json](https://github.com/nlohmann/json)               | ★☆☆☆☆     | 数据预处理必备                             |
| [opencv/opencv](https://github.com/opencv/opencv)               | ★★★☆☆     | 图像预处理、DNN 模块                       |
| [Tencent/ncnn](https://github.com/Tencent/ncnn)                 | ★★★☆☆     | 手机端推理框架                             |
| [alibaba/MNN](https://github.com/alibaba/MNN)                   | ★★★★☆     | 阿里移动端推理引擎                         |
| [microsoft/onnxruntime](https://github.com/microsoft/onnxruntime) | ★★★☆☆   | 跨平台模型推理                             |
| [pytorch/pytorch (LibTorch)](https://github.com/pytorch/pytorch) | ★★★★☆   | C++ 动态图、自定义算子                     |
| [huawei-noah/UCM](https://github.com/huawei-noah/UCM) | ★★★★☆ | AI推理缓存管理、长序列推理优化 |
| [openvinotoolkit/openvino](https://github.com/openvinotoolkit/openvino) | ★★★★☆ | 英特尔推理引擎、模型优化、异构计算 |
| [dmlc/xgboost](https://github.com/dmlc/xgboost) | ★★★★☆ | 梯度提升树算法、分布式训练、机器学习工程化 |
| [PaddlePaddle/Paddle](https://github.com/PaddlePaddle/Paddle) | ★★★★☆ | 飞桨推理引擎、自定义Op、分布式训练 |
| [oneapi-src/oneDNN](https://github.com/oneapi-src/oneDNN)   | ★★★☆☆ | DNN原语库、AVX512向量化、Intel/ARM优化 |
| [kaldi-asr/kaldi](https://github.com/kaldi-asr/kaldi)       | ★★★★☆ | 语音识别工具链、声学模型、特征提取 |

### 系统编程/内核开发
| 项目名称                                                         | 难度       | 核心技能                                   |
|------------------------------------------------------------------|------------|--------------------------------------------|
| [gabime/spdlog](https://github.com/gabime/spdlog)               | ★☆☆☆☆     | 高性能日志                                 |
| [sqlite/sqlite](https://github.com/sqlite/sqlite)               | ★★★★☆     | 数据库内核、B-tree                         |
| [facebook/folly](https://github.com/facebook/folly)             | ★★★★★     | Facebook 底层库                            |
| [microsoft/Detours](https://github.com/microsoft/Detours)       | ★★★★☆     | Windows Hook                               |
| [ClickHouse/ClickHouse](https://github.com/ClickHouse/ClickHouse) | ★★★★★   | 列式数据库、向量化执行                     |
| [torvalds/linux](https://github.com/torvalds/linux)             | ★★★★★     | 内核开发                                   |
| [llvm/llvm](https://github.com/llvm/llvm) | ★★★★★ | 编译器架构、中间代码优化、多语言支持 |
| [valgrind/valgrind](https://github.com/valgrind/valgrind) | ★★★★☆ | 内存调试、性能分析、程序错误检测 |
| [jemalloc/jemalloc](https://github.com/jemalloc/jemalloc) | ★★★★☆ | 高性能内存分配器、内存碎片优化 |

### 数据处理与存储
| 项目名称 | 难度 | 核心技能 |
|----------------------------------------------------------------|--------|----------------------------------------|
| [apache/thrift](https://github.com/apache/thrift) | ★★★☆☆ | 跨语言序列化、数据传输协议、分布式通信 |
| [rapidjson/rapidjson](https://github.com/Tencent/rapidjson) | ★★☆☆☆ | 高性能JSON解析、内存高效处理、跨平台适配 |
| [leveldb/leveldb](https://github.com/google/leveldb) | ★★★☆☆ | 嵌入式键值数据库、LSM树存储、数据压缩 |
| [reactos/reactos](https://github.com/reactos/reactos)       | ★★★★★ | 开源Windows NT内核、驱动模型、文件系统 |
| [nanomsg/nng](https://github.com/nanomsg/nng)               | ★★☆☆☆ | 轻量消息库、ZeroMQ后继、异步通信 |
| [libevent/libevent](https://github.com/libevent/libevent)   | ★★★☆☆ | 事件驱动库、epoll/kqueue、Reactor模式 |

### 安全相关开发
| 项目名称 | 难度 | 核心技能 |
|----------------------------------------------------------------|--------|----------------------------------------|
| [openssl/openssl](https://github.com/openssl/openssl) | ★★★★☆ | 加密算法实现、SSL/TLS协议、安全通信 |
| [curl/curl](https://github.com/curl/curl) | ★★★☆☆ | 网络请求安全、多协议支持、证书验证 |
| [libssh2/libssh2](https://github.com/libssh2/libssh2) | ★★★☆☆ | SSH2协议实现、安全远程连接、数据加密传输 |

### 分布式系统开发
| 项目名称 | 难度 | 核心技能 |
|----------------------------------------------------------------|--------|----------------------------------------|
| [ceph/ceph](https://github.com/ceph/ceph) | ★★★★★ | 分布式存储系统、对象存储、集群管理 |
| [etcd-io/etcd-cpp-apiv3](https://github.com/etcd-io/etcd-cpp-apiv3) | ★★★☆☆ | 分布式键值存储客户端、服务发现、一致性协议 |
| [apache/rocketmq-client-cpp](https://github.com/apache/rocketmq-client-cpp) | ★★★☆☆ | 消息队列客户端、异步通信、分布式消息投递 |


## 面试题
[static 关键字的作用](interview_questions/README.md#static-关键字的作用)  
[const 关键字的作用](interview_questions/README.md#const-关键字的作用)  
[inline 内联函数和宏定义的区别](interview_questions/README.md#inline-内联函数和宏定义的区别)  
[explicit 关键字的作用](interview_questions/README.md#explicit-关键字的作用)  
[nullptr 和 NULL 的区别](interview_questions/README.md#nullptr-和-null-的区别)  
[sizeof 和 strlen 的区别](interview_questions/README.md#sizeof-和-strlen-的区别)  
[new 和 malloc 的区别](interview_questions/README.md#new-和-malloc-的区别)  
[delete 和 delete[] 的区别](interview_questions/README.md#delete-和-delete-的区别)  
[四种 cast 转换](interview_questions/README.md#四种-cast-转换)  
[C++ 程序编译链接全过程](interview_questions/README.md#c-程序编译链接全过程)  
[struct 和 class 的区别](interview_questions/README.md#struct-和-class-的区别)  
[C 和 C++ 的区别](interview_questions/README.md#c-和-c-的区别)  
[volatile 关键字的作用](interview_questions/README.md#volatile-关键字的作用)  
[多态是怎么实现的？虚函数表了解吗](interview_questions/README.md#多态是怎么实现的虚函数表了解吗)  
[基类析构函数为什么必须是虚函数](interview_questions/README.md#基类析构函数为什么必须是虚函数)  
[构造函数能否是虚函数？析构函数可以是纯虚函数吗](interview_questions/README.md#构造函数能否是虚函数析构函数可以是纯虚函数吗)  
[重载、重写、重定义的区别](interview_questions/README.md#重载重写重定义的区别)  
[拷贝构造函数和赋值运算符重载的区别](interview_questions/README.md#拷贝构造函数和赋值运算符重载的区别)  
[深拷贝和浅拷贝的区别](interview_questions/README.md#深拷贝和浅拷贝的区别)  
[Rule of Three / Rule of Five](interview_questions/README.md#rule-of-three--rule-of-five)  
[final 和 override 关键字](interview_questions/README.md#final-和-override-关键字)  
[为什么构造函数不能是虚函数](interview_questions/README.md#为什么构造函数不能是虚函数)  
[纯虚函数和虚函数的区别](interview_questions/README.md#纯虚函数和虚函数的区别)  
[抽象类和接口的区别](interview_questions/README.md#抽象类和接口的区别)  
[friend 关键字的作用](interview_questions/README.md#friend-关键字的作用)  
[C++ 中如何防止一个类被继承](interview_questions/README.md#c-中如何防止一个类被继承)  
[C++ 内存分区](interview_questions/README.md#c-内存分区)  
[堆和栈的区别](interview_questions/README.md#堆和栈的区别)  
[内存泄漏怎么检测和定位](interview_questions/README.md#内存泄漏怎么检测和定位)  
[什么是野指针、悬空指针？如何避免](interview_questions/README.md#什么是野指针悬空指针如何避免)  
[RAII 原理](interview_questions/README.md#raii-原理)  
[智能指针了解哪些](interview_questions/README.md#智能指针了解哪些)  
[shared_ptr 实现原理？循环引用怎么解决](interview_questions/README.md#shared_ptr-实现原理循环引用怎么解决)  
[unique_ptr 可以拷贝吗](interview_questions/README.md#unique_ptr-可以拷贝吗)  
[weak_ptr 解决循环引用原理](interview_questions/README.md#weak_ptr-解决循环引用原理)  
[内存对齐规则](interview_questions/README.md#内存对齐规则)  
[vector 底层实现和扩容机制](interview_questions/README.md#vector-底层实现和扩容机制)  
[iterator 失效场景有哪些](interview_questions/README.md#iterator-失效场景有哪些)  
[map 和 unordered_map 的区别？什么时候用哪个](interview_questions/README.md#map-和-unordered_map-的区别什么时候用哪个)  
[unordered_map 哈希冲突怎么解决](interview_questions/README.md#unordered_map-哈希冲突怎么解决)  
[set 和 map 的底层实现](interview_questions/README.md#set-和-map-的底层实现)  
[emplace_back 和 push_back 区别](interview_questions/README.md#emplace_back-和-push_back-区别)  
[常用 STL 算法](interview_questions/README.md#常用-stl-算法)  
[list 和 vector 的区别](interview_questions/README.md#list-和-vector-的区别)  
[STL 六大组件](interview_questions/README.md#stl-六大组件)  
[红黑树和 AVL 树的区别](interview_questions/README.md#红黑树和-avl-树的区别)  
[C++11 最重要的几个新特性](interview_questions/README.md#c11-最重要的几个新特性)  
[移动语义和完美转发](interview_questions/README.md#移动语义和完美转发)  
[std::move 的作用](interview_questions/README.md#stdmove-的作用)  
[std::forward 的作用](interview_questions/README.md#stdforward-的作用)  
[lambda 表达式底层实现](interview_questions/README.md#lambda-表达式底层实现)  
[noexcept 的作用](interview_questions/README.md#noexcept-的作用)  
[auto 和 decltype 的区别](interview_questions/README.md#auto-和-decltype-的区别)  
[右值引用和左值引用的区别](interview_questions/README.md#右值引用和左值引用的区别)  
[std::atomic 原理？a++ 是原子操作吗](interview_questions/README.md#stdatomic-原理a-是原子操作吗)  
[死锁产生的四个条件？如何避免](interview_questions/README.md#死锁产生的四个条件如何避免)  
[线程安全单例怎么写](interview_questions/README.md#线程安全单例怎么写)  
[mutex、condition_variable 怎么配合使用](interview_questions/README.md#mutexcondition_variable-怎么配合使用)  
[线程同步方式有哪些](interview_questions/README.md#线程同步方式有哪些)  
[进程和线程的区别](interview_questions/README.md#进程和线程的区别)  
[TCP 和 UDP 的区别？适用场景？](interview_questions/README.md#tcp-和-udp-的区别适用场景)  
[select、poll、epoll 的区别与原理](interview_questions/README.md#selectpoll_epoll-的区别与原理)  
[什么是粘包/拆包？如何解决？](interview_questions/README.md#什么是粘包拆包如何解决)  
[TCP 三次握手、四次挥手](interview_questions/README.md#tcp-三次握手四次挥手)  
[手撕线程安全单例](interview_questions/README.md#手撕线程安全单例)  
[手撕 LRU Cache](interview_questions/README.md#手撕-lru-cache)  
[手撕快速排序](interview_questions/README.md#手撕快速排序)  
[手撕归并排序](interview_questions/README.md#手撕归并排序)  
[手撕字符串反转](interview_questions/README.md#手撕字符串反转)  
[手撕两数之和](interview_questions/README.md#手撕两数之和)
[extern "C" 的作用](interview_questions/README.md#extern-c-的作用)  
[volatile 关键字的作用](interview_questions/README.md#volatile-关键字的作用)  
[C++程序从源代码到可执行文件的详细过程](interview_questions/README.md#c程序从源代码到可执行文件的详细过程)  
[虚函数表指针在对象内存布局中的位置](interview_questions/README.md#虚函数表指针在对象内存布局中的位置)  
[多重继承下派生类对象有几个虚函数表](interview_questions/README.md#多重继承下派生类对象有几个虚函数表)  
[什么是菱形继承](interview_questions/README.md#什么是菱形继承)  
[placement new 是什么](interview_questions/README.md#placement-new-是什么)  
[除了智能指针还有哪些避免内存泄漏的方法](interview_questions/README.md#除了智能指针还有哪些避免内存泄漏的方法)  
[vector 的 resize 和 reserve 有什么区别](interview_questions/README.md#vector-的-resize-和-reserve-有什么区别)  
[unordered_map 的负载因子是什么意思](interview_questions/README.md#unordered-map-的负载因子是什么意思)  
[STL 容器的 allocator 有什么作用](interview_questions/README.md#stl-容器的-allocator-有什么作用)  
[std::function 和 std::bind 有什么作用](interview_questions/README.md#std-function-和-std-bind-有什么作用)  
[什么是移动语义](interview_questions/README.md#什么是移动语义)  
[C++11 的 enum class 相比传统的 enum 有什么优点](interview_questions/README.md#c11-的-enum-class-相比传统的-enum-有什么优点)  
[什么是 std::initializer_list](interview_questions/README.md#什么是-std-initializer-list)  
[std::unique_lock 和 std::lock_guard 有什么区别](interview_questions/README.md#std-unique-lock-和-std-lock-guard-有什么区别)  
[C++ 内存模型中的 std::memory_order 有哪几种](interview_questions/README.md#c-内存模型中的-std-memory-order-有哪几种)  
[什么是虚假唤醒](interview_questions/README.md#什么是虚假唤醒)  
[简述无锁编程的优缺点](interview_questions/README.md#简述无锁编程的优缺点)  
[TIME_WAIT 状态是什么](interview_questions/README.md#time-wait-状态是什么)  
[什么是 Reactor 和 Proactor 网络模型](interview_questions/README.md#什么是-reactor-和-proactor-网络模型)  
[MySQL 的存储引擎 InnoDB 和 MyISAM 的区别是什么？如何选择？](interview_questions/README.md#mysql-的存储引擎-innodb-和-myisam-的区别是什么如何选择)  
[什么是事务？请详细解释 MySQL 事务的 ACID 特性。](interview_questions/README.md#什么是事务请详细解释-mysql-事务的-acid-特性)  
[什么是脏读、不可重复读和幻读？MySQL 是如何通过事务隔离级别解决这些问题的？](interview_questions/README.md#什么是脏读不可重复读和幻读mysql-是如何通过事务隔离级别解决这些问题的)  
[详细解释 MySQL 的四种事务隔离级别（读未提交、读已提交、可重复读、串行化）。](interview_questions/README.md#详细解释-mysql-的四种事务隔离级别读未提交读已提交可重复读串行化)  
[MySQL InnoDB 的默认隔离级别是什么？它是如何解决幻读问题的？](interview_questions/README.md#mysql-innodb-的默认隔离级别是什么它是如何解决幻读问题的)  
[什么是 MVCC（多版本并发控制）？InnoDB 是如何实现 MVCC 的？](interview_questions/README.md#什么是-mvcc多版本并发控制innodb-是如何实现-mvcc-的)  
[说说你对 InnoDB 聚簇索引和非聚簇索引的理解。为什么主键查询效率高？](interview_questions/README.md#说说你对-innodb-聚簇索引和非聚簇索引的理解为什么主键查询效率高)  
[为什么推荐使用自增主键？使用 UUID 或者业务字段作为主键有什么潜在问题？](interview_questions/README.md#为什么推荐使用自增主键使用-uuid-或者业务字段作为主键有什么潜在问题)  
[什么是覆盖索引？它为什么能显著提升查询性能？](interview_questions/README.md#什么是覆盖索引它为什么能显著提升查询性能)  
[索引的最左前缀原则是什么？请举例说明。](interview_questions/README.md#索引的最左前缀原则是什么请举例说明)  
[在哪些情况下，即使建立了索引，MySQL 也不会使用它？](interview_questions/README.md#在哪些情况下即使建立了索引mysql-也不会使用它)  
[如何进行 SQL 查询的性能优化？你通常会从哪些方面入手？](interview_questions/README.md#如何进行-sql-查询的性能优化你通常会从哪些方面入手)  
[什么是数据库的慢查询？如何定位和优化慢查询？](interview_questions/README.md#什么是数据库的慢查询如何定位和优化慢查询)  
[什么是间隙锁（Gap Lock）？它解决了什么问题？](interview_questions/README.md#什么是间隙锁gap-lock它解决了什么问题)  
[数据库连接池的作用是什么？在 C++ 程序中为什么要使用连接池？](interview_questions/README.md#数据库连接池的作用是什么在-c++-程序中为什么要使用连接池)  
[什么是数据库的死锁？MySQL 中如何检测和避免死锁？](interview_questions/README.md#什么是数据库的死锁mysql-中如何检测和避免死锁)  
[简述一下 MySQL 的 Binlog 和 Redo Log 的作用和区别。](interview_questions/README.md#简述一下-mysql-的-binlog-和-redo-log-的作用和区别)  
[如何进行 MySQL 的读写分离和分库分表？它们分别解决了什么问题？](interview_questions/README.md#如何进行-mysql-的读写分离和分库分表它们分别解决了什么问题)  
[MySQL 索引为什么使用 B+树而不是 B 树或哈希表？](interview_questions/README.md#mysql-索引为什么使用-b+树而不是-b-树或哈希表)  
[请详细描述 B+树的结构特点，InnoDB 中的 B+树索引有哪些优化？](interview_questions/README.md#请详细描述-b+树的结构特点innodb-中的-b+树索引有哪些优化)  
