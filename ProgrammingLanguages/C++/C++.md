# Cherno   C++

## 前菜

C++源文件  ==>  编译器  ==>  二进制可执行文件。

```c++
/* 第一个C++程序 */
#include <iostream>   
// main函数，程序的入口，main函数默认返回值是0
int main()
{
	std::cout << "Hello World!" << std::endl;
	std::cin.get();
}
```

#之后的都是预处理语句，编译器优先处理的在实际编译之前就去处理的，include表示需要找到某个文件，此处是找到iostream这个文件然后就拷贝到当前程序源文件中，这些文件也称之为“头文件”。

X86：win32。X64：win64。

```c++
/* Log.cpp */
#include <iostream>
void Log(const char* message)
{
	std::cout << message << std::endl;
}
/* Main.cpp */
#include <iostream>
void Log(const char* message);
int main()
{
	Log("Hello World!");
	std::cin.get();
}
```



预处理器阶段   实际编译阶段  链接阶段  





