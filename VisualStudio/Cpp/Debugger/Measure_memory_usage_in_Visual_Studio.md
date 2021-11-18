# Measure memory usage in Visual Studio

我们可以使用 Visual Studio 的调试器集成的内存使用诊断工具进行调试，高效地查找内存泄漏和低效内存。

最简单的使用方法：我们可以在应用程序的开始位置和结束位置分别设置断点，拍摄开始位置和结束位置的堆内存的快照，分析应用程序整个生命周期内的内存使用情况，检查是否存在内存泄漏以及查找内存泄漏的源代码位置。

## References

- [Measure performance in Visual Studio - Visual Studio (Windows) | Microsoft Docs](https://docs.microsoft.com/en-us/visualstudio/profiling/?view=vs-2022)
- [Measure memory usage in your apps - Visual Studio (Windows) | Microsoft Docs](https://docs.microsoft.com/en-us/visualstudio/profiling/memory-usage?view=vs-2022)
- [Analyze memory usage in the Performance Profiler - Visual Studio (Windows) | Microsoft Docs](https://docs.microsoft.com/en-us/visualstudio/profiling/memory-usage-without-debugging2?view=vs-2022)
- [Memory Profiling in Visual C++ 2015 - C++ Team Blog (microsoft.com)](https://devblogs.microsoft.com/cppblog/memory-profiling-in-visual-c-2015/)

