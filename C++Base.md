# 第一部分 C++基础



## 第一章 输入输出

C++ 是 C 的一个超集，事实上，任何合法的 C 程序都是合法的 C++ 程序。



### 1.1 开始框架

#### 1.1.1 基本概念

C++ 是一种静态类型的、编译式的、通用的、大小写敏感的、不规则的编程语言，支持过程化编程、面向对象编程和泛型编程。

C++ 被认为是一种**中级**语言，它综合了高级语言和低级语言的特点。

C++ 是由 Bjarne Stroustrup 于 1979 年在新泽西州美利山贝尔实验室开始设计开发的。C++ 进一步扩充和完善了 C 语言，最初命名为带类的C，后来在 1983 年更名为 C++。

C++ 是 C 的一个超集，事实上，任何合法的 C 程序都是合法的 C++ 程序。

**注意：**使用静态类型的编程语言是在编译时执行类型检查，而不是在运行时执行类型检查。

##### 面向对象程序设计

C++ 完全支持面向对象的程序设计，包括面向对象开发的四大特性：

+ 封装
+ 抽象
+ 继承
+ 多态

减少代码量/提高复用性

##### 标准库

标准的 C++ 由三个重要部分组成：

+ 核心语言，提供了所有构件块，包括变量、数据类型和常量，等等。
+ C++ 标准库，提供了大量的函数，用于操作文件、字符串等。
+ 标准模板库（STL），提供了大量的方法，用于操作数据结构等。

##### ANSI 标准

ANSI 标准是为了确保 C++ 的便携性 —— 您所编写的代码在 Mac、UNIX、Windows、Alpha 计算机上都能通过编译。

由于 ANSI 标准已稳定使用了很长的时间，所有主要的 C++ 编译器的制造商都支持 ANSI 标准。

##### 学习 C++

学习 C++，关键是要理解概念，而不应过于深究语言的技术细节。

学习程序设计语言的目的是为了成为一个更好的程序员，也就是说，是为了能更有效率地设计和实现新系统，以及维护旧系统。

C++ 支持多种编程风格。您可以使用 Fortran、C、Smalltalk 等任意一种语言的编程风格来编写代码。每种风格都能有效地保证运行时间效率和空间效率。

##### C++ 的使用

基本上每个应用程序领域的程序员都有使用 C++。

C++ 通常用于编写设备驱动程序和其他要求实时性的直接操作硬件的软件。

C++ 广泛用于教学和研究。

任何一个使用苹果电脑或 Windows PC 机的用户都在间接地使用 C++，因为这些系统的主要用户接口是使用 C++ 编写的。

#### 1.1.2 C++程序框架

```c++
#include<iostream>

using namespace std;

int main()
{
    fantio
    system("pause");
    return 0;
}
```

#### 1.1.3 编译运行程序

  主函数main和return返还值0为没有错误非0的一般由系统定义，通常指出系统错误。

### 1.2 初识C++的输入输出

#### 1.2.1 C++输入输出库

  c++语言并未定义任何输入输出（IO）语句，取而代之，包含了一个全面的标准库来提供IO机制（以及很多其他设施），本章只了解一部分基本概念和操作。

#### 1.2.2 C++输入

  标准库中定义了四个IO对象，

1. cin为istream类型的对象，这个对象也被称为==**标准输入**==。

2. cout为ostream类型的对象，这个对象也被称为==**标准输出**==。

3. cerr通常用来输出警告和错误，被称为==**标准错误**==。

4. clog用来输出程序运行时的一般性信息。

  系统通常会将程序运行的窗口与这些对象联系起来。因此，当我们通过cin，数据将从程序正在运行的窗口读入，当我们像cout，cerr，clog写入数据时，将会写到同一个窗口。

#### 1.2.3 C++输出

  想要使用输入出输出（iostream）库必须要添加一个**头文件**（header）#include指令必须出现在所有函数之外。一般将一个程序的所有#include指令都放在完文件的开始。



#### 1.2.4 输出符号

```c++
#include<iostream>

using namespace std;

int main()
{
    cout << "输入两个数字:" << endl;
    int v1 = 0, v2 = 0;
    cin >> v1 >> v2;
    cout << "第一个数" << v1 << "和第二个数" << v2 
              << "的和是" << v1 + v2 << endl;
    
    system("pause");
    return 0;
}
```

  其中main的函数体的第一条语句执行了一个**表达式**。在c++中一个表达式产生一个计算结果，它由一个或多个运算对象和一个运算符组成。

```c++
    cout << "输入两个数字:" << endl;
```

 这条语句使用了**输出运算符**（<<）在标准输出上打印消息。

 << 运算符接受两个运算对象：

   + **左侧**：运算对象必须是一个ostream对象。

   + **右侧**：运算对象为要打印的值。

  此运算符将给定的值写到给定的ostream（**左侧**）对象中，输出运算符的计算结果就是其左侧运算对象（ostream）。

```c++
    cout << "输入两个数字:" << endl;
```

  第一个输出运算符是打印一条消息，这个消息是一个**字符串字面值常量**。

**字符串字面值常量**：是一对用双引号包围的字符序列，在双引号之间的文本被打印到标准输出。

  第二个输出运算符打印endl，这是一个被称为**操纵符**的特殊值。

**操纵符**：是为了结束当前行（相当于换行），并将与设备关联的[^ 缓冲区]中的内容冲刷到设备中。

[^ 缓冲区]: 内存四区。

#### 1.2.5 使用标准库中的名字

```c++
using namespace std;
```

  这句话指出cout和endl等是定义在名为std的**命名空间**。

**命名空间**： 可以帮助我们避免不经意的名字定义冲突，以及使用库中相同名字导致的冲突。标准库定义的所有名字都在命名空间std中。

  通过标准空间使用标准库有一个副作用，当使用标准库中的一个名字时，必须显式说明我们想使用来自命名空间std中的名字。

```c++
    std :: cout << "输入两个数字:" << endl;
```

通过（::）**作用域运算符**来指出我们想使用的定义在命名空间std中的名字cout

而使用

```c++
using namespace std;
```

  写在开头可以省略std:: 。

#### 1.2.6 输入符号

```c++
    cin >> v1 >> v2;
```

**输入运算符**（>>）和输出运算符类似

**输入运算符：**

+ 左侧：接受一个istream作为运算对象。
+ 右侧：接受一个对象作为运算对象。

此式等价于

```c++
  (  cin >> v1 )>> v2;
```

```c++
cin >> v1;
cin >> v2;
```

其作用为通过cin读取两个值并且将第一个值存入v1，讲第二个值存入v2中。


### 1.3 注释

#### 1.3.1 注释简介

  注释是用于解释代码段的意思便于读者理解，但是编译器会忽视。

#### 1.3.2 C++注释种类

  c++中注释有两种：**单行注释**和**多行注释**

1. 单行注释

     以双斜线（//）开始，以换行符结束。

     也就是说当前行双斜线右侧的所有内容都会被编译器忽略。

     这种注释可以包括任何文本。

     常用于半行和单行注释

2. 多行注释

     这种注释继承于C语言的两个定界符（/\* 和 \*/）。这种注释以 /\* 开始，以 \*/ 结束，可以包含除了 \*/ 之外的所有内容（包括换行符）。编译器会将（/\* 和 \*/）中的所有内容忽略。

​       常用于多行注释，注释时不能嵌套。

```c++
#include<iostream>

/*
*   
*简单主函数
*常用*号分行
*
*/
```

### 1.4 完成程序

```c++
    cout << "第一个数" << v1 << "和第二个数" << v2 
              << "的和是" << v1 + v2 << endl;
```

输出的结果就是v1和v2的和。



## 第二章 基础

### 2.1 变量和基本类型

#### C++ 数据类型

使用编程语言进行编程时，需要用到各种变量来存储各种信息。变量保留的是它所存储的值的内存位置。这意味着，当您创建一个变量时，就会在内存中保留一些空间。

您可能需要存储各种数据类型（比如字符型、宽字符型、整型、浮点型、双浮点型、布尔型等）的信息，操作系统会根据变量的数据类型，来分配内存和决定在保留内存中存储什么。

#### 基本的内置类型

C++ 为程序员提供了种类丰富的内置数据类型和用户自定义的数据类型。下表列出了七种基本的 C++ 数据类型：

| 类型     | 关键字  |
| :------- | :------ |
| 布尔型   | bool    |
| 字符型   | char    |
| 整型     | int     |
| 浮点型   | float   |
| 双浮点型 | double  |
| 无类型   | void    |
| 宽字符型 | wchar_t |

其实 wchar_t 是这样来的：

```
typedef short int wchar_t;
```

所以 wchar_t 实际上的空间是和 short int 一样。

一些基本类型可以使用一个或多个类型修饰符进行修饰：

+ signed
+ unsigned
+ short
+ long

下表显示了各种变量类型在内存中存储值时需要占用的内存，以及该类型的变量所能存储的最大值和最小值。

**注意：**不同系统会有所差异，一字节为 8 位。

**注意：**默认情况下，int、short、long都是带符号的，即 signed。

**注意：**long int 8 个字节，int 都是 4 个字节，早期的 C 编译器定义了 long int 占用 4 个字节，int 占用 2 个字节，新版的 C/C++ 标准兼容了早期的这一设定。

| 类型               | 位            | 范围                                                         |
| :----------------- | :------------ | :----------------------------------------------------------- |
| char               | 1 个字节      | -128 到 127 或者 0 到 255                                    |
| unsigned char      | 1 个字节      | 0 到 255                                                     |
| signed char        | 1 个字节      | -128 到 127                                                  |
| int                | 4 个字节      | -2147483648 到 2147483647                                    |
| unsigned int       | 4 个字节      | 0 到 4294967295                                              |
| signed int         | 4 个字节      | -2147483648 到 2147483647                                    |
| short int          | 2 个字节      | -32768 到 32767                                              |
| unsigned short int | 2 个字节      | 0 到 65,535                                                  |
| signed short int   | 2 个字节      | -32768 到 32767                                              |
| long int           | 8 个字节      | -9,223,372,036,854,775,808 到 9,223,372,036,854,775,807      |
| signed long int    | 8 个字节      | -9,223,372,036,854,775,808 到 9,223,372,036,854,775,807      |
| unsigned long int  | 8 个字节      | 0 到 18,446,744,073,709,551,615                              |
| float              | 4 个字节      | 精度型占4个字节（32位）内存空间，+/- 3.4e +/- 38 (~7 个数字) |
| double             | 8 个字节      | 双精度型占8 个字节（64位）内存空间，+/- 1.7e +/- 308 (~15 个数字) |
| long double        | 16 个字节     | 长双精度型 16 个字节（128位）内存空间，可提供18-19位有效数字。 |
| wchar_t            | 2 或 4 个字节 | 1 个宽字符                                                   |

> 注意，各种类型的存储大小与系统位数有关，但目前通用的以64位系统为主。
>
> 以下列出了32位系统与64位系统的存储大小的差别（windows 相同）：
>
> ![img](https://www.runoob.com/wp-content/uploads/2014/09/32-64.jpg)

从上表可得知，变量的大小会根据编译器和所使用的电脑而有所不同。

下面实例会输出您电脑上各种数据类型的大小。

#### 实例

~~~c++
#include<iostream>  
#include <limits>
 
using namespace std;  
  
int main()  
{  
    cout << "type: \t\t" << "************size**************"<< endl;  
    cout << "bool: \t\t" << "所占字节数：" << sizeof(bool);  
    cout << "\t最大值：" << (numeric_limits<bool>::max)();  
    cout << "\t\t最小值：" << (numeric_limits<bool>::min)() << endl;  
    cout << "char: \t\t" << "所占字节数：" << sizeof(char);  
    cout << "\t最大值：" << (numeric_limits<char>::max)();  
    cout << "\t\t最小值：" << (numeric_limits<char>::min)() << endl;  
    cout << "signed char: \t" << "所占字节数：" << sizeof(signed char);  
    cout << "\t最大值：" << (numeric_limits<signed char>::max)();  
    cout << "\t\t最小值：" << (numeric_limits<signed char>::min)() << endl;  
    cout << "unsigned char: \t" << "所占字节数：" << sizeof(unsigned char);  
    cout << "\t最大值：" << (numeric_limits<unsigned char>::max)();  
    cout << "\t\t最小值：" << (numeric_limits<unsigned char>::min)() << endl;  
    cout << "wchar_t: \t" << "所占字节数：" << sizeof(wchar_t);  
    cout << "\t最大值：" << (numeric_limits<wchar_t>::max)();  
    cout << "\t\t最小值：" << (numeric_limits<wchar_t>::min)() << endl;  
    cout << "short: \t\t" << "所占字节数：" << sizeof(short);  
    cout << "\t最大值：" << (numeric_limits<short>::max)();  
    cout << "\t\t最小值：" << (numeric_limits<short>::min)() << endl;  
    cout << "int: \t\t" << "所占字节数：" << sizeof(int);  
    cout << "\t最大值：" << (numeric_limits<int>::max)();  
    cout << "\t最小值：" << (numeric_limits<int>::min)() << endl;  
    cout << "unsigned: \t" << "所占字节数：" << sizeof(unsigned);  
    cout << "\t最大值：" << (numeric_limits<unsigned>::max)();  
    cout << "\t最小值：" << (numeric_limits<unsigned>::min)() << endl;  
    cout << "long: \t\t" << "所占字节数：" << sizeof(long);  
    cout << "\t最大值：" << (numeric_limits<long>::max)();  
    cout << "\t最小值：" << (numeric_limits<long>::min)() << endl;  
    cout << "unsigned long: \t" << "所占字节数：" << sizeof(unsigned long);  
    cout << "\t最大值：" << (numeric_limits<unsigned long>::max)();  
    cout << "\t最小值：" << (numeric_limits<unsigned long>::min)() << endl;  
    cout << "double: \t" << "所占字节数：" << sizeof(double);  
    cout << "\t最大值：" << (numeric_limits<double>::max)();  
    cout << "\t最小值：" << (numeric_limits<double>::min)() << endl;  
    cout << "long double: \t" << "所占字节数：" << sizeof(long double);  
    cout << "\t最大值：" << (numeric_limits<long double>::max)();  
    cout << "\t最小值：" << (numeric_limits<long double>::min)() << endl;  
    cout << "float: \t\t" << "所占字节数：" << sizeof(float);  
    cout << "\t最大值：" << (numeric_limits<float>::max)();  
    cout << "\t最小值：" << (numeric_limits<float>::min)() << endl;  
    cout << "size_t: \t" << "所占字节数：" << sizeof(size_t);  
    cout << "\t最大值：" << (numeric_limits<size_t>::max)();  
    cout << "\t最小值：" << (numeric_limits<size_t>::min)() << endl;  
    cout << "string: \t" << "所占字节数：" << sizeof(string) << endl;  
    // << "\t最大值：" << (numeric_limits<string>::max)() << "\t最小值：" << (numeric_limits<string>::min)() << endl;  
    cout << "type: \t\t" << "************size**************"<< endl;  
    return 0;  
}
本实例使用了 endl，这将在每一行后插入一个换行符，<< 运算符用于向屏幕传多个值，sizeof() 函数用来获取各种数据类型的大小。

当上面的代码被编译和执行时，它会产生以下的结果，结果会根据所使用的计算机而有所不同：

type:         ************size**************
bool:         所占字节数：1    最大值：1        最小值：0
char:         所占字节数：1    最大值：        最小值：?
signed char:     所占字节数：1    最大值：        最小值：?
unsigned char:     所占字节数：1    最大值：?        最小值：
wchar_t:     所占字节数：4    最大值：2147483647        最小值：-2147483648
short:         所占字节数：2    最大值：32767        最小值：-32768
int:         所占字节数：4    最大值：2147483647    最小值：-2147483648
unsigned:     所占字节数：4    最大值：4294967295    最小值：0
long:         所占字节数：8    最大值：9223372036854775807    最小值：-9223372036854775808
unsigned long:     所占字节数：8    最大值：18446744073709551615    最小值：0
double:     所占字节数：8    最大值：1.79769e+308    最小值：2.22507e-308
long double:     所占字节数：16    最大值：1.18973e+4932    最小值：3.3621e-4932
float:         所占字节数：4    最大值：3.40282e+38    最小值：1.17549e-38
size_t:     所占字节数：8    最大值：18446744073709551615    最小值：0
string:     所占字节数：24
type:         ************size**************
~~~



本实例使用了 **endl**，这将在每一行后插入一个换行符，**<<** 运算符用于向屏幕传多个值，**sizeof()** 函数用来获取各种数据类型的大小。

当上面的代码被编译和执行时，它会产生以下的结果，结果会根据所使用的计算机而有所不同：

```
type:         ************size**************
bool:         所占字节数：1    最大值：1        最小值：0
char:         所占字节数：1    最大值：        最小值：?
signed char:     所占字节数：1    最大值：        最小值：?
unsigned char:     所占字节数：1    最大值：?        最小值：
wchar_t:     所占字节数：4    最大值：2147483647        最小值：-2147483648
short:         所占字节数：2    最大值：32767        最小值：-32768
int:         所占字节数：4    最大值：2147483647    最小值：-2147483648
unsigned:     所占字节数：4    最大值：4294967295    最小值：0
long:         所占字节数：8    最大值：9223372036854775807    最小值：-9223372036854775808
unsigned long:     所占字节数：8    最大值：18446744073709551615    最小值：0
double:     所占字节数：8    最大值：1.79769e+308    最小值：2.22507e-308
long double:     所占字节数：16    最大值：1.18973e+4932    最小值：3.3621e-4932
float:         所占字节数：4    最大值：3.40282e+38    最小值：1.17549e-38
size_t:     所占字节数：8    最大值：18446744073709551615    最小值：0
string:     所占字节数：24
type:         ************size**************
```

#### typedef 声明

您可以使用 **typedef** 为一个已有的类型取一个新的名字。下面是使用 typedef 定义一个新类型的语法：

```
typedef type newname; 
```

例如，下面的语句会告诉编译器，feet 是 int 的另一个名称：

```
typedef int feet;
```

现在，下面的声明是完全合法的，它创建了一个整型变量 distance：

```
feet distance;
```

#### 枚举类型

枚举类型(enumeration)是C++中的一种派生数据类型，它是由用户定义的若干枚举常量的集合。

如果一个变量只有几种可能的值，可以定义为枚举(enumeration)类型。所谓"枚举"是指将变量的值一一列举出来，变量的值只能在列举出来的值的范围内。

创建枚举，需要使用关键字 **enum**。枚举类型的一般形式为：

```
enum 枚举名{ 
     标识符[=整型常数], 
     标识符[=整型常数], 
... 
    标识符[=整型常数]
} 枚举变量;
    
```

如果枚举没有初始化, 即省掉"=整型常数"时, 则从第一个标识符开始。

例如，下面的代码定义了一个颜色枚举，变量 c 的类型为 color。最后，c 被赋值为 "blue"。

```
enum color { red, green, blue } c;
c = blue;
```

默认情况下，第一个名称的值为 0，第二个名称的值为 1，第三个名称的值为 2，以此类推。但是，您也可以给名称赋予一个特殊的值，只需要添加一个初始值即可。例如，在下面的枚举中，**green** 的值为 5。

```
enum color { red, green=5, blue };
```

在这里，**blue** 的值为 6，因为默认情况下，每个名称都会比它前面一个名称大 1，但 red 的值依然为 0。



### 2.2 字符串、向量和数组

### 2.3 表达式

### 2.4 语句

### 2.5 函数





## 类和对象

  在C++语言中，我们使用自己定义的类型数据。通过定义新的类型来跟容易编写，调试和修改程序。

#### 2.6.1 定义抽象数据类型

##### 2.6.1.1 设计Sales_data类

  Sales_data的接口应该包含以下操作

+ 一个isbn成员函数，用于返回对象的ISBN编号。

+ 一个combine成员函数，用于将一个Sales_data对象加到另一个对象上。

+ 一个名为add的函数，执行两个Sales_data对象的加法。

+ 一个read函数，将数据从istream读入到Sales_data对象中。

+ 一个print函数，将Sales_data对象的值输出到ostrea。

```c++
#include<iostream>
#include<string>

using namespace std;

int main() 
{
	Sales_data total;
	if (read(cin, total)) 
	{
		Sales_data trans;
		while (read(cin, trans)) 
		{
			if (total.isbn() == trans.isbn()) 
			{
				total.combine(trans);
			} 
			else 
			{
				print (cout, total) << endl;
				total = trans;
			}
		}
		print (cout, total) << endl;
	} 
	else 
	{
		cerr << "No datd?!" <<endl;
	}
	
	
	system("pause");
	return 0;
}
```

最终Sales_data应该为

```c++
struct Sales_data{
    string isbn() const {return bookNo;}
    Sales_data& combine{const Sales_data&};
    double avg_price() const;
    
    string bookNo;
    unsigned units_sold = 0;
    double revenue = 0.0;
};
```

##### 2.6.1.2 **定义成员函数**

​     所有成员都必须在类内声明但是成员函数体可以定义在类内也可以定义在类外。

对于Sales_data类来说isbn函数定义在了类内，而combine和avg_price定义在了类外。

先看isbn函数

```c++
string isbn() const {return bookNo;}
```

 其中isbn函数块体中只有一条return语句用于返回bookNo数据成员

##### 2.6.1.3 **引入this**

   this常量指针

##### 2.6.1.4 引入const成员函数

   isbn函数后面紧跟const是为了修饰this表示this是一个指向常量的指针。

像这样使用const的成员函数称为**常量成员函数**。

##### 2.6.1.5 类作用域和成员函数

  类本身就是一个作用域，类的成员函数定义嵌套在类作用域之内。

##### 2.6.1.6 在类的外部定义成员函数

  

```c++
double Sales_data::avg_price() const
{
    if (units_soid)
        return revenue/units_sold;
    else
        return 0;
}
```

函数名Sales_data::avg_price使用作用域运算符来说明

+ 定义了一个名为avg_price的函数
+ 并且该函数被声明在类Sales_data的作用域内

##### 2.6.1.7 定义类相关的非成员函数

 类内通常需要定义一些辅助函数比如add、read、等虽然从概念上说属于类的接口组成部分，但实际上并不属于类本身。

**定义read和print函数**

```c++
istream &read (istream &is, Sales_datd &item)
{
    double price = 0;
    is >> item.bookNo >> item.nuits_sold >> price;
    item.revenue = price * item.units_sold;
    return is;
}

ostream &print (ostream &os, const Sales_data &item)
{
    os << item.isbn() << " " << item.units_sold << " "
        << item.revenue << " " << item.avg_price();
    return os;
}
```

**定义add函数**

~~~ c++
Slaes_data add (const Sales_data &lhs, const Sales_data &rhs)
{
    Sales_data sum = lhs;
    
    sum.combine(rhs);
    return sum;
}
~~~

##### 2.6.1.8 构造函数

  每个类都定义了一个或几个特殊的成员函数来控制其对象的初始化过程这些函数叫做**构造函数**。

构造函数的名字和类名相同，并且没有返回类型。类可以包含多个构造函数，不同的构造函数必须在参数数量和参数类型上有所区别。且构造函数不能被生成const。

**合成的默认构造函数**

  由编译器创建的构造函数无须任何实参。

Sales_data的构造函数

~~~c++
struct Slaes_data{
    Salea_data () = default;
    Salea_data (const string &s) : bookNo(s) {}
    Salea_data (const string &s, unsigned n,double p): 
                bookNo(s), units_sold(n), revenue(p*n){}
    Salea_data (istream &);
}
~~~

**= default的含义**

要求编译器生成默认的构造函数。

下面两个在：和{}之间的部分称为**构造函数初始值列表**。

##### 2.6.1.9 拷贝、赋值和析构

调用完函数之后调用的函数为析构函数。

#### 2.6.2 访问控制与封装

  在C++中使用访问说明符加强类的封装性：

+ **public：** 定义在public说明符之后的成员在整个程序内都可被访问
+ **protected：** 类内访问类外不访问（保护）
+ **private：** 定义在private说明符之后的成员可以被类的成员函数访问（私有）

**class和struct**

  class和struct的默认访问权限不一样，struct默认都是public而class默认都是private

成员属性私有化

+ 可读写性自己控制
+ 对于写可以检测数据

用类创建对象时叫做实例化。

```c++
#include<iostream>

using namespace std;

class Cube
{
public:

	//设置长
	void setl(int l)
	{
		m_l = l;
	}

	//获取长
	int getl()
	{
		return m_l;
	}

	//设置宽
	void setw(int w)
	{
		m_w = w;
	}

	//获取宽
	int getw()
	{
		return m_w;
	}

	//设置高
	void seth(int h)
	{
		m_h = h;
	}

	//获取高
	int geth()
	{
		return m_h;
	}
	//获取面积
	int calculaters()
	{
		return 2 * m_l * m_w + 2 * m_h * m_l + 2 * m_w * m_h;
	}

	//获取体积
	int calculaterv()
	{
		return m_l * m_h * m_w;
	}
	Cube();
	~Cube();

private:

	int m_l;//长
	int m_w;//宽
	int m_h;//高
};

Cube::Cube()
{
}

Cube::~Cube()
{
}

int main()
{
	Cube c1;
	c1.setl(10);
	c1.setw(10);
	c1.seth(10);

	cout << "c1的面积" << c1.calculaters() << endl;
	cout << "c1的面积" << c1.calculaterv() << endl;

	system("pause");
	return 0;
}
```





##### 2.6.2.1 友元

  类可以允许其他类或者函数访问它的非公有成员，方法就是令其他类或者函数称为他的友元

只需加上friend关键字就可以友元只能出现在类定义的内部

**封装的好处**

+ 确保代码不会无意间破坏
+ 细节修改方便



#### 2.6.3 类的其他特性

  这些特性包括：类型成员、类的成员的类内初始值、可变数据成员、内联成员函数、从成员函数返回\*this、

##### 2.6.3.1 类成员

  Sreen和Window_mgr

**定义一个类型成员**

  ~~~c++
  Class Screen {
      public:
          typedef std::string::size_type pos;
      private:
          pos cursor = 0;
          pos height = 0, width = 0;
          std::string contents;
  };
  ~~~

**Screen的成员函数**

```c++
Class Screen {
    public:
        typedef std::string::size_type pos;
        Screen() = default;
        Screen(pos ht, pos wd, char c): height(ht), width(wd),
        contents(ht * wd, c) {}
        char get() const
         { return contents[cursor];}
        inline char get(pos ht, pos wd) const;
        Screen &move(pos r, pos c);
    private:
        pos cursor = 0;
        pos height = 0, width = 0;
        std::string contents;
};
```



#### 2.6.4 类的作用域

#### 2.6.5 再探构造函数

#### 2.6.6 类的静态成员

### 2.7构造函数和析构函数

#### 2.7.1构造函数与析构函数语法

可以不用手动写入编译器会自动补上

构造函数一般用于初始化

析构函数用于清除数据

没有返回类型不用写void

函数名与类名相同

自动调用且只会调用一次

~~~c++

#include<iostream>


using namespace std;

class Person
{
public:

	Person()
	{
		cout << "Persong构造数的调用" << endl;
	}

	~Person()
	{
		cout << "Person析构函数" << endl;
	}

};

void test01()
{
	Person p;
}

int main()
{
	test01();
	Person p1;

	system("pause");

	return 0;
}
~~~



#### 2.7.2 构造函数分类和调用

1. 分类
   + 有参和无参
   + 拷贝构造函数



### 2.8 友元

~~~c++
#include<iostream>
#include<string>

using namespace std;

class Buding
{
public:
    
    Buding()
    {
        m_SittingRoom = "客厅";
        m_BedRoom = "卧室";
    }
    
 public:
    string m_SittingRoom;
 private:
    string m_BedRoom;
};

void goodGay(Building*building)
{
    cout << "好基友正在访问：" << building->m_SittingRoom <<endl;
}

void test01()
{
    Building buiding;
    goodGay(&building);
}

int main()
{
    test01();
    
    system("pause");
    
    return 0;
}
~~~



### 复合类型

#### 1.引用



#### 2.指针







# 第二部分 C++进阶



## C++进阶

### 1. 内存四区

#### 1.1 全局区

~~~c++
#include<iostream>
#include<cstdlib>

using namespace std;

//c - const  g - global  l - local
//全局变量
int g_a = 10;
int g_b = 10;

//全局常量
const int c_g_a = 10;
const int c_g_b = 10;

int main()
{
	//局部变量
	int a = 10;
	int b = 10;

	//打印地址
	cout << "局部变量a地址：" << (int)&a << endl;
	cout << "局部变量b地址：" << (int)&b << endl;

	cout << "全局变量g_a地址：" << (int)&g_a << endl;
	cout << "全局变量g_b地址：" << (int)&g_b << endl;

	//静态变量
	static int s_a = 10;
	static int s_b = 10;

	cout << "静态变量s_a地址：" << (int)&s_a << endl;
	cout << "静态变量s_b地址：" << (int)&s_b << endl;

	cout << "字符串常量地址：" << (int)&"hello world" << endl;
	cout << "字符串常量地址：" << (int)&"hello world1" << endl;

	cout << "全局常量c_g_a地址：" << (int)&c_g_a << endl;
	cout << "全局常量c_g_b地址：" << (int)&c_g_b << endl;

	const int c_l_a = 10;
	const int c_l_b = 10;

	cout << "局部常量c_l_a地址：" << (int)&c_l_a << endl;
	cout << "局部常量c_l_b地址：" << (int)&c_l_b << endl;

	system("pause");

	return 0;
}
~~~



#### 1.2 栈区

~~~c++
#include<iostream>
#include<cstdlib>

using namespace std;

int* func()
{
	//局部变量
	int a = 10;

	//返回局部变量地址
	return &a;
}

int main()
{
	int* p = func();
	cout << *p << endl;
	cout << *p << endl;//第一次编译器进行保留


	system("pause");

	return 0;
}
~~~



#### 1.3 堆区

~~~c++
#include<iostream>

using namespace std;

//堆区开辟数据用new关键字delete

int* func()
{
	//用栈区的针接收堆区的返回地址
	int* p = new int(10);

	return p;
}

int main()
{
	int* p = func();

	cout << *p << endl;
	cout << *p << endl;
	cout << *p << endl;
	cout << *p << endl;

	system("pause");

	return 0;
}
~~~



#### 1.4 new指针的使用

~~~c++
#include<iostream>

using namespace std;

int* func()
{
	//在堆区创建数据
	int* p = new int(10);

	return p;
}

void test01()
{
	int* p = func();

	cout << *p << endl;
	cout << *p << endl;
	cout << *p << endl;

	//堆区数据不会自动释放
	delete p;

	//cout << *p << endl;内存已经释放无权访问

}

void test02()
{
	int* arr = new int[10];//代表有10个元素

	for (int i = 0; i < 10; i++)
	{
		arr[i] = i + 1;
	}

	for (int i = 0; i < 10; i++)
	{
		cout << arr[i] << endl;
	}
	//释放数组
	delete[] arr;
}

int main()
{
	test01();
	test02();

	system("pause");

	return 0;
}
~~~







### 2 C++运算符重载

#### 2.1 加号重载

~~~c++
#include<iostream>

using namespace std;

//加号运算符重载

class Person
{
public:

	//成员函数重载
	//Person operator+(Person& p)
	//{
	//	Person temp;
	//	temp.m_A = this->m_A + p.m_A;
	//	temp.m_B = this->m_B + p.m_B;
	//	return temp;
	//}

	int m_A;
	int m_B;

};

//全局重载
Person operator+(Person& p1, Person& p2)
{
	Person temp;

	temp.m_A = p1.m_A + p2.m_A;
	temp.m_B = p1.m_B + p2.m_B;

	return temp;
}

Person operator+(Person& p1, int num)
{
	Person temp;

	temp.m_A = p1.m_A + num;
	temp.m_B = p1.m_B + num;

	return temp;
}

void test01()
{
	Person p1;
	p1.m_A = 10;
	p1.m_B = 10;

	Person p2;
	p2.m_A = 10;
	p2.m_B = 10;

	//成员函数本质
	//Person p3 = p1.operator+(p2);
	
	//全局函数本质
	//Person p3 = operator+(p1, p2);

	Person p3 = p1 + p2;

	Person p4 = p1 + 100;

	cout << "p3.m_A = " << p3.m_A << endl;
	cout << "p3.m_B = " << p3.m_B << endl;

	cout << "p4.m_A = " << p4.m_A << endl;
	cout << "p4.m_B = " << p4.m_B << endl;

}

int main()
{
	test01();

	system("pause");

	return 0;
}
~~~



#### 2.2 左移运算符重载

~~~c++
#include<iostream>

using namespace std;

class Person
{
public:

	//利用成员函数重载
	//无法实现
	//void operator<<(Person &p )
	//{

	//}

	int m_A;
	int m_B;
};

//全局函数重载
ostream& operator<<(ostream& cout, Person p)
{
	cout << "m_A = " << p.m_A << " " << "m_B = " << p.m_B;
	return cout;
}

void test01()
{
	Person p;
	p.m_A = 10;
	p.m_B = 10;

	cout << p << endl;
}

int main()
{
	test01();
	
	system("pause");

	return 0;
}
~~~



#### 2.3 递增运算符重载

~~~c++
#include<iostream>

using namespace std;

//重载与运算符

class MyInteger
{
	friend ostream& operator<<(ostream& cout, MyInteger myint);

public:
	MyInteger()
	{
		int m_Num = 0;
	}

	//重载运算符
	//1.前置
	MyInteger& operator++()
	{
		m_Num++;

		return *this;
	}

	//2.后置
	void operator++(int)
	{

	}

private:
	int m_Num;
};

//重载左移运算符
ostream& operator<<(ostream& cout, MyInteger myint)
{
	cout << myint.m_Num;
	return cout;
}

void test01()
{
	MyInteger myint;

	cout << ++myint << endl;
}

int main()
{


	system("pause");

	return 0;
}
~~~







### 3 实参函数传递引用

#### 3.1 交换实参传递

~~~c++
#include<iostream>

using namespace std;

void test01(int a, int b)
{
	int temp = 0;
	temp = a;
	a = b;
	b = temp;

	cout << "值传递的a：" << a << endl;
	cout << "值传递的b：" << b << endl;
}

void test02(int* a, int* b)
{
	int temp = 0;
	temp = *a;
	*a = *b;
	*b = temp;

	cout << "指针的a：" << *a << endl;
	cout << "指针的b：" << *b << endl;
}

void test03(int& a, int& b)
{
	int temp = 0;
	temp = a;
	a = b;
	b = temp;

	cout << "引用的a：" << a << endl;
	cout << "引用的b：" << b << endl;
}

int main()
{
	int a = 10;
	int b = 20;

	cout << "初始a：" << a << endl;
	cout << "初始b：" << b << endl;

	test01(a, b);
	test02(&a, &b);
	test03(a, b);


	system("pause");

	return 0;
}
~~~



#### 3.2 常量引用

~~~c++
#include<iostream>

using namespace std;

void show(int& val)
{
	val = 1000;
	cout << "val=" << val << endl;
}

int main()
{
	//int a = 10;
	//const int& ref = 10;
	////相当于
	////int temp = 10;
	////const int& ref = temp;

	int a = 100;
	cout << "a=" << a << endl;
	show(a);
	cout << "a=" << a << endl;
	//加入const防止误操作




	system("pause");

	return 0;
}
~~~



#### 3.3 函数返回值

~~~c++
#include<iostream>

using namespace std;

//引用返回函数值
//不能返回局部变量
int& test01()
{
	int a = 10;
	return a;
}

//函数调用可以为左值
int& test02()
{
	static int a = 10;//静态全局
	return a;
}

int main()
{
	int &ref_a = test01();
	cout << "ref_a=" << ref_a << endl;
	cout << "ref_a=" << ref_a << endl;

	int& rec_a = test02();
	cout << "rec_a=" << rec_a << endl;
	cout << "rec_a=" << rec_a << endl;

	test02() = 1000;
	cout << "rec_a=" << rec_a << endl;

	system("pause");

	return 0;
}
~~~



#### 3.4 引用的本质

~~~c++
#include<iostream>

using namespace std;

void func(int& ref)
{
	ref = 100;
}

int main()
{
	int a = 10;

	int& ref = a;
	//相当于int* const ref = &a;常量指针，指向不能更改
	ref = 20;
	//相当于*ref = 20;

	cout << "a=" << a << endl;
	cout << "ref=" << ref << endl;

	func(a);
	cout << "a=" << a << endl;
	cout << "ref=" << ref << endl;

	system("pause");

	return 0;
}
~~~







### 4 函数高阶

#### 4.1 函数默认参数

~~~c++
#include<iostream>

using namespace std;

int test01(int a, int b, int c)
{
	return a + b + c;
}

int test02(int a, int b = 20, int c = 30)
{
	return a + b + c;
}

int test03(int a, int b = 20, int c = 30)
{
	return a + b + c;
}
//注意
//如果有默认参数则从此位置之后必须都有默认参数
//int test03(int a, int b = 20, int c, int d)
//{
//	return a + b + c + d;
//}

//如果函数声明有默认参数则函数实现不能有
int test04(int a = 10, int b = 20);

int test04(int a,int b)
{
	return a + b;
}

int main()
{
	cout << test01(10, 20, 30) << endl;
	cout << test02(10) << endl;
	cout << test02(10, 40) << endl;


	system("pause");

	return 0;
}
~~~



#### 4.2 函数的占位

~~~c++
#include<iostream>

using namespace std;

void test01(int a)
{
	cout << "hello" << endl;
}

void test02(int a, int)
{
	cout << "hello2" << endl;
}
//占位参数可以有默认值
void test03(int a, int = 10)
{
	cout << "hello2" << endl;
}

int main()
{
	test01(10);
	test02(10, 10);
	test03(10);

	system("pause");

	return 0;
}
~~~



#### 4.3 函数重载

~~~c++
#include<iostream>

using namespace std;

//可以让函数名相同
//提高复用性

//1.同一个作用域
//2.名称相同
//3.参数类型不同或者个数不同或者顺序不同

void test01()
{
	cout << "hello" << endl;
}

void test01(int a)
{
	cout << "hello1" << endl;
}

void test01(double a)
{
	cout << "hello1" << endl;
}

void test01(int a, double b)
{
	cout << "hello1" << endl;
}

void test01(double a, int b)
{
	cout << "hello1" << endl;
}

int main()
{
	test01();
	test01(10);
	test01(3.1415);
	test01(10, 3.14);
	test01(3.14, 10);

	system("pause");

	return 0;
}
~~~



#### 4.4 函数重载注意

~~~c++
#include<iostream>

using namespace std;

void test01(int& a)
{
	cout << "hello1" << endl;
}

void test01(const int& a)
{
	cout << "hello1const" << endl;
}


void test02(int a)
{
	cout << "hello2" << endl;
}

void test02(int a,int b)
{
	cout << "hello2b" << endl;
}

void test02(int a, int b = 10)
{
	cout << "hello2bbb" << endl;
}

int main()
{
	int a = 10;
	const int b = 10;

	test01(a);
	test01(10);
	test01(b);

	test02(10);
	test02(10, 10);

	system("pause");

	return 0;
}
~~~







### 5 文件操作

#### 5.1 写文本文件

~~~c++
#include<iostream>
#include<fstream>

using namespace std;

void test01()
{
	//头文件
	//创建对象
	ofstream ofs;

	//打开
	ofs.open("test.txt", ios::out);

	//写
	ofs << "姓名：张三" << endl;
	ofs << "姓别：男" << endl;
	ofs << "年龄：20" << endl;

	ofs.close();


}

int main()
{
	test01();

	system("pause");

	return 0;
}
~~~



#### 5.2 读文本文件

~~~c++
#include<iostream>
#include<fstream>
#include<string>

using namespace std;

void test01()
{
	//包含头文件
	//创建对象
	
	ifstream ifs;

	//打开并判断
	ifs.open("test.txt", ios::in);

	if (!ifs.is_open())
	{
		cout << "打开失败" << endl;
		return;
	}

	//读取数据
	 
	////第一种
	//char buf[1024] = { 0 };
	//while (ifs >> buf)
	//{
	//	cout << buf << endl;
	//}

	////第二种
	//char buf[1024] = { 0 };
	//while (ifs.getline(buf, sizeof(buf)))
	//{
	//	cout << buf << endl;
	//}

	////第三种
	//string buf;
	//while (getline(ifs, buf))
	//{
	//	cout << buf << endl;
	//}

	////第四种
	//char c;
	//while (c = ifs.get() != EOF)
	//{
	//	cout << c;
	//}


	//关闭
	ifs.close();
}


int main()
{
	test01();

	system("pause");

	return 0;
}
~~~



#### 5.3 写二进制文件

~~~c++
#include<iostream>
#include<fstream>

using namespace std;

class Person
{
public:

	char m_Name[64];
	int m_Age;
};

void test01()
{	 
	ofstream ofs;
	ofs.open("Person.txt", ios::out | ios::binary);
	//ofstream ofs("Person.txt", ios::out | ios::binary);

	Person p = { "张三",18 };
	ofs.write((const char*)&p, sizeof(Person));

	ofs.close();

}

int main()
{
	test01();

	system("pause");

	return 0;
}
~~~



#### 5.4 读二进制文件

~~~c++
#include<iostream>
#include<fstream>

using namespace std;

class Person
{
public:

	char m_Name[64];
	int m_Age;
};

void test01()
{
	ifstream ifs;

	ifs.open("Person.txt", ios::in | ios::binary);

	if (!ifs.is_open())
	{
		cout << "文件打开失败" << endl;
		return;
	}

	Person p;

	ifs.read((char*)&p, sizeof(Person));
	cout << "姓名:" << p.m_Name << "\n" << "年龄:" << p.m_Age << endl;

	ifs.close();
}

int main()
{
	test01();

	system("pause");

	return 0;
}
~~~







### 6 对象的初始化和清理

#### 6.1 构造函数和析构函数

~~~c++
#include<iostream>
#include<cstdlib>

using namespace std;

//构造函数和析构函数
//构造函数主要用于初始化
//析构函数主要用于进行清理
//构造函和析构函数没有返回类型也不用谢void
//函数名与类名相同


class Person
{
public:

	Person()
	{
		cout << "Persong构造数的调用" << endl;
	}

	~Person()
	{
		cout << "Person析构函数" << endl;
	}

};

void test01()
{
	Person p;
}

int main()
{
	test01();
	Person p1;

	system("pause");

	return 0;
}
~~~



#### 6.2 构造函数的分类和调用

~~~c++
#include<iostream>

using namespace std;

class Person
{
public:

	Person()
	{
		cout << "Persong构造数的调用" << endl;
	}
	Person(int a)
	{
		age = a;
		cout << "Persong有参构造数的调用" << endl;
	}

	Person(const Person& p)
	{
		age = p.age;
		cout << "Persong有参拷贝构造数的调用" << endl;
	}

	~Person()
	{
		cout << "Person析构函数" << endl;
	}

	int age;
};


void test01()
{
	//括号法
	Person p1;
	Person p2(10);
	Person p3(p2);

	//cout << "p2的年龄" << p2.age << endl;
	//cout << "p3的年龄" << p3.age << endl;
	
	//显示法
	Person p4;
	Person p5 = Person(10);
	Person p6 = Person(p5);

	//Person(10);//匿名对象
	//cout << "aaa" << endl;

	//隐式转换法
	Person p7 = 10;
	//相当于Person p7 = Person(10);
	Person P8 = p7;

}

int main()
{
	test01();


	system("pause");

	return 0;
}
~~~



#### 6.3 拷贝函数的调用

~~~c++
#include<iostream>

using namespace std;


class Person
{
public:
	Person()
	{
		cout << "Person默认构造函数调用" << endl;
	}

	Person(int age)
	{
		m_Age = age;
		cout << "Person有参构造函数调用" << endl;
	}

	Person(const Person& p)
	{
		m_Age = p.m_Age;
		cout << "Person拷贝构造函数调用" << endl;
	}

	~Person()
	{
		cout << "Person默认析构函数调用" << endl;
	}

	int m_Age;
};


void test01()
{
	Person p1(20);
	Person p2(p1);

	cout << "p1的年龄:" << p1.m_Age << endl;
	cout << "p2的年龄:" << p2.m_Age << endl;

}

void doWork(Person p)
{
	
}

void test02()
{
	Person p;
	doWork(p);
}

Person doWork2()
{
	Person p1;

	cout << (int*)&p1 << endl;

	return p1;
}

void test03()
{
	Person p = doWork2();
	cout << (int*)&p << endl;
}

int main()
{
	test01();

	cout << "aaaaaaaaa" << endl;

	test02();

	cout << "aaaaaaaaa" << endl;

	test03();

	system("pause");

	return 0;
}
~~~



#### 6.4 构造函数规则

~~~c++
#include<iostream>

using namespace std;

//默认情况下c++编译器会提供至少三个构造函数
//1.默认构造（空实现）
//2.构造函数（空实现）
//3.拷贝构造（值拷贝）

class Person
{
public:
	Person()
	{
		cout << "默认构造函数" << endl;
	}

	Person(int age)
	{
		m_Age = age;
		cout << "默认有参构造函数" << endl;
	}

	//Person(const Person& p)
	//{
	//	m_Age = p.m_Age;
	//	cout << "默认拷贝构造函数" << endl;
	//}

	~Person()
	{
		cout << "默认析构函数" << endl;
	}

	int m_Age;
};

void test01()
{
	Person p;
	p.m_Age = 18;

	cout << "p的年龄：" << p.m_Age << endl;

	Person p2(p);

	cout << "p2的年龄：" << p2.m_Age << endl;


}

void test02()
{
	Person p;
}

int main()
{
	//test01();

	test02();
	system("pause");

	return 0;
}
~~~



#### 6.5 深浅拷贝

~~~c++
#include<iostream>

using namespace std;

//深浅拷贝

class Person
{
public:
	Person()
	{
		cout << "Person的默认构造函数" << endl;
	}


	Person(int age, int height)
	{
		m_Age = age;
		m_Height = new int(height);
		cout << "Person的有参构造函数" << endl;
	}

	Person(const Person& p)
	{
		m_Age = p.m_Age;
		m_Height = p.m_Height;
		cout << "Person的拷贝构造函数" << endl;

		m_Height = new int(*p.m_Height);//深拷贝
	}

	~Person()
	{
		//用于释放堆区数据
		if (m_Height != nullptr)
		{
			delete m_Height;
			m_Height = nullptr;
		}

		cout << "Person的默认析构函数" << endl;
	}

	int m_Age;
	int* m_Height;
};

void test01()
{
	Person p1(18, 160);

	cout << "p1的年龄：" << p1.m_Age << endl;
	cout << "p1的身高：" << *p1.m_Height << endl;

	Person p2(p1);

	cout << "p2的年龄：" << p2.m_Age << endl;
	cout << "p2的身高：" << *p2.m_Height << endl;

}

int main()
{
	test01();

	system("pause");

	return 0;
}
~~~



#### 6.6 初始化列表

~~~c++
#include<iostream>

using namespace std;

class Person
{
public:
	////传统上初始化
	//Person(int a, int b, int c)
	//{
	//	m_A = a;
	//	m_B = b;
	//	m_C = c;
	//}

	//初始化列表的方式
	Person() :m_A(10), m_B(20), m_C(30)
	{

	}

	Person(int a,int b,int c) :m_A(a), m_B(b), m_C(c)
	{

	}

	int m_A;
	int m_B;
	int m_C;
};

void test01()
{
	//Person p1(11, 21, 31);
	//
	//cout << "m_A=" << p1.m_A << endl;
	//cout << "m_B=" << p1.m_B << endl;
	//cout << "m_C=" << p1.m_C << endl;

	Person p2(30, 20, 10);
	cout << "m_A=" << p2.m_A << endl;
	cout << "m_B=" << p2.m_B << endl;
	cout << "m_C=" << p2.m_C << endl;
}

int main()
{
	test01();

	system("pause");

	return 0;
}
~~~



#### 6.7 类对象成为类成员

~~~c++
#include<iostream>
#include<string>

using namespace std;

class Phone
{
public:

	Phone(string pName):m_Name(pName)
	{
		//m_Name = pName;
		cout << "手机的构造函数" << endl;
	}

	~Phone()
	{
		cout << "手机的析构函数" << endl;
	}

	string m_Name;
};

class Person
{
public:

	Person(string name, string pName) :m_Name(name), m_Phone(pName)
	{
		//Phone m_Phone = pName;
		cout << "人的构造函数" << endl;
	}

	~Person()
	{
		cout << "人的析构函数" << endl;
	}

	//姓名
	string m_Name;

	//手机
	Phone m_Phone;
};

void test01()
{
	Person p("张三", "苹果");

	cout << "姓名：" << p.m_Name << "手机:" << p.m_Phone.m_Name << endl;
}

int main()
{
	test01();

	system("pause");

	return 0;
}
~~~



#### 6.8 静态成员

~~~c++
#include<iostream>

using namespace std;

//静态成员函数
//所有对象共同享用一个函数
//静态的成员函数只能访问静态成员变量

class Person
{
public:
	//静态成员函数
	static void func()
	{
		m_A = 100;
		//m_B = 200;
		cout << "static void func()的调用" << endl;
	}

	static int m_A;
	int m_B;
};

void test01()
{
	Person p;
	p.func();

	Person::func();
	
}

int Person::m_A = 0;

int main()
{
	test01();

	system("pause");

	return 0;
}
~~~







### 7 C++对象模型和this指针

#### 7.1 成员变量和成员函数分开储存

~~~c++
#include<iostream>

using namespace std;

class Person
{
public:

	int m_A;

	static int m_B;


};

int Person::m_B = 0;

void test01()
{
	Person p;

	cout << "size of p =" << sizeof(p) << endl;
}

int main()
{
	test01();

	system("pause");

	return 0;
}
~~~



#### 7.2 this指针的概念

~~~c++
#include<iostream>

using namespace std;

//解决名称冲突

class Person
{
public:

	Person(int age)
	{
		m_Age = age;
	}

	Person& PersonAddAge(Person& p)
	{
		this->m_Age += p.m_Age;

		return *this;
	}

	int m_Age;
};

void test01()
{
	Person p1(18);

}

void test02()
{
	Person p1(10);

	Person p2(10);

	//链式编程思想   无限追加
	p2.PersonAddAge(p1).PersonAddAge(p1).PersonAddAge(p1);

	cout << "p2的年龄:" << p2.m_Age << endl;
}

int main()
{
	test01();

	test02();

	system("pause");

	return 0;
}
~~~



#### 7.3 空指针成员函数

~~~c++
#include<iostream>

using namespace std;

class Person
{
public:

	void showClassName()
	{
		cout << "this is Person class" << endl;
	}

	void showClassAge()
	{
		if (this == nullptr)
		{
			return;
		}


		cout << "age=" << m_Age << endl;
	}

	int m_Age;
};

void test01()
{
	Person* p = nullptr;

	p->showClassName();

	p->showClassAge();

}

int main()
{
	test01();

	system("pause");

	return 0;
}
~~~



#### 7.4 const修饰成员函数

~~~c++
#include<iostream>

using namespace std;

class Person
{
public:

	//this的本质是一个指针常量指针指向无法修改
	void showPerson() const
	{
		//m_A = 100;
	}

	int m_A;
};

void test01()
{
	Person p;

	p.showPerson();

}

int main()
{


	system("pause");

	return 0;
}
~~~





### 8 类和对象封装

#### 8.1 封装意义

~~~c++
#include<iostream>

using namespace std;

//将行为和属性包装
//设计一个圆的类
//求圆的周长

const double PI = 3.14;

class Cricle
{
	//权限
public:
	//属性
	//半径
	int m_r;

	//行为
	//获取周长
	double calculateC()
	{
		return 2 * PI * m_r;
	}
};

int main()
{
	//实例化
	Cricle c1;

	c1.m_r = 10;

	cout << "圆的周长:" << c1.calculateC() << endl;

	system("pause");

	return 0;
}
~~~



#### 8.2 封装按例

~~~c++
#include<iostream>
#include<string>

using namespace std;

//设计一个学生类
//有姓名有学号可以显示

class Student
{
public:
	//属性
	//姓名
	string m_Name;

	//学号
	int m_Id;
	//行为
	//显示
	void showStudent()
	{
		cout << "姓名：" << m_Name << "\t" << "学号" << m_Id << endl;
	}

	void setName(string name)
	{
		m_Name = name;
	}

	void setId(int id)
	{
		m_Id = id;
	}
};

int main()
{
	Student s1;

	s1.m_Name = "张三";
	s1.m_Id = 1;

	s1.showStudent();

	Student s2;

	s2.setName("李四");
	s2.setId(2);

	s2.showStudent();

	system("pause");

	return 0;
}
~~~



#### 8.3 封装权限

~~~c++
#include<iostream>
#include<string>

using namespace std;

//访问权限
//三种
//1.公共 public        成员 内可访问外也可以

//2.保护 protected     成员 内可访问外不可以

//3.私有 private       成员 内可访问外不可以


class Person
{
public:
	//公共权限
	//姓名
	string m_Name;

protected:
	//保护权限
	//汽车 
	string m_Car;

private:
	//私有权限
	int m_Password;


public:
	void func()
	{
		m_Name = "张三";
		m_Car = "拖拉机";
		m_Password = 123456;
	}

};

int main()
{
	Person p1;
	p1.m_Name = "李四";
	//p1.m_Car = "奔驰";
	//p1.m_Psaaword = 234567;

	p1.func();

	system("pause");

	return 0;
}

//struct 和 class 区别
//struct默认公共 public
//class默认私有  private
~~~



#### 8.4 封装私有化

~~~c++
#include<iostream>
#include<string>

using namespace std;

class Person
{
public:
	//设置姓名
	void setName(string name)
	{
		m_Name = name;
	}

	//获取姓名
	string getName()
	{
		return m_Name;
	}

	//获取年龄
	int getAge()
	{
		//m_Age = 0;
		return m_Age;
	}

	//设置年龄必须在0~150
	void setAge(int age)
	{
		if (age < 0 || age>150)
		{
			m_Age = 0;
			cout << "输入有误！" << endl;
			return;
		}
		m_Age = age;
	}

	//设置只写
	void setLover(string lover)
	{
		m_Lover = lover;
	}

private:
	//私有
	//姓名 可读可写
	string m_Name;

	//年龄 只读
	int m_Age;
	
	//情人 只写
	string m_Lover;
};

int main()
{
	Person p;

	p.setName("张三");
	cout << "姓名为：" << p.getName() << endl;
	//p.Age
	cout << "年龄为：" << p.getAge() << endl;

	p.setLover("李四");
	//cout << "情人：" << p.Lover << endl;

	p.setAge(1000);
	cout << "年龄为：" << p.getAge() << endl;

	p.setAge(18);
	cout << "年龄为：" << p.getAge() << endl;

	system("pause");

	return 0;
}
~~~



#### 8.5 设计案例类1

~~~c++
#include<iostream>
#include<cstdlib>

using namespace std;

//立方体设计类
//创建立方体
//设计属性和行为
//获取立方体的面积和体积

class Cube
{
public:

	//设置长
	void setL(int l)
	{
		m_L = l;
	}

	//获取长
	int getL()
	{
		return m_L;
	}

    //设置宽
	void setW(int w)
	{
		m_W = w;
	}
	
	//获取宽
	int getW()
	{
		return m_W;
	}

	//设置高
	void setH(int h)
	{
		m_H = h;
	}

	//获取高
	int getH()
	{
		return m_H;
	}

	//获取立方体面积
	int calculateS()
	{
		return 2 * m_L * m_W + 2 * m_H * m_W + 2 * m_L * m_H;
	}

	//获取立方体体积
	int calculateV()
	{
		return m_L * m_W * m_H;
	}

	bool isSameByClass(Cube &c)
	{
		if (m_L == c.getL() && m_W == c.getW() && m_H == c.getH())
		{
			return true;
		}

		return false;
	}


private:

	//长
	int m_L;

	//宽
	int m_W;

	//高
	int m_H;

};

//利用全局函数判断
bool isSame(Cube& c1, Cube& c2)
{
	if (c1.getL() == c2.getL() && c1.getW() == c2.getW() && c1.getH() == c2.getH())
	{
		return true;
	}

	return false;
}

int main()
{

	Cube c1;
	c1.setL(10);
	c1.setW(10);
	c1.setH(10);


	cout << "c1的面积" << c1.calculateS() << endl;
	cout << "c1的体积" << c1.calculateV() << endl;

	Cube c2;
	c2.setL(10);
	c2.setW(10);
	c2.setH(10);


	cout << "c2的面积" << c2.calculateS() << endl;
	cout << "c2的体积" << c2.calculateV() << endl;

	bool ret = isSame(c1, c2);
	if (ret)
	{
		cout << "c1和c2相等" << endl;
	}
	else
	{
		cout << "c1和c2不相等" << endl;
	}

	bool rec = c1.isSameByClass(c2);
	if (rec)
	{
		cout << "c1和c2相等" << endl;
	}
	else
	{
		cout << "c1和c2不相等" << endl;
	}


	system("pause");

	return 0;
}
~~~



#### 8.6 设计案例类2

~~~c++
#include<iostream>
#include"Point.h"
#include"Cricle.h"

using namespace std;

点和圆的关系
设计类以及点和圆的关系


//点类
class Point
{

public:
	//设置X
	void setX(int x)
	{
		m_X = x;
	}

	//获取X
	int getX()
	{
		return m_X;
	}

	//设置Y
	void setY(int y)
	{
		m_Y = y;
	}

	//获取Y
	int getY()
	{
		return m_Y;
	}


private:

	int m_X;

	int m_Y;

};

点类
	设置X
void Point::setX(int x)
{
	m_X = x;
}

获取X
int Point::getX()
{
	return m_X;
}

设置Y
void Point::setY(int y)
{
	m_Y = y;
}

获取Y
int Point::getY()
{
	return m_Y;
}


//圆类
class Cricle
{
public:

	//设置
	void setR(int r)
	{
		m_R = r;
	}

	//获取
	int getR()
	{
		return m_R;
	}

	//设置
	void setCenter(Point center)
	{
		m_Center = center;
	}

	//获取
	Point getCenter()
	{
		return m_Center;
	}


private:

	int m_R;//半径

	Point m_Center;//圆心
	//注意在类中可以让另一个类作为本类中的成员

};

圆类
	设置
void Cricle::setR(int r)
{
	m_R = r;
}

获取
int Cricle::getR()
{
	return m_R;
}

设置
void Cricle::setCenter(Point center)
{
	m_Center = center;
}

获取
Point Cricle::getCenter()
{
	return m_Center;
}


判断关系全局函数
void isInCricle(Cricle& c, Point& p)
{
	计算两点之间距离 平方
	int distance =
		(c.getCenter().getX() - p.getX()) * (c.getCenter().getX() - p.getX()) + (c.getCenter().getY() - p.getY()) * (c.getCenter().getY() - p.getY());

	计算半径的平方
	int rdistance = c.getR() * c.getR();

	判断关系
	if (distance == rdistance)
	{
		cout << "点在圆上" << endl;
	}
	else if (distance > rdistance)
	{
		cout << "点在圆外" << endl;
	}
	else
	{
		cout << "点在圆内" << endl;
	}

}

int main()
{
	创建点和圆
	Cricle c;
	c.setR(10);

	Point center;
	center.setX(10);
	center.setY(0);
	c.setCenter(center);

	创建点
	Point p;
	p.setX(10);
	p.setY(10);

	Point p1;
	p1.setX(10);
	p1.setY(11);

	Point p2;
	p2.setX(10);
	p2.setY(9);

	判断关系
	isInCricle(c, p);
	isInCricle(c, p1);
	isInCricle(c, p2);


	system("pause");

	return 0;
}
~~~





### 9 类和对象继承

#### 9.1 基本语法

~~~c++
#include<iostream>

using namespace std;

////java举例
//class Java
//{
//public:
//	void header()
//	{
//		cout << "首页、公开课、登录注册....（登录注册）" << endl;
//	}
//
//	void footer()
//	{
//		cout << "帮助中心、交流合作、站内地图....（公共底部）" << endl;
//	}
//
//	void left()
//	{
//		cout << "Java、Python、C++、...(公共分类页表)" << endl;
//	}
//
//	void content()
//	{
//		cout << "Java学科视频" << endl;
//	}
//
//};
//
////Python的视频
//class Python
//{
//public:
//	void header()
//	{
//		cout << "首页、公开课、登录注册....（登录注册）" << endl;
//	}
//
//	void footer()
//	{
//		cout << "帮助中心、交流合作、站内地图....（公共底部）" << endl;
//	}
//
//	void left()
//	{
//		cout << "Java、Python、C++、...(公共分类页表)" << endl;
//	}
//
//	void content()
//	{
//		cout << "Python学科视频" << endl;
//	}
//
//};
//
////c++页面
////Python的视频
//class Cpp
//{
//public:
//	void header()
//	{
//		cout << "首页、公开课、登录注册....（登录注册）" << endl;
//	}
//
//	void footer()
//	{
//		cout << "帮助中心、交流合作、站内地图....（公共底部）" << endl;
//	}
//
//	void left()
//	{
//		cout << "Java、Python、C++、...(公共分类页表)" << endl;
//	}
//
//	void content()
//	{
//		cout << "C++学科视频" << endl;
//	}
//
//};

//继承

//公共部分
class BasePage
{
public:
	void header()
	{
		cout << "首页、公开课、登录注册....（登录注册）" << endl;
	}

	void footer()
	{
		cout << "帮助中心、交流合作、站内地图....（公共底部）" << endl;
	}

	void left()
	{
		cout << "Java、Python、C++、...(公共分类页表)" << endl;
	}
};


//语法：class 子类 ： 继承方式 父类
// 子类 也叫 派生类 
// 父类 也叫 基类
//Java举例
class Java :public BasePage
{
public:
	void content()
	{
		cout << "Java学科视频" << endl;
	}
};

//Python举例
class Python :public BasePage
{
public:
	void content()
	{
		cout << "Python学科视频" << endl;
	}
};

//C++举例
class Cpp :public BasePage
{
public:
	void content()
	{
		cout << "C++学科视频" << endl;
	}
};

void test01()
{
	cout << "Java的下载视频" << endl;

	Java ja;
	ja.header();
	ja.footer();
	ja.left();
	ja.content();

	cout << "Python的下载视频" << endl;

	Python py;
	py.header();
	py.footer();
	py.left();
	py.content();

	cout << "C++的下载视频" << endl;

	Cpp cpp;
	cpp.header();
	cpp.footer();
	cpp.left();
	cpp.content();
}

int main()
{
	test01();

	system("pause");

	return 0;
}
~~~



#### 9.2 继承方式

~~~c++
#include<iostream>

using namespace std;

//继承方式
//公共继承
class Base1
{
public:
	int m_A;

protected:
	int m_B;

private:
	int m_C;
};

class Son :public Base1
{
public:

	void func()
	{
		m_A = 10;  //父类中公共权限 继承之后还是公共的权限
		m_B = 10;  //父类中保护权限 继承之后还是保护的权限
		//m_C = 10;
	}
};

class Base2
{
public:
	int m_A;

protected:
	int m_B;

private:
	int m_C;
};

class Son2 :protected Base2
{
public:
	void func()
	{
		m_A = 10;  //父类中公共权限 继承之后变为保护的权限
		m_B = 10;  //父类中保护权限 继承之后还是保护的权限
		//m_C = 10; 私有成员还是访问不到
	}
};


class Base3
{
public:
	int m_A;

protected:
	int m_B;

private:
	int m_C;
};

class Son3 :private Base3
{
public:
	void func()
	{
		m_A = 10;  //变为私有
		m_B = 10;  //变为私有
		//m_C = 10; 私有成员还是访问不到
	}
};

class GrandSon3 :public Son3
{
public:
	void func()
	{
		//m_A = 10;  变为私有
		//m_B = 10;  变为私有
		//m_C = 10; 私有成员还是访问不到
	}
};

void test01()
{
	Son s1;
	s1.m_A = 100;
	//s1.m_B = 100; 还是保护权限访问不了
}

void test02()
{
	Son2 s2;
	//s2.m_A = 100; 
}

void test03()
{
	Son3 s3;
	//s3.m_A = 100;  都变成私有均访问不到
	//s3.m_B = 100;
	//s3.m_B = 100;
}

int main()
{

	system("pause");

	return 0;
}
~~~



#### 9.3 继承中的对象模型

~~~c++
#include<iostream>

using namespace std;

class Base
{
public:
	int m_A;

protected:
	int m_B;

private:
	int m_C;

};

class Son :public Base
{
public:

	int m_D;
};

void test01()
{

	cout << "size of Son = " << sizeof(Son) << endl;
}

int main()
{
	test01();

	system("pause");

	return 0;
}
~~~



#### 9.4 继承中的构造析构顺序

~~~c++
#include<iostream>

using namespace std;

class Base
{
public:
	Base()
	{
		cout << "Base的构造函数" << endl;
	}

	~Base()
	{
		cout << "Base的析构函数" << endl;
	}
};

class Son :public Base
{
public:
	Son()
	{
		cout << "Son的构造函数" << endl;
	}

	~Son()
	{
		cout << "Son的析构函数" << endl;
	}
};

void test01()
{
	Son s;
}

int main()
{
	test01();

	system("pause");

	return 0;
}
~~~



#### 9.5 继承中同名成员处理方式

~~~c++
#include<iostream>

using namespace std;

class Base
{
public:
	Base()
	{
		m_A = 100;
	}

	void func()
	{
		cout << "Base-func 的调用" << endl;
	}

	int m_A;
};

class Son :public Base
{
public:

	Son()
	{
		m_A = 200;
	}

	void func()
	{
		cout << "Son-func 的调用" << endl;
	}

	int m_A;
};

void test01()//同名成员属性
{
	Son s;
	cout << "Son  下面的" << s.m_A << endl;// 直接调用子类
	cout << "Base 下面的" << s.Base::m_A << endl;//加作用域访问父类

}

void test02()//同名成员函数
{
	Son s;

	s.func();//直接子类
	s.Base::func();//作用域父类
}

int main()
{
	test01();

	test02();


	system("pause");

	return 0;
}

//子类会隐藏所有父类中的同名函数除非加作用域访问父类
~~~



#### 9.6 继承同名静态成员处理方式

~~~c++
#include<iostream>

using namespace std;

class Base
{
public:

	static int m_A;

};

class Son :public Base
{
public:

	static int m_A;

};

int Base::m_A = 100;
int Son::m_A = 200;

void test01()
{
	Son s;

	cout << "通过类名访问" << endl;
	cout << "Son  下面的" << s.m_A << endl;// 直接调用子类
    cout << "Base 下面的" << s.Base::m_A << endl;//加作用域访问

	cout << "通过类名访问" << endl;
	cout << "Son  下面的" << Son::m_A << endl;
	cout << "Base 下面的" << Son::Base::m_A << endl;
}

int main()
{
	test01();

	system("pause");

	return 0;
}
~~~



#### 9.7 多继承语法

~~~c++
#include<iostream>

using namespace std;

class Base1
{
public:

	Base1()
	{
		m_A = 100;
		m_E = 600;
	}

	int m_A;
	int m_E;
};

class Base2
{
public:

	Base2()
	{
		m_B = 200;
		m_E = 700;
	}

	int m_B;
	int m_E;
};

class Son :public Base1, public Base2
{
public:

	Son()
	{
		m_C = 300;
		m_D = 400;
	}

	int m_C;
	int m_D;
};

void test01()
{
	Son s;

	cout << "sizeof多大" << sizeof(s) << endl;
	cout << "Base1中的m_A" << s.m_A << endl;
	cout << "Base1中的m_E" << s.Base1::m_E << endl;
	cout << "Base2中的m_E" << s.Base2::m_E << endl;

}

int main()
{
	test01();

	system("pause");

	return 0;
}
~~~



#### 9.8 菱形继承

~~~c++
#include<iostream>

using namespace std;

class Animal
{
public:

	int m_Age;
};

//继承之前加上virtual
//虚继承

class Ma :virtual public Animal {};

class Lv :virtual public Animal {};

class Luo:public Ma,public Lv{};

void test01()
{
	Luo luo;

	luo.Ma::m_Age = 18;
	luo.Lv::m_Age = 28;

	cout << "Ma里面继承的" << luo.Ma::m_Age << endl;
	cout << "Lv里面继承的" << luo.Lv::m_Age << endl;
	cout << "Luo里面继承的" << luo.m_Age << endl;


}

int main()
{
	test01();

	system("pause");

	return 0;
}

// Vbptr ----- vbtable
// v - virtual
// b - base
// ptr - pointer
//
~~~






### 10 类和对象多态

#### 10.1 多态的基本概念

~~~c++
#include<iostream>

using namespace std;

class Animal
{
public:

	virtual void speak()
	{
		cout << "动物可以叫" << endl;
	}
};

class Cat :public Animal
{
public:

	void speak()
	{
		cout << "小猫叫" << endl;
	}
};

class Dog :public Animal
{
public:

	void speak()
	{
		cout << "小狗叫" << endl;
	}
};

void doSpeak(Animal& animal)
{
	animal.speak();
}

void test01()
{
	Cat cat;
	doSpeak(cat);

	Dog dog;
	doSpeak(dog);
}

int main()
{
	test01();

	system("pause");

	return 0;
}
~~~



#### 10.2 多态按例计算器

~~~c++
#include<iostream>
#include<string>

using namespace std;

class Calculator
{
public:

	int getResult(string oper)
	{
		if (oper == "+")
		{
			return m_Num1 + m_Num2;
		}
		else if (oper == "-")
		{
			return m_Num1 - m_Num2;
		}
	}

	// 如果扩展新功能需要修改源码
	// 开闭原则
	// 开发进行开放 修改进行关闭

	int m_Num1;
	int m_Num2;
};

void test01()
{
	Calculator c;
	c.m_Num1 = 10;
	c.m_Num2 = 10;

	cout << c.m_Num1 << "+" << c.m_Num2 << "=" << c.getResult("+") << endl;
	cout << c.m_Num1 << "-" << c.m_Num2 << "=" << c.getResult("-") << endl;
}

class AbstractCalculator
{
public:

	virtual int getResult()
	{
		return 0;
	}

	int m_Num1;
	int m_Num2;
};

// 加法计算
class AddCalculator :public AbstractCalculator
{
public:

	virtual int getResult()
	{
		return m_Num1 + m_Num2;
	}
};

class SubCalculator :public AbstractCalculator
{
public:

	virtual int getResult()
	{
		return m_Num1 - m_Num2;
	}
};

void test02()
{
	// 多态的使用
	//父类的指针或者引用指向子类对象

	AbstractCalculator* abc = new AddCalculator;
	abc->m_Num1 = 10;
	abc->m_Num2 = 10;
	cout << abc->m_Num1 << "+" << abc->m_Num2 << "=" << abc->getResult() << endl;
	delete abc;

	abc = new SubCalculator;
	abc->m_Num1 = 10;
	abc->m_Num2 = 10;
	cout << abc->m_Num1 << "-" << abc->m_Num2 << "=" << abc->getResult() << endl;
	delete abc;
}

int main()
{
	test01();

	test02();

	system("pause");

	return 0;
}
~~~



#### 10.3 纯虚函数和抽象类

~~~c++
#include<iostream>

using namespace std;

class Base
{
public:

	// 纯虚函数
	// 只要有一个纯虚函数就是抽象类
	// 抽象类特点
	//1.无法实例化对象
	//2.抽象类的子类必须重写父类中的纯虚函数 否则也为抽象类
	virtual void func() = 0;
};

class Son :public Base
{
public:

	virtual void func()
	{
		cout << "func调用" << endl;
	}
};

void test01()
{
	Base* base = new Son;
	base->func();
}

int main()
{
	test01();

	system("pause");

	return 0;
}
~~~



#### 10.4 按例2制作饮品

~~~c++
#include<iostream>

using namespace std;

class AbstractDrinking
{
public:

	//煮水
	virtual void Boil() = 0;

	//冲泡
	virtual void Brew() = 0;

	//倒入杯中
	virtual void PoutInCup() = 0;

	//加入辅料
	virtual void PoutSomething() = 0;

	//制作
	void makeDrink()
	{
		Boil();
		Brew();
		PoutInCup();
		PoutSomething();
	}
};

class Coffee :public AbstractDrinking
{
public:

	//煮水
	virtual void Boil()
	{
		cout << "农夫山泉" << endl;
	}

	//冲泡
	virtual void Brew()
	{
		cout << "冲泡咖啡" << endl;
	}

	//倒入杯中
	virtual void PoutInCup()
	{
		cout << "倒入咖啡杯中" << endl;
	}

	//加入辅料
	virtual void PoutSomething()
	{
		cout << "加入奶和糖" << endl;
	}
};

class Tea :public AbstractDrinking
{
public:

	//煮水
	virtual void Boil()
	{
		cout << "矿泉水" << endl;
	}

	//冲泡
	virtual void Brew()
	{
		cout << "冲泡茶叶" << endl;
	}

	//倒入杯中
	virtual void PoutInCup()
	{
		cout << "倒入玻璃杯中" << endl;
	}

	//加入辅料
	virtual void PoutSomething()
	{
		cout << "加入柠檬" << endl;
	}
};

void doWork(AbstractDrinking* abs)
{
	abs->makeDrink();

	cout << "------------------" << endl;
	
	delete abs;
}

void test01()
{
	doWork(new Coffee);

	doWork(new Tea);

}

int main()
{
	test01();

	system("pause");

	return 0;
}
~~~



#### 10.5 虚析构和纯虚析构

~~~c++
#include<iostream>
#include<string>

using namespace std;

class Animal
{
public:

	Animal()
	{
		cout << "Animal的构造函数调用" << endl;
	}

	virtual ~Animal()
	{
		cout << "Animal的析构函数调用" << endl;
	}

	//virtual ~Animal() = 0;

	virtual void speak() = 0;
};

//纯虚析构
//Animal::~Animal()
//{
//	cout << "Animal的析构函数调用" << endl;
//}

class Cat :public Animal
{
public:

	Cat(string name)
	{
		cout << "Cat构造函数调用" << endl;
		m_Name = new string(name);
	}

	virtual void speak()
	{
		cout << *m_Name << "小猫说话" << endl;
	}

	~Cat()
	{
		if (m_Name != nullptr)
		{
			cout << "Cat的析构函数调用" << endl;
			delete m_Name;
			m_Name = nullptr;
		}
	}

	string* m_Name;
};

void test01()
{
	Animal* animal = new Cat("Tom");
	animal->speak();
	delete animal;
}


int main()
{
	test01();

	system("pause");

	return 0;
}
~~~



#### 10.6 按例3电脑组装

~~~c++
#include<iostream>

using namespace std;

//抽象类
//CPU
class CPU
{
public:

	//计算函数
	virtual void calculate() = 0;
};

class VideoCard
{
public:

	//显示函数
	virtual void display() = 0;
};

class Memory
{
public:

	//内存函数
	virtual void storage() = 0;
};

//电脑类
class Computer
{
public:
	Computer(CPU* cpu, VideoCard* vc, Memory* mem)
	{
		m_cpu = cpu;
		m_vc = vc;
		m_mem = mem;
	}

	//工作函数
	void work()
	{
		//调用接口
		m_cpu->calculate();

		m_vc->display();

		m_mem->storage();

		cout << "----------" << endl;
	}

	~Computer()
	{
		if (m_cpu != nullptr)
		{
			delete m_cpu;
			m_cpu = nullptr;
		}

		if (m_vc != nullptr)
		{
			delete m_vc;
			m_vc = nullptr;
		}

		if (m_mem != nullptr)
		{
			delete m_mem;
			m_mem = nullptr;
		}
	}

private:
	CPU* m_cpu;
	VideoCard* m_vc;
	Memory* m_mem;
};

//具体厂商
class IntelCPU :public CPU
{
public:

	virtual void calculate()
	{
		cout << "Intel的cpu开始计算" << endl;
	}
};

class IntelVideoCard :public VideoCard
{
public:

	virtual void display()
	{
		cout << "Intel的显卡开始显示" << endl;
	}
};

class IntelMenory :public Memory
{
public:

	virtual void storage()
	{
		cout << "Intel的内存开始存储" << endl;
	}
};


//Lenovo
class LenovoCPU :public CPU
{
public:

	virtual void calculate()
	{
		cout << "Lenovo的cpu开始计算" << endl;
	}
};

class LenovoVideoCard :public VideoCard
{
public:

	virtual void display()
	{
		cout << "Lenovo的显卡开始显示" << endl;
	}
};

class LenovoMenory :public Memory
{
public:

	virtual void storage()
	{
		cout << "Lenovo的内存开始存储" << endl;
	}
};

void test01()
{
	//创建零件
	CPU* intelCPU = new IntelCPU;
	VideoCard* intelCard = new IntelVideoCard;
	Memory* intelMen = new IntelMenory;

	//创建第一台电脑
	Computer* computer1 = new Computer(intelCPU, intelCard, intelMen);
	computer1->work();
	delete computer1;

	//创建第二台电脑
	Computer* computer2 = new Computer(new LenovoCPU, new LenovoVideoCard, new LenovoMenory);
	computer2->work();
	delete computer2;

	//创建第三台电脑
	Computer* computer3 = new Computer(new IntelCPU, new LenovoVideoCard, new IntelMenory);
	computer3->work();
	delete computer3;
}

int main()
{
	test01();

	system("pause");

	return 0;
}
~~~







# 第三部分 C++高级



## C++泛型编程和模板

### 1.模板

#### 1.1 模板的概念

提高复用性ppt模板，word模板等

不能直接去用需要修改

只是一个框架

通用性很强但不是万能



#### 1.2 模板函数

+ c++中**面向对象**思想和**泛型编程**
+ c++提供两种模板**函数模板**和**类模板**



##### 1.2.1 函数模板语法

~~~c++
template<typname T>
//函数的声明或定义
~~~

解释：

template  ---  声明创建模板

typname  ---  表明其后面的符号是一种数据类型，可以用class替代

T  ---  通用数据类型，名称可以替换，通常为大写字母

~~~c++
#include<iostream>
#include<cstdlib>

using namespace std;

//函数模板

//交换两个整形交换
void swapInt(int& a, int& b)
{
    int temp = a;
    a = b;
    b = temp;
}

//交换两个整形交换
void swapDouble(double& a, double& b)
{
    double temp = a;
    a = b;
    b = temp;
}

void test01()
{
    int a = 10;
    int b = 20;

    swapInt(a, b);
    cout << "a = " << a << endl;
    cout << "b = " << b << endl;

    double c = 1.1;
    double d = 2.2;

    swapDouble(c, d);
    cout << "c = " << c << endl;
    cout << "d = " << d << endl;
}

int main()
{
    test01();

    system("pause");

    return 0;
}
~~~



~~~c++
//函数模板
template<typename T>
void mySwap(T& a, T& b)
{
    T temp = a;
    a = b;
    b = temp;
}
~~~

模板有两种使用方法

1. 自动推导

~~~c++
void test02()
{
	int a = 10;
	int b = 20;

	mySwap(a, b);
	cout << "a = " << a << endl;
	cout << "b = " << b << endl;
}
~~~

2. 显示指定类型

~~~c++
void test03()
{
	int a = 10;
	int b = 20;

	mySwap<int>(a, b);
	cout << "a = " << a << endl;
	cout << "b = " << b << endl;
}
~~~



##### 1.2.2 函数模板注意事项

+ 自动推导必须明确T的类型
+ 切类型明确

~~~c++
template<typename T>
void mySwap(T& a, T& b)
{
	T temp = a;
	a = b;
	b = temp;
}

void test01()
{
	int a = 10;
	int b = 20;
    int char = 'c';

	mySwap(a, b);
    //mySwap(a, c);
	cout << "a = " << a << endl;
	cout << "b = " << b << endl;
}

template<typename T>
void func()
{
	cout << "func的调用" << endl;
}

void test02()
{
	func<int>();
}
~~~

使用模板时必须确定数据类型切统一



##### 1.2.3 函数模板按例

+ 利用函数模板封装一个排序

~~~c++
#include<iostream>

using namespace std;

//从大到小int和char

//交换
template<typename T>
void mySwap(T& a, T& b)
{
	T temp = a;
	a = b;
	b = temp;
}

//排序模板
template<typename T>
void mySort(T arr[], int len)
{
	for (int i = 0; i < len; i++)
	{
		int max = i;
		for (int j = i + 1; j < len; j++)
		{
			if (arr[max] < arr[j])
			{
				max = j;
			}
		}
		if (max != i)
		{
			mySwap(arr[max], arr[i]);
		}
	}
}

//打印输出
template<typename T>
void printArray(T arr[], int len)
{
	for (int i = 0; i < len; i++)
	{
		cout << arr[i] << " ";
	}
	cout << endl;
}

//字符测试
void test01()
{
	char charArr[] = "abcdefgh";

	int num = sizeof(charArr) / sizeof(char);

	mySort(charArr, num);

	printArray(charArr, num);

}

//int测试
void test02()
{
	int intArr[] = { 1,2,3,4,5,6 };

	int num = sizeof(intArr) / sizeof(int);

	mySort(intArr, num);

	printArray(intArr, num);
}

int main()
{
	test01();
	test02();

	system("pause");

	return 0;
}
~~~



##### 1.2.4 普通函数和函数模板区别

+ 自动类型推导可以发生隐式类型转换
+ 显示指定类型可以发生隐式类型转换
+ 普通函数可以发生类型转换

~~~c++
#include<iostream>

using namespace std;

int add(int a, int b)
{
	return a + b;
}

void test01()
{
	int a = 10;
	int b = 20;
	char c = 'a';

	cout << add(a, b) << endl;
	cout << add(a, c) << endl;
}

int main()
{
	test01();

	system("pause");

	return 0;
}
~~~

模板

~~~c++
template<typename T>
T add02(T a, T b)
{
	return a + b;
}

void test02()
{
	int a = 10;
	int b = 20;
	char c = 'a';

	cout << add02(a, b) << endl;
	//cout << add02(a, c) << endl;
    cout << add02<int>(a, b) << endl;
}
~~~



##### 1.2.5 普通函数和函数模板的调用规则

1. 优先调用普通函数
2. 可以用**空模板参数列表**强制调用函数模板
3. 函数模板可以发生重载
4. 如果函数模板可以跟好的匹配则优先调用函数模板

~~~c++
#include<iostream>

using namespace std;

void print(int a, int b)
{
	cout << "普通函数调用" << endl;
}

template<typename T>
void print(T a, T b)
{
	cout << "函数模板调用" << endl;
}

void test01()
{
	int a = 10;
	int b = 20;

	print(a, b);
}

int main()
{
	test01();

	system("pause");

	return 0;
}
~~~

空模板强制调用

~~~c++
void test02()
{
	int a = 10;
	int b = 20;

	print<>(a, b);
}
~~~

重载模板

~~~c++
template<typename T>
void print(T a, T b, T c)
{
	cout << "函数模板abc调用" << endl;
}

void test03()
{
	int a = 10;
	int b = 20;
	int c = 30;

	print(a, b, c);
}
~~~

更好的匹配

~~~c++
void test04()
{
	char a = 'a';
	char b = 'b';

	print(a, b);
}
~~~



##### 1.2.6 模板的局限性

~~~c++
template<typename T>
void t(T a, T b)
{
	a = b;
}
~~~

数组或者比大小

有一定局限性并不是万能的

有些需要具体化方式做特殊实现

~~~c++
#include<iostream>
#include<string>
#include<cstdbool>

using namespace std;

class Person
{
public:

	Person(string name,int age)
	{
		this->m_name = name;
		this->m_age = age;
	}

	string m_name;

	int m_age;
};

template<typename T>
bool myCompare(T& a, T& b)
{
	if (a == b)//可以重载==
	{
		return true;
	}
	else
	{
		return false;
	}
}

void test01()
{
	int a = 10;
	int b = 20;

	bool ret = myCompare(a, b);

	if (ret)
	{
		cout << "a=b" << endl;
	}
	else
	{
		cout << "a!=b" << endl;
	}
}

void test02()
{
	Person p1("Tom", 10);
	Person p2("Tom", 10);

	bool ret = myCompare(p1, p2);

	if (ret)
	{
		cout << "p1=p2" << endl;
	}
	else
	{
		cout << "p1!=p2" << endl;
	}
}

int main()
{
	test01();
	test02();

	system("pause");

	return 0;
}
~~~

利用重载

~~~c++
//利用具体化Person重载
template<> bool myCompare(Person& p1, Person& p2)
{
	if (p1.m_name == p2.m_name && p2.m_age == p2.m_age)
	{
		return true;
	}
	else
	{
		return false;
	}
}
~~~



#### 1.3 类模板

##### 1.3.1 类模板的基本语法

~~~c++
template<class T>
//类
~~~

后面紧跟一个类

~~~c++
#include<iostream>
#include<string>
#include<cstdbool>

using namespace std;

template<class NameType,class AgeType>
class Person
{
public:

	Person(NameType name,AgeType age)
	{
		this->m_Name = name;
		this->m_Age = age;
	}

	void showPerson()
	{
		cout << "姓名：" << this->m_Name << endl;
		cout << "年龄：" << this->m_Age << endl;
	}

	NameType m_Name;
	AgeType m_Age;
};

void test01()
{
	Person<string, int> p1("张三", 18);

	p1.showPerson();
}

int main()
{
	test01();


	system("pause");

	return 0;
}
~~~

这个类称为类模板



##### 1.3.2 类模板与函数模板的区别

+ 类模板没有自动推导类型
+ 类模板在模板参数列表中可以有默认参数

~~~c++
void test01()
{
	Person p1("zhangsna", 18);//不能自动推导
}
~~~

尖括号里面可有有默认的参数

~~~c++
template<class NameType,class AgeType = int>
    
void test01()
{
	Person<string> p1("zhangsna", 18);
}
~~~



##### 1.3.3 类模板中成员函数创建的时机

+ 普通类成员函数一开始就创建
+ 类模板中的成员函数调用时才会创建

~~~c++
#include<iostream>
#include<string>
#include<cstdbool>

using namespace std;

class Person1
{
public:

	void showPerson1()
	{
		cout << "Person1de" << endl;
	}
};

class Person2
{
public:

	void showPerson2()
	{
		cout << "Person2de" << endl;
	}
};

template<class T>
class myClass
{
public:

	T obj;

	void func1()
	{
		obj.showPerson1();
	}

	void func2()
	{
		obj.showPerson2();
	}

};

void test01()
{
	myClass<Person1> m;

	m.func1();

	//m.func2();

}

int main()
{
	test01();


	system("pause");

	return 0;
}
~~~



##### 1.3.4 类模板对象做函数参数

类模板实例化出的参数，向函数传递参数

一共有三种方式：

1. 指定传入类型
2. 参数模板化
3. 整个类模板化

第一种

~~~c++
#include<iostream>
#include<string>
#include<cstdlib>

using namespace std;

template<class T1,class T2>
class Person
{
public:

	Person(T1 name, T2 age)
	{
		this->m_Name = name;
		this->m_Age = age;
	}

	void showPerson()
	{
		cout << "姓名：" << this->m_Name << endl;
		cout << "年龄：" << this->m_Age << endl;
	}

	T1 m_Name;
	T2 m_Age;
};

void printPerson1(Person<string, int>& p)
{
	p.showPerson();
}

void test01()
{
	Person<string, int> p("张三", 18);

	printPerson1(p);
}

int main()
{
	test01();
	test02();
	test03();


	system("pause");

	return 0;
}
~~~



第二种

~~~C++
template<class T1,class T2>
void printPerson2(Person<T1, T2>& p)
{
	p.showPerson();
	cout << "T1的类型" << typeid(T1).name() << endl;
	cout << "T2的类型" << typeid(T2).name() << endl;
}

void test02()
{
	Person<string, int> p2("李四", 19);

	printPerson2(p2);
}
~~~



第三种

~~~C++
template<class T>
void printPerson3(T& p)
{
	p.showPerson();
	cout << "T的类型" << typeid(T).name() << endl;
}

void test03()
{
	Person<string, int> p3("王五", 20);

	printPerson3(p3);
}
~~~



第一种最常用

函数模板配合类模板



typeid（名称）.name（）---返回类型名称的名称

##### 1.3.5 类模板与继承

+ ==当子类继承的父类是一个类模板的时候要指定父类中的T的类型==
+ 如果不指定编译器无法分配内存
+ 子类有些时候也需要变成类模板

~~~c++
#include<iostream>
#include<string>
#include<cstdlib>

using namespace std;

template<class T>
class Base
{
public:

	T m;
};

void test01()
{
	Son s1;
}

//灵活运用子类也变成类模on2<int, char> s2;
}

int main()
{
	test01();

	system("pause");

	return 0;
}
~~~



~~~c++
template<class T1,class T2>
class Son2 :public Base<T2>
{
	T obj;
};

void test02()
{
	Son2<int, char> s2;
}
~~~

int传给T1char传给T2



##### 1.3.6 类模板成员函数类外实现

类模板中成员函数的类外实现

~~~c++
#include<iostream>
#include<string>
#include<cstdlib>

using namespace std;

template<class T1,class T2>
class Person
{
public:

	Person(T1 name, T2 age);

	void showPerson();

	T1 m_Name;
	T2 m_Age;
};

//构造函数的类外实现
template<class T1, class T2>
Person<T1, T2>::Person(T1 name, T2 age)
{
	this->m_Name = name;
	this->m_Age = age;
}

template<class T1, class T2>
void Person<T1, T2>::showPerson()
{
	cout << "姓名" << this->m_Name << endl;
	cout << "年龄" << this->m_Age << endl;
}

void test01()
{
	Person<string, int> p1("张三", 18);
    
    p1.showPerson();
}

int main()
{
	test01();

	system("pause");

	return 0;
}
~~~



##### 1.3.7 类模板份文件填写

类模板中成员函数创建的时机是在调用阶段，所以在分文件编写时是连接不到的

+ 两种解决方法
+ 直接包含源文件.cpp
+ 将声明和实现写在同一文件中改为.hpp

头文件中

~~~c++
#pragma once
#include<iostream>
#include<string>
#include<cstdlib>

using namespace std;

template<class T1, class T2>
class Person
{
public:

	Person(T1 name, T2 age);

	void showPerson();

	T1 m_Name;
	T2 m_Age;
};
~~~

源文件中

~~~c++
#include"person.h"

using namespace std;

template<class T1, class T2>
Person<T1, T2>::Person(T1 name, T2 age)
{
	this->m_Name = name;
	this->m_Age = age;
}

template<class T1, class T2>
void Person<T1, T2>::showPerson()
{
	cout << "姓名" << this->m_Name << endl;
	cout << "年龄" << this->m_Age << endl;
}
~~~

主程序

~~~c++
#include<iostream>

using namespace std;

//直接包含源文件cpp
#include"person.cpp"

void test01()
{
	Person<string, int> p1("张三", 28);

	p1.showPerson();
}

int main()
{
	test01();

	system("pause");

	return 0;
}
~~~



+ 第二种方法

将.h和.cpp中的东西写到一起后缀名称改为.hpp

~~~c++
#include"person.hpp"
~~~



##### 1.3.8 类模板与友元

类内实现加friend关键字即可

类外实现则需要让编译器提前识别过程繁琐

~~~c++
#include<iostream>
#include<string>
#include<cstdlib>

using namespace std;

template<class T1, class T2>
class Person;

template<class T1, class T2>
void printPerson2(Person<T1, T2> p)
{
	cout << "类外实现" << endl;
	cout << "姓名" << p.m_Name << endl;
	cout << "年龄" << p.m_Age << endl;
}

template<class T1,class T2>
class Person
{
	//全局函数类内实现
	friend void printPerson(Person<T1, T2> p)//加关键字即可
	{
		cout << "姓名" << p.m_Name << endl;
		cout << "年龄" << p.m_Age << endl;
	}


	friend void printPerson2<>(Person<T1, T2> p);//加<>将普通函数变为模板函数

public:

	Person(T1 name,T2 age)
	{
		this->m_Name = name;
		this->m_Age = age;
	}

private:

	T1 m_Name;
	T2 m_Age;
};

void test01()
{
	Person<string, int> p1("张三", 18);

	printPerson(p1);
}

void test02()
{
	Person<string, int> p2("李四", 20);

	printPerson2(p2);
}

int main()
{
	test01();
	test02();

	system("pause");

	return 0;
}
~~~



##### 1.3.9 类模板按例

通用数组类

+ 可以存储各种数据类型
+ 将数据存入堆区
+ 构造函数闯入数组容量
+ 防止浅拷贝
+ 提供数组增加删减
+ 可以通过下标访问数组元素
+ 可以获取数组中当前元素个数和数组容量

myArray.hpp中的代码

~~~c++
#pragma once

#include<iostream>
#include<string>
#include<cstdlib>

using namespace std;

template<class T>
class MyArray
{
public:

	MyArray(int capacity)
	{
		cout << "Myarray有参构造" << endl;
		this->m_Capacity = capacity;
		this->m_Size = 0;
		this->pAddress = new T[this->m_Capacity];
	}

	//拷贝构造
	MyArray(const MyArray& arr)
	{
		cout << "Myarray拷贝构造" << endl;
		this->m_Capacity = arr.m_Capacity;
		this->m_Size = arr.m_Size;
		//this->pAddress = arr.pAddress;

		//深拷贝
		this->pAddress = new T[arr.m_Capacity];

		for (int i = 0; i < this->m_Size; i++)
		{
			this->pAddress[i] = arr.pAddress[i];
		}
	}

	MyArray& operator=(const MyArray& arr)
	{
		cout << "Myarray重载构造" << endl;
		if (this->pAddress != nullptr)
		{
			delete[] this->pAddress;
			this->pAddress = nullptr;
			this->m_Capacity = 0;
			this->m_Size = 0;
		}

		this->m_Capacity = arr.m_Capacity;
		this->m_Size = arr.m_Size;
		this->pAddress = new T[arr.m_Capacity];

		for (int i = 0; i < this->m_Size; i++)
		{
			this->pAddress[i] = arr.pAddress[i];
		}

		return *this;
	}

	//尾插法
	void Push_Back(const T& val)
	{
		//判断容量是否等于大小
		if (this->m_Capacity == this->m_Size)
		{
			return;
		}
		this->pAddress[this->m_Size] = val;
		this->m_Size++;
	}

	//尾插法
	void Pop_Back()
	{
		if (this->m_Size == 0)
		{
			return;
		}
		this->m_Size--;
	}

	//下标方式
	T& operator[](int index)
	{
		return this->pAddress[index];
	}

	//返回数组容量
	int getCapacity()
	{
		return this->m_Capacity;
	}
	
	//返回数组大小
	int getSize()
	{
		return this->m_Size;
	}

	~MyArray()
	{
		cout << "Myarray析构构造" << endl;
		if (this->pAddress != nullptr)
		{
			delete[] this->pAddress;
			this->pAddress = nullptr;
		}
	}

private:

	T* pAddress;//指针指向堆区

	int m_Capacity;

	int m_Size;

};
~~~



中的代码

~~~c++
#include<iostream>
#include<string>

using namespace std;

#include"maArray.hpp"

void printIntArray(MyArray<int>& arr)
{
	for (int i = 0; i < arr.getSize(); i++)
	{
		cout << arr[i] << endl;
	}
}

void test01()
{
	MyArray<int> arr1(5);

	for (int i = 0; i < 5; i++)
	{
		arr1.Push_Back(i);
	}

	cout << "arr1的打印输出为：" << endl;

	printIntArray(arr1);

	cout << "arr1的容量为：" << arr1.getCapacity() << endl;
	cout << "arr1的大小为：" << arr1.getSize() << endl;

	MyArray<int> arr2(arr1);

	cout << "arr2的打印输出为：" << endl;

	printIntArray(arr2);

	arr2.Pop_Back();

	cout << "arr2尾删后输出：" << endl;
	cout << "arr2的容量为：" << arr2.getCapacity() << endl;
	cout << "arr2的大小为：" << arr2.getSize() << endl;

	//MyArray<int> arr3(100);
	//arr3 = arr1;
}

class Person
{
public:

	Person() {};
	Person(string name, int age)
	{
		this->m_Name = name;
		this->m_Age = age;
	}

	string m_Name;
	int m_Age;
};

void printPersonArray(MyArray<Person>& arr)
{
	for (int i = 0; i < arr.getSize(); i++)
	{
		cout << "姓名" << arr[i].m_Name << endl;
		cout << "年龄" << arr[i].m_Age << endl;
	}
}

void test02()
{
	MyArray<Person> arr(10);


	Person p1("张三", 19);
	Person p2("李四", 20);
	Person p3("王五", 28);
	Person p4("赵六", 29);
	Person p5("周七", 38);


	arr.Push_Back(p1);
	arr.Push_Back(p2);
	arr.Push_Back(p3);
	arr.Push_Back(p4);
	arr.Push_Back(p5);

	printPersonArray(arr);

	//输出容量
	cout << "arr2的容量为：" << arr.getCapacity() << endl;
	cout << "arr2的大小为：" << arr.getSize() << endl;
}

int main()
{
	test01();

	cout << endl;

	test02();

	system("pause");

	return 0;
}
~~~









### 2.STL初识

#### 2.1 STL的诞生

C++ STL（标准模板库）是一套功能强大的 C++ 模板类，提供了通用的模板类和函数，这些模板类和函数可以实现多种流行和常用的算法和数据结构，如向量、链表、队列、栈。

为了提高复用性

为了建立数据结构和算法的一套标准



#### 2.2 STL基本概念

**STL（Standard Template Library，标准模板库）**

| 容器（Containers）  | 容器是用来管理某一类对象的集合。C++ 提供了各种不同类型的容器，比如 deque、list、vector、map 等。 |
| ------------------- | :----------------------------------------------------------- |
| 算法（Algorithms）  | 算法作用于容器。它们提供了执行各种操作的方式，包括对容器内容执行初始化、排序、搜索和转换等操作。 |
| 迭代器（iterators） | 迭代器用于遍历对象集合的元素。这些集合可能是容器，也可能是容器的子集。 |

+ **容器**和**算法**之间通过**迭代器**进行衔接
+ STL几乎所有代码都采用了模板（类模板或者函数模板）



#### 2.3 STL六大组件

六大组件细分：容器、算法、迭代器、仿函数、适配器、空间配置器



1. 容器：各种数据结构，如vector，list，deque，set，map等，用来存放数据
2. 算法：各种常用的算法，如sort，find，copy，等
3. 迭代器：连接算法与容器
4. 仿函数：行为类似函数，可作为算法的某种策略
5. 适配器：一种用来修饰容器或者仿函数或者迭代器的东西
6. 空间配置器：负责空间的配置与管理



#### 2.4 STL中容器、算法、迭代器

容器

STL容器就是将常用的一些数据结构实现出来

常用的数据结构：数组，链表，树，栈，队列，集合，映射表等

分为两种

1. 序列式容器：强调值的排序，容器中每个元素都有固定的位置
2. 关联式容器：二叉树结构，各元素之间没有严格的物理顺序关系



算法

有限步骤解决逻辑或者数学问题，（Algoritms）

分为两种

1. 质变算法：运算期间会改变元素内容，如拷贝、替换、删除等等
2. 非质变算法：运算期间不会改变元素内容，如遍历、查找、计数



迭代器

每个容器都有自己专属的迭代器

可以理解为指针

分为五种

1. 输入迭代器：对数据只读访问
2. 输出迭代器：对数据只写访问
3. 向前迭代器：读写操作，并能向前推进
4. 双向迭代器：读写操作，并能向前后推进
5. 随机访问迭代器：读写操作，并且可以跳跃访问，功能强大

常用迭代器为双向迭代器和随机访问迭代器



#### 2.5 容器算法迭代器

STL中最常用的为vector

##### 2.5.1 vector存放内置数据类型

容器：`vector`

算法： `for_each`

迭代器：`vector<int>::itearator`

例子

~~~c++
#include<iostream>

using namespace std;

#include<cstdlib>
#include<string>
#include<vector>
#include<algorithm>

void myPrint(int val)
{
	cout << val << endl;
}

void test01()
{
	vector<int> v;

	//向容器中插入数据
	v.push_back(10);
	v.push_back(20);
	v.push_back(30);
	v.push_back(40);

	//通过迭代器访问容器中的数据
	vector<int>::iterator itBegin = v.begin();
	vector<int>::iterator itEnd = v.end();

	//第一种遍历方式
	while (itBegin != itEnd)
	{
		cout << *itBegin << endl;
		itBegin++;
	}

	//第二种方式
	for (vector<int>::iterator it = v.begin(); it != v.end(); it++)
	{
		cout << *it << endl;
	}

	//第三种方式利用STL自带的遍历算法
	for_each(v.begin(), v.end(), myPrint);

}


int main()
{
	test01();

	system("pause");

	return 0;
}
~~~



##### 2.5.2 vector存放自定义数据类型

自定义数据类型的存储

~~~c++
#include<iostream>

using namespace std;

#include<string>
#include<cstdlib>
#include<vector>
#include<algorithm>

class Person
{
public:
	Person(string name, int age)
	{
		this->m_Name = name;
		this->m_Age = age;
	}

	int m_Age;
	string m_Name;
};

void test01()
{
	vector<Person> v;

	Person p1("aaa", 10);
	Person p2("bbb", 20);
	Person p3("ccc", 30);
	Person p4("ddd", 40);
	Person p5("eee", 50);

	v.push_back(p1);
	v.push_back(p2);
	v.push_back(p3);
	v.push_back(p4);
	v.push_back(p5);

	for (vector<Person>::iterator it = v.begin(); it != v.end(); it++)
	{
		cout << "姓名：" << (*it).m_Name << endl;
		cout << "年龄：" << (*it).m_Age << endl;


		cout << "huozhe" << endl;
		cout << endl;

		cout << "姓名：" << it->m_Name << endl;
		cout << "年龄：" << it->m_Age << endl;
	}
}

int main()
{
	test01();

	cout << endl;
	cout << endl;
	cout << endl;

	test02();

	system("pause");

	return 0;
}
~~~



自定义数据类型的指针的存储

~~~c++
void test02()
{
	vector<Person*> v;

	Person p1("aaa", 10);
	Person p2("bbb", 20);
	Person p3("ccc", 30);
	Person p4("ddd", 40);
	Person p5("eee", 50);

	v.push_back(&p1);
	v.push_back(&p2);
	v.push_back(&p3);
	v.push_back(&p4);
	v.push_back(&p5);

	for (vector<Person*>::iterator it = v.begin(); it != v.end(); it++)
	{
		cout << "姓名：" << (*it)->m_Name << endl;
		cout << "年龄：" << (*it)->m_Age << endl;
	}
}
~~~



##### 2.5.3 Vector容器嵌套容器

~~~c++
#include<iostream>
using namespace std;

#include<vector>

void test01()
{
	vector<vector<int>> v;

	//创建小容器
	vector<int> v1;
	vector<int> v2;
	vector<int> v3;
	vector<int> v4;

	//创建数据
	for (int i = 0; i < 4; i++)
	{
		v1.push_back(i + 1);
		v2.push_back(i + 2);
		v3.push_back(i + 3);
		v4.push_back(i + 4);
	}

	//将小容器放入大容器内
	v.push_back(v1);
	v.push_back(v2);
	v.push_back(v3);
	v.push_back(v4);

	//通过大容器进行数据遍历
	for (vector<vector<int>>::iterator it = v.begin(); it != v.end(); it++)
	{
		// （*it）--- 容器 vector<int>
		for (vector<int>::iterator vit = (*it).begin(); vit != (*it).end(); vit++)
		{
			cout << *vit << " ";
		}
		cout << endl;

	}
}

int main()
{
	test01();

	system("pause");

	return 0;
}
~~~



### 3.STL-常用容器

#### 3.1 string容器

##### 3.1.1 string基本概念

**本质：**

+ `string`是c++风格的字符串，而`string`本质上是一个类

**`string`和`char*`的区别：**

+ `char*`是一个指针
+ `string`是一个类内部封装了`char*`，管理字符串，是一个`char*`的容器

**特点：**

+ string类内部分装了很多成员方法

  例如：查找`find`、拷贝`copy`、删除`delete`、替换`replace`、插入`insert`



##### 3.1.2 string构造函数

~~~c++
#include<iostream>
using namespace std;
#include<string>

//stirng的构造hanshu
void test01()
{
	string s1;//默认构造

	const char* str = "hello world";
	string s2(str);
	cout << "s2=" << s2 << endl;

	string s3(s2);
	cout << "s3=" << s3 << endl;

	string s4(10, 'a');
	cout << "s4=" << s4 << endl;
}

int main()
{
	test01();

	system("pause");

	return 0;
}
~~~



##### 3.1.3 string赋值操作

```c++
#include<iostream>
using namespace std;
#include<string>

void test01()
{
	string s1;
	s1 = "hello world";
	cout << "s1=" << s1 << endl;

	string s2;
	s2 = s1;
	cout << "s2=" << s2 << endl;

	string s3;
	s3 = 'a';
	cout << "s3=" << s3 << endl;

	string s4;
	s4.assign("hello C++");
	cout << "s4=" << s4 << endl;

	string s5;
	s5.assign("hello C++", 5);
	cout << "s5=" << s5 << endl;

	string s6;
	s6.assign(s5);
	cout << "s6=" << s6 << endl;

	string s7;
	s7.assign(5, 'a');
	cout << "s7=" << s7 << endl;
}

int main()
{
	test01();

	system("pause");

	return 0;
}
```



##### 3.1.4 string字符串拼接

~~~c++
#include<iostream>
using namespace std;
#include<string>


void test01()
{
	string s1 = "hello";
	s1 += " world";
	cout << "s1=" << s1 << endl;

	s1 += ':';
	cout << "s1=" << s1 << endl;

	string s2 = " dns";
	s1 += s2;
	cout << "s1=" << s1 << endl;

	string s3 = "I ";
	s3.append(" love");
	cout << "s3=" << s3 << endl;

	s3.append("game abcd", 6);
	cout << "s3=" << s3 << endl;

	s3.append(s2);
	cout << "s3=" << s3 << endl;

	//str1.append(str2,0,4);
	//从另一个字符串，第几个位置，截取几个字符
	//三参数拼接
}

int main()
{
	test01();

	system("pause");

	return 0;
}
~~~



##### 3.1.5 string查找和替换

查找：查找指定字符串是否存在

替换：在指定位置替换字符串

~~~c++
#include<iostream>
using namespace std;
#include<string>

//1.查找
void test01()
{
	string str1 = "abcdefghid";

	int pos = str1.find("d");

	if (pos == -1)
	{
		cout << "未找到字符串" << endl;
	}
	else
	{
		cout << "pos=" << pos << endl;
	}

	//rfind和find区别
	//rfind从左往右，find从左往右
	pos = str1.rfind("d");

	cout << "pos=" << pos << endl;
}

//2.替换
void test02()
{
	string str1 = "abcdefg";

	str1.replace(1, 3, "1111");
	//replace替换
	//第一个参数 < 第几个起
	//第二个参数 < 替换几个
	//第三个参数 < 替换成

	cout << "str1=" << str1 << endl;
	
}

int main()
{
	test01();
	test02();

	system("pause");

	return 0;
}
~~~



##### 3.1.6 string字符串比较

进行字符串之间的比较

按照ASCII码值进行比较

+ = 返回 0
+ \> 返回 1
+ \< 返回 -1

~~~c++
#include<iostream>
#include<string>

using namespace std;

void test01()
{
	string str1 = "xello";
	string str2 = "hello";

	if (str1.compare(str2) == 0)
	{
		cout << "str1等于str2" << endl;
	}
	else if (str1.compare(str2) > 0)
	{
		cout << "str1大于str2" << endl;
	}
	else
	{
		cout << "str1小于str2" << endl;
	}
}

int main()
{
	test01();

	system("pause");

	return 0;
}
~~~



##### 3.1.7 string字符串存取

~~~c++
#include<iostream>
#include<string>

using namespace std;


//字符串存取
void test01()
{
	string str = "hello";

	//通过[]访问
	for (int i = 0; i < str.size(); i++)
	{
		cout << str[i] << " ";
	}
	cout << endl;

	//通过at访问
	for(int i=0;i<str.size();i++)
	{
		cout << str.at(i) << " ";
	}
	cout << endl;

	//修改
	//中括号或者at()都可以
}

int main()
{
	test01();

	system("pause");

	return 0;
}
~~~



##### 3.1.8 string插入和删除

~~~c++
#include<iostream>
#include<string>

using namespace std;

void test01()
{
	string str = "hello";

	//插入
	str.insert(1, "111");
	cout << "str = " << str << endl;

	//删除
	str.erase(1, 3);
	cout << "str = " << str << endl;
}

int main()
{
	test01();

	system("pause");

	return 0;
}
~~~



##### 3.1.9 string子串获取

~~~c++
#include<iostream>
#include<string>

using namespace std;

void test01()
{
	string str = "abcdefg";

	string subStr = str.substr(1, 3);

	cout << "subSter = " << subStr << endl;
}

void test02()
{
	string email = "abcdefg@163.com";

	//地址中获取信息
	int pos = email.find("@");

	string usrName = email.substr(0, pos);

	cout << "usrName = " << usrName << endl;
}

int main()
{
	test01();
	test02();

	system("pause");

	return 0;
}
~~~





#### 3.2 vector容器

##### 3.2.1 vector基本概念

+ `vector`容器与**数组**十分相似，也称为单端数组

区别：

+ `vector`与普通数组的区别在于数组是静态的空间，而vector可以动态扩展
+ ==但是==：动态扩展并不是继续扩展而是找更大的空间存放
+ 将原有空间数据拷贝到新空间，释放原有空间



##### 3.2.2 vector构造函数

进行构造创建vector容器

实现方法

~~~c++
#include<iostream>
#include<vector>

using namespace std;

void printVector(vector<int>& v)
{
	for (vector<int>::iterator it = v.begin(); it != v.end(); it++)
	{
		cout << *it << " ";
	}
	cout << endl;
}

void test01()
{
	//1.默认构造，无参构造
	vector<int> v1;


	for (int i = 0; i < 10; i++)
	{
		v1.push_back(i);
	}

	printVector(v1);


	//2.通过区间进行构造
	vector<int> v2(v1.begin(), v1.end());
	printVector(v2);

	//3.n个elem方式
	vector<int> v3(10, 100);
	printVector(v3);

	//4.拷贝构造
	vector<int> v4(v3);
	printVector(v4);
}

int main()
{
	test01();

	system("pause");

	return 0;
}
~~~



##### 3.2.3 vector赋值操作

+ 对vector进行赋值

方法：

~~~c++
#include<iostream>
#include<vector>

using namespace std;

void printVector(vector<int>& v)
{
	for (vector<int>::iterator it = v.begin(); it != v.end(); it++)
	{
		cout << *it << " ";
	}
	cout << endl;
}

void test01()
{
	vector<int> v1;
	for (int i = 0; i < 10; i++)
	{
		v1.push_back(i);
	}
	printVector(v1);

	//赋值
	vector<int> v2;
	v2 = v1;
	printVector(v2);

	//assign
	vector<int> v3;
	v3.assign(v1.begin(), v1.end());
	printVector(v3);

	//assign,n 个elem
	vector<int> v4;
	v4.assign(10, 100);
	printVector(v4);
}

int main()
{
	test01();

	system("pause");

	return 0;
}
~~~



##### 3.2.4 vector容量和大小

+ `empty();`//判断容器是否为空
+ `capacity();`//容器的容量
+ `size();`//容器中个数
+ `resize(int num)`//指定容器长度
+ `resize(int num,elem);`//指定长度若变长则用elem填充

容量一定大于等于个数

~~~c++
#include<iostream>
#include<vector>

using namespace std;

void printVector(vector<int>& v)
{
	for (vector<int>::iterator it = v.begin(); it != v.end(); it++)
	{
		cout << *it << " ";
	}
	cout << endl;
}

void test01()
{
	vector<int> v1;
	for (int i = 0; i < 10; i++)
	{
		v1.push_back(i);
	}
	printVector(v1);

	if (v1.empty())
	{
		cout << "v1为空" << endl;
	}
	else
	{
		cout << "v1不为空" << endl;
		cout << "v1的容量为：" << v1.capacity() << endl;
		cout << "v1的大小为：" << v1.size() << endl;
	}


	//重新指定大小
	v1.resize(15);
	printVector(v1);

	//加长默认补零也可以自定义
	v1.resize(18, 8);
	printVector(v1);

	//减短将多余删除
	v1.resize(5);
	printVector(v1);
}

int main()
{
	test01();

	system("pause");

	return 0;
}
~~~



##### 3.2.5 vector插入和删除

+ `push_back(ele);`//尾部插入
+ `pop_back();`//删除尾部
+ `insert(const_iterator pos,ele);`//向指定pos位置插入ele
+ `insert(const_iterator pos,,int count,ele);`//向指定位置pos插入count个ele
+ `erase(const_iterator pos);`//删除指向的元素
+ `erase(const_iterator start,const_iterator end);`//删除指定区间内的元素
+ `clear();`//清空容器

~~~c++
#include<iostream>
#include<vector>

using namespace std;

void printVector(vector<int>& v)
{
	for (vector<int>::iterator it = v.begin(); it != v.end(); it++)
	{
		cout << *it << " ";
	}
	cout << endl;
}

void test01()
{
	vector<int> v1;
	v1.push_back(1);
	v1.push_back(2);
	v1.push_back(3);
	v1.push_back(4);
	v1.push_back(5);
	printVector(v1);

	//尾删
	v1.pop_back();
	printVector(v1);

	//插入
	v1.insert(v1.begin(), 100);
	printVector(v1);

	v1.insert(v1.begin(), 2, 80);
	printVector(v1);

	vector<int> v2;
	v2 = v1;

	//删除
	v1.erase(v1.begin());
	printVector(v1);

	v1.erase(v1.begin(), v1.end());
	printVector(v1);

	//清空
	printVector(v2);
	v2.clear();
	printVector(v2);
}

int main()
{
	test01();

	system("pause");

	return 0;
}
~~~



##### 3.2.6 vector数据存取

+ `at(int idx);`
+ `operator[];`
+ `front();`
+ `back();`

~~~c++
#include<iostream>
#include<vector>

using namespace std;

void test01()
{
	vector<int> v1;
	for (int i = 0; i < 10; i++)
	{
		v1.push_back(i);
	}

	//利用[]
	for (int i = 0; i < v1.size(); i++)
	{
		cout << v1[i] << " ";
	}
	cout << endl;

	//利用at
	for (int i = 0; i < v1.size(); i++)
	{
		cout << v1.at(i) << " ";
	}
	cout << endl;

	//第一个元素
	cout << "第一各元素：" << v1.front() << endl;

	//最后一个元素
	cout << "最后一个元素：" << v1.back() << endl;
}

int main()
{
	test01();

	system("pause");

	return 0;
}
~~~



##### 3.2.7 vector互换容器

+ `swap(vec);`

~~~c++
#include<iostream>
#include<vector>

using namespace std;

void printVector(vector<int>& v)
{
	for (vector<int>::iterator it = v.begin(); it != v.end(); it++)
	{
		cout << *it << " ";
	}
	cout << endl;
}

void test01()
{
	vector<int> v1;
	for (int i = 0; i < 10; i++)
	{
		v1.push_back(i);
	}
	printVector(v1);

	vector<int> v2;
	for (int i = 10; i > 0; i--)
	{
		v2.push_back(i);
	}
	printVector(v2);

	cout << "交换后" << endl;
	v1.swap(v2);
	cout << "v1" << endl;
	printVector(v1);
	cout << "v2" << endl;
	printVector(v2);
}


//实际用途
void test02()
{
	vector<int> v;
	for (int i = 0; i < 100000; i++)
	{
		v.push_back(i);
	}

	cout << "v1的容量：" << v.capacity() << endl;
	cout << "v1的大小：" << v.size() << endl;


	//重新指定大小
	v.resize(3);
	cout << "v1的容量：" << v.capacity() << endl;
	cout << "v1的大小：" << v.size() << endl;

	//利用swap收缩空间
	vector<int>(v).swap(v);
	cout << "v1的容量：" << v.capacity() << endl;
	cout << "v1的大小：" << v.size() << endl;
}

int main()
{
	test01();
	test02();

	system("pause");

	return 0;
}
~~~

匿名对象在当前行执行后将会释放



##### 3.2.8 vector预留空间

减少vector动态扩展cishu

+ `reserve(int len);` //预留len，但是未初始化不能访问

~~~c++
#include<iostream>
#include<vector>

using namespace std;

void printVector(vector<int>& v)
{
	for (vector<int>::iterator it = v.begin(); it != v.end(); it++)
	{
		cout << *it << " ";
	}
	cout << endl;
}

void test01()
{
	vector<int> v;
	int num = 0;
	int* p = nullptr;

	for (int i = 0; i < 100000; i++)
	{
		v.push_back(i);

		if (p != &v[0])
		{
			p = &v[0];
			num++;
		}
	}

	cout << "num = " << num << endl;
	cout << "v1的容量：" << v.capacity() << endl;
	cout << "v1的大小：" << v.size() << endl;

}

void test02()
{
	vector<int> v;
	v.reserve(100000);
	int num = 0;
	int* p = nullptr;

	for (int i = 0; i < 100000; i++)
	{
		v.push_back(i);

		if (p != &v[0])
		{
			p = &v[0];
			num++;
		}
	}

	cout << "num = " << num << endl;
	cout << "v1的容量：" << v.capacity() << endl;
	cout << "v1的大小：" << v.size() << endl;

}

int main()
{
	test01();
	test02();

	system("pause");

	return 0;
}
~~~



#### 3.3 deque容器

##### 3.3.1 deque基本概念

双端数组

**deque与vector的区别:**

+ vector头部插入效率低
+ deque的头部插入效率高
+ 但是vector访问速度比deuqe快



##### 3.3.2 deque构造函数

创造deque容器

默认构造和拷贝构造

~~~c++
#include<iostream>
#include<deque>

using namespace std;

void printDeque(const deque<int>& d)
{
	for (deque<int>::const_iterator it = d.begin(); it != d.end(); it++)
	{
		//*it=100;
		cout << *it << " ";
	}
	cout << endl;
}

void test01()
{
	deque<int> d1;
	for (int i = 0; i < 10; i++)
	{
		d1.push_back(i);
	}
	printDeque(d1);

	deque<int> d2(d1.begin(), d1.end());
	printDeque(d2);

	deque<int> d3(10, 8);
	printDeque(d3);

	deque<int> d4(d3);
	printDeque(d4);

}

int main()
{
	test01();

	system("pause");

	return 0;
}
~~~



##### 3.3.3 deque赋值操作

~~~c++
#include<iostream>
#include<deque>

using namespace std;

void printDeque(const deque<int>& d)
{
	for (deque<int>::const_iterator it = d.begin(); it != d.end(); it++)
	{
		//*it=100;
		cout << *it << " ";
	}
	cout << endl;
}

void test01()
{
	deque<int> d1;
	for (int i = 0; i < 10; i++)
	{
		d1.push_back(i);
	}
	printDeque(d1);

	//等号赋值
	deque<int> d2;
	d2 = d1;
	printDeque(d2);

	//assign
	deque<int> d3;
	d3.assign(d1.begin(), d1.end());
	printDeque(d3);

	deque<int> d4;
	d4.assign(10, 100);
	printDeque(d4);
}

int main()
{
	test01();

	system("pause");

	return 0;
}
~~~



##### 3.3.4 deque大小操作

和vector很像

deque容器中没有容量的概念

empty（），size（），resize（），



##### 3.3.5 deque插入删除

+ `push_back(elem);`//尾部删除
+ `push_front(elem);`//头部插入
+ `pop_back();`//尾部删除
+ `pop_front();/`/尾部插入

指定位置：

+ `insert(pos,elem);`//指定位置插入
+ `insert(pos,n,elem);`//
+ `insert(pos,beg,ebd);`//
+ `clear();`//清除
+ `erase(beg,end);`//指定位置删除
+ `erase(pos);`//



##### 3.3.6 deque数据存取

和vector一样用at方式或者中括号的方式

+ `at(int idx);`
+ `operator[];`

同时提供了两种头尾查询

+ `front();`//返回第一个元素
+ `back();`//返回最后一个元素



##### 3.3.7 deque排序

利用`sort(iterator beg,iterator end)`//对区间进行排序

对于可以利用随机访问的迭代器的容器都可以用sort访问

如vector也可以用sort

用的时候要包含标准算法头文件库`algorithem`

~~~c++
#include<iostream>
#include<deque>
#include<algorithm>

using namespace std;

void printDeque(const deque<int>& d)
{
	for (deque<int>::const_iterator it = d.begin(); it != d.end(); it++)
	{
		cout << *it << " ";
	}
	cout << endl;
}

void test01()
{
	deque<int> d1;
	d1.push_back(1);
	d1.push_back(2);
	d1.push_back(3);
	d1.push_front(4);
	d1.push_front(5);

	printDeque(d1);

	//排序
	sort(d1.begin(), d1.end());
	printDeque(d1);
	cout << "默认从小到大" << endl;

}

int main()
{
	test01();

	system("pause");

	return 0;
}
~~~



#### 3.4 打分按例

利用vector和deque容器

1. vector中存放选手
2. 将平分放入deque中
3. 利用sort去除最高分和最低分
4. 累加总分
5. 取平均数



##### 3.4.1 代码实现

~~~c++
#include<iostream>
#include<vector>
#include<deque>
#include<string>
#include<algorithm>

using namespace std;

class Person
{
public:
	Person(string name, int score)
	{
		this->m_Name = name;
		this->m_Score = score;
	}


	string m_Name;//姓名
	int m_Score;//平均分
};

void createPerson(vector<Person>& v)
{
	string nameSeed = "ABCDE";
	for (int i = 0; i < 5; i++)
	{
		string name = "选手";
		name += nameSeed[i];

		int score = 0;

		Person p(name, score);

		v.push_back(p);
	}
}

void printPersonCore(const vector<Person>& v)
{
	for (vector<Person>::const_iterator it = v.begin(); it != v.end(); it++)
	{
		cout << "姓名：" << (*it).m_Name << "\t" << "分数：" << (*it).m_Score << endl;
	}
}

//打分
void setScore(vector<Person>& v)
{
	for (vector<Person>::iterator it = v.begin(); it != v.end(); it++)
	{
		deque<int> d;
		for (int i = 0; i < 10; i++)
		{
			int score = rand() % 41 + 60;
			d.push_back(score);
			cout << score << " ";
		}
		cout << endl;

		//排序
		sort(d.begin(), d.end());

		//去除最高分最低分
		d.pop_front();
		d.pop_back();

		//取平均分
		int sum = 0;
		for (deque<int>::iterator dit = d.begin(); dit != d.end(); dit++)
		{
			sum += *dit;
		}

		int avg = sum / d.size();

		it->m_Score = avg;
	}
}

int main()
{
	//1. 创建5名选手
	vector<Person> v;
	createPerson(v);
	setScore(v);

	printPersonCore(v);
	
	//2. 给选手打分
	 
	//3. 显示得分

	system("pause");

	return 0;
}
~~~

#### 3.5 stack容器

##### 3.5.1 stack基本概念

堆栈容器——先进后出

入栈出栈，都从栈顶，不允许有遍历行为



##### 3.5.2 stack常用接口

`stack<int> s;`//默认构造

+ `push();/`/入栈
+ `pop();`//出栈
+ `top();`//返回栈顶元素
+ `size();/`/大小
+ `empty();`//是否为空



#### 3.6 queue容器

##### 3.6.1 queue基本概念

队列数据结构

一端只能进入一端只能输出



##### 3.6.2 queue常用接口

`queue<int> q;`//构造函数

+ push
+ pop
+ back
+ front
+ empty
+ size

~~~c++
#include<iostream>
#include<queue>

using namespace std;

class Person
{
public:
	Person(string name, int age)
	{
		this->m_Name = name;
		this->m_Age = age;
	}

public:
	string m_Name;
	int m_Age;
};

void test01()
{
	queue<Person> q;

	Person p1("张三", 18);
	Person p2("张四", 19);
	Person p3("王五", 20);
	Person p4("赵六", 17);

	q.push(p1);
	q.push(p2);
	q.push(p3);
	q.push(p4);

	while (!q.empty())
	{
		cout << "队头-姓名：" << q.front().m_Name << "\t" << "年龄：" << q.front().m_Age << endl;
		cout << "队尾-姓名：" << q.back().m_Name << "\t" << "年龄：" << q.back().m_Age << endl;

		q.pop();
	}

	cout << "空" << endl;
}

int main()
{
	test01();

	system("pause");

	return 0;
}
~~~



#### 3.7 list容器

##### 3.7.1 list基本概念

链表结构

STL中是一种双向循环链表

可以快速对任意位置插入删除

物理上不连续但是逻辑上连续

+ list和vector是STL中非常常用的两个容器
+ 链表（list）插入和删除十分方便，利用动态内存不会浪费空间
+ 但是链表遍历时间更长



##### 3.7.2 list构造函数

+ list<T> l;
+ list(beg,end);
+ list(n,elem);
+ list(const list& l);//拷贝构造
+ 与其他几个容器相似



##### 3.7.3 list赋值交换

+ assign(beg,end);
+ assign(n,elem);
+ list& operator=(const list& l);
+ swap(l);



##### 3.7.4 list大小操作

+ size();
+ empty();
+ resize(num);
+ resize(num,elem);



##### 3.7.5 list插入删除

+ push_back(elem);//
+ pop_back();//
+ push_front(elem);//
+ pop_front();//

在指定位置

+ insert(pos,elem);//
+ insert(pos,n,elem);//
+ insert(pos,beg,end);//
+ clear();//
+ erase(beg,end);//
+ erea(pos);//
+ remove(elem);//删除容器中所有elem元素



##### 3.7.6 list数据存取

+ front();//返回第一个元素

+ back();//返回最后一个元素

list容器不支持随机访问



##### 3.7.7 list反转排序

+ reverse();//反转
+ sort();//升序排列

~~~c++
bool myCompare(int v1, int v2)
{
    return v1 > v2;
}

l.sort(myCompare);//降序
~~~





##### 3.7.8 list排序按例

自定义数据类型排序的时候要指定规则

~~~c++
#include<iostream>
#include<list>
#include<string>

using namespace std;

class Person
{
public:
	Person(string name, int age, int height)
	{
		this->m_Name = name;
		this->m_Age = age;
		this->m_Height = height;
	}

	string m_Name;	//姓名
	int m_Age;		//年龄
	int m_Height;	//身高
};

void printList(list<Person>& l)
{
	for (list<Person>::iterator it = l.begin(); it != l.end(); it++)
	{
		cout << "姓名：" << (*it).m_Name << "\t" << "年龄：" << it->m_Age << "\t" << "身高：" << it->m_Height << endl;
	}
	cout << endl;
}

bool comparePerson(Person& p1, Person p2)
{
	if (p1.m_Age == p2.m_Age)
	{
		return p1.m_Height < p2.m_Height;
	}
	return p1.m_Age < p2.m_Age;
}

void test01()
{
	list<Person> l;

	Person p1("刘备", 35, 175);
	Person p2("曹操", 45, 180);
	Person p3("孙权", 40, 170);
	Person p4("赵云", 25, 190);
	Person p5("张飞", 35, 160);
	Person p6("关羽", 35, 200);

	l.push_back(p1);
	l.push_back(p2);
	l.push_back(p3);
	l.push_back(p4);
	l.push_back(p5);
	l.push_back(p6);

	printList(l);
	l.sort(comparePerson);
	printList(l);
}

int main()
{
	test01();

	system("pause");

	return 0;
}
~~~



#### 3.8 set/multiset容器

##### 3.8.1 set基本概念

**特点：**

+ 进入的元素会自动排序
+ 插入数据只能用insert();
+ 同时不允许插入重复的值

**本质：**

+ set/multiset属于关联容器，利用二叉树实现

**set和multiset区别：**

+ set不可以有重复元素
+ multiset里面可以有重复元素



##### 3.8.2 set构造赋值

创建set容器以及赋值

**构造：**

+ set<T> st;
+ set(const set& st);

**赋值：**

+ set& operator=(cont set&st);



##### 3.8.3 set大小交换

不允许重新指定大小

+ size();
+ empty();
+ swap(st);



##### 3.8.4 set插入删除

不能指定位置插入

插入后自动排序

+ insert(elem);
+ clear();
+ erase(pos);
+ erase(beg,end);//效果和清空一样
+ erase(elem);



##### 3.8.5 set统计查找

用于统计数据

+ find(key);//查找key是否存在
+ count(key);//统计key的个数
+ 对于set而言count非零即一

~~~c++
set<int>::iterator pos = s.find(key);

if(pos != s.end())
{
    cout << "找到元素" << *pos << endl;
}
else
{
    cout << "未找到元素" << endl;
}
~~~

对于set而言find和count效果差不多



##### 3.8.6 set和multiset

原因：

+ set插入时会有检测不允许重复插入
+ multiset插入时不会检测

~~~c++
pair<set<int>::iterator ,bool> ret = s.insert(10);

if(ret.second)
{
    cout << "插入成功" << endl;
}
else
{
    cout << "插入失败" << endl;
}
~~~

multiset也会自动排序



##### 3.8.7 pair对组创建

成对出现的数据利用对组可以返回两个数据

两种创建方式：

+ `pair<type, type> p(value1, value2);`
+ `pair<type, type> p = make_pair(value1, value2);`

使用时无需特殊头文件

用first和second取出第一和第二个数据

##### 3.8.8 set容器排序

默认从小到大排序

利用==仿函数==，可以改变排序规则

示例一：

存放内置类型

~~~c++
#include<iostream>
#include<set>

using namespace std;

class MyCompare
{
public:
	bool operator()(int v1, int v2)const
	{
		return v1 > v2;
	}
};

void printSet(set<int>& s)
{
	for (set<int>::iterator it = s.begin(); it != s.end(); it++)
	{
		cout << *it << " ";
	}
	cout << endl;
}

void test01()
{
	set<int> s1;

	s1.insert(1);
	s1.insert(5);
	s1.insert(3);
	s1.insert(4);
	s1.insert(2);

	printSet(s1);

	set<int, MyCompare> s2;

	s2.insert(1);
	s2.insert(5);
	s2.insert(3);
	s2.insert(4);
	s2.insert(2);

	for (set<int, MyCompare>::iterator it = s2.begin(); it != s2.end(); it++)
	{
		cout << *it << " ";
	}
	cout << endl;
}

int main()
{
	test01();

	system("pause");

	return 0;
}
~~~



示例二：存放自定义数据类型时

~~~c++
#include<iostream>
#include<string>
#include<set>

using namespace std;

class Person
{
public:
	Person(string name, int age)
	{
		this->m_Name = name;
		this->m_Age = age;
	}

	string m_Name;
	int m_Age;
};

class comparePerson
{
public:
	bool operator()(const Person& p1, const Person& p2)const
	{
		return p1.m_Age > p2.m_Age;
	}
};

void test01()
{
	set<Person, comparePerson> s;

	Person p1("刘备", 35);
	Person p2("曹操", 45);
	Person p3("孙权", 40);
	Person p4("赵云", 25);

	s.insert(p1);
	s.insert(p2);
	s.insert(p3);
	s.insert(p4);

	for (set<Person, comparePerson>::iterator it = s.begin(); it != s.end(); it++)
	{
		cout << "姓名：" << it->m_Name << "\t" << "年龄：" << it->m_Age << " ";
	}
	cout << endl;
}

int main()
{
	test01();

	system("pause");

	return 0;
}
~~~

自定义数据类型需要写仿函数进行指定排序方式




#### 3.9 map/mulitmap容器

##### 3.9.1 map基本概念

**特点：**

+ map容器中所有的元素都是pair
+ pair中第一个为key（键值），起到索引作用，第二个为value（实值）
+ 所有元素会根据key自动排序

**本质：**

+ map/multimap都属于关联容器，利用二叉树实现

**优点：**

+ 可以根据key值快速找到value

map和multimap区别：

+ map不允许有重复的key值



##### 3.9.2 map构造赋值

示例：

~~~c++
#include<iostream>
#include<map>

using namespace std;

void printMap(map<int, int>& m)
{
	for (map<int, int>::iterator it = m.begin(); it != m.end(); it++)
	{
		cout << "key = " << it->first << "\t" << "value = " << it->second << endl;
	}
}

void test01()
{
	map<int, int> m;

	m.insert(pair<int, int> (1, 10));
	m.insert(pair<int, int> (2, 20));
	m.insert(pair<int, int> (3, 30));
	m.insert(pair<int, int> (4, 40));

	printMap(m);
	cout << endl;

	map<int, int> m2(m);
	printMap(m2);
	cout << endl;

	map<int, int> m3;
	m3 = m;
	printMap(m3);
}

int main()
{
	test01();

	system("pause");

	return 0;
}
~~~





##### 3.9.3 map大小交换

+ size();
+ empty();
+ swap();



##### 3.9.4 map插入删除

+ insert(ele);
+ clear();
+ erase(pos);
+ erase(beg,end);
+ erase(key);



insert示例：

~~~c++
#include<iostream>
#include<map>

using namespace std;

void test01()
{
	map<int, int> m;

	//插入
	//第一种
	m.insert(pair<int, int>(1, 10));

	//第二种
	m.insert(make_pair(2, 20));

	//第三种
	m.insert(map<int, int>::value_type(3, 30));

	//第四种
	m[4] = 40;
}

int main()
{
	test01();

	system("pause");

	return 0;
}
~~~





##### 3.9.5 map查找统计

按key值查找

+ find(key);
+ count(key);

同理count统计非零即一



##### 3.9.6 map容器排序

默认按照key从小到大排序

利用仿函数可以改变排序规则

~~~c++
#include<iostream>
#include<map>

using namespace std;

class MyCompare
{
public:
	bool operator()(int v1, int v2)const
	{
		return v1 > v2;
	}
};

void test01()
{
	map<int, int, MyCompare> m;

	m.insert(make_pair(1, 10));
	m.insert(make_pair(2, 20));
	m.insert(make_pair(3, 30));
	m.insert(make_pair(4, 40));
	m.insert(make_pair(5, 50));

	for (map<int, int, MyCompare>::iterator it = m.begin(); it != m.end(); it++)
	{
		cout << "key = " << it->first << "\t" << "value = " << it->second << endl;
	}
}

int main()
{
	test01();

	system("pause");

	return 0;
}
~~~

和set相似要在插入之前进行修改



#### 3.10 容器按例

##### 3.10.1 实现

1. 创建10名员工
2. 进行随机分组
3. 分组后存入multimap中
4. 显示信息

代码：

~~~c++
#include<iostream>
#include<string>
#include<vector>
#include<map>
#include<ctime>

using namespace std;

#define CEHUA 0
#define MEISHU 1
#define YANFA 2

class Worker
{
public:
	string m_Name;
	int m_Salary;
};

void createWorker(vector<Worker>& v)
{
	string nameSeed = "ABCDEFGHIJ";
	for (int i = 0; i < 10; i++)
	{
		Worker worker;
		worker.m_Name = "员工";
		worker.m_Name += nameSeed[i];

		worker.m_Salary = rand() % 1001 + 1000;

		v.push_back(worker);
	}
}

void printVector(vector<Worker>& v)
{
	for (vector<Worker>::iterator it = v.begin(); it != v.end(); it++)
	{
		cout << "姓名：" << it->m_Name << "\t" << "工资：" << it->m_Salary << endl;
	}
}

void setGroup(vector<Worker>& v, multimap<int, Worker>& m)
{
	for (vector<Worker>::iterator it = v.begin(); it != v.end(); it++)
	{
		int deptId = rand() % 3;

		m.insert(make_pair(deptId, *it));
	}
}

void showWorkerByGroup(multimap<int, Worker>& m)
{
	cout << "策划部门：" << endl;
	multimap<int, Worker>::iterator pos = m.find(CEHUA);

	int count = m.count(CEHUA);
	int index = 0;
	for (; pos != m.end() && index < count; pos++, index++)
	{
		cout << "姓名：" << pos->second.m_Name << "\t" << "工资：" << pos->second.m_Salary << endl;
	}

	cout << "---------" << endl;
	cout << "美术部门：" << endl;
	pos = m.find(MEISHU);

	count = m.count(MEISHU);
	index = 0;
	for (; pos != m.end() && index < count; pos++, index++)
	{
		cout << "姓名：" << pos->second.m_Name << "\t" << "工资：" << pos->second.m_Salary << endl;
	}

	cout << "---------" << endl;
	cout << "研发部门：" << endl;
	pos = m.find(YANFA);

	count = m.count(YANFA);
	index = 0;
	for (; pos != m.end() && index < count; pos++, index++)
	{
		cout << "姓名：" << pos->second.m_Name << "\t" << "工资：" << pos->second.m_Salary << endl;
	}
}

int main()
{
	srand((unsigned int)time(nullptr));

	vector<Worker> vWorker;
	createWorker(vWorker);

	//printVector(vWorker);

	multimap<int, Worker> mWorker;
	setGroup(vWorker, mWorker);

	showWorkerByGroup(mWorker);

	system("pause");

	return 0;
}
~~~





### 4.STL-函数对象

#### 4.1 函数对象

##### 4.1.1 函数对象的概念

**概念：**

+ 重载函数调用的操作作符
+ 其对象常称为函数对象
+ 函数对象使用重载的（）时，行为类似函数调用，也叫仿函数

**本质：**

仿函数是一个类



##### 4.1.2 函数对象的使用

**特点：**

+ 函数对象在使用时可以像普通函数一样
+ 函数对象可以有自己的状态
+ 函数对象可以作为参数传递

~~~c++
#include<iostream>
#include<string>

using namespace std;

class MyAdd
{
public:

	//类内写的函数
	int operator()(int v1, int v2)
	{
		return v1 + v2;
	}
};

void test01()
{
	MyAdd myAdd;

	cout << myAdd(10, 11) << endl;
}

class MyPrint
{
public:
	MyPrint()
	{
		this->count = 0;
	}

	void operator()(string test)
	{
		cout << test << endl;
		this->count++;
	}

	int count;//内部自己的状态
};

void test02()
{
	MyPrint myPrint;
	myPrint("hello world");

	cout << "myPrint调用次数" << myPrint.count << endl;
}

void doPrint(MyPrint& mp, string test)
{
	cout << test << endl;
}

void test03()
{
	MyPrint myPrint;
	doPrint(myPrint, "hello c++");
}

int main()
{
	test01();
	test02();
	test03();

	system("pause");

	return 0;
}
~~~





#### 4.2 谓词

##### 4.2.1 谓词的概念

概念：

+ 返回bool类型的仿函数为谓词
+ 如果operator（）接受一个参数，叫做一元谓词
+ 如果operator（）接受两个参数，叫做二元谓词

##### 4.2.2 一元谓词

##### 4.2.3 二元谓词





#### 4.3 内建函数对象

##### 4.3.1 内建函数对象的意义

STL内建了一些仿函数

使用时需要加入头文件`#include<functional>`



##### 4.3.2 算数仿函数

+ 主要功能实现四则运算
+ 其中negate是一元运算，其他都是二元

**函数原型：**

+ `template<class T> T plus<T>`         //加法
+ `template<class T> T minus<T>`        //减法
+ `template<class T> T multiplies<T>`   //乘法
+ `template<class T> T divides<T>`      //除法
+ `template<class T> T modulus<T>`      //取模
+ `template<class T> T negate<T>`       //取反

negate：/plus：

~~~c++
#include<iostream>
#include<functional>

using namespace std;

void test01()
{
	negate<int> n;

	cout << n(50) << endl;
}

void test02()
{
	plus<int> p;
	cout << p(10, 20) << endl;
}

int main()
{
	test01();
	test02();

	system("pause");

	return 0;
}
~~~





##### 4.3.3 关系仿函数

+ `template<class T> bool equal_to<T>`         //等于
+ `template<class T> bool not_equal_to<T>`     //不等于
+ `template<class T> bool greater<T>`           //大于
+ `template<class T> bool greater_equal<T>`     //大于等于
+ `template<class T> bool less<T>`              //小于
+ `template<class T> bool less_equal<T>`       //小于等于



~~~c++
#include<iostream>
#include<vector>
#include<functional>
#include<algorithm>

using namespace std;

class MyCompare
{
public:
	bool operator()(int v1, int v2)
	{
		return v1 > v2;
	}
};

void test01()
{
	vector<int> v;

	v.push_back(1);
	v.push_back(2);
	v.push_back(4);
	v.push_back(5);
	v.push_back(3);

	for (vector<int>::iterator it = v.begin(); it != v.end(); it++)
	{
		cout << *it << " ";
	}
	cout << endl;

	//sort(v.begin(), v.end(), MyCompare());
	sort(v.begin(), v.end(), greater<int>());

	for (vector<int>::iterator it = v.begin(); it != v.end(); it++)
	{
		cout << *it << " ";
	}
	cout << endl;
}

int main()
{
	test01();

	system("pause");

	return 0;
}
~~~





##### 4.3.4 逻辑仿函数

+ `template<class T> bool logical_and<T>`      //与
+ `template<class T> bool logical_or<T>`       //或
+ `template<class T> bool logical_not<T>`      //非



~~~c++
#include<iostream>
#include<vector>
#include<functional>
#include<algorithm>

using namespace std;

class MyCompare
{
public:
	bool operator()(int v1, int v2)
	{
		return v1 > v2;
	}
};

void test01()
{
	vector<bool> v;

	v.push_back(true);
	v.push_back(false);
	v.push_back(true);
	v.push_back(false);

	for (vector<bool>::iterator it = v.begin(); it != v.end(); it++)
	{
		cout << *it << " ";
	}
	cout << endl;

	//取反
	vector<bool> v2;
	v2.resize(v.size());

	transform(v.begin(), v.end(), v2.begin(), logical_not<bool>());

	for (vector<bool>::iterator it = v2.begin(); it != v2.end(); it++)
	{
		cout << *it << " ";
	}
	cout << endl;
}

int main()
{
	test01();

	system("pause");

	return 0;
}
~~~





### 5.STL-常用算法

#### 5.1 常用遍历算法

+ 算法主要是由头文件`<algorithm>``<functional>``<numeric>`组成
+ `<algorithm>`是STL头文件中最大的一个，涉及范围广
+ `<numeric>`体积小，只包括几个简单数学运算的模板函数
+ `<functional>`定义了一些模板类，以声明函数



##### 5.1.1 for_each

+ `for_each(iterator beg, iterator end, _func);`

~~~c++
#include<iostream>
#include<vector>
#include<algorithm>

using namespace std;

void print01(int val)
{
	cout << val << " ";
}

class print02
{
public:
	void operator()(int val)
	{
		cout << val << " ";
	}
};

void test01()
{
	vector<int> v;
	for (int i = 0; i < 10; i++)
	{
		v.push_back(i);
	}

	for_each(v.begin(), v.end(), print01);
	cout << endl;

	for_each(v.begin(), v.end(), print02());
	cout << endl;
}

int main()
{
	test01();

	system("pause");

	return 0;
}
~~~





##### 5.1.2 transform

transform(iterator beg1, iterator end1, iterator beg2, _func);

~~~c++
#include<iostream>
#include<vector>
#include<algorithm>

using namespace std;

class TransFrom
{
public:
	int operator()(int v)
	{
		return v + 2;
	}
};

class MyPrint
{
public:
	void operator()(int val)
	{
		cout << val << " ";
	}
};

void test01()
{
	vector<int> v;
	for (int i = 0; i < 10; i++)
	{
		v.push_back(i);
	}

	vector<int> vTarget;
	vTarget.resize(v.size());

	transform(v.begin(), v.end(), vTarget.begin(), TransFrom());

	for_each(vTarget.begin(), vTarget.end(), MyPrint());

	cout << endl;
}

int main()
{
	test01();

	system("pause");

	return 0;
}
~~~





#### 5.2 常用查找算法

+ find

+ find_if

+ adjacent_find

+ binary_search

+ count

+ count_if



##### 5.2.1 find

find(iterator beg, iterator end, value);

利用find查找指定元素，返回迭代器

~~~c++
#include<iostream>
#include<vector>
#include<string>

using namespace std;

//内置类型
void test01()
{
	vector<int> v;
	for (int i = 0; i < 10; i++)
	{
		v.push_back(i);
	}

	vector<int>::iterator pos = find(v.begin(), v.end(), 5);

	if (pos == v.end())
	{
		cout << "没有找到" << endl;
	}
	else
	{
		cout << "找到" << " " << *pos << endl;
	}
}

class Person
{
public:

	Person(string name, int age)
	{
		this->m_Name = name;
		this->m_Age = age;
	}

	//重载==给find
	bool operator==(const Person& p)
	{
		if (this->m_Name == p.m_Name && this->m_Age == p.m_Age)
		{
			return true;
		}
		else
		{
			return false;
		}
	}

	string m_Name;
	int m_Age;
};

//自定义类型
void test02()
{
	vector<Person> v;

	Person p1("aaa", 10);
	Person p2("bbb", 20);
	Person p3("ccc", 30);
	Person p4("ddd", 40);

	v.push_back(p1);
	v.push_back(p2);
	v.push_back(p3);
	v.push_back(p4);

	Person p("bbb", 20);

	vector<Person>::iterator pos = find(v.begin(), v.end(), p);
	if (pos == v.end())
	{
		cout << "没有找到" << endl;
	}
	else
	{
		cout << "找到" << " " << "姓名：" << pos->m_Name << "\t" << "年龄" << pos->m_Age << endl;
	}
}

int main()
{
	test01();
	test02();

	system("pause");

	return 0;
}
~~~



##### 5.2.2 find_if

find_if(iterator beg, iterator end, _Pred);

区间内满足条件的返回迭代器

~~~c++
#include<iostream>
#include<vector>
#include<string>
#include<algorithm>

using namespace std;

class GreatFive
{
public:
	bool operator()(int val)
	{
		return val > 5;
	}
};

//内置类型
void test01()
{
	vector<int> v;
	for (int i = 0; i < 10; i++)
	{
		v.push_back(i);
	}

	vector<int>::iterator pos = find_if(v.begin(), v.end(), GreatFive());

	if (pos == v.end())
	{
		cout << "没有找到" << endl;
	}
	else
	{
		cout << "找到" << " " << *pos << endl;
	}
}

class Person
{
public:

	Person(string name, int age)
	{
		this->m_Name = name;
		this->m_Age = age;
	}

	string m_Name;
	int m_Age;
};

class Greater20
{
public:
	bool operator()(Person& p)
	{
		return p.m_Age > 20;
	}
};

//自定义类型
void test02()
{
	vector<Person> v;

	Person p1("aaa", 10);
	Person p2("bbb", 20);
	Person p3("ccc", 30);
	Person p4("ddd", 40);

	v.push_back(p1);
	v.push_back(p2);
	v.push_back(p3);
	v.push_back(p4);

	vector<Person>::iterator pos = find_if(v.begin(), v.end(), Greater20());

	if (pos == v.end())
	{
		cout << "没有找到" << endl;
	}
	else
	{
		cout << "找到" << " " << pos->m_Name << endl;
	}
}

int main()
{
	test01();
	test02();


	system("pause");

	return 0;
}
~~~





##### 5.2.3 adjacent_find

+ adjacent_find(iterator beg, iterator end);

~~~c++
#include<iostream>
#include<vector>
#include<algorithm>

using namespace std;

void test01()
{
	vector<int> v;

	v.push_back(0);
	v.push_back(2);
	v.push_back(0);
	v.push_back(3);
	v.push_back(1);
	v.push_back(3);
	v.push_back(3);
	v.push_back(4);

	vector<int>::iterator pos = adjacent_find(v.begin(), v.end());

	if (pos == v.end())
	{
		cout << "未找到！" << endl;
	}
	else
	{
		cout << "找到" << *pos << endl;
	}


}

int main()
{
	test01();

	system("pause");

	return 0;
}
~~~





##### 5.2.4 binary_search

+ bool binary_search(iterator beg,iterator end,value);

在无序序列中不能使用

利用二分查找法速度非常快

~~~c++
#include<iostream>
#include<vector>
#include<algorithm>

using namespace std;

void test01()
{
	vector<int> v;
	for (int i = 0; i < 10; i++)
	{
		v.push_back(i);
	}
	cout << endl;

	bool ret = binary_search(v.begin(), v.end(), 9);

	if (ret)
	{
		cout << "找到元素" << endl;
	}
	else
	{ 
		cout << "未找到元素" << endl;
	}
}

int main()
{
	test01();

	system("pause");

	return 0;
}
~~~





##### 5.2.5 count

+ count(iterator beg, iterator end, valus)

常用统计算法



##### 5.2.6 count_if

+ count(iterator beg, iterator end, _Pred)

按条件进行统计



#### 5.3 常用排序算法

##### 5.3.1 sort

对容器内数据进行排序

默认从小大大进行排序



##### 5.3.2 random_shuffle

洗牌进行数据打乱

提供一个beg和end区间进行打乱



##### 5.3.3 merge

容器中元素合并，并存储到另一元素中

+ `merge(iterator beg1, iterator end1, iterator beg2, iterator end2, iterator dest);`

~~~c++
#include<iostream>
#include<vector>
#include<algorithm>
#include<string>

using namespace std;

void myPrint(int val)
{
	cout << val << " ";
}

void test01()
{
	vector<int> v1;
	vector<int> v2;

	for (int i = 0; i < 10; i++)
	{
		v1.push_back(i);
		v2.push_back(i + 1);
	}

	for_each(v1.begin(), v1.end(), myPrint);
	cout << endl;
	for_each(v2.begin(), v2.end(), myPrint);
	cout << endl;

	vector<int> vTarget;
	vTarget.resize(v1.size() + v2.size());

	merge(v1.begin(), v1.end(), v2.begin(), v2.end(), vTarget.begin());

	for_each(vTarget.begin(), vTarget.end(), myPrint);
	cout << endl;
}

int main()
{
	test01();

	system("pause");

	return 0;
}
~~~





##### 5.3.4 reverse

反转指定范围内元素

+ reverse(iterator beg, iterator end);



#### 5.4 常用拷贝和替换算法

将指定范围内的数据进行修改



##### 5.4.1 copy

拷贝，和等号的区别是可以指定区间

+ copy(iterator beg, iterator end, iterator dest)

目标容器的起始迭代器



##### 5.4.2 replace

修改/替换

+ replace(iterator beg, iterator end, oldValue, newValue)



##### 5.4.3 replace_if

满足条件替换

+ replace(iterator beg, iterator end, _Pred, newValue)



##### 5.4.4 swap

交换

+ swap(c1, c2)

c1和c2必须是同种类型的



#### 5.5 常用算数生成算法

+ 算数生成算法属于小型算法，使用时一般要包含头文件`#include<numeric>`



##### 5.5.1 accumlate

计算容器内区间总和

+ accumlate(beg, end, value);

value起始值



##### 5.5.2 fill

向容器中添加元素

+ fill(beg, end, value);



#### 5.6 常用集合算法

##### 5.6.1 set_intersection

交集

+ set_intersection(beg1, end1, beg2, end2, dest);

~~~c++
#include<iostream>
#include<vector>
#include<algorithm>
#include<numeric>

using namespace std;


void myPrint(int val)
{
	cout << val;
}


void test01()
{
	vector<int> v1;
	vector<int> v2;

	for (int i = 0; i < 10; i++)
	{
		v1.push_back(i);
		v2.push_back(i + 5);
	}

	vector<int> vTarget;

	vTarget.resize(min(v1.size(), v2.size()));
	vector<int>::iterator itEnd = set_intersection(v1.begin(), v1.end(), v2.begin(), v2.end(), vTarget.begin());

	for_each(vTarget.begin(), itEnd, myPrint);
	cout << endl;
}

int main()
{
	test01();

	system("pause");

	return 0;
}
~~~





##### 5.6.2 set_union

并集

+ set_union(beg1, end1, beg2, end2, dest);



##### 5.6.3 set_difference

差集

+ set_difference(beg1, end1, beg2, end2, dest);
