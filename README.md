# C++ 零基础入门到面试通关：2025 一站式学习指南
🌟 本仓库旨在为学习 C++ 的程序员们提供学习资源导航

💡 涵盖从基础知识到实战项目的资料与示例，帮助你快速入门并逐步进阶！

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
- [推荐资源](#推荐资源)
- [常用工具](#常用工具)
- [应用方向](#应用方向)
- [实战项目](#实战项目)
- [面试题](#面试题)

## 学习路线

<details open>
  <summary>点击收起 / 展开 C++ 学习路线图</strong></summary>
  <br>
  
  <img src="https://raw.githubusercontent.com/0voice/awesome-modern-cpp-2025/main/roadmap/cpp-roadmap.svg" 
       width="100%" 
       style="max-height: 900px;">
       
</details>

### 阶段0（0.5-1天）
- **核心目标**：完成环境搭建，能编译运行第一个 C++ 程序，上手基础工具
- **环境搭建**：
    - Windows：MinGW-w64 / MSVC + VS Code
    - Mac：Xcode Command Line Tools
    - Linux：GCC/Clang

### 阶段 1：入门基础（2-3 周）
- **核心目标**：理解 C++ 基本语法规则与底层逻辑，实现“输入→处理→输出”规范逻辑，规避入门常见坑
- **关键知识点**：
  - 核心语法：变量/数据类型、运算符、循环/分支（if-else、for、while）、函数（定义/调用/参数传递）、数组/字符串
  - 底层基础：编译链接流程（预处理→编译→汇编→链接）、头文件保护宏（#ifndef）、指针入门、引用（&）入门（与指针简单对比）
  - 关键关键字：const/volatile 基础用法、static 基础（局部静态变量）
  - 常见坑：变量未初始化、数组越界、指针空悬、编译报错和链接报错区分
- **工具学习**：CMake 基础（编写简单 CMakeLists.txt，实现多文件编译）
- **学习产出**：独立完成 2-3 个小 Demo（带引用/const 优化的控制台计算器、猜数字游戏、简易通讯录（数组版，支持增删改查+排序））
- **阶段检验**：能独立编写 100 行内规范程序；能解释“指针和引用的3个区别”“编译与链接报错的差异”；解决语法+链接层面基础问题

### 阶段 2：核心特性（3-4 周）
- **核心目标**：掌握 C++ 面向对象核心，能设计规范类与对象，规避 OOP 常见陷阱（拆分复杂知识点，分步骤消化）
- **关键知识点**（分模块学习）：
  - 模块 1：类与对象基础（1 周）—— 封装、访问控制（public/private/protected）、构造函数/析构函数
  - 模块 2：拷贝与重载（1 周）—— 拷贝构造函数、赋值运算符重载（深拷贝和浅拷贝）、运算符重载
  - 模块 3：继承与多态（1 周）—— 继承语法、虚函数（vtable/vptr 底层原理）、多态实现逻辑
  - 模块 4：补充特性（1 周）—— static 关键字（静态成员/静态函数）、友元函数、模板基础（函数模板/类模板）
  - 常见坑：浅拷贝导致内存泄漏、析构函数未设为虚函数的问题、子类访问父类私有成员的误区
- **工具学习**：Git 基础（提交、分支、合并，管理项目代码）
- **学习产出**：独立完成 1-2 个小型项目（带深拷贝逻辑的学生信息管理系统、简易图书管理系统）
- **阶段检验**：能手写带深拷贝的类、虚函数继承示例；能使用面向对象思想拆解问题，编写结构化程序

### 阶段 3：进阶基础（2-3 周）
- **核心目标**：熟练使用 STL 与现代 C++ 特性，具备基础问题解决能力与工程化编码思维（增加 STL 实操时间）
- **关键知识点**（分模块学习）：
  - 模块 1：STL 容器与底层（1 周）—— STL 容器（vector、list、map、set）底层原理与适用场景、vector 动态扩容机制
  - 模块 2：STL 算法与迭代器（1 周）—— STL 算法（排序、查找）、迭代器（使用+失效场景）、Lambda 表达式（配合 STL 算法使用）
  - 模块 3：实用技能与现代 C++（1 周）—— 文件 IO（读写文本/二进制文件）、异常处理（try-catch）、C++11+ 基础特性（auto/范围 for/nullptr）
  - 常见坑：STL 迭代器失效、vector 扩容导致的性能问题、异常未捕获导致程序崩溃
- **工具学习**：Clang-Format（统一代码风格）
- **学习产出**：独立完成 1 个实用小工具（高性能词频统计工具、简易日志系统）
- **阶段检验**：能借助 STL 高效实现功能；能解释“vector和list 的区别”“Lambda 捕获列表的作用”；处理程序异常与数据持久化

### 阶段 4：实战提升（4-6 周）
- **核心目标**：深入理解 C++ 主流应用场景，具备小型项目完整开发能力（延长实战周期，保证项目质量）
- **关键知识点**（分模块+项目驱动）：
  - 模块 1：内存管理（1 周）—— 智能指针（unique_ptr/shared_ptr）、内存池基础、内存泄漏检测（Valgrind 工具）
  - 模块 2：多线程编程（1-2 周）—— 线程创建、互斥锁/条件变量、多线程死锁规避、线程池实现
  - 模块 3：网络编程（1-2 周）—— TCP/UDP 基础、Socket 编程、可选进阶（IO 多路复用 select/poll/epoll）
  - 模块 4：设计模式与工程化（1 周）—— 常用设计模式（单例/工厂/策略）、接口设计原则（单一职责/依赖倒置）、GDB 调试基础
  - 常见坑：智能指针循环引用、多线程死锁、网络粘包、内存池碎片
- **工具学习**：GProf 基础（性能分析）、Valgrind（内存泄漏检测）
- **学习产出**（可选方向，贴合岗位需求，选 1 个深入做）：
  - 嵌入式/系统方向：简易嵌入式日志工具（日志级别、内存优化、硬件适配）
  - 后端/服务器方向：简易 HTTP 服务器（静态文件访问+请求解析+多线程处理）
  - 游戏开发方向：简易贪吃蛇/打砖块游戏（ECS 架构、碰撞检测、计时器）
  - 通用方向：高性能线程池（任务队列+线程管理+异常处理）
- **阶段检验**：能独立设计项目结构；能解决多线程/内存管理/网络通信等实际问题；能使用调试/性能工具定位优化问题

### 阶段 5：面试冲刺（2-3 周）
- **核心目标**：掌握高频面试题，清晰表达技术思路，提升面试竞争力（延长复盘时间，避免遗漏）
- **关键动作**：
  - 知识点复盘（1 周）：核心语法、OOP 特性（封装/继承/多态）、STL 底层、内存管理、多线程、C++11+ 特性
  - 刷题训练（1 周）：高频概念题（指针和引用/深拷贝和浅拷贝/虚函数原理）、编程题（数组/字符串/链表/简单算法）
  - 项目复盘（1 周）：总结项目亮点（性能优化/线程安全设计）、问题解决方案（内存泄漏排查/死锁修复）
- **学习产出**：个人面试笔记（知识点+错题+项目复盘）、编程题错题集
- **阶段检验**：应对基础面试无压力；编程题能在规定时间内完成并解释思路；能清晰阐述项目设计与问题解决方案

### 打卡表
| 周数 | 阶段 | 推荐资源 | 阶段任务 |
|------|----------|----------------|--------------|
| 第0周 | 阶段0 | [清晰易懂的C+＋开发环境搭建教程](https://blog.51cto.com/u_16349720/14112761)| 完成开发环境搭建 |
| 第1-3周  | 阶段 1 | [黑马程序员](https://www.bilibili.com/video/BV1et411b73Z/?spm_id_from=333.337.search-card.all.click&vd_source=b1133efda5c53025ed35233121e57402)或 [翁恺《C++ 程序设计》](https://www.bilibili.com/video/BV1dr4y1n7vA/?spm_id_from=333.337.search-card.all.click&vd_source=b1133efda5c53025ed35233121e57402) | 完成3个demo放GitHub |
| 第4-7周  | 阶段 2 | 《C++ Primer》 | 学生/图书管理系统完整版 |
| 第7-9周  | 阶段 3 | 《Effective Modern C++》 | 词频统计工具 |
| 第10-15周 | 阶段 4 | [实战项目](#实战项目)中选一个大项目 | 完成项目传GitHub |
| 第16-18周 | 阶段 5 | 牛客/LeetCode C++ 专区 | 高频笔面题 + 项目复盘 |

## 核心知识点
### 基础语法篇
  - **变量与数据类型**：整型/浮点型/字符型/布尔型、const、typedef
  - **运算符与表达式**：算术/关系/逻辑运算符、复合赋值、自增自减（前置和后置）
  - **控制流**：if-else、switch、for/while/do-while、break/continue、cin/cout+iomanip、namespace
  - **函数**：定义/声明、值/引用/指针传参、返回值、函数重载、默认参数、lambda简介
  - **数组与字符串**：一维数组、C风格字符串和std::string（常用操作）
  - **指针入门**：定义/解引用/取地址、指针与数组/函数、野指针/nullptr、指针和引用（核心区别）

### 面向对象篇
  - **类与对象**：class/struct区别、成员变量/函数、对象创建（栈/堆）、访问控制（public/private/protected）
  - **构造与析构**：默认/带参/拷贝/移动构造与移动赋值、析构函数（虚析构必要性）、初始化列表、RAII原则、智能指针初步认识、Rule of Five
  - **继承与多态**：继承语法、基类/派生类、虚函数、纯虚函数+抽象类、vtable简介
  - **运算符重载**：赋值/算术/关系/<<运算符、深拷贝和浅拷贝
  - **模板基础**：函数模板、类模板、STL容器底层关联

### 进阶基础篇
  - **STL**：容器（vector/list/map/unordered_map/set）、迭代器（失效场景）、常用算法（sort/find/count/for_each）、lambda配合STL
  - **文件IO**：文本/二进制文件读写、fstream、文件指针操作、数据持久化
  - **异常处理**：try-catch/throw、自定义异常类、noexcept
  - **内存管理**：new/delete、malloc/free区别、智能指针（unique_ptr/shared_ptr/weak_ptr）、内存泄漏避免
  - **现代特性**：auto、decltype、lambda

### 实战提升篇
  - **多线程**：std::thread、mutex/lock_guard、condition_variable、atomic、线程池原理、死锁避免
  - **网络编程**：TCP/UDP基础、Socket编程流程（服务端/客户端）、TCP粘包问题、IO多路复用简介
  - **设计模式**：单例（线程安全版）、简单工厂/工厂方法、策略模式（适用场景+核心代码）



## 推荐资源
### 视频推荐
| 视频名称 | 链接 |
|----------|------|
| 浙江大学翁恺教你C语言程序设计！C语言基础入门！ | [Bilibili](https://www.bilibili.com/video/BV1dr4y1n7vA/?spm_id_from=333.337.search-card.all.click&vd_source=b1133efda5c53025ed35233121e57402) |
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
| 书籍名称 | 作者 | 简介 |
|----------|------|------|
| 《C++ Primer》（第 5/6 版） | Stanley B. Lippman 等 | 全面入门圣经，从语法到 STL，强调现代实践，适合零基础自学者。 |
| 《Accelerated C++》 | Andrew Koenig & Barbara E. Moo | 项目驱动快速上手，聚焦高效代码，适合有基础初学者。 |
| 《Programming: Principles and Practice Using C++》（第 2 版） | Bjarne Stroustrup | 原则+实践教材，讲解抽象与算法，适合理解语言哲学者。 |
| 《Effective C++》（第 3 版） | Scott Meyers | 55 条最佳实践，避免陷阱，提升中级代码质量。 |
| 《The C++ Programming Language》（第 4 版） | Bjarne Stroustrup | 官方参考手册，详尽标准与高级特性，资深开发者必备。 |
| 《Modern C++ Design》 | Andrei Alexandrescu | 模板元编程与泛型模式，深度设计技巧，针对经验程序员。 |

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
- [MSVC](https://learn.microsoft.com/en-us/cpp/windows/latest-supported-vc-redist?view=msvc-170)：Windows 原生

### 2. 集成开发环境
- [Visual Studio](https://visualstudio.microsoft.com/)：全功能 IDE
- [CLion](https://www.jetbrains.com/clion/)：智能 IDE
- [VSCode](https://code.visualstudio.com/)：轻量编辑器
- [Code::Blocks](http://www.codeblocks.org/)：免费开源
- [Dev-C++](https://www.dev-cpp.com/)：轻量简单

### 3. 构建系统
- [CMake](https://cmake.org/)：跨平台构建
- [Make](https://www.gnu.org/software/make/)：经典 Unix 工具
- [Ninja](https://ninja-build.org/)：快速构建

### 4. 调试器
- [GDB](https://sourceware.org/gdb/)：开源调试
- [LLDB](https://lldb.llvm.org/)：LLVM 调试

### 5. 版本控制
- [Git](https://git-scm.com/)：分布式控制

### 6. 包管理器
- [vcpkg](https://vcpkg.io/)：Microsoft 库管理
- [Conan](https://conan.io/)：开源包管理

### 7. 代码分析与测试
- [Clang-Tidy](https://clang.llvm.org/extra/clang-tidy/)：静态分析
- [Cppcheck](https://cppcheck.sourceforge.net/)：检测 bug
- [Google Test](https://github.com/google/googletest)：单元测试
- [Catch2](https://github.com/catchorg/Catch2)：轻量测试

### 8. 开发辅助
- [Clang-Format](https://clang.llvm.org/docs/ClangFormat.html)：代码格式化
- [Valgrind](https://valgrind.org/)：内存检测
- [Perf](https://perfwiki.github.io/main/)：性能分析
- [Docker](https://www.docker.com/)：容器部署

## 应用方向

| 应用方向 | 核心场景 | 推荐框架/库 |
|----------|----------|-------------|
| **桌面应用开发** | 办公软件、工业控制界面、桌面工具、设计类软件 |  [Qt](https://www.qt.io/)：跨平台全栈框架，集成 GUI、网络、数据库、多媒体。<br> [MFC](https://learn.microsoft.com/en-us/cpp/mfc/mfc-desktop-applications)：Windows 原生框架，适合 legacy 项目。<br> [wxWidgets](https://www.wxwidgets.org/)：跨平台轻量框架，原生风格。 |
| **嵌入式开发** | 车载中控、智能家居面板、医疗设备、工业控制器、路由器固件 |  [Qt Embedded](https://www.qt.io/qt-for-embedded-linux)：嵌入式 GUI，适配 ARM 等。<br> [FreeRTOS](https://www.freertos.org/)：轻量 RTOS，资源受限设备。<br> [Yocto/Buildroot](https://www.yoctoproject.org/)：Linux 嵌入式系统。 |
| **后端/服务器开发** | 分布式系统、API 网关、数据库内核、高并发服务（游戏服务器、支付系统） |  [Boost.Asio](https://www.boost.org/doc/libs/1_85_0/doc/html/boost_asio.html)：异步网络库，TCP/UDP/HTTP。<br> [Muduo](https://github.com/chenshuo/muduo)：Reactor 模式高并发服务器。<br> [Brpc](https://github.com/apache/incubator-brpc)：RPC 框架，多协议支持。<br> [Drogon](https://drogon.org/)：HTTP 框架，异步 IO + ORM。 |
| **游戏开发** | 3A 游戏客户端、游戏引擎、游戏服务器、独立游戏 |  [Unreal Engine](https://www.unrealengine.com/)：开源引擎，蓝图系统 + C++。<br> [Cocos2d-x](https://www.cocos.com/en/cocos2d-x)：跨平台 2D 引擎。<br> [Unity](https://unity.com/)：C# 上层 + C++ 优化。 |
| **音视频/流媒体开发** | 播放器、直播推流/拉流、视频编辑、音视频转码、监控安防 |  [FFmpeg](https://ffmpeg.org/)：音视频处理库，解码/编码/传输。<br> [GStreamer](https://gstreamer.freedesktop.org/)：流媒体管道框架。<br> [SDL](https://www.libsdl.org/)：多媒体库，音频/渲染。<br> [OpenCV](https://opencv.org/)：视频分析（如人脸识别）。 |
| **人工智能/机器学习** | 深度学习框架底层、模型推理优化、高性能计算（HPC） |  [TensorFlow C++ API](https://www.tensorflow.org/api_docs/cc)：模型部署接口。<br> [LibTorch (PyTorch C++)](https://pytorch.org/cppdocs/)：动态图推理库。<br> [OpenCV](https://opencv.org/)：图像预处理/特征提取。<br> [Eigen](http://eigen.tuxfamily.org/)：矩阵运算库。<br> [ONNX Runtime](https://onnxruntime.ai/)：跨框架推理引擎。 |
| **系统编程/内核开发** | 操作系统内核、驱动程序、数据库内核、文件系统 |  [Linux Kernel](https://www.kernel.org/)：内核 API 开发。<br> [WDF/KMDF](https://learn.microsoft.com/en-us/windows-hardware/drivers/wdf/)：Windows 驱动框架。<br> [SQLite](https://www.sqlite.org/)：嵌入式数据库内核。 |
| **金融科技/高频交易** | 高频交易系统、量化交易引擎、金融风控系统（要求低延迟、高可靠） |  [QuickFIX](http://www.quickfixengine.org/)：FIX 协议库。<br> [Boost.Asio](https://www.boost.org/)：低延迟网络。 |

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

### 嵌入式开发
| 项目名称                                                         | 难度       | 核心技能                                   |
|------------------------------------------------------------------|------------|--------------------------------------------|
| [bblanchon/ArduinoJson](https://github.com/bblanchon/ArduinoJson) | ★☆☆☆☆   | 静态内存 JSON                              |
| [lvgl/lvgl](https://github.com/lvgl/lvgl)                      | ★★☆☆☆     | 嵌入式 GUI 最强库                          |
| [zephyrproject-rtos/zephyr](https://github.com/zephyrproject-rtos/zephyr) | ★★★★☆ | 现代 RTOS、BLE、驱动                       |
| [platformio/platformio-core](https://github.com/platformio/platformio-core) | ★★★☆☆ | 嵌入式构建系统                             |
| [RT-Thread/rt-thread](https://github.com/RT-Thread/rt-thread)   | ★★★★☆     | 国产最强 RTOS、组件化                      |
| [espressif/esp-idf](https://github.com/espressif/esp-idf)      | ★★★★☆     | ESP32 官方 SDK、低功耗                     |

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

### 游戏开发
| 项目名称                                                         | 难度       | 核心技能                                   |
|------------------------------------------------------------------|------------|--------------------------------------------|
| [SFML/SFML](https://github.com/SFML/SFML)                       | ★☆☆☆☆     | 轻量 2D 游戏库                             |
| [skypjack/entt](https://github.com/skypjack/entt)               | ★★☆☆☆     | ECS 架构                                   |
| [RobLoach/raylib-cpp](https://github.com/RobLoach/raylib-cpp)   | ★★☆☆☆     | 极简游戏开发库                             |
| [TheCherno/Hazel](https://github.com/TheCherno/Hazel)           | ★★★★☆     | 从零写游戏引擎（教学级）                   |
| [godotengine/godot](https://github.com/godotengine/godot)      | ★★★★☆     | 完整开源引擎                               |
| [cocos2d/cocos-engine](https://github.com/cocos2d/cocos-engine)| ★★★★☆     | 国内手游最强引擎                           |

### 音视频/流媒体开发
| 项目名称                                                         | 难度       | 核心技能                                   |
|------------------------------------------------------------------|------------|--------------------------------------------|
| [obsproject/obs-studio](https://github.com/obsproject/obs-studio) | ★★★★☆   | 实时推流、插件系统                         |
| [FFmpeg/FFmpeg](https://github.com/FFmpeg/FFmpeg)               | ★★★★☆     | 音视频编解码全家桶                         |
| [bluenviron/mediamtx](https://github.com/bluenviron/mediamtx)   | ★★★☆☆     | 零依赖流媒体服务器                         |
| [Haivision/srt](https://github.com/Haivision/srt)               | ★★★★☆     | 低延迟传输协议                             |
| [isl-org/Open3D](https://github.com/isl-org/Open3D)             | ★★★★☆     | 3D 数据处理、点云                          |

### 人工智能/机器学习
| 项目名称                                                         | 难度       | 核心技能                                   |
|------------------------------------------------------------------|------------|--------------------------------------------|
| [nlohmann/json](https://github.com/nlohmann/json)               | ★☆☆☆☆     | 数据预处理必备                             |
| [opencv/opencv](https://github.com/opencv/opencv)               | ★★★☆☆     | 图像预处理、DNN 模块                       |
| [Tencent/ncnn](https://github.com/Tencent/ncnn)                 | ★★★☆☆     | 手机端推理框架                             |
| [alibaba/MNN](https://github.com/alibaba/MNN)                   | ★★★★☆     | 阿里移动端推理引擎                         |
| [microsoft/onnxruntime](https://github.com/microsoft/onnxruntime) | ★★★☆☆   | 跨平台模型推理                             |
| [pytorch/pytorch (LibTorch)](https://github.com/pytorch/pytorch) | ★★★★☆   | C++ 动态图、自定义算子                     |

### 系统编程/内核开发
| 项目名称                                                         | 难度       | 核心技能                                   |
|------------------------------------------------------------------|------------|--------------------------------------------|
| [gabime/spdlog](https://github.com/gabime/spdlog)               | ★☆☆☆☆     | 高性能日志                                 |
| [sqlite/sqlite](https://github.com/sqlite/sqlite)               | ★★★★☆     | 数据库内核、B-tree                         |
| [facebook/folly](https://github.com/facebook/folly)             | ★★★★★     | Facebook 底层库                            |
| [microsoft/Detours](https://github.com/microsoft/Detours)       | ★★★★☆     | Windows Hook                               |
| [ClickHouse/ClickHouse](https://github.com/ClickHouse/ClickHouse) | ★★★★★   | 列式数据库、向量化执行                     |
| [torvalds/linux](https://github.com/torvalds/linux)             | ★★★★★     | 内核开发                                   |

## 面试题
