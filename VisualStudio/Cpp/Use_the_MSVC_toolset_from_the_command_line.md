# 通过命令行使用 MSVC 工具集

在开发人员命令提示下，输入以下命令来编译程序：

```powershell
cl /EHsc hello.cpp
```

cl.exe 编译器会生成包含已编译代码的 hello.obj 文件，然后运行链接器来创建名为 hello.exe 的可执行程序。若要运行 hello.exe 程序，请在命令提示处输入 hello.exe 。

`/EHsc` 命令行选项指示编译器启用标准 C++ 异常处理行为。 如果没有它，则引发的异常可能导致未受损对象和资源泄漏。 有关详细信息，请参阅 [/EH（异常处理模型）](https://docs.microsoft.com/zh-cn/cpp/build/reference/eh-exception-handling-model?view=msvc-160)。

若要编译包含其他源代码文件的程序，请在命令行上将它们全部输入：

```powershell
cl /EHsc file1.cpp file2.cpp file3.cpp
```

提供其他源文件时，编译器会使用第一个输入文件创建程序名。 在本例中，编译器输出一个名为 file1.exe 的程序。 若要将名称更改为 program1.exe，请添加 [/out](https://docs.microsoft.com/zh-cn/cpp/build/reference/out-output-file-name?view=msvc-160) 链接器选项：

```powershell
cl /EHsc file1.cpp file2.cpp file3.cpp /link /out:program1.exe
```

若要自动捕获更多编程错误，我们建议使用 [/W3](https://docs.microsoft.com/zh-cn/cpp/build/reference/compiler-option-warning-level?view=msvc-160) 或 [/W4](https://docs.microsoft.com/zh-cn/cpp/build/reference/compiler-option-warning-level?view=msvc-160) 警告级别选项进行编译：

```powershell
cl /W4 /EHsc file1.cpp file2.cpp file3.cpp /link /out:program1.exe
```

编译器 cl.exe 还有很多选项。 可以应用这些选项来生成、优化、调试和分析你的代码。 如需快速列表，请在开发人员命令提示下输入 `cl /?`。 你还可以单独编译和链接，并在更复杂的生成方案中应用链接器选项。 有关编译器和链接器选项及用法的详细信息，请参阅 [C/C++ 生成参考](https://docs.microsoft.com/zh-cn/cpp/build/reference/c-cpp-building-reference?view=msvc-160)。

C 和 C++ 语言相似，但并不相同。 MSVC 编译器使用一个简单的规则来确定在编译代码时使用哪种语言。 默认情况下，MSVC 编译器将以 `.c` 结尾的文件视为 C 源代码，将以 `.cpp` 结尾的所有文件视为 C++ 源代码 。 要强制编译器将所有文件视为独立于文件扩展名的 C++，请使用 [/TP](https://docs.microsoft.com/zh-cn/cpp/build/reference/tc-tp-tc-tp-specify-source-file-type?view=msvc-160) 编译器选项。



> ## *References*
>
> [演练：在命令行上编译本机 C++ 程序 | Microsoft Docs](https://docs.microsoft.com/zh-cn/cpp/build/walkthrough-compiling-a-native-cpp-program-on-the-command-line?view=msvc-160)
>
> [Walkthrough: Compiling a Native C++ Program on the Command Line | Microsoft Docs](https://docs.microsoft.com/en-us/cpp/build/walkthrough-compiling-a-native-cpp-program-on-the-command-line?view=msvc-160)
>
> [Visual Studio 概述 | Microsoft Docs](https://docs.microsoft.com/zh-cn/visualstudio/get-started/visual-studio-ide?view=vs-2019)
>
> [Overview of Visual Studio | Microsoft Docs](https://docs.microsoft.com/en-us/visualstudio/get-started/visual-studio-ide?view=vs-2019)
>
> [Microsoft C/C++ 文档 | Microsoft Docs](https://docs.microsoft.com/zh-cn/cpp/?view=msvc-160)
>
> [Microsoft C/C++ Documentation | Microsoft Docs](https://docs.microsoft.com/en-us/cpp/?view=msvc-160)
>
> [在 C++ 项目中使用库和组件 | Microsoft Docs](https://docs.microsoft.com/zh-cn/cpp/build/adding-references-in-visual-cpp-projects?view=msvc-160)
>
> [Consuming libraries and components in C++ projects | Microsoft Docs](https://docs.microsoft.com/en-us/cpp/build/adding-references-in-visual-cpp-projects?view=msvc-160)
>
> [演练：创建和使用自己的动态链接库 (C++) | Microsoft Docs](https://docs.microsoft.com/zh-cn/cpp/build/walkthrough-creating-and-using-a-dynamic-link-library-cpp?view=msvc-160)
>
> [Walkthrough: Create and use your own Dynamic Link Library (C++) | Microsoft Docs](https://docs.microsoft.com/en-us/cpp/build/walkthrough-creating-and-using-a-dynamic-link-library-cpp?view=msvc-160)
>
> [演练：创建并使用静态库 (C++) | Microsoft Docs](https://docs.microsoft.com/zh-cn/cpp/build/walkthrough-creating-and-using-a-static-library-cpp?view=msvc-160)
>
> [Walkthrough: Create and use a static library (C++) | Microsoft Docs](https://docs.microsoft.com/en-us/cpp/build/walkthrough-creating-and-using-a-static-library-cpp?view=msvc-160)
>
> 

