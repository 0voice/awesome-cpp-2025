# C++ High-Frequency Interview Questions
[中文版](https://github.com/0voice/awesome-modern-cpp-2025/blob/main/interview_questions/README.md)
## Table of Contents
[Language Basics](#language-basics)  
[Object-Oriented Programming](#object-oriented-programming)  
[Memory Management](#memory-management)  
[STL and Containers](#stl-and-containers)   
[Modern C++ Features](#modern-c-features)  
[Multithreading and Concurrency](#multithreading-and-concurrency)  
[Network Programming](#network-programming)  
[Coding Exercises](#coding-exercises)  

## Language Basics

### The Role of the `static` Keyword
- Modifies ordinary variables: Extends lifetime to program termination, stored in static storage area, initialized only once.
- Modifies ordinary functions/global variables: Restricts symbol to internal linkage, visible only within the translation unit.
- Modifies class data members: Shared by all objects, belongs to the class rather than individual objects.
- Modifies class member functions: No `this` pointer, can only access static members.

### The Role of the `const` Keyword
- Modifies variables as read-only.
- Modifies pointers to form top-level const (pointer itself immutable) and bottom-level const (pointed object immutable).
- Modifies member functions: Promises not to modify member variables, callable by const objects.
- Modifies references: Often used for function parameters to avoid copying and prevent modification.
- `constexpr` (since C++11): Indicates a compile-time constant.

### Differences Between `inline` Functions and Macros
- `inline` functions support type checking, scope control, and debugging.
- Macros are preprocessor text replacements, lacking type checking, prone to side effects, and non-debuggable.
- `inline` functions can take addresses; macros cannot.
- Modern C++ recommends `inline` or `constexpr` functions instead of macros.

### The Role of the `explicit` Keyword
- Modifies single-parameter constructors to prohibit implicit type conversion.
- Allows only explicit construction to prevent unintended type conversion errors.

### Differences Between `nullptr` and `NULL`
- `NULL` is a macro, usually defined as `0` or `(void*)0`.
- `nullptr` is a dedicated null pointer constant of type `std::nullptr_t` introduced in C++11.
- `nullptr` is type-safe and avoids ambiguity with integer overloading.

### Differences Between `sizeof` and `strlen`
- `sizeof` is a compile-time operator that returns the number of bytes occupied by a type or object.
- `strlen` is a runtime function that returns the number of characters in a C-style string before `\0`.
- `sizeof` does not decay arrays; `strlen` requires a `char*` parameter.

### Differences Between `new` and `malloc`
- `new` is a C++ operator; `malloc` is a C standard library function.
- `new` automatically calculates size and calls constructors; `malloc` requires manual byte count.
- `new` returns a correctly typed pointer; `malloc` returns `void*`.
- `new` can be overloaded; `malloc` cannot.
- `new` throws `std::bad_alloc` on failure; `malloc` returns `NULL`.

### Differences Between `delete` and `delete[]`
- `delete` is used for single objects allocated with `new`.
- `delete[]` is used for arrays allocated with `new[]`, calling destructors of each element in reverse order.
- Mixing them causes undefined behavior (especially for classes with non-trivial destructors).

### Four Types of Cast Conversions
- `static_cast`: Basic type conversion, class hierarchy up/down casting (no runtime check), `void*` conversion.
- `const_cast`: Removes or adds `const`/`volatile` qualifiers.
- `reinterpret_cast`: Arbitrary pointer type conversion, pointer-integer conversion (most dangerous).
- `dynamic_cast`: Type-safe downcasting in polymorphic class hierarchies, returns `nullptr` or throws an exception on failure.

### The Entire Process of C++ Program Compilation and Linking
- Preprocessing: Macro expansion, `#include` expansion, conditional compilation → `.i` file.
- Compilation: Generates assembly code → `.s` file.
- Assembly: Converts assembly code to object file → `.o`/`.obj` file.
- Linking: Symbol resolution, address relocation, merging multiple object files and libraries → executable file.

### Differences Between `struct` and `class`
- The only difference is default access control: `struct` defaults to `public`, `class` defaults to `private`.
- Default inheritance access also differs: `struct` uses public inheritance by default, `class` uses private inheritance.

### Differences Between C and C++
- C is a procedural language; C++ is a multi-paradigm language supporting OOP and generic programming.
- C++ has classes, inheritance, polymorphism, templates, exception handling, and the STL.
- C++ enforces stricter type checking and disallows implicit `void*` conversion.
- C++ supports function overloading, references, `new`/`delete`, and namespaces.

### The Role of the `volatile` Keyword
- Tells the compiler the variable may be modified unexpectedly by external factors (e.g., hardware, interrupts, other threads).
- Prohibits compiler optimizations for access to the variable (e.g., register caching).
- Commonly used in embedded systems, device drivers, signal processing, and multi-threaded status flags.

## Object-Oriented Programming

### How is Polymorphism Implemented? Do You Understand Virtual Function Tables?
- Runtime polymorphism is implemented via virtual function tables (vtables).
- Each class with virtual functions has a unique vtable.
- Objects contain a vptr pointer (usually at the start) pointing to the class's vtable.
- Calling a virtual function involves looking up the function address via vptr → vtable for dynamic binding.

### Why Must the Base Class Destructor Be Virtual?
- When deleting a derived class object via a base class pointer/reference, a non-virtual base destructor only calls the base class destructor.
- This causes incomplete destruction of the derived class and resource leaks.
- The base class destructor must be `virtual` if there's any possibility of deleting via a base class pointer.

### Can Constructors Be Virtual? Can Destructors Be Pure Virtual?
- Constructors cannot be virtual: The vptr is initialized during constructor execution, making dynamic binding impossible.
- Destructors can be pure virtual but must provide a definition (the base destructor is still called).

### Differences Between Overloading, Overriding, and Redefinition
- Overloading: Same function name, different parameter lists in the same scope.
- Overriding: Derived class virtual function has an identical signature to a base class virtual function (explicitly marked with `override` since C++11).
- Redefinition (hiding): Derived class defines a non-virtual function with the same name, hiding all base class functions of that name.

### Differences Between Copy Constructors and Assignment Operator Overloading
- Copy constructor: Initializes a new object from an existing one (creation from scratch).
- Assignment operator: Overwrites an existing object with another existing object.
- Copy constructor parameters must be references; the assignment operator returns a `*this` reference to support chaining.

### Differences Between Deep Copy and Shallow Copy
- Shallow copy: Copies only pointer values, with multiple objects pointing to the same memory.
- Deep copy: Copies the content pointed to by pointers, allocating independent memory for each object.
- Shallow copy risks double free; deep copy is safe but has higher overhead.

### Rule of Three / Rule of Five
- Rule of Three: If a class requires a custom destructor, copy constructor, or copy assignment operator, all three should be customized.
- Rule of Five: Extends the Rule of Three with move constructor and move assignment operator (since C++11), all five are typically needed if any is customized.

### The `final` and `override` Keywords
- `override`: Explicitly indicates the function intends to override a base class virtual function (compiler checks validity).
- `final`: Modifies virtual functions to prevent further overriding; modifies classes to prevent inheritance.

### Why Can't Constructors Be Virtual?
- Virtual functions rely on vptr and vtable, but the vptr is initialized only during constructor execution.
- A virtual constructor would have no valid vtable to look up, making dynamic dispatch impossible.

### Differences Between Pure Virtual Functions and Virtual Functions
- Virtual functions have implementations (default provided) and can be overridden.
- Pure virtual functions have no implementation (`= 0`); classes containing them are abstract and cannot be instantiated.
- Pure virtual functions force derived classes to provide an implementation.

### Differences Between Abstract Classes and Interfaces
- Abstract classes: Contain pure virtual functions, may have data members and non-pure virtual functions.
- Interfaces (typically pure abstract classes in C++): No data members or implementations, representing "capabilities".

### The Role of the `friend` Keyword
- Breaks encapsulation to allow specified functions or classes to access `private`/`protected` members.
- Commonly used for operator overloading, global functions, and interactions between related classes.

### How to Prevent a Class from Being Inherited in C++?
- C++11: Mark the class with `final`.
- C++03: Declare the destructor as `private`, or use the "friend + virtual inheritance" trick.

## Memory Management

### C++ Memory Partitions
- Code segment (text), constant area, static/global area, BSS segment, heap, stack.

### Differences Between Heap and Stack
- Stack: Automatically managed, contiguous memory, fast access, size-limited.
- Heap: Manually managed (via `new`/`delete`), dynamic allocation, prone to fragmentation, theoretically limited by virtual memory.

### How to Detect and Locate Memory Leaks?
- Linux: `valgrind`, `AddressSanitizer` (`-fsanitize=address`), `mtrace`.
- Windows: Visual Studio Diagnostic Tools, CRT Debug Heap.
- General: Smart pointers + RAII, regular code reviews.

### What Are Wild Pointers and Dangling Pointers? How to Avoid Them?
- Wild pointers: Pointers to invalid memory (uninitialized or deleted).
- Dangling pointers: Pointers to memory that has been freed.
- Avoidance: Initialize to `nullptr`, set to `nullptr` after `delete`, use smart pointers.

### RAII Principle
- Resource Acquisition Is Initialization.
- Binds resource management to object lifetime: Acquire resources in the constructor, release in the destructor.
- Leverages automatic stack object destruction to ensure exception safety.

### What Smart Pointers Do You Know?
- `unique_ptr`: Exclusive ownership, non-copyable, movable.
- `shared_ptr`: Shared ownership, reference-counted.
- `weak_ptr`: Solves `shared_ptr` circular references, non-owning.

### Implementation Principle of `shared_ptr`? How to Solve Circular References?
- Control block contains strong reference count, weak reference count, and deleter.
- Strong reference count increments on copy and decrements on destructor; resources are freed when it reaches 0.
- Circular reference: Class A contains `shared_ptr<B>`, class B contains `shared_ptr<A>`, preventing reference counts from reaching 0.
- Solution: Replace one side of the circle with `weak_ptr`.

### Can `unique_ptr` Be Copied?
- By default, `unique_ptr` is non-copyable (copy constructor and assignment operator are deleted).
- Ownership can be transferred via `std::move`, leaving the original pointer as `nullptr`.

### Principle of `weak_ptr` in Solving Circular References
- `weak_ptr` does not increment the strong reference count.
- `lock()` attempts to promote it to a `shared_ptr`; returns a null `shared_ptr` if the resource has been freed.

### Memory Alignment Rules
- The compiler pads members to ensure each member's address is an integer multiple of its alignment value.
- The total size of a struct is an integer multiple of the largest alignment value among its members.
- Purpose: Improve CPU read efficiency (avoid cross-cache-line access).

## STL and Containers

### Underlying Implementation and Expansion Mechanism of `vector`
- Contiguous memory, dynamic array.
- Typically expands to 1.5x or 2x the current capacity when full (implementation-dependent).
- Expansion involves reallocating memory, moving elements, and invalidating all iterators.

### What Are the Scenarios of Iterator Invalidation?
- `vector`/`deque`: Insertion causing expansion, deletion causing element shifting.
- `string` expansion.
- Associative containers: Only the iterator to the deleted node is invalidated; others remain valid.

### Differences Between `map` and `unordered_map`? When to Use Which?
- `map`: Red-black tree, ordered, O(log n) time complexity, supports range queries.
- `unordered_map`: Hash table, unordered, average O(1) time complexity.
- Use `map` for ordered requirements or `lower_bound`; use `unordered_map` for maximum performance with unordered data.

### How to Resolve Hash Collisions in `unordered_map`?
- Mainstream implementation uses separate chaining (each bucket has a linked list).
- Rehashes and expands when the load factor is too high.

### Underlying Implementation of `set` and `map`
- Both are implemented with red-black trees.
- `set` uses keys as values; `map` stores `pair<const Key, T>` as values.

### Differences Between `emplace_back` and `push_back`
- `push_back`: Accepts pre-constructed objects, involving at least one copy or move.
- `emplace_back`: Constructs objects in-place by forwarding parameters to the constructor, theoretically more efficient.

### Common STL Algorithms
- Non-modifying algorithms: `find`, `count`, `for_each`, `transform`.
- Modifying algorithms: `sort`, `remove`, `unique`, `partition`.
- Numeric algorithms: `accumulate`, `inner_product`.

### Differences Between `list` and `vector`
- `list`: Doubly linked list, non-contiguous memory, O(1) insertion/deletion, O(n) random access.
- `vector`: Contiguous array, O(1) random access, fast tail insertion, slow middle insertion.

### Six Major Components of STL
- Containers
- Allocators
- Algorithms
- Iterators
- Functors (Function Objects)
- Adapters

### Differences Between Red-Black Trees and AVL Trees
- AVL trees: Strictly balanced (height difference ≤ 1), faster lookups, more rotations during insertion/deletion.
- Red-black trees: Approximate balance (relaxed balance conditions), more efficient insertion/deletion, widely used in STL.

## Modern C++ Features

### Several Most Important New Features of C++11
- `auto`, `decltype`, rvalue references, move semantics, smart pointers, lambdas, `nullptr`, `override`/`final`, `constexpr`, uniform initialization, variadic templates.

### Move Semantics and Perfect Forwarding
- Move semantics: "Steals" resources instead of copying, suitable for temporary objects.
- Perfect forwarding: Preserves the lvalue/rvalue nature of parameters when passing them to another function.

### The Role of `std::move`
- Unconditionally converts an lvalue to an rvalue reference.
- Does not move data itself; only forces move semantics to be triggered.

### The Role of `std::forward`
- Converts parameters to rvalues only if they are rvalue references (core of perfect forwarding).

### Underlying Implementation of Lambda Expressions
- The compiler generates an anonymous class type and overloads `operator()`.
- Capture lists become class member variables, initialized by the constructor.

### The Role of `noexcept`
- Declares that a function will not throw exceptions.
- Enables more aggressive compiler optimizations (e.g., move constructors with `noexcept` provide strong exception safety).
- Violating `noexcept` directly calls `std::terminate()` during exception propagation.

### Differences Between `auto` and `decltype`
- `auto`: Deduces variable type from the initializer, ignoring top-level `const` and references.
- `decltype`: Deduces the type of an expression, preserving `const` and references.

### Differences Between Rvalue References and Lvalue References
- Lvalue references: Bind to lvalues (named entities).
- Rvalue references: Bind to rvalues (temporaries, xvalues).
- Rvalue references extend the lifetime of temporary objects and enable move semantics.

## Multithreading and Concurrency

### Implementation Principle of `std::atomic`? Is `a++` an Atomic Operation?
- `std::atomic` uses CPU atomic instructions (e.g., `lock` prefix, `cmpxchg`) or compiler intrinsics.
- `a++` is not atomic; it involves read-modify-write three steps.
- Use `a.fetch_add(1)` or the atomic version of `a++` instead.

### Four Conditions for Deadlock? How to Avoid It?
- Mutual exclusion, hold and wait, no preemption, circular wait.
- Avoidance: Lock in a fixed order, hold locks for the shortest time possible, use `std::lock`, implement timeout mechanisms.

### How to Write a Thread-Safe Singleton?
- Simplest way since C++11: Static local variable (`static Singleton instance;`), inherently thread-safe.
- Double-checked locking + `volatile` (pre-C++11).
- `std::call_once` + `std::once_flag`.

### How to Use `mutex` and `condition_variable` Together?
- `mutex` protects shared data.
- `condition_variable` enables thread waiting/notification.
- Typical pattern: `while (condition not met) wait(lock);` wake with `notify_one()`/`notify_all()`.

### What Are the Thread Synchronization Methods?
- `mutex`, `condition_variable`, `atomic`, `semaphore` (C++20), `barrier` (C++20), `latch` (C++20), `futex` (low-level).

### Differences Between Processes and Threads
- Processes have independent address spaces; threads share the process's address space.
- Process context switching has higher overhead; thread switching is faster.
- A process crash does not affect other processes, but a thread crash may cause the entire process to exit.

## Network Programming

### Differences Between TCP and UDP? Application Scenarios?
#### Core Differences
1. TCP: Connection-oriented, reliable transmission (no loss/duplication/out-of-order), flow/congestion control, large header overhead, byte stream.
2. UDP: Connectionless, best-effort delivery (possible loss/out-of-order), no control mechanisms, small header overhead, datagram (preserves message boundaries).

#### Application Scenarios
1. TCP: File transfer, web access, payment transactions, database connections, and other scenarios requiring reliability.
2. UDP: Live streaming/video calls, online games, DNS resolution, and other scenarios requiring real-time performance/low overhead.

### Differences and Principles of `select`, `poll`, and `epoll`
- `select`: Uses `fd_set` bitmaps, O(n) scanning, limited number of file descriptors (usually 1024).
- `poll`: Uses `pollfd` arrays, O(n) scanning, no limit on the number of file descriptors.
- `epoll`: Event-driven, kernel maintains a red-black tree + ready list, O(1) return of ready events, supports level-triggered/edge-triggered modes.

### What Are Sticky Packets and Packet Fragmentation? How to Solve Them?
- TCP is a byte stream protocol: Multiple `send` calls may be merged (sticky packets), and one `send` may be split (packet fragmentation).
- Solutions: Custom application-layer protocols (e.g., message length prefix, fixed-length messages, delimiters).

### TCP Three-Way Handshake and Four-Way Wave
#### Three-Way Handshake
1. The client sends a synchronization packet (SYN packet) to the server, indicating a connection request, and then enters the SYN_SENT state.
2. After receiving the request, the server replies with a synchronization + acknowledgment packet (SYN+ACK packet), confirming the client's request and synchronizing its own sequence number, then enters the SYN_RCVD state.
3. After receiving the server's reply, the client sends an acknowledgment packet (ACK packet) to confirm receipt of the synchronization information. Both the client and server enter the ESTABLISHED state, and the connection is officially established.
Core Purpose: Verify that both parties' sending and receiving capabilities are normal, avoiding invalid connections caused by network delays.

#### Four-Way Wave
1. The party initiating the connection closure (client or server) sends a finish packet (FIN packet) to the other party, indicating it will no longer send data and requesting a connection closure, then enters the FIN_WAIT_1 state.
2. After receiving the finish packet, the passive closing party sends an acknowledgment packet (ACK packet) to notify the initiator of receipt, enters the CLOSE_WAIT state, and the initiator enters the FIN_WAIT_2 state upon receiving the acknowledgment.
3. After sending all remaining data, the passive closing party sends a finish packet (FIN packet) to indicate no more data will be sent, requests a connection closure, and enters the LAST_ACK state.
4. After receiving the passive party's finish packet, the initiator sends an acknowledgment packet (ACK packet) to confirm the closure, enters the TIME_WAIT state (waits for 2MSL to ensure the passive party receives the acknowledgment), and both parties finally close the connection.
Core Purpose: Ensure both parties have sent and received all data, avoiding data loss during connection closure.

## Coding Exercises

### Implement a Thread-Safe Singleton
Core: Static local variable initialization in C++11 is inherently thread-safe; prohibit copy/assignment to ensure a single instance.
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

### Implement LRU Cache
Core: Hash table (O(1) lookup) + doubly linked list (O(1) insertion/deletion); head stores recently used items, tail stores least recently used items.
```cpp
#include <unordered_map>
#include <list>
using namespace std;

class LRUCache {
    int cap;
    list<pair<int, int>> cacheList; // (key, val) to maintain access order
    unordered_map<int, list<pair<int, int>>::iterator> cacheMap; // key → iterator
public:
    LRUCache(int capacity) : cap(capacity) {}
    int get(int key) {
        if (!cacheMap.count(key)) return -1;
        // Move hit item to head (recently used)
        cacheList.splice(cacheList.begin(), cacheList, cacheMap[key]);
        return cacheMap[key]->second;
    }
    void put(int key, int value) {
        if (cacheMap.count(key)) {
            // Update value and move to head if key exists
            cacheMap[key]->second = value;
            cacheList.splice(cacheList.begin(), cacheList, cacheMap[key]);
            return;
        }
        // Add new item to head
        cacheList.emplace_front(key, value);
        cacheMap[key] = cacheList.begin();
        // Remove tail (least recently used) if capacity is exceeded
        if (cacheList.size() > cap) {
            cacheMap.erase(cacheList.back().first);
            cacheList.pop_back();
        }
    }
};
```

### Implement Quicksort
Core: Divide-and-conquer; select a pivot, partition the array (elements smaller than pivot on left, larger on right), recursively sort left and right subarrays.
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
    swap(nums[l], nums[i]); // Place pivot in correct position
    return i;
}
void quickSort(vector<int>& nums, int l, int r) {
    if (l >= r) return;
    int pivotIdx = partition(nums, l, r);
    quickSort(nums, l, pivotIdx - 1);
    quickSort(nums, pivotIdx + 1, r);
}
```

### Implement Mergesort
Core: Divide-and-conquer + merge; split the array into subarrays, recursively sort them, then merge two sorted subarrays (stable sort).
```cpp
#include <vector>
using namespace std;

void merge(vector<int>& nums, int l, int mid, int r) {
    vector<int> temp(r - l + 1);
    int i = l, j = mid + 1, k = 0;
    // Merge two sorted subarrays
    while (i <= mid && j <= r) {
        temp[k++] = nums[i] <= nums[j] ? nums[i++] : nums[j++];
    }
    // Copy remaining elements
    while (i <= mid) temp[k++] = nums[i++];
    while (j <= r) temp[k++] = nums[j++];
    // Write back to original array
    for (int p = 0; p < temp.size(); p++) nums[l + p] = temp[p];
}
void mergeSort(vector<int>& nums, int l, int r) {
    if (l >= r) return;
    int mid = l + (r - l) / 2; // Avoid overflow
    mergeSort(nums, l, mid);
    mergeSort(nums, mid + 1, r);
    merge(nums, l, mid, r);
}
```

### Implement String Reversal
Core: Two pointers moving towards each other, swapping characters in-place (O(n) time, O(1) space).
```cpp
#include <string>
#include <algorithm>
using namespace std;

void reverseString(string& s) {
    int l = 0, r = s.size() - 1;
    while (l < r) swap(s[l++], s[r--]);
}
```

### Implement Two Sum
Core: Use a hash table to store indices of traversed values, O(n) time to find the complement (target - current value).
```cpp
#include <vector>
#include <unordered_map>
using namespace std;

vector<int> twoSum(vector<int>& nums, int target) {
    unordered_map<int, int> numMap; // key: value, value: index
    for (int i = 0; i < nums.size(); i++) {
        int complement = target - nums[i];
        if (numMap.count(complement)) return {numMap[complement], i};
        numMap[nums[i]] = i;
    }
    return {}; // Problem guarantees a solution, can be omitted
}
```
