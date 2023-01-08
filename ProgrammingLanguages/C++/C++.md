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



# 基础

## 数据类型

C++的基本数据类型分为算术数据类型和空类型（void）。

算术数据类型：字符、整数、浮点数、布尔值。

| 数据类型    | 含义                  | 最小尺寸     |
| ----------- | --------------------- | ------------ |
| bool        | 布尔类型，true、false | 未定义       |
| char        | 字符型，单个字符      | 8位          |
| wchar_t     | 宽字符                | 16位         |
| char16_t    | Unicode字符           | 16位         |
| char32_t    | Unicode字符           | 32位         |
| short       | 短整型                | 16位         |
| int         | 整形                  | 16位         |
| long        | 长整型                | 32位         |
| long long   | 长整型                | 64位         |
| float       | 单精度浮点型          | 6位有效数字  |
| double      | 双精度浮点型          | 10位有效数字 |
| long double | 拓展精度浮点数        | 10位有效数字 |

无符号整型：unsigned short、unsigned int（简写为unsigned）、unsigned long、unsigned long long。

字符型的无符号类型：字符型分为三种——char、signed char、unsigned char，char的具体表现为带符号还是不带符号由编译器决定。

**关于数据类型的选择：**

1. 整数运算常用int，如果数的长度超过int那么使用long long，不用long是因为long一般和int的尺寸一样。
2. 算术运算中不要涉及char、bool，如果需要用char来定义一个不大的整数那也应该指明是无符号类型还是有符号类型。
3. 浮点运算常用double。

**数据类型的自动转换机制：**

1. 数值赋给bool，0为false，其他的为true；bool的值赋给非布尔类型，true为1、false为0。
2. 浮点数赋给整数，只保留小数点前的数值；整数赋给浮点数时小数部分记为0，如果该整数超过浮点数的范围那将会导致精度损失。
3. 赋给无符号类型的值超过其范围，结果将是该值对该类型的的最大值取模后的余数。



| 转义字符 | 含义       |
| -------- | ---------- |
| \n       | 换行       |
| \t       | 横向制表符 |
| \v       | 纵向制表符 |
| \ "      | 双引号     |
| \ '      | 单引号     |
| \ \      | 反斜       |
| \r       | 回车       |
| \?       | 问号       |
| \f       | 进纸符     |
| \b       | 退格符     |

## 变量

















