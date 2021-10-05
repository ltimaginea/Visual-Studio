# Visual Studio Debug only user code with Just My Code

By default, the debugger skips over non-user code (if you want more details, see [Just My Code](https://docs.microsoft.com/en-us/visualstudio/debugger/just-my-code?view=vs-2019)).

*Just My Code* is a Visual Studio debugging feature that automatically steps over calls to system, framework, and other non-user code. In the **Call Stack** window, Just My Code collapses these calls into **[External Code]** frames.

Just My Code works differently in .NET, C++, and JavaScript projects.

## Visual Studio Enable or disable Just My Code

For most programming languages, Just My Code is enabled by default.

- To enable or disable Just My Code in Visual Studio, under **Tools** > **Options** (or **Debug** > **Options**) > **Debugging** > **General**, select or deselect **Enable Just My Code**.

**Enable Just My Code** is a global setting that applies to all Visual Studio projects in all languages.

![](https://github.com/ltimaginea/Visual-Studio/blob/main/VisualStudio/Images/Cpp/CppDebugger_SettingJMC.png)



## C++ Just My Code

To set this compiler option in the Visual Studio development environment:

1. Open the project's **Property Pages** dialog box. For details, see [Set C++ compiler and build properties in Visual Studio](https://docs.microsoft.com/en-us/cpp/build/working-with-project-properties?view=msvc-160).
2. Select the **Configuration Properties** > **C/C++** > **General** property page.
3. Modify the **Support Just My Code Debugging** property, then the setting will only apply to this project.

![](https://github.com/ltimaginea/Visual-Studio/blob/main/VisualStudio/Images/Cpp/CppDebugger_JMC.png)



> ## References
>
> [visualstudio-docs/just-my-code.md at master · MicrosoftDocs/visualstudio-docs · GitHub](https://github.com/MicrosoftDocs/visualstudio-docs/blob/master/docs/debugger/just-my-code.md)
>
> [Tutorial: Debug C++ code - Visual Studio (Windows) | Microsoft Docs](https://docs.microsoft.com/en-us/visualstudio/debugger/getting-started-with-the-debugger-cpp?view=vs-2019)
>
> [教程：调试 C++ 代码 - Visual Studio (Windows) | Microsoft Docs](https://docs.microsoft.com/zh-cn/visualstudio/debugger/getting-started-with-the-debugger-cpp?view=vs-2019)
>
> [Debug user code with Just My Code - Visual Studio (Windows) | Microsoft Docs](https://docs.microsoft.com/en-us/visualstudio/debugger/just-my-code?view=vs-2019)
>
> [使用“仅我的代码”调试用户代码 - Visual Studio (Windows) | Microsoft Docs](https://docs.microsoft.com/zh-cn/visualstudio/debugger/just-my-code?view=vs-2019)
>
> [/JMC (Just My Code debugging) | Microsoft Docs](https://docs.microsoft.com/en-us/cpp/build/reference/jmc?view=msvc-160)
>
> [Announcing C++ Just My Code Stepping in Visual Studio - C++ Team Blog (microsoft.com)](https://devblogs.microsoft.com/cppblog/announcing-jmc-stepping-in-visual-studio/)
>
> [Visual Studio C++调试技巧和窍门 | Microsoft Docs](https://docs.microsoft.com/zh-cn/archive/blogs/c/visual-studio-c调试技巧和窍门)
>
> [Debugging Tips and Tricks for C++ in Visual Studio - C++ Team Blog (microsoft.com)](https://devblogs.microsoft.com/cppblog/debugging-tips-and-tricks-for-c-in-visual-studio/)
>
> 