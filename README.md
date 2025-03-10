# compiler
learn compiler

# Todo list

## LLVM

- [ ] [My First Frontend](https://llvm.org/docs/tutorial/MyFirstLanguageFrontend/index.html)
- [ ] Clang Frontend
- [ ] Clang Static Analysis
- [ ] IR
- [ ] MLIR
- [ ] JIT

## Clang

- [ ] Clang Preprocessor
    - [ ] Lexer
        - 负责将源代码解析为 Token 流，供后续阶段使用。
    - [ ] Macro Processor
        - 处理 `#define`、`#undef`、`#pragma` 等预处理指令，实现宏展开与替换。
    - [ ] Conditional Compilation
        - 解析 `#if`、`#ifdef`、`#ifndef`、`#else`、`#elif`、`#endif` 语句，控制代码的编译行为。
    - [ ] Include Handling
        - 处理 `#include` 指令，管理头文件的搜索路径、文件依赖和文件缓存优化。

- [ ] Clang Sema
    - [ ] Name Lookup
        - 解析变量、函数、类和命名空间作用域中的标识符，确保正确解析符号。
    - [ ] Type Checking
        - 进行类型推导、类型转换（隐式与显式）及类型兼容性检查。
    - [ ] Overload Resolution
        - 处理函数、运算符重载，选择最合适的重载版本。
    - [ ] Template Instantiation
        - 解析和实例化 C++ 模板，展开泛型代码，提高编译器优化能力。
    - [ ] Semantic Error Handling
        - 检测并报告语义错误，提供恢复机制，避免编译过程崩溃。

- [ ] Clang Diagnostics
    - [ ] Diagnostic Engine
        - 统一管理错误、警告和提示信息的收集与输出。
    - [ ] Diagnostic Consumers
        - 负责接收、格式化和展示诊断信息，如终端输出、IDE 提示或日志文件记录。
    - [ ] Diagnostic Messages & IDs
        - 维护错误与警告的唯一标识符，确保一致性和可追溯性。
    - [ ] Fix-it Hints
        - 为部分错误提供自动修复方案，例如变量未声明时自动添加 `#include` 头文件。
    - [ ] Extensible Diagnostics
        - 允许自定义诊断规则，扩展 Clang 对特定代码风格或 API 误用的检测能力。

- [ ] Clang LibTooling
    - [ ] AST Traversal & Matching
        - 使用 `RecursiveASTVisitor` 和 AST Matcher 提取特定的 AST 结构，实现静态分析。
    - [ ] Source Rewriting
        - 通过 `Rewriter` 修改源代码，实现代码自动转换和重构。
    - [ ] Source Manager
        - 维护源码文件、文件偏移、位置映射，为分析工具提供高效索引。
    - [ ] Clang Tooling Framework
        - 提供开发工具（如 Clang-Tidy、Clang-Format）的基础设施，支持代码分析和格式化。
    - [ ] Plugin and Extension Development
        - 允许开发者基于 LibTooling 构建自定义插件，实现代码检查、重构和转换工具。
