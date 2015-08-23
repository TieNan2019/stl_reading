#sgi stl source code reading

origin version: v3.3, [DOWNLOAD](https://www.sgi.com/tech/stl/stl.tar)

##调试方法:

g++-4.8 可能不兼容 sgi stl.

所以使用 clang++-3.8 编译器, 配置步骤如下:

1. 先将 stl_algobase.h 和 stl_construct.h 中的 `include <new.h>` 改为 `include <new>`.
2. -I 指向 sgi stl 目录.
3. 再开启如下宏:
-D__STL_CLASS_PARTIAL_SPECIALIZATION -D__STL_HAS_NAMESPACES -D__STL_HAS_WCHAR_T -D__STL_CLASS_PARTIAL_SPECIALIZATION -D__STL_PARTIAL_SPECIALIZATION_SYNTAX -D__STL_FUNCTION_TMPL_PARTIAL_ORDER -D__STL_MEMBER_TEMPLATES -D__STL_TEMPLATE_FRIENDS -D__STL_EXPLICIT_FUNCTION_TMPL_ARGS -D__STL_LONG_LONG -D__STL_MEMBER_TEMPLATE_KEYWORD -D__STL_ASSERTIONS -D__STL_USE_NEW_IOSTREAMS
