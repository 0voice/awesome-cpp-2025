# Awesome Modern C++ 2025
🌟 A one-stop navigation repository for anyone learning modern C++.  
💡 From absolute beginner to building real projects and passing technical interviews.  
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

[中文版 README](https://github.com/0voice/awesome-modern-cpp-2025/blob/main/README.md)

**Target Audience**
- Complete programming beginners
- CS/EE students
- Developers switching from other languages (Python/Java/Go → C++)
- Junior C++ engineers who want to solidify foundations and prepare for interviews

**Why Learn C++ in 2025?**
- Unmatched performance & control over system resources
- Dominant in high-performance domains: game engines, trading systems, embedded, browsers, databases, AI inference
- Modern C++ (C++17/20/23/26) is safe, expressive, and productive
- Strong transferable skills → Rust, systems programming, performance engineering
- Consistently high-paying and in-demand (gaming, finance, autonomous vehicles, robotics, HPC)

Relevant discussions:
- [Why you should learn C++](https://www.youtube.com/shorts/1Zku-mXDY9g)
- [C++ Applications & Why Learn It](https://www.youtube.com/watch?v=brqRL_t0RmM)
- [Should You Learn C++ in the AI Era?](https://www.youtube.com/watch?v=1POqwCxIhjo)
- [The Truth About C++ (Is It Still Worth Your Time?)](https://www.youtube.com/watch?v=q1ZmFc-sqNc)
- [Best C/C++ Learning Roadmap 2025](https://www.youtube.com/watch?v=gO4Jp78nM0g)

## Table of Contents
- [Learning Roadmap](#learning-roadmap)
- [Core Knowledge](#core-knowledge)
- [Advanced Modern C++ Features](advanced-modern-c-features-c20--c23)
- [Recommended Resources](#recommended-resources)
- [Tools](#tools)
- [Application Fields](#application-fields)
- [Real-World Projects](#real-world-projects)
- [Interview Preparation](#interview-preparation)

## Learning Roadmap

  <img src="https://raw.githubusercontent.com/0voice/awesome-modern-cpp-2025/main/roadmap/cpp-roadmap.en.svg">

### Stage 0: Preparation (0.5–1 day)
**Goal**: Set up environment, compile and run your first C++ program  
- Windows (MinGW + VS Code)
- macOS (Xcode Command Line Tools)
- Linux (GCC/Clang)

If you haven't completed this step or encounter any difficulties, please refer to the [C++ Development Environment Setup Guide](https://github.com/0voice/awesome-modern-cpp-2025/blob/main/environment_setup/README.md).

### Stage 1: Fundamentals (2–3 weeks)
**Goal**: Master basic syntax, understand compilation process, avoid common pitfalls  
**Key Topics**
- Variables, data types, operators, control flow, functions, arrays, strings
- Pointers & references basics, const/volatile/static basics
- Compilation & linking, header guards
- CMake basics (multi-file projects)

**Project**: [Calculator](https://github.com/arash28134/simple-calculator), [Guess-the-number](https://github.com/mrnazu/guess-the-number)

### Stage 2: Core OOP (3–4 weeks)
**Goal**: Design clean classes and understand polymorphism  
**Modules**
1. Classes & objects, constructors/destructors
2. Copy/move semantics, deep vs shallow copy
3. Inheritance, virtual functions, vtable
4. static members, friend, basic templates

**Project**: [Student management system](https://github.com/abhiishekpanchal/STUDENT-MANAGEMENT-SYSTEM---OOPS-CONCEPTS) / [Library management system](https://github.com/MAbubakkar/Library-Management-System) 

### Stage 3: Modern C++ & STL (2–3 weeks)
**Goal**: Write idiomatic, efficient code  
**Topics**
- All STL containers & algorithms
- Iterators & invalidation
- Lambda, auto, range-for, smart pointers
- Exception handling, file I/O

**Project**: [High-performance word frequency tool](https://github.com/NimraGJay/STL), [Simple logger](https://github.com/Ahmed-Ibrahim-30/Logging-System)

### Stage 4: Systems Programming (4–6 weeks)
**Goal**: Build real production-grade components  
**Topics**
- RAII & smart pointers in depth
- Multithreading (std::thread, mutex, condition_variable, atomic)
- Thread pool implementation
- Socket programming (TCP/UDP), simple HTTP server
- Design patterns, debugging & profiling

**Major Project (choose one)**
- [High-Performance Thread Pool](https://github.com/progschj/ThreadPool)
- [Lightweight HTTP Server with Thread Pool](https://github.com/yhirose/cpp-httplib)
- [High-Performance Chat Server](https://github.com/chronoxor/CppServer)

### Stage 5: Interview Sprint (2–3 weeks)
**Goal**: Pass technical interviews confidently  
- Full knowledge review
- 150+ high-frequency questions
- Project storytelling & mock interviews

### Timeline Table
| Week | Stage | Recommended Resources | Tasks |
|------|-------|-----------------------|-------|
| 0    | Stage 0 | Environment setup tutorials | Finish setup |
| 1–3  | Stage 1 | The Cherno / freeCodeCamp C++ | 3 small demos → GitHub |
| 4–7  | Stage 2 | C++ Primer | Student/Library system |
| 7–9  | Stage 3 | Effective Modern C++ | Word frequency tool |
| 10–15| Stage 4 | Major Project (choose one)  | One big project → GitHub |
| 16–18| Stage 5 | LeetCode + mock interviews | 150 questions + resume projects |

## Core Knowledge

### [Basic Syntax](https://github.com/0voice/awesome-modern-cpp-2025/blob/main/core_knowledge/%E5%9F%BA%E7%A1%80%E8%AF%AD%E6%B3%95%E7%AF%87.md)
- **Variables & Data Types**: Integral/floating-point/char/bool, `const`, `typedef`/`using`
- **Operators & Expressions**: Arithmetic/relational/logical operators, compound assignment, increment/decrement (prefix vs postfix)
- **Control Flow**: `if-else`, `switch`, `for`/`while`/`do-while`, `break`/`continue`, `cin`/`cout` + `iomanip`, `namespace`
- **Functions**: Definition vs declaration, pass-by-value/reference/pointer, return values, function overloading, default arguments, lambda introduction
- **Arrays & Strings**: One-dimensional arrays, C-style strings vs `std::string` (common operations)
- **Pointers Basics**: Definition/dereference/address-of, pointer arithmetic, pointers to arrays/functions, dangling/wild pointers, `nullptr`, core differences between pointers and references

### [Object-Oriented Programming](https://github.com/0voice/awesome-modern-cpp-2025/blob/main/core_knowledge/%E9%9D%A2%E5%90%91%E5%AF%B9%E8%B1%A1%E7%AF%87.md)
- **Classes & Objects**: `class` vs `struct`, member variables/functions, object creation (stack vs heap), access specifiers (`public`/`private`/`protected`)
- **Constructors & Destructors**: Default/parameterized/copy/move constructors, move assignment, virtual destructor necessity, initialization lists, RAII principle, introduction to smart pointers, Rule of Five
- **Inheritance & Polymorphism**: Inheritance syntax, base/derived classes, virtual functions, pure virtual functions + abstract classes, brief introduction to vtable/vptr
- **Operator Overloading**: Assignment/arithmetic/relational/stream (`<<`/`>>`) operators, deep copy vs shallow copy
- **Templates Basics**: Function templates, class templates, connection to STL containers

### [Intermediate & Modern C++](https://github.com/0voice/awesome-modern-cpp-2025/blob/main/core_knowledge/%E8%BF%9B%E9%98%B6%E5%9F%BA%E7%A1%80%E7%AF%87.md)
- **STL**: Containers (`vector`, `list`, `map`, `unordered_map`, `set`), iterators & invalidation scenarios, common algorithms (`sort`, `find`, `count`, `for_each`, etc.), lambda with STL
- **File I/O**: Text/binary file read/write, `fstream`, file stream states, data persistence
- **Exception Handling**: `try`/`catch`/`throw`, custom exception classes, `noexcept`
- **Memory Management**: `new`/`delete` vs `malloc`/`free`, smart pointers (`unique_ptr`, `shared_ptr`, `weak_ptr`), avoiding memory leaks and circular references
- **Modern C++ Features**: `auto`, `decltype`, lambda expressions, `nullptr`, move semantics, `std::move`, perfect forwarding

### [Practical & Systems Programming](https://github.com/0voice/awesome-modern-cpp-2025/blob/main/core_knowledge/%E5%AE%9E%E6%88%98%E6%8F%90%E5%8D%87%E7%AF%87.md)
- **Multithreading**: `std::thread`, `mutex`/`lock_guard`/`unique_lock`, `condition_variable`, `std::atomic`, thread pool principle & implementation, deadlock prevention
- **Network Programming**: TCP/UDP fundamentals, Socket programming workflow (server/client), TCP sticky packet problem, introduction to I/O multiplexing (`select`/`poll`/`epoll`)
- **Design Patterns**: Thread-safe Singleton, Simple Factory/Factory Method, Strategy pattern (use cases + core code)

## Advanced Modern C++ Features (C++20 & C++23)

### 1. Concepts and requires (C++20)
**Purpose**: Add clear, readable constraints to template parameters, replacing complex SFINAE.  
**When to use**: Mandatory for all generic libraries and custom template functions/classes.

```cpp
template<typename T>
concept Integral = std::is_integral_v<T>;

template<Integral T>
T add(T a, T b) { return a + b; }

// Custom complex concept
template<typename T>
concept Hashable = requires(T x) {
    { std::hash<T>{}(x) } -> std::convertible_to<std::size_t>;
};

template<Hashable T>
class Cache { /* ... */ };
```

**Common pitfall**: Overly strict concepts may break valid code.  
**Recommendation**: Start with loose constraints and tighten gradually.

---

### 2. Ranges Library (C++20)
**Purpose**: Functional-style sequence processing with lazy evaluation and pipe syntax, making code more concise and efficient.  
**When to use**: Anytime filter/map/take/drop/sort operations are needed.  
**Advantages**: No intermediate containers, cache-friendly, 50% less code.

```cpp
std::vector<int> v = {1, 2, 3, 4, 5, 6, 7, 8, 9, 10};

auto result = v
    | std::views::filter([](int x) { return x % 2 == 0; })   // Even numbers
    | std::views::transform([](int x) { return x * x; })     // Square
    | std::views::take(4);                                   // First 4 elements

for (int x : result) std::cout << x << ' ';  // Output: 4 16 36 64
```

---

### 3. std::span (C++20)
**Purpose**: Lightweight, non-owning view of fixed-size arrays/containers for safe continuous data passing.  
**When to use**: Replace raw pointers/size pairs with span for all "continuous memory" function parameters.

```cpp
void process(std::span<const int> data) {
    for (int x : data) std::cout << x << ' ';
}

std::vector<int> vec{1, 2, 3};
int arr[] = {4, 5, 6};
process(vec);
process(arr);
```

**Common mistake**: Span stores a view - dangling occurs if the original data is destructed.  
**Note**: Ensure the original data outlives the span.

---

### 4. Coroutines (C++20)
**Purpose**: Write asynchronous/generator code more naturally without callbacks or threads.

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
    bool next() { /* Practical use requires a coroutine library */ return false; }
    int value() { return 0; }
};
```

---

### 5. deducing this (C++23)
**Purpose**: Allow member functions to treat `this` as a regular parameter, perfectly solving pain points in CRTP and recursive lambdas.

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

---

### 6. std::expected (C++23)
**Purpose**: Modern return type that carries either a value or an error message, lighter than exceptions and return-code pairs.  
**Use cases**: All operations that may fail but don't warrant exceptions (parsing, I/O, calculations, etc.).

```cpp
std::expected<int, std::string> safe_divide(int a, int b) {
    if (b == 0) return std::unexpected("division by zero");
    return a / b;
}

auto result = safe_divide(42, 7)
                .and_then([](int x) { return safe_divide(100, x); })
                .value_or(-1);
```

---

### 7. std::mdspan (C++23)
**Purpose**: Non-owning multi-dimensional array view, ideal for images, matrices, and scientific computing scenarios.

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

---

### 8. std::flat_map / std::flat_set (C++23)
**Purpose**: Ordered map/set based on contiguous containers, offering better cache locality and faster lookup speeds.  
**When to use**: Replace `std::map` with `std::flat_map` for configuration tables, dictionaries, and frequently accessed small datasets (< 100,000 entries).

```cpp
std::flat_map<std::string, int> m = {
    {"apple", 5}, {"banana", 3}, {"orange", 8}
};
// Automatically sorted, contiguous memory, ideal for hot data.
```

---

### 9. Multi-dimensional subscript operator[] (C++23)
**Purpose**: Natively support multi-dimensional array subscript operations with intuitive syntax.

```cpp
int arr[3][4][5]{};
arr[1, 2, 3] = 42;        // Equivalent to arr[1][2][3] = 42;
```

---

### 10. Lambda Enhancements (C++23)
**Purpose**: Support template parameters and attribute markers for stronger expressiveness.

```cpp
auto templated_lambda = []<typename T>(T a, T b) {
    return a + b;
};

auto attributed = [] [[nodiscard]] (int x) { return x * x; };
```

## Recommended Resources

### Video
| Title | Link |
|-------|------|
| C++ Programming Course - Beginner to Advanced (2024) | https://www.youtube.com/watch?v=8jLOx1hD3_o |
| Full C++ Crash Course for Beginners (2025 Edition) | https://www.youtube.com/watch?v=zKddJjNc0_s |
| C++ FULL COURSE For Beginners (7+ hours) | https://www.youtube.com/watch?v=GQp1zzTwrIg |
| The Cherno – C++ Series (150+ episodes, gold standard) | https://www.youtube.com/playlist?list=PLlrATfBNZ98dudnM48yfGUldqGD0S4FFb |
| cpp-weekly by Jason Turner (modern C++ best practices) | https://www.youtube.com/c/lefticus1 |
| CppCon talks (latest standards & real-world usage) | https://www.youtube.com/c/CppCon |

### Physical Book
| Book Title                                           | Author                          | Difficulty | Description                                                                 |
|------------------------------------------------------|---------------------------------|------------|-----------------------------------------------------------------------------|
| C++ Primer Plus (6th Edition)                        | Stephen Prata                   | ★★☆☆☆     | Beginner-friendly, easy-to-read language, life-related examples, gradual progression from syntax to OOP, exercises in every chapter. Perfect for pure newbies to steadily build a foundation. The only downside is that it does not cover C++11+ modern idioms. |
| C++ Primer (6th Edition)                             | Stanley B. Lippman et al.       | ★★★☆☆     | The comprehensive and systematic “C++ Bible”, covering syntax, STL, and C++11+ modern features with a strong emphasis on real-world practice. High knowledge density and in-depth explanations. Much more beginner-friendly than the 5th edition; ideal for solidifying your knowledge base or advancing to modern style after some foundation. |
| Accelerated C++                                      | Andrew Koenig & Barbara E. Moo  | ★★★☆☆     | Project-driven fast-track introduction, skips redundant content, focuses on efficient and idiomatic production code. Best for learners with slight prior programming experience who want to get to real projects quickly. |
| Programming: Principles and Practice Using C++ (2nd Edition) | Bjarne Stroustrup (creator of C++) | ★★★☆☆     | Balances principles and practice; goes beyond syntax to develop abstraction and algorithmic thinking. Perfect for those who want to understand the design philosophy of C++ and build solid underlying logic. |
| Effective C++ (3rd Edition)                          | Scott Meyers                    | ★★★★☆     | Distills 55 core best-practice guidelines that directly target code pitfalls. Essential reading for the transition from beginner to intermediate; dramatically improves code quality in a short time. |
| The C++ Programming Language (4th Edition)          | Bjarne Stroustrup (creator of C++) | ★★★★★     | The official authoritative reference manual, exhaustive coverage of the C++ standard and advanced features (including modern ones). Suitable for developers at all stages as a lookup resource. |
| Modern C++ Design                                    | Andrei Alexandrescu             | ★★★★★     | In-depth exploration of template metaprogramming and generic design patterns, focusing on high-level development techniques. Only for experienced C++ programmers—newbies beware. |

Difficulty guide (from a true zero-basis perspective):  
★☆☆☆☆ ~ ★★☆☆☆ : Can be read by absolute beginners  
★★★☆☆          : Requires patience + daily coding practice  
★★★★☆ ~ ★★★★★ : Mid-to-advanced level only  

### Free Electronic Book / PDF
| Book Title                                              | Author                          | Description                                                                                   |
|---------------------------------------------------------|---------------------------------|-----------------------------------------------------------------------------------------------|
| [A Complete Guide to Programming in C++](https://www.idpoisson.fr/volkov/C%2B%2B.pdf) | Ulla Kirchartz & Peter Müller   | From zero to advanced. Covers syntax, OOP, and STL with exercises and solutions. |
| [Beginning C++ Programming](https://notalentgeek.github.io/note/note/project/project-independent/pi-brp-beginning-c-programming/document/20170807-1504-cet-1-book-and-source-1.pdf) | Ivor Horton                     | Step-by-step beginner guide focusing on syntax, functions, and classes. |
| [C++ Tutorial](https://cds.iisc.ac.in/wp-content/uploads/DS286.AUG2016.Lab2_.cpp_tutorial.pdf) | IISc Bangalore                  | Concise university-style tutorial focusing on core syntax, pointers, and file I/O. |
| [CS 200: Concepts of Programming using C++ (Spring 2025)](https://rachel.likespizza.com/course-archives/202501_CS200.pdf) | Rachel Wil Singh                | 2025 course notes covering fundamentals, data structures, and debugging. |
| [C++ Annotations (Version 11.0)](https://www.icce.rug.nl/documents/cplusplus/11.0/C++Annotations-11.0.pdf) | Frank B. Brokken                | Comprehensive, freely available reference. In-depth coverage of OOP, multithreading, and modern features. |

### Websites

| Website Name                  | Description                                                                                           |
|-------------------------------|-------------------------------------------------------------------------------------------------------|
| [LearnCpp.com](https://www.learncpp.com/) | The best free step-by-step C++ tutorial on the internet. Emphasizes best practices, modern C++, and avoids common pitfalls. Perfect for beginners to intermediate learners. |
| [cppreference.com](https://en.cppreference.com/w/) | The definitive, most accurate C++ standard library and language reference. Used daily by professional developers worldwide. |
| [CPlusPlus.com](https://cplusplus.com/) | Classic reference site with tutorials, full standard library documentation, examples, and active forums. |
| [GeeksforGeeks – C++](https://www.geeksforgeeks.org/c-plus-plus/) | Huge collection of C++ articles, data structures, algorithms, and interview questions with clean code examples. Extremely popular among job seekers. |
| [Codecademy – Learn C++](https://www.codecademy.com/learn/learn-c-plus-plus) | Interactive browser-based course. Great for hands-on practice from basics to intermediate topics. |
| [Coursera – C++ Courses](https://www.coursera.org/courses?query=c%2B%2B) | University-level C++ specializations (e.g., University of London, UC Santa Cruz, Stanford). Includes videos, quizzes, and certificates. |
| [LeetCode (C++ track)](https://leetcode.com/problemset/all/?search=C%2B%2B) | The #1 platform for coding interview preparation. Thousands of problems with C++ solutions and discussion. |
| [HackerRank – C++](https://www.hackerrank.com/domains/tutorials/10-days-of-cpp) | Beginner-friendly challenges and 30-day C++ tutorials. |
| [Exercism – C++ Track](https://exercism.org/tracks/cpp) | Free mentoring platform with high-quality exercises and code reviews from real developers. |
| [Awesome C++](https://github.com/fffaraz/awesome-cpp) | Curated list of awesome C++ frameworks, libraries, resources, and tools. A must-bookmark for exploring the ecosystem. |
| [Compiler Explorer (Godbolt)](https://godbolt.org/) | Instantly see how your C++ code compiles to assembly across different compilers and optimization levels. Invaluable for learning and performance tuning. |

## Tools
### Compilers
- [GCC](https://gcc.gnu.org/) – Open-source, cross-platform, de-facto standard on Linux/Unix
- [Clang/LLVM](https://clang.llvm.org/) – Modern compiler with excellent diagnostics and fast compilation
- [MSVC](https://learn.microsoft.com/en-us/cpp/windows/latest-supported-vc-redist?view=msvc-170) – Microsoft Visual C++, native Windows compiler (part of Visual Studio)

### Integrated Development Environments (IDEs) & Editors
- [Visual Studio](https://visualstudio.microsoft.com/) – Full-featured flagship IDE (Windows)
- [CLion](https://www.jetbrains.com/clion/) – Powerful cross-platform IDE by JetBrains
- [VS Code](https://code.visualstudio.com/) – Lightweight, highly extensible editor (with C/C++ extension)
- [Code::Blocks](http://www.codeblocks.org/) – Free, open-source, cross-platform IDE
- [Dev-C++](https://www.dev-cpp.com/) – Simple and lightweight IDE (Windows)

### Build Systems
- [CMake](https://cmake.org/) – Industry-standard cross-platform build generator (must-learn)
- [Make](https://www.gnu.org/software/make/) – Classic Unix Makefile tool
- [Ninja](https://ninja-build.org/) – Small, high-speed build system (often used with CMake)

### Debuggers
- [GDB](https://sourceware.org/gdb/) – GNU Debugger, powerful open-source debugger
- [LLDB](https://lldb.llvm.org/) – LLVM project debugger (faster startup, better integration with Clang)

### Version Control
- [Git](https://git-scm.com/) – Distributed version control system (essential for all developers)

### Package Managers
- [vcpkg](https://vcpkg.io/) – Microsoft’s C/C++ library manager (easy integration with Visual Studio & CMake)
- [Conan](https://conan.io/) – Decentralized, open-source C/C++ package manager

### Code Analysis & Testing
- [Clang-Tidy](https://clang.llvm.org/extra/clang-tidy/) – Modern static analyzer and code fixer
- [Cppcheck](https://cppcheck.sourceforge.net/) – Static analysis tool for finding bugs
- [Google Test](https://github.com/google/googletest) – Google’s C++ testing framework (industry standard)
- [Catch2](https://github.com/catchorg/Catch2) – Header-only, lightweight testing framework

### Development Utilities
- [Clang-Format](https://clang.llvm.org/docs/ClangFormat.html) – Automatic code formatter (enforces consistent style)
- [Valgrind](https://valgrind.org/) – Memory leak detection & profiling (Linux/macOS)
- [Perf](https://perfwiki.github.io/main/) – Linux performance analysis tool
- [Docker](https://www.docker.com/) – Containerization for consistent build & runtime environments

## Application Fields
| Application Domain       | Core Scenarios                                      | Recommended Frameworks/Libraries                                                                 |
|--------------------------|-----------------------------------------------------|--------------------------------------------------------------------------------------------------|
| **Desktop App Development** | Office software, industrial control interfaces, desktop tools, design software | [Qt](https://www.qt.io/): Cross-platform full-stack framework with GUI, networking, database, multimedia.<br>[MFC](https://learn.microsoft.com/en-us/cpp/mfc/mfc-desktop-applications): Native Windows framework for legacy projects.<br>[wxWidgets](https://www.wxwidgets.org/): Lightweight cross-platform framework with native look & feel.<grok-card data-id="e563d7" data-type="citation_card"></grok-card><grok-card data-id="ab9310" data-type="citation_card"></grok-card> |
| **Embedded Development** | In-vehicle infotainment, smart home panels, medical devices, industrial controllers, router firmware | [Qt for Embedded](https://www.qt.io/qt-for-embedded-linux): Embedded GUI for ARM etc.<br>[Zephyr RTOS](https://www.zephyrproject.org/): Scalable open-source RTOS for resource-constrained IoT.<br>[FreeRTOS](https://www.freertos.org/): Lightweight RTOS for resource-limited devices.<grok-card data-id="17f3e4" data-type="citation_card"></grok-card><grok-card data-id="293dde" data-type="citation_card"></grok-card> |
| **Backend/Server Development** | Distributed systems, API gateways, database kernels, high-concurrency services (game servers, payment systems) | [Boost.Asio](https://www.boost.org/doc/libs/1_85_0/doc/html/boost_asio.html): Asynchronous networking for TCP/UDP/HTTP.<br>[Muduo](https://github.com/chenshuo/muduo): Reactor-pattern high-concurrency server.<br>[brpc](https://github.com/apache/brpc): Industrial-grade RPC framework with multi-protocol support.<br>[Drogon](https://drogon.org/): Fast HTTP framework with async I/O + ORM.<grok-card data-id="01d022" data-type="citation_card"></grok-card><grok-card data-id="b8dba9" data-type="citation_card"></grok-card> |
| **Game Development**    | AAA game clients, game engines, game servers, indie games | [Unreal Engine](https://www.unrealengine.com/): Open-source engine with Blueprint system + C++.<br>[Godot Engine](https://godotengine.org/): Free open-source engine with C++ support (via GDExtension).<br>[O3DE](https://o3de.org/): Open 3D Engine by Amazon, modular C++ architecture.<grok-card data-id="ad021b" data-type="citation_card"></grok-card><grok-card data-id="99fe34" data-type="citation_card"></grok-card> |
| **Audio/Video Streaming** | Players, live streaming push/pull, video editing, transcoding, surveillance | [FFmpeg](https://ffmpeg.org/): Comprehensive audio/video processing (decode/encode/transmit).<br>[GStreamer](https://gstreamer.freedesktop.org/): Streaming media pipeline framework.<br>[SDL](https://www.libsdl.org/): Multimedia library for audio/rendering.<br>[OpenCV](https://opencv.org/): Video analysis (e.g., face recognition).<grok-card data-id="213fd8" data-type="citation_card"></grok-card><grok-card data-id="3029b2" data-type="citation_card"></grok-card> |
| **AI/Machine Learning**  | Deep learning framework backends, model inference optimization, high-performance computing (HPC) | [TensorFlow C++ API](https://www.tensorflow.org/api_docs/cc): Model deployment interface.<br>[LibTorch (PyTorch C++)](https://pytorch.org/cppdocs/): Dynamic graph inference library.<br>[OpenCV](https://opencv.org/): Image preprocessing/feature extraction.<br>[Eigen](http://eigen.tuxfamily.org/): High-performance matrix library.<br>[ONNX Runtime](https://onnxruntime.ai/): Cross-framework inference engine.<grok-card data-id="a55ab9" data-type="citation_card"></grok-card> |
| **Systems/Kernel Development** | OS kernels, drivers, database kernels, file systems | [Linux Kernel](https://www.kernel.org/): Kernel API development.<br>[WDF/KMDF](https://learn.microsoft.com/en-us/windows-hardware/drivers/wdf/): Windows driver framework.<br>[SQLite](https://www.sqlite.org/): Embedded database kernel. |
| **FinTech/High-Frequency Trading** | HFT systems, quant trading engines, financial risk systems (low-latency, high-reliability) | [QuickFIX](http://www.quickfixengine.org/): FIX protocol library.<br>[Boost.Asio](https://www.boost.org/): Low-latency networking.<br>Custom lock-free data structures & kernel bypass techniques.<grok-card data-id="85980e" data-type="citation_card"></grok-card><grok-card data-id="f55608" data-type="citation_card"></grok-card> |

## Real-World Projects

### Embedded / IoT / RTOS
| Project                                                          | Difficulty | Core Skills Learned                                  |
|------------------------------------------------------------------|------------|------------------------------------------------------|
| [bblanchon/ArduinoJson](https://github.com/bblanchon/ArduinoJson)         | ★☆☆☆☆     | Static-memory JSON parsing (embedded must-know)      |
| [lvgl/lvgl](https://github.com/lvgl/lvgl)                                 | ★★☆☆☆     | Most popular embedded GUI library                    |
| [zephyrproject-rtos/zephyr](https://github.com/zephyrproject-rtos/zephyr) | ★★★★☆     | Modern RTOS, BLE, drivers, device tree               |
| [platformio/platformio-core](https://github.com/platformio/platformio-core) | ★★★☆☆   | Full-stack embedded build system                     |
| [espressif/esp-idf](https://github.com/espressif/esp-idf)                 | ★★★★☆     | Official ESP32 SDK, FreeRTOS, low-power design       |

### Backend / High-Performance Servers
| Project                                                          | Difficulty | Core Skills Learned                                  |
|------------------------------------------------------------------|------------|------------------------------------------------------|
| [yhirose/cpp-httplib](https://github.com/yhirose/cpp-httplib)             | ★☆☆☆☆     | Single-header HTTP server (perfect first project)   |
| [drogonframework/drogon](https://github.com/drogonframework/drogon)       | ★★☆☆☆     | High-performance async web framework + ORM           |
| [chenshuo/muduo](https://github.com/chenshuo/muduo)                       | ★★★★☆     | Classic Reactor pattern, event-driven networking     |
| [apache/brpc](https://github.com/apache/brpc)                             | ★★★★☆     | Industrial-grade RPC, bthread, zero-copy             |
| [Tencent/libco](https://github.com/Tencent/libco)                         | ★★★★☆     | Coroutine library (used in WeChat backend)           |
| [scylladb/seastar](https://github.com/scylladb/seastar)                   | ★★★★★     | Share-nothing, lock-free, million QPS framework      |
| [userver-framework/userver](https://github.com/userver-framework/userver) | ★★★★★     | Modern C++20 coroutine service framework             |

### Game Development & Engines
| Project                                                          | Difficulty | Core Skills Learned                                  |
|------------------------------------------------------------------|------------|------------------------------------------------------|
| [SFML/SFML](https://github.com/SFML/SFML)                                 | ★☆☆☆☆     | Lightweight 2D multimedia library                    |
| [skypjack/entt](https://github.com/skypjack/entt)                         | ★★☆☆☆     | Industry-standard ECS (Entity-Component-System)      |
| [raylib](https://github.com/raysan5/raylib) (raylib-cpp wrapper)          | ★★☆☆☆     | Extremely simple game dev library                    |
| [TheCherno/Hazel](https://github.com/TheCherno/Hazel)                     | ★★★★☆     | From-scratch game engine (amazing teaching series)   |
| [godotengine/godot](https://github.com/godotengine/godot)                 | ★★★★☆     | Full open-source engine with C++ modules/GDExtension |
| [o3de/o3de](https://github.com/o3de/o3de)                                 | ★★★★★     | Amazon’s Open 3D Engine (AAA-grade)                  |

### Audio / Video / Streaming
| Project                                                          | Difficulty | Core Skills Learned                                  |
|------------------------------------------------------------------|------------|------------------------------------------------------|
| [obsproject/obs-studio](https://github.com/obsproject/obs-studio)         | ★★★★☆     | Real-time streaming, plugin architecture, GPU       |
| [FFmpeg/FFmpeg](https://github.com/FFmpeg/FFmpeg)                         | ★★★★☆     | The ultimate audio/video codec toolbox               |
| [bluenviron/mediamtx](https://github.com/bluenviron/mediamtx)             | ★★★☆☆     | Zero-dependency RTSP/WebRTC/HLS server               |
| [Haivision/srt](https://github.com/Haivision/srt)                         | ★★★★☆     | Secure Reliable Transport (low-latency over UDP)    |
| [isl-org/Open3D](https://github.com/isl-org/Open3D)                       | ★★★★☆     | 3D data processing, point clouds, reconstruction     |

### AI / Machine Learning / Inference
| Project                                                          | Difficulty | Core Skills Learned                                  |
|------------------------------------------------------------------|------------|------------------------------------------------------|
| [nlohmann/json](https://github.com/nlohmann/json)                         | ★☆☆☆☆     | Header-only JSON (used everywhere in ML pipelines)  |
| [opencv/opencv](https://github.com/opencv/opencv)                         | ★★★☆☆     | Image processing + DNN module                        |
| [Tencent/ncnn](https://github.com/Tencent/ncnn)                           | ★★★☆☆     | Mobile & embedded deep learning inference            |
| [microsoft/onnxruntime](https://github.com/microsoft/onnxruntime)         | ★★★☆☆     | High-performance cross-platform inference engine     |
| [pytorch/pytorch (LibTorch)](https://github.com/pytorch/pytorch)          | ★★★★☆     | Official PyTorch C++ frontend + custom operators     |

### Systems / Kernel / Infrastructure
| Project                                                          | Difficulty | Core Skills Learned                                  |
|------------------------------------------------------------------|------------|------------------------------------------------------|
| [gabime/spdlog](https://github.com/gabime/spdlog)                         | ★☆☆☆☆     | Blazing-fast logging library                         |
| [sqlite/sqlite](https://github.com/sqlite/sqlite)                         | ★★★★☆     | Embedded database engine, B-tree implementation      |
| [facebook/folly](https://github.com/facebook/folly)                       | ★★★★★     | Facebook’s core low-level library (futures, fibers)  |
| [microsoft/Detours](https://github.com/microsoft/Detours)                 | ★★★★☆     | Windows API hooking                                  |
| [ClickHouse/ClickHouse](https://github.com/ClickHouse/ClickHouse)         | ★★★★★     | Columnar DBMS with vectorized execution              |
| [torvalds/linux](https://github.com/torvalds/linux)                       | ★★★★★     | The Linux kernel (ultimate systems learning)         |

## Interview Preparation
[The Role of the `static` Keyword](interview_questions/README.en.md#the-role-of-the-static-keyword)  
[The Role of the `const` Keyword](interview_questions/README.en.md#the-role-of-the-const-keyword)  
[Differences Between `inline` Functions and Macros](interview_questions/README.en.md#differences-between-inline-functions-and-macros)  
[The Role of the `explicit` Keyword](interview_questions/README.en.md#the-role-of-the-explicit-keyword)  
[Differences Between `nullptr` and `NULL`](interview_questions/README.en.md#differences-between-nullptr-and-null)  
[Differences Between `sizeof` and `strlen`](interview_questions/README.en.md#differences-between-sizeof-and-strlen)  
[Differences Between `new` and `malloc`](interview_questions/README.en.md#differences-between-new-and-malloc)  
[Differences Between `delete` and `delete[]`](interview_questions/README.en.md#differences-between-delete-and-delete)  
[Four Types of Cast Conversions](interview_questions/README.en.md#four-types-of-cast-conversions)  
[The Entire Process of C++ Program Compilation and Linking](interview_questions/README.en.md#the-entire-process-of-c-program-compilation-and-linking)  
[Differences Between `struct` and `class`](interview_questions/README.en.md#differences-between-struct-and-class)  
[Differences Between C and C++](interview_questions/README.en.md#differences-between-c-and-c)  
[The Role of the `volatile` Keyword](interview_questions/README.en.md#the-role-of-the-volatile-keyword)  
[How is Polymorphism Implemented? Do You Understand Virtual Function Tables?](interview_questions/README.en.md#how-is-polymorphism-implemented-do-you-understand-virtual-function-tables)  
[Why Must the Base Class Destructor Be Virtual?](interview_questions/README.en.md#why-must-the-base-class-destructor-be-virtual)  
[Can Constructors Be Virtual? Can Destructors Be Pure Virtual?](interview_questions/README.en.md#can-constructors-be-virtual-can-destructors-be-pure-virtual)  
[Differences Between Overloading, Overriding, and Redefinition](interview_questions/README.en.md#differences-between-overloading-overriding-and-redefinition)  
[Differences Between Copy Constructors and Assignment Operator Overloading](interview_questions/README.en.md#differences-between-copy-constructors-and-assignment-operator-overloading)  
[Differences Between Deep Copy and Shallow Copy](interview_questions/README.en.md#differences-between-deep-copy-and-shallow-copy)  
[Rule of Three / Rule of Five](interview_questions/README.en.md#rule-of-three--rule-of-five)  
[The `final` and `override` Keywords](interview_questions/README.en.md#the-final-and-override-keywords)  
[Why Can't Constructors Be Virtual?](interview_questions/README.en.md#why-cant-constructors-be-virtual)  
[Differences Between Pure Virtual Functions and Virtual Functions](interview_questions/README.en.md#differences-between-pure-virtual-functions-and-virtual-functions)  
[Differences Between Abstract Classes and Interfaces](interview_questions/README.en.md#differences-between-abstract-classes-and-interfaces)  
[The Role of the `friend` Keyword](interview_questions/README.en.md#the-role-of-the-friend-keyword)  
[How to Prevent a Class from Being Inherited in C++?](interview_questions/README.en.md#how-to-prevent-a-class-from-being-inherited-in-c)  
[C++ Memory Partitions](interview_questions/README.en.md#c-memory-partitions)  
[Differences Between Heap and Stack](interview_questions/README.en.md#differences-between-heap-and-stack)  
[How to Detect and Locate Memory Leaks?](interview_questions/README.en.md#how-to-detect-and-locate-memory-leaks)  
[What Are Wild Pointers and Dangling Pointers? How to Avoid Them?](interview_questions/README.en.md#what-are-wild-pointers-and-dangling-pointers-how-to-avoid-them)  
[RAII Principle](interview_questions/README.en.md#raii-principle)  
[What Smart Pointers Do You Know?](interview_questions/README.en.md#what-smart-pointers-do-you-know)  
[Implementation Principle of `shared_ptr`? How to Solve Circular References?](interview_questions/README.en.md#implementation-principle-of-shared_ptr-how-to-solve-circular-references)  
[Can `unique_ptr` Be Copied?](interview_questions/README.en.md#can-unique_ptr-be-copied)  
[Principle of `weak_ptr` in Solving Circular References](interview_questions/README.en.md#principle-of-weak_ptr-in-solving-circular-references)  
[Memory Alignment Rules](interview_questions/README.en.md#memory-alignment-rules)  
[Underlying Implementation and Expansion Mechanism of `vector`](interview_questions/README.en.md#underlying-implementation-and-expansion-mechanism-of-vector)  
[What Are the Scenarios of Iterator Invalidation?](interview_questions/README.en.md#what-are-the-scenarios-of-iterator-invalidation)  
[Differences Between `map` and `unordered_map`? When to Use Which?](interview_questions/README.en.md#differences-between-map-and-unordered_map-when-to-use-which)  
[How to Resolve Hash Collisions in `unordered_map`?](interview_questions/README.en.md#how-to-resolve-hash-collisions-in-unordered_map)  
[Underlying Implementation of `set` and `map`](interview_questions/README.en.md#underlying-implementation-of-set-and-map)  
[Differences Between `emplace_back` and `push_back`](interview_questions/README.en.md#differences-between-emplace_back-and-push_back)  
[Common STL Algorithms](interview_questions/README.en.md#common-stl-algorithms)  
[Differences Between `list` and `vector`](interview_questions/README.en.md#differences-between-list-and-vector)  
[Six Major Components of STL](interview_questions/README.en.md#six-major-components-of-stl)  
[Differences Between Red-Black Trees and AVL Trees](interview_questions/README.en.md#differences-between-red-black-trees-and-avl-trees)  
[Several Most Important New Features of C++11](interview_questions/README.en.md#several-most-important-new-features-of-c11)  
[Move Semantics and Perfect Forwarding](interview_questions/README.en.md#move-semantics-and-perfect-forwarding)  
[The Role of `std::move`](interview_questions/README.en.md#the-role-of-stdmove)  
[The Role of `std::forward`](interview_questions/README.en.md#the-role-of-stdforward)  
[Underlying Implementation of Lambda Expressions](interview_questions/README.en.md#underlying-implementation-of-lambda-expressions)  
[The Role of `noexcept`](interview_questions/README.en.md#the-role-of-noexcept)  
[Differences Between `auto` and `decltype`](interview_questions/README.en.md#differences-between-auto-and-decltype)  
[Differences Between Rvalue References and Lvalue References](interview_questions/README.en.md#differences-between-rvalue-references-and-lvalue-references)  
[Implementation Principle of `std::atomic`? Is `a++` an Atomic Operation?](interview_questions/README.en.md#implementation-principle-of-stdatomic-is-a-an-atomic-operation)  
[Four Conditions for Deadlock? How to Avoid It?](interview_questions/README.en.md#four-conditions-for-deadlock-how-to-avoid-it)  
[How to Write a Thread-Safe Singleton?](interview_questions/README.en.md#how-to-write-a-thread-safe-singleton)  
[How to Use `mutex` and `condition_variable` Together?](interview_questions/README.en.md#how-to-use-mutex-and-condition_variable-together)  
[What Are the Thread Synchronization Methods?](interview_questions/README.en.md#what-are-the-thread-synchronization-methods)  
[Differences Between Processes and Threads](interview_questions/README.en.md#differences-between-processes-and-threads)  
[Differences Between TCP and UDP? Application Scenarios?](interview_questions/README.en.md#differences-between-tcp-and-udp-application-scenarios)  
[Differences and Principles of `select`, `poll`, and `epoll`](interview_questions/README.en.md#differences-and-principles-of-select-poll-and-epoll)  
[What Are Sticky Packets and Packet Fragmentation? How to Solve Them?](interview_questions/README.en.md#what-are-sticky-packets-and-packet-fragmentation-how-to-solve-them)  
[TCP Three-Way Handshake and Four-Way Wave](interview_questions/README.en.md#tcp-three-way-handshake-and-four-way-wave)  
[Implement a Thread-Safe Singleton](interview_questions/README.en.md#implement-a-thread-safe-singleton)  
[Implement LRU Cache](interview_questions/README.en.md#implement-lru-cache)  
[Implement Quicksort](interview_questions/README.en.md#implement-quicksort)  
[Implement Mergesort](interview_questions/README.en.md#implement-mergesort)  
[Implement String Reversal](interview_questions/README.en.md#implement-string-reversal)  
[Implement Two Sum](interview_questions/README.en.md#implement-two-sum)
