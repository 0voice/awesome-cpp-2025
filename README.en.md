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

Want to know what the father of C++, **Bjarne Stroustrup**, has personally answered about C++ in interviews and Q&As?  
Please refer to: [Bjarne Stroustrup's FAQ](#bjarne-stroustrups-faq).

Want to read the latest C++ Standards Committee (WG21) proposals and papers?  
Please visit: [WG21 Papers](https://github.com/0voice/cpp-learning-2025/tree/main/WG21-Papers).

## Table of Contents
- [Learning Roadmap](#learning-roadmap)
- [Core Knowledge](#core-knowledge)
- [Advanced Modern C++ Features](advanced-modern-c-features-c20--c23)
- [C++ Development on Linux](https://github.com/0voice/awesome-modern-cpp-2025/tree/main/cpp-on-linux)
- [Recommended Resources](#recommended-resources)
- [Tools](#tools)
- [Application Fields](#application-fields)
- [Real-World Projects](#real-world-projects)
- [Interview Preparation](#interview-preparation)
- [LeetCode Problems](#leetcode-problems)
- [Bjarne Stroustrup's FAQ](bjarne-stroustrups-faq)
- [Resource Declaration](#resource-declaration)

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
| C++ Primer                              | Stanley B. Lippman et al.       | ★★★☆☆     | The comprehensive and systematic “C++ Bible”, covering syntax, STL, and C++11+ modern features with a strong emphasis on real-world practice. High knowledge density and in-depth explanations. ideal for solidifying your knowledge base or advancing to modern style after some foundation. |
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
- [GCC](https://gcc.gnu.org/) – Open-source, cross-platform king
- [Clang/LLVM](https://clang.llvm.org/) – Modern compiler with excellent diagnostics
- [MSVC](https://learn.microsoft.com/en-us/cpp/windows/latest-supported-vc-redist) – Native Windows compiler (Visual Studio)
- [MinGW-w64](https://www.mingw-w64.org/) – GCC on Windows
- [Intel oneAPI DPC++/C++ Compiler](https://www.intel.com/content/www/us/en/developer/tools/oneapi/dpc-compiler.html) – AVX-512 & vectorization beast
- [Emscripten](https://emscripten.org/) – Compile C++ to WebAssembly

### Integrated Development Environments (IDEs)
- [Visual Studio](https://visualstudio.microsoft.com/) – Full-featured Windows powerhouse
- [CLion](https://www.jetbrains.com/clion/) – Best JetBrains C++ IDE
- [VS Code + C/C++ extensions](https://code.visualstudio.com/) – Lightweight & hugely popular
- [Qt Creator](https://www.qt.io/product/development-tools) – Official Qt IDE
- [VS Code + CMake Tools + clangd](https://code.visualstudio.com/) – The most popular combo in 2025
- [CodeLite](https://codelite.org/) – Free open-source alternative
- [Cevelop](https://www.cevelop.com/) – Modernized Eclipse CDT fork

### Build Systems
- [CMake](https://cmake.org/) – De-facto industry standard
- [Meson](https://mesonbuild.com/) – Faster & cleaner than CMake (fastest growing in 2025)
- [Ninja](https://ninja-build.org/) – Extremely fast build backend
- [Bazel](https://bazel.build/) – Google-scale monorepo build system
- [xmake](https://xmake.io/) – Modern Chinese build system with Lua config (very smooth)
- [Premake](https://premake.github.io/) – Lightweight cross-platform project generator

### Debuggers & Performance Profiling
- [GDB](https://sourceware.org/gdb/) / [LLDB](https://lldb.llvm.org/) – Classic command-line debuggers
- [WinDbg](https://learn.microsoft.com/en-us/windows-hardware/drivers/debugger/) – Windows kernel & driver debugging
- [Tracy Profiler](https://github.com/wolfpld/tracy) – Hottest frame-level profiler in 2025
- [Perfetto](https://perfetto.dev/) – Google’s system-wide tracing tool
- [Valgrind](https://valgrind.org/) + [AddressSanitizer](https://clang.llvm.org/docs/AddressSanitizer.html) – Memory error detectors
- [RenderDoc](https://renderdoc.org/) – Graphics debugging (Vulkan/DX/OpenGL)

### Package Managers
- [vcpkg](https://vcpkg.io/) – Microsoft official, seamless VS integration
- [Conan 2.x](https://conan.io/) – Most mature C++ package manager
- [cppan](https://cppan.org/) – Veteran (still usable)
- [Hunter](https://github.com/cpp-pm/hunter) – Native CMake integration
- [Buckaroo](https://buckaroo.pm/) – Modern newcomer

### Static Analysis & Testing
- [Clang-Tidy](https://clang.llvm.org/extra/clang-tidy/) – Official static analyzer
- [Cppcheck](https://cppcheck.net/) – Lightweight bug finder
- [PVS-Studio](https://pvs-studio.com/) – Industrial-grade analyzer (free for open-source)
- [Google Test](https://github.com/google/googletest) / [Catch2](https://github.com/catchorg/Catch2) – Industry-standard testing frameworks
- [doctest](https://github.com/doctest/doctest) – Single-header, ultra-lightweight testing
- [ApprovalTests.cpp](https://github.com/approvals/ApprovalTests.cpp) – Golden-master / snapshot testing

### Code Formatting & Refactoring
- [clang-format](https://clang.llvm.org/docs/ClangFormat.html) – Industry standard formatter
- [uncrustify](https://github.com/uncrustify/uncrustify) – Highly configurable
- [astyle](http://astyle.sourceforge.net/) – Veteran formatter
- [Sourcery](https://sourcery.ai/) (paid) – AI-powered refactoring suggestions

### Memory & Performance Tools
- [Valgrind](https://valgrind.org/) – Heavyweight memory checker
- [Address/Memory/Thread Sanitizers](https://clang.llvm.org/docs/) – Built into Clang/GCC
- [gperftools](https://github.com/gperftools/gperftools) – CPU & heap profiler
- [tcmalloc](https://github.com/google/tcmalloc) – High-performance allocator

### Documentation & Visualization
- [Doxygen](https://www.doxygen.nl/) – Classic code documentation generator
- [Sphinx + Breathe](https://www.sphinx-doc.org/) – Modern documentation system
- [Graphviz](https://graphviz.org/) – Class / call-graph visualization

### Development Helpers
- [Git](https://git-scm.com/) + [GitKraken](https://www.gitkraken.com/) / [Fork](https://git-fork.com/) – Version control
- [Docker](https://www.docker.com/) – Environment isolation
- [CMake GUI / ccmake](https://cmake.org/cmake/gui/) – Visual CMake configuration
- [Ninja + ccache](https://ccache.dev/) – 5–10× faster incremental builds
- [include-what-you-use](https://include-what-you-use.org/) – Header dependency analyzer
- [cpplint](https://github.com/cpplint/cpplint) – Google style checker
- [GitHub Copilot / Codeium / Tabnine](https://github.com/features/copilot) – AI-powered code completion

## Application Fields

| Domain                     | Core Scenarios                                                                 | Recommended Frameworks / Libraries                                                                                                    |
|----------------------------|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| **Desktop Application Development** | Office software, industrial control panels, desktop utilities, design tools    | [Qt](https://www.qt.io/) – Full-stack cross-platform framework (GUI, networking, DB, multimedia)<br>[MFC](https://learn.microsoft.com/en-us/cpp/mfc/mfc-desktop-applications) – Native Windows framework (good for legacy)<br>[wxWidgets](https://www.wxwidgets.org/) – Cross-platform, native look & feel<br>[FLTK](http://www.fltk.org/) – Fast Light Toolkit<br>[ImGui](https://github.com/ocornut/imgui) – Immediate-mode GUI, minimal dependencies<br>[JUCE](https://juce.com/) – All-in-one cross-platform audio/application framework |
| **Embedded Development**   | Car infotainment, smart home panels, medical devices, industrial controllers, router firmware | [Qt for Embedded](https://www.qt.io/qt-for-embedded-linux) – GUI on ARM etc.<br>[FreeRTOS](https://www.freertos.org/) – Lightweight RTOS<br>[Yocto / Buildroot](https://www.yoctoproject.org/) – Embedded Linux distro builders<br>[ETL](https://github.com/ETLCPP/etl) – Embedded Template Library (no STL)<br>[tbox](https://github.com/tboox/tbox) – Cross-platform glib-like utils<br>[lwIP](https://savannah.nongnu.org/projects/lwip/) – Lightweight TCP/IP stack<br>[DPDK](https://www.dpdk.org/) – High-speed packet processing |
| **Backend / Server Development** | Distributed systems, API gateways, database kernels, high-concurrency services (game servers, payment systems) | [Boost.Asio](https://www.boost.org/doc/libs/1_85_0/doc/html/boost_asio.html) – Async networking<br>[Muduo](https://github.com/chenshuo/muduo) – High-performance Reactor server<br>[Brpc](https://github.com/apache/incubator-brpc) – Multi-protocol RPC framework<br>[Drogon](https://drogon.org/) – Async HTTP + ORM framework<br>[Seastar](https://seastar.io/) – Lock-free high-performance server framework<br>[Folly](https://github.com/facebook/folly) – Facebook’s high-performance library collection<br>[Crow](https://crowcpp.org/) – Micro web framework (Flask-like) |
| **Game Development**       | AAA game clients, game engines, game servers, indie games                     | [Unreal Engine](https://www.unrealengine.com/) – Open-source engine with Blueprints + C++<br>[Cocos2d-x](https://www.cocos.com/en/cocos2d-x) – Cross-platform 2D engine<br>[Unity](https://unity.com/) – C# on top + C++ plugins<br>[raylib](https://www.raylib.com/) – Simple & fun game programming library<br>[SFML](https://www.sfml-dev.org/) – Simple and Fast Multimedia Library<br>[SDL2](https://www.libsdl.org/) – Low-level multimedia layer<br>[EnTT](https://github.com/skypjack/entt) – Modern C++ ECS framework |
| **Audio/Video & Streaming** | Players, live streaming (push/pull), video editing, transcoding, surveillance | [FFmpeg](https://ffmpeg.org/) – The Swiss army knife of multimedia<br>[GStreamer](https://gstreamer.freedesktop.org/) – Pipeline-based media framework<br>[SDL](https://www.libsdl.org/) – Audio & rendering<br>[OpenCV](https://opencv.org/) – Computer vision & video analysis<br>[PortAudio](http://www.portaudio.com/) – Cross-platform audio I/O<br>[miniaudio](https://miniaud.io/) – Single-header audio library<br>[libav](https://libav.org/) – FFmpeg-based multimedia toolkit |
| **AI / Machine Learning**  | Deep-learning inference, model optimization, high-performance computing (HPC) | [TensorFlow C++ API](https://www.tensorflow.org/api_docs/cc)<br>[LibTorch (PyTorch C++)](https://pytorch.org/cppdocs/) – Dynamic-graph inference<br>[OpenCV](https://opencv.org/) – Image preprocessing<br>[Eigen](http://eigen.tuxfamily.org/) – Linear algebra<br>[ONNX Runtime](https://onnxruntime.ai/) – Cross-framework inference engine<br>[Dlib](https://dlib.net/) – ML toolkit<br>[ncnn](https://github.com/Tencent/ncnn) – Mobile neural-network inference<br>[mlpack](https://mlpack.org/) – Scalable ML library |
| **Systems Programming / Kernel** | OS kernels, drivers, database engines, filesystems                           | [Linux Kernel](https://www.kernel.org/) – Kernel API development<br>[WDF/KMDF](https://learn.microsoft.com/en-us/windows-hardware/drivers/wdf/) – Windows driver framework<br>[SQLite](https://www.sqlite.org/) – Embedded DB engine<br>[Boost](https://www.boost.org/) – General-purpose libraries<br>[Abseil](https://abseil.io/) – Google’s common C++ libraries<br>[jemalloc](https://jemalloc.net/) – High-performance allocator |
| **FinTech / High-Frequency Trading** | HFT engines, quant trading platforms, risk systems (ultra-low latency)       | [QuickFIX](http://www.quickfixengine.org/) – FIX protocol engine<br>[Boost.Asio](https://www.boost.org/) – Low-latency networking<br>[QuantLib](https://www.quantlib.org/) – Open-source quantitative finance library |

## Real-World Projects
### Desktop Application Development
| Project | Difficulty | Core Skills |
|-------|------------|-------------|
| [ocornut/imgui](https://github.com/ocornut/imgui) | ★★☆☆☆ | Immediate-mode GUI, debugging overlays |
| [microsoft/terminal](https://github.com/microsoft/terminal) | ★★★★☆ | Large-scale modern desktop, GPU-accelerated rendering |
| [flameshot-org/flameshot](https://github.com/flameshot-org/flameshot) | ★★★☆☆ | Screenshot tool, Qt + image processing |
| [deskflow/deskflow](https://github.com/deskflow/deskflow) (ex-Barrier) | ★★★★☆ | Cross-computer mouse/keyboard sharing, networking |
| [transmission/transmission](https://github.com/transmission/transmission) | ★★★☆☆ | Cross-platform BitTorrent client, async I/O |
| [qBittorrent/qBittorrent](https://github.com/qBittorrent/qBittorrent) | ★★★☆☆ | Full-featured Qt torrent client |
| [sqlitebrowser/sqlitebrowser](https://github.com/sqlitebrowser/sqlitebrowser) | ★★★☆☆ | Database visualization tool, SQL parsing |
| [mltframework/shotcut](https://github.com/mltframework/shotcut) | ★★★★☆ | Professional video editor, FFmpeg integration |
| [Genymobile/scrcpy](https://github.com/Genymobile/scrcpy) | ★★★☆☆ | Android screen mirroring, low-latency USB/Wi-Fi |

### Embedded Development
| Project | Difficulty | Core Skills |
|-------|------------|-------------|
| [lvgl/lvgl](https://github.com/lvgl/lvgl) | ★★☆☆☆ | Leading embedded GUI library |
| [zephyrproject-rtos/zephyr](https://github.com/zephyrproject-rtos/zephyr) | ★★★★☆ | Modern RTOS, BLE, drivers |
| [espressif/esp-idf](https://github.com/espressif/esp-idf) | ★★★★☆ | Official ESP32 SDK, low-power |
| [ARM-software/CMSIS_5](https://github.com/ARM-software/CMSIS_5) | ★★★☆☆ | ARM Cortex standard interface |
| [wolfSSL/wolfSSL](https://github.com/wolfSSL/wolfSSL) | ★★★☆☆ | Lightweight TLS/SSL for embedded |
| [project-chip/connectedhomeip](https://github.com/project-chip/connectedhomeip) | ★★★★☆ | Matter (smart home) protocol stack |

### Backend / Server Development
| Project | Difficulty | Core Skills |
|-------|------------|-------------|
| [yhirose/cpp-httplib](https://github.com/yhirose/cpp-httplib) | ★☆☆☆☆ | Header-only HTTP server |
| [drogonframework/drogon](https://github.com/drogonframework/drogon) | ★★☆☆☆ | High-performance async web framework |
| [chenshuo/muduo](https://github.com/chenshuo/muduo) | ★★★★☆ | Classic Reactor network library |
| [apache/brpc](https://github.com/apache/brpc) | ★★★★☆ | Baidu RPC framework, bthread |
| [scylladb/seastar](https://github.com/scylladb/seastar) | ★★★★★ | Shard-per-core, lock-free, million QPS |
| [grpc/grpc](https://github.com/grpc/grpc) | ★★★★☆ | High-performance RPC, Protobuf |
| [oatpp/oatpp](https://github.com/oatpp/oatpp) | ★★☆☆☆ | Zero-dependency web framework + ORM |

### Game Development
| Project | Difficulty | Core Skills |
|-------|------------|-------------|
| [SFML/SFML](https://github.com/SFML/SFML) | ★☆☆☆☆ | Simple 2D multimedia layer |
| [skypjack/entt](https://github.com/skypjack/entt) | ★★☆☆☆ | Modern ECS architecture |
| [raysan5/raylib](https://github.com/raysan5/raylib) | ★★☆☆☆ | Minimalist game programming library |
| [TheCherno/Hazel](https://github.com/TheCherno/Hazel) | ★★★★☆ | From-scratch engine (educational) |
| [godotengine/godot](https://github.com/godotengine/godot) | ★★★★☆ | Full open-source engine |
| [bkaradzic/bgfx](https://github.com/bkaradzic/bgfx) | ★★★★☆ | Cross-platform rendering backend |
| [NVIDIA-Omniverse/PhysX](https://github.com/NVIDIA-Omniverse/PhysX) | ★★★★☆ | Physics simulation engine |

### Audio/Video & Streaming
| Project | Difficulty | Core Skills |
|-------|------------|-------------|
| [obsproject/obs-studio](https://github.com/obsproject/obs-studio) | ★★★★☆ | Live streaming, plugin system |
| [FFmpeg/FFmpeg](https://github.com/FFmpeg/FFmpeg) | ★★★★☆ | Complete multimedia processing suite |
| [bluenviron/mediamtx](https://github.com/bluenviron/mediamtx) | ★★★☆☆ | Zero-dependency RTMP/RTSP/WebRTC server |
| [Haivision/srt](https://github.com/Haivision/srt) | ★★★★☆ | Secure Reliable Transport protocol |
| [GStreamer/gstreamer](https://github.com/GStreamer/gstreamer) | ★★★★☆ | Pipeline-based media framework |

### AI / Machine Learning
| Project | Difficulty | Core Skills |
|-------|------------|-------------|
| [opencv/opencv](https://github.com/opencv/opencv) | ★★★☆☆ | Image processing & DNN module |
| [Tencent/ncnn](https://github.com/Tencent/ncnn) | ★★★☆☆ | Mobile neural network inference |
| [microsoft/onnxruntime](https://github.com/microsoft/onnxruntime) | ★★★☆☆ | Cross-platform model inference |
| [pytorch/pytorch (LibTorch)](https://github.com/pytorch/pytorch) | ★★★★☆ | C++ frontend, custom operators |
| [openvinotoolkit/openvino](https://github.com/openvinotoolkit/openvino) | ★★★★☆ | Intel inference engine & optimization |
| [dmlc/xgboost](https://github.com/dmlc/xgboost) | ★★★★☆ | Gradient boosting library |

### Systems Programming / Kernel
| Project | Difficulty | Core Skills |
|-------|------------|-------------|
| [gabime/spdlog](https://github.com/gabime/spdlog) | ★☆☆☆☆ | Ultra-fast logging |
| [sqlite/sqlite](https://github.com/sqlite/sqlite) | ★★★★☆ | Embedded database engine, B-tree |
| [facebook/folly](https://github.com/facebook/folly) | ★★★★★ | Facebook infrastructure libraries |
| [ClickHouse/ClickHouse](https://github.com/ClickHouse/ClickHouse) | ★★★★★ | Columnar DBMS, vectorized execution |
| [torvalds/linux](https://github.com/torvalds/linux) | ★★★★★ | Linux kernel development |
| [llvm/llvm-project](https://github.com/llvm/llvm-project) | ★★★★★ | Compiler infrastructure |

### Data Processing & Storage
| Project | Difficulty | Core Skills |
|-------|------------|-------------|
| [google/leveldb](https://github.com/google/leveldb) | ★★★☆☆ | LSM-tree key-value store |
| [Tencent/rapidjson](https://github.com/Tencent/rapidjson) | ★★☆☆☆ | High-performance JSON parser |
| [apache/thrift](https://github.com/apache/thrift) | ★★★☆☆ | Cross-language serialization & RPC |
| [libevent/libevent](https://github.com/libevent/libevent) | ★★★☆☆ | Event notification library |

### Security
| Project | Difficulty | Core Skills |
|-------|------------|-------------|
| [openssl/openssl](https://github.com/openssl/openssl) | ★★★★☆ | Cryptography & SSL/TLS |
| [curl/curl](https://github.com/curl/curl) | ★★★☆☆ | Secure HTTP client, certificate handling |

### Distributed Systems
| Project | Difficulty | Core Skills |
|-------|------------|-------------|
| [ceph/ceph](https://github.com/ceph/ceph) | ★★★★★ | Distributed object store & filesystem |
| [etcd-io/etcd](https://github.com/etcd-io/etcd) (C++ client) | ★★★☆☆ | Distributed key-value store |

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

## LeetCode Problems
- [LeetCode 1 Two Sum](https://leetcode.com/problems/two-sum/)
- [LeetCode 2 Add Two Numbers](https://leetcode.com/problems/add-two-numbers/)
- [LeetCode 3 Longest Substring Without Repeating Characters](https://leetcode.com/problems/longest-substring-without-repeating-characters/)
- [LeetCode 4 Median of Two Sorted Arrays](https://leetcode.com/problems/median-of-two-sorted-arrays/)
- [LeetCode 5 Longest Palindromic Substring](https://leetcode.com/problems/longest-palindromic-substring/)
- [LeetCode 10 Regular Expression Matching](https://leetcode.com/problems/regular-expression-matching/)
- [LeetCode 11 Container With Most Water](https://leetcode.com/problems/container-with-most-water/)
- [LeetCode 15 3Sum](https://leetcode.com/problems/3sum/)
- [LeetCode 17 Letter Combinations of a Phone Number](https://leetcode.com/problems/letter-combinations-of-a-phone-number/)
- [LeetCode 19 Remove Nth Node From End of List](https://leetcode.com/problems/remove-nth-node-from-end-of-list/)
- [LeetCode 20 Valid Parentheses](https://leetcode.com/problems/valid-parentheses/)
- [LeetCode 21 Merge Two Sorted Lists](https://leetcode.com/problems/merge-two-sorted-lists/)
- [LeetCode 22 Generate Parentheses](https://leetcode.com/problems/generate-parentheses/)
- [LeetCode 23 Merge k Sorted Lists](https://leetcode.com/problems/merge-k-sorted-lists/)
- [LeetCode 31 Next Permutation](https://leetcode.com/problems/next-permutation/)
- [LeetCode 32 Longest Valid Parentheses](https://leetcode.com/problems/longest-valid-parentheses/)
- [LeetCode 33 Search in Rotated Sorted Array](https://leetcode.com/problems/search-in-rotated-sorted-array/)
- [LeetCode 34 Find First and Last Position of Element in Sorted Array](https://leetcode.com/problems/find-first-and-last-position-of-element-in-sorted-array/)
- [LeetCode 39 Combination Sum](https://leetcode.com/problems/combination-sum/)
- [LeetCode 42 Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/)
- [LeetCode 46 Permutations](https://leetcode.com/problems/permutations/)
- [LeetCode 48 Rotate Image](https://leetcode.com/problems/rotate-image/)
- [LeetCode 49 Group Anagrams](https://leetcode.com/problems/group-anagrams/)
- [LeetCode 53 Maximum Subarray](https://leetcode.com/problems/maximum-subarray/)
- [LeetCode 55 Jump Game](https://leetcode.com/problems/jump-game/)
- [LeetCode 56 Merge Intervals](https://leetcode.com/problems/merge-intervals/)
- [LeetCode 62 Unique Paths](https://leetcode.com/problems/unique-paths/)
- [LeetCode 64 Minimum Path Sum](https://leetcode.com/problems/minimum-path-sum/)
- [LeetCode 70 Climbing Stairs](https://leetcode.com/problems/climbing-stairs/)
- [LeetCode 72 Edit Distance](https://leetcode.com/problems/edit-distance/)
- [LeetCode 75 Sort Colors](https://leetcode.com/problems/sort-colors/)
- [LeetCode 76 Minimum Window Substring](https://leetcode.com/problems/minimum-window-substring/)
- [LeetCode 78 Subsets](https://leetcode.com/problems/subsets/)
- [LeetCode 79 Word Search](https://leetcode.com/problems/word-search/)
- [LeetCode 84 Largest Rectangle in Histogram](https://leetcode.com/problems/largest-rectangle-in-histogram/)
- [LeetCode 85 Maximal Rectangle](https://leetcode.com/problems/maximal-rectangle/)
- [LeetCode 94 Binary Tree Inorder Traversal](https://leetcode.com/problems/binary-tree-inorder-traversal/)
- [LeetCode 96 Unique Binary Search Trees](https://leetcode.com/problems/unique-binary-search-trees/)
- [LeetCode 98 Validate Binary Search Tree](https://leetcode.com/problems/validate-binary-search-tree/)
- [LeetCode 101 Symmetric Tree](https://leetcode.com/problems/symmetric-tree/)
- [LeetCode 102 Binary Tree Level Order Traversal](https://leetcode.com/problems/binary-tree-level-order-traversal/)
- [LeetCode 104 Maximum Depth of Binary Tree](https://leetcode.com/problems/maximum-depth-of-binary-tree/)
- [LeetCode 105 Construct Binary Tree from Preorder and Inorder Traversal](https://leetcode.com/problems/construct-binary-tree-from-preorder-and-inorder-traversal/)
- [LeetCode 114 Flatten Binary Tree to Linked List](https://leetcode.com/problems/flatten-binary-tree-to-linked-list/)
- [LeetCode 121 Best Time to Buy and Sell Stock](https://leetcode.com/problems/best-time-to-buy-and-sell-stock/)
- [LeetCode 124 Binary Tree Maximum Path Sum](https://leetcode.com/problems/binary-tree-maximum-path-sum/)
- [LeetCode 128 Longest Consecutive Sequence](https://leetcode.com/problems/longest-consecutive-sequence/)
- [LeetCode 136 Single Number](https://leetcode.com/problems/single-number/)
- [LeetCode 139 Word Break](https://leetcode.com/problems/word-break/)
- [LeetCode 141 Linked List Cycle](https://leetcode.com/problems/linked-list-cycle/)
- [LeetCode 142 Linked List Cycle II](https://leetcode.com/problems/linked-list-cycle-ii/)
- [LeetCode 146 LRU Cache](https://leetcode.com/problems/lru-cache/)
- [LeetCode 148 Sort List](https://leetcode.com/problems/sort-list/)
- [LeetCode 152 Maximum Product Subarray](https://leetcode.com/problems/maximum-product-subarray/)
- [LeetCode 155 Min Stack](https://leetcode.com/problems/min-stack/)
- [LeetCode 160 Intersection of Two Linked Lists](https://leetcode.com/problems/intersection-of-two-linked-lists/)
- [LeetCode 169 Majority Element](https://leetcode.com/problems/majority-element/)
- [LeetCode 198 House Robber](https://leetcode.com/problems/house-robber/)
- [LeetCode 200 Number of Islands](https://leetcode.com/problems/number-of-islands/)
- [LeetCode 206 Reverse Linked List](https://leetcode.com/problems/reverse-linked-list/)
- [LeetCode 207 Course Schedule](https://leetcode.com/problems/course-schedule/)
- [LeetCode 208 Implement Trie (Prefix Tree)](https://leetcode.com/problems/implement-trie-prefix-tree/)
- [LeetCode 215 Kth Largest Element in an Array](https://leetcode.com/problems/kth-largest-element-in-an-array/)
- [LeetCode 221 Maximal Square](https://leetcode.com/problems/maximal-square/)
- [LeetCode 226 Invert Binary Tree](https://leetcode.com/problems/invert-binary-tree/)
- [LeetCode 234 Palindrome Linked List](https://leetcode.com/problems/palindrome-linked-list/)
- [LeetCode 236 Lowest Common Ancestor of a Binary Tree](https://leetcode.com/problems/lowest-common-ancestor-of-a-binary-tree/)
- [LeetCode 238 Product of Array Except Self](https://leetcode.com/problems/product-of-array-except-self/)
- [LeetCode 239 Sliding Window Maximum](https://leetcode.com/problems/sliding-window-maximum/)
- [LeetCode 240 Search a 2D Matrix II](https://leetcode.com/problems/search-a-2d-matrix-ii/)
- [LeetCode 253 Meeting Rooms II](https://leetcode.com/problems/meeting-rooms-ii/)
- [LeetCode 279 Perfect Squares](https://leetcode.com/problems/perfect-squares/)
- [LeetCode 283 Move Zeroes](https://leetcode.com/problems/move-zeroes/)
- [LeetCode 287 Find the Duplicate Number](https://leetcode.com/problems/find-the-duplicate-number/)
- [LeetCode 297 Serialize and Deserialize Binary Tree](https://leetcode.com/problems/serialize-and-deserialize-binary-tree/)
- [LeetCode 300 Longest Increasing Subsequence](https://leetcode.com/problems/longest-increasing-subsequence/)
- [LeetCode 322 Coin Change](https://leetcode.com/problems/coin-change/)
- [LeetCode 337 House Robber III](https://leetcode.com/problems/house-robber-iii/)
- [LeetCode 338 Counting Bits](https://leetcode.com/problems/counting-bits/)
- [LeetCode 347 Top K Frequent Elements](https://leetcode.com/problems/top-k-frequent-elements/)
- [LeetCode 394 Decode String](https://leetcode.com/problems/decode-string/)
- [LeetCode 399 Evaluate Division](https://leetcode.com/problems/evaluate-division/)
- [LeetCode 406 Queue Reconstruction by Height](https://leetcode.com/problems/queue-reconstruction-by-height/)
- [LeetCode 416 Partition Equal Subset Sum](https://leetcode.com/problems/partition-equal-subset-sum/)
- [LeetCode 437 Path Sum III](https://leetcode.com/problems/path-sum-iii/)
- [LeetCode 438 Find All Anagrams in a String](https://leetcode.com/problems/find-all-anagrams-in-a-string/)
- [LeetCode 448 Find All Numbers Disappeared in an Array](https://leetcode.com/problems/find-all-numbers-disappeared-in-an-array/)
- [LeetCode 461 Hamming Distance](https://leetcode.com/problems/hamming-distance/)
- [LeetCode 494 Target Sum](https://leetcode.com/problems/target-sum/)
- [LeetCode 538 Convert BST to Greater Tree](https://leetcode.com/problems/convert-bst-to-greater-tree/)
- [LeetCode 543 Diameter of Binary Tree](https://leetcode.com/problems/diameter-of-binary-tree/)
- [LeetCode 560 Subarray Sum Equals K](https://leetcode.com/problems/subarray-sum-equals-k/)
- [LeetCode 581 Shortest Unsorted Continuous Subarray](https://leetcode.com/problems/shortest-unsorted-continuous-subarray/)
- [LeetCode 617 Merge Two Binary Trees](https://leetcode.com/problems/merge-two-binary-trees/)
- [LeetCode 621 Task Scheduler](https://leetcode.com/problems/task-scheduler/)
- [LeetCode 647 Palindromic Substrings](https://leetcode.com/problems/palindromic-substrings/)
- [LeetCode 739 Daily Temperatures](https://leetcode.com/problems/daily-temperatures/)

## Bjarne Stroustrup's FAQ
### General
- [What's so great about classes?](https://www.stroustrup.com/bs_faq.html#class)
- [What is "OOP" and what's so great about it?](https://www.stroustrup.com/bs_faq.html#oop)
- [What is "generic programming" and what's so great about it?](https://www.stroustrup.com/bs_faq.html#generic)
- [What is C++?](https://www.stroustrup.com/bs_faq.html#what-is)
- [Why does C++ allow unsafe code?](https://www.stroustrup.com/bs_faq.html#unsafe)
- [What is "multiparadigm programming"?](https://www.stroustrup.com/bs_faq.html#multiparadigm)
- [Is C++ in decline?](https://www.stroustrup.com/bs_faq.html#decline)
- [What's being done to improve C++?](https://www.stroustrup.com/bs_faq.html#improve)
- [Is it true that ...?](https://www.stroustrup.com/bs_faq.html#true)

### Learning C++
- [What is the best book to learn C++ from?](https://www.stroustrup.com/bs_faq.html#best-book)
- [How long does it take to learn C++?](https://www.stroustrup.com/bs_faq.html#How-long)
- [Knowing C is a prerequisite for learning C++, right?](https://www.stroustrup.com/bs_faq.html#prerequisite)
- [Should I learn a pure OO language before C++ to become a real OO programmer?](https://www.stroustrup.com/bs_faq.html#learn-pure)
- [How do I start learning C++?](https://www.stroustrup.com/bs_faq.html#how-to-start)
- [Will you help me with my homework?](https://www.stroustrup.com/bs_faq.html#homework)
- [Where can I get a free C++ compiler?](https://www.stroustrup.com/bs_faq.html#free)
- [What's the best way to improve my C++ programs?](https://www.stroustrup.com/bs_faq.html#improve-my-C++-programs)
- [Does it matter which programming language I use?](https://www.stroustrup.com/bs_faq.html#which-programming-language)
- [Where can I learn about the background of C++?](https://www.stroustrup.com/bs_faq.html#background)

### Standardization
- [Did the ANSI/ISO standards committee spoil C++?](https://www.stroustrup.com/bs_faq.html#spoil-C++)
- [When will we have a C++ standard?](https://www.stroustrup.com/bs_faq.html#When-standard)
- [Where can I get a machine-readable version of the standard?](https://www.stroustrup.com/bs_faq.html#machine-readable-standard)
- [Are there any features you'd like to remove from C++?](https://www.stroustrup.com/bs_faq.html#remove-from-C++)
- [Why doesn't C++ have garbage collection?](https://www.stroustrup.com/bs_faq.html#garbage-collection)
- [Why doesn't C++ have a GUI?](https://www.stroustrup.com/bs_faq.html#gui)
- [Why doesn't C++ support threads?](https://www.stroustrup.com/bs_faq.html#threads)
- [What is the difference between C++98 and C++14?](https://www.stroustrup.com/bs_faq.html#C++03)
- [What will the next standard look like?](https://www.stroustrup.com/bs_faq.html#When-next-standard)

### Books
- [When will you publish a 4th edition of "The C++ Programming Language"?](https://www.stroustrup.com/bs_faq.html#4th)
- [Do you like e-books?](https://www.stroustrup.com/bs_faq.html#e-books)
- [Where do I find free machine-readable copies of your books?](https://www.stroustrup.com/bs_faq.html#machinereadable)
- [What's the difference between the "TC++PL" and "Programming" books?](https://www.stroustrup.com/bs_faq.html#3rd-programming)

### Other languages
- [Is Java the language you would have designed if you didn't have to be compatible with C?](https://www.stroustrup.com/bs_faq.html#Java)
- [What do you think of C#?](https://www.stroustrup.com/bs_faq.html#Csharp)
- [What do you think of C++/CLI?](https://www.stroustrup.com/bs_faq.html#CppCLI)
- [What do you think of EC++?](https://www.stroustrup.com/bs_faq.html#EC++)
- [C++ got its Object-Oriented concepts from Smalltalk?](https://www.stroustrup.com/bs_faq.html#from-Smalltalk)
- [Do you really recommend Ada over C++ for larger projects?](https://www.stroustrup.com/bs_faq.html#Ada)
- [Would you compare C++ to "some language"?](https://www.stroustrup.com/bs_faq.html#compare)
- [Others do compare their languages to C++; doesn't that annoy you?](https://www.stroustrup.com/bs_faq.html#Others-do-compare)
- [You won't compare C++ to other languages, but you write diatribes about C++?](https://www.stroustrup.com/bs_faq.html#diatribes)
- [How can a legacy language like C++ compete with modern, advanced languages?](https://www.stroustrup.com/bs_faq.html#advanced)
- [Why are you so keen on portability?](https://www.stroustrup.com/bs_faq.html#portability)

### C and C++
- [C is better than C++ for small projects, right?](https://www.stroustrup.com/bs_faq.html#C-is-better)
- [Is C a subset of C++?](https://www.stroustrup.com/bs_faq.html#C-is-subset)
- [What is the difference between C and C++?](https://www.stroustrup.com/bs_faq.html#difference)
- [Do you really think that C and C++ could be merged into a single language?](https://www.stroustrup.com/bs_faq.html#merge)
- [What do you think of C/C++?](https://www.stroustrup.com/bs_faq.html#C-slash)
- [Why is the code generated for the "Hello world" program ten times larger for C++ than for C?](https://www.stroustrup.com/bs_faq.html#Hello-world)
- [Why did you make C++ (almost) compatible with C?](https://www.stroustrup.com/bs_faq.html#whyC)

### History of C++
- [When was C++ invented?](https://www.stroustrup.com/bs_faq.html#invention)
- [Why did you invent C++?](https://www.stroustrup.com/bs_faq.html#why)
- [Why did AT&T support the development of C++?](https://www.stroustrup.com/bs_faq.html#why-ATT)
- [Do you own C++?](https://www.stroustrup.com/bs_faq.html#revenues)
- [Where did the name "C++" come from?](https://www.stroustrup.com/bs_faq.html#name)
- [Which language did you use to write C++?](https://www.stroustrup.com/bs_faq.html#bootstrapping)
- [Did you really not understand what you were doing?](https://www.stroustrup.com/bs_faq.html#understand)

### Etc. C++ questions
- [Why is C++ so BIG?](https://www.stroustrup.com/bs_faq.html#big)
- [Is C++ an Object-Oriented language?](https://www.stroustrup.com/bs_faq.html#Object-Oriented-language)
- [What is "legacy code"?](https://www.stroustrup.com/bs_faq.html#legacy)
- [Is the number of C++ users still doubling every year?](https://www.stroustrup.com/bs_faq.html#number-of-C++-users)
- [Does anyone use C++ these days?](https://www.stroustrup.com/bs_faq.html#use-C++)
- [Why isn't C++ used for Operating Systems?](https://www.stroustrup.com/bs_faq.html#use-C++-for-OS)
- [What do you think of Boost?](https://www.stroustrup.com/bs_faq.html#boost)
- [What do you think of template metaprogramming?](https://www.stroustrup.com/bs_faq.html#metaprogramming)
- [Did you expect C++ to become such a success?](https://www.stroustrup.com/bs_faq.html#C++success)
- [What's a good certification for C++ programmers?](https://www.stroustrup.com/bs_faq.html#certification)
- [What C++ compiler do you recommend? Which libraries?](https://www.stroustrup.com/bs_faq.html#recommend)
- [Are lists evil?](https://www.stroustrup.com/bs_faq.html#list)

### Personal
- [How do you pronounce "Bjarne Stroustrup"?](https://www.stroustrup.com/bs_faq.html#pronounce)
- [Can I ask you a question?](https://www.stroustrup.com/bs_faq.html#ask)
- [Why don't you answer your email?](https://www.stroustrup.com/bs_faq.html#email)
- [Why don't you make your website look modern?](https://www.stroustrup.com/bs_faq.html#looks)
- [Is "bjarne" an impostor?](https://www.stroustrup.com/bs_faq.html#impostor)
- [You are Swedish?](https://www.stroustrup.com/bs_faq.html#Swedish)
- [Did you really say that?](https://www.stroustrup.com/bs_faq.html#really-say-that)
- [Did you really give an interview to IEEE?](https://www.stroustrup.com/bs_faq.html#IEEE)
- [Why did you go to work at Morgan Stanley?](https://www.stroustrup.com/bs_faq.html#morgan)
- [Why did you go to work at Texas A&M University?](https://www.stroustrup.com/bs_faq.html#tamu)
- [Why did you go to work at Bell labs?](https://www.stroustrup.com/bs_faq.html#btl)
- [What are you working on now?](https://www.stroustrup.com/bs_faq.html#working-on-now)

## Resource Declaration

This repository is created solely for personal learning, organization, and non-commercial sharing purposes. All materials, links, and code snippets collected herein are sourced from publicly available resources on the Internet.

All resources are intended **exclusively for study and exchange** and must not be used for any commercial purposes.

Copyright of all content remains with the original authors or respective platforms. The maintainer of this repository claims no ownership or copyright over the included materials.

If any original author or copyright holder believes that a link or resource has been included inappropriately, please contact me via GitHub Issues or email. I will remove the relevant content or links immediately upon notification.

Special thanks to all the generous contributors and authors across the Internet — it is because of your openly shared knowledge that more people can learn C++ efficiently and at low cost!
