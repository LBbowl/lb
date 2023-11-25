# 1. C++入门



## 1.1 第一个程序“hello world”

**1.编写C++程序的步骤**

- 创建项目
- 创建文件
- 编写代码
- 运行程序

**2.编写“hello world”**

```c++
#include <iostream>
using namespace std;

int main()
{
    cout << "hello world" <<endl;
    system("pause");
    
    return 0;
}
```







## 1.2 程序的注释

**作用：**在代码中添加注释，方便理解。

**两种格式**

**1.单行注释**

`//+描述信息 `    放在语句的末尾，或一句代码的上方对该信息进行说明。

**2.多行注释**

`/* 描述信息*/`    放在一段代码上方，对整段代码进行说明（可多行注释）。







## 1.3 变量

变量创建的语法：数据类型 变量名=变量初始值

实例

``` c++
#include <iostream>
using namespace std;

int main()
{
    int a=0
    system("pause");
    
    return 0;
}
```







## 1.4 常量

**作用：用于记录程序中不可更改的数据**

C++定义常量的两种方式

1**.`#define 宏常量`“： <u>#define 常量名 常量值</u>**

- 通常在文件上方定义，表示一个常量

2.**`const修饰的变量`：<u>const 数据类型 常量名+常量值</u>**

- 通常在变量定义前加关键字const,修饰该变量为常量，不可修改

``````c++
#include <iostream>
using namespace std;
//宏常量
#define a=1
int main()
{
    //const修饰的变量为常量
    const int b =1
    system("pause");
    
    return 0;
}
``````







## 1.5 关键字

**作用：**C++中预先保留的单词（标识符）

- **在定义变量和常量时不要使用关键字**







## 1.6 标识符命名规则

**作用：**C++规定给标识符（变量，常量）命名时保证程序正确运行。

- 标识符不能是关键字
- 标识符只能由字母，数字，下划线组成
- 第一个字符必须为字母或下划线
- 标识符中字母区分大小写







# 2. 数据类型



## 2.1 整型

**作用：**整型变量表示的是整数类型的数据

C++中能够表示整型的类型有以下几种方式，区别在于**所占空间的不同：**

- short(短整型)  
  - 占用**2**字节空间
  - 取值范围为**（-2^15 ~ 2^15-1)**

- int(整型)
  - 占用**4**字节空间
  - 取值范围为**（-2^31 ~ 2^31-1）**

- long(长整型)
  - 占用空间**4**字节（windows,linux 32位），**8**字节（linux 64位）
  - 取值范围为**（-2^31 ~ 2^31-1）**

- long long(长长整型)
  - 占用**8**字节空间
  - 取值范围为**（-2^63 ~ 2^63-1)**







## 2.2 sizeof关键字

**作用：**统计数据类型所占内存的大小

**语法：**`sizeof(数据类型/变量)`

**示例：**

```c++

int main()
{
    cout <<"int 类型所占内存空间为："<<sizeof(int) <<endl;
    system("pause");
    
    return 0;
}
```







## 2.3 实型（浮点型）

**作用：**用于表示小数

浮点型变量分为两种：

- 1.单精度float
- 2.双精度double

两者**区别**在于**有效数字范围不同**



**1.float**

- 占用空间**4**字节
- 范围为**7**位有效数字

**2.double**

- 占用空间**8**字节
- 范围为**15~16**位有效数字

**示例**

`float a=1.01f;`

> C++默认双精度，使用float接受会多一步双精度向单精度转换，因此在末尾加上f以提示







## 2.4 字符型

**作用：**字符型变量用于显示单个字符

**语法：**`char ch=‘a’；`

> PS：1.在显示字符型变量时，用单引号将字符括起来，不要用双引号
>
> 2.单引号内只能有一个字符，不可以是字符串



**例を挙げる：**

```c++
int main()
{
    char ch ='a';//不能为双引号，不能是多个字符
    cout <<ch <<endl;
    system("pause");
    
    return 0;
}
```

awa







## 2.5 转义字符

**作用：**用于表示不能显示出来的ASCII字符

常用的有：`\n  \\  \t`







## 2.6 字符串型

**作用：**用于表示一串字符

**语法：**`string 变量名= “字符串值”`



**示例**

```c++
#include<iostream>
using namespace std;
#include <string>//用C++风格字符串的时候需要包含这个头文件
int main()
{
    //string 变量名= “字符串值”
    string awa="helloworld";
    cout << awa << endl;
    
    system("pause");
   
    return 0;
}
```







## 2.7 布尔类型

**作用：**布尔数据类型代表真或假的值

bool类型只有两个值：

-  true  -- 真（1）
- false   --假（0）
- bool类型占**1个字节**大小

示例：

```c++
int main()
{
    bool awa = true ;
    cout << awa <<endl; // 1
    system("pause");
   
    return 0;
}
```

将显示结果1







## 2.8 数据的输入

**作用：用于从键盘获取数据**

**关键字：**cin

**语法**：```cin >> 变量```

**示例：**

```c++
#include <iostream>
using  namespace std;

int main()
{
//1. 整型输入
    int a=1;
    cin >> a;
    cout << a << endl;
//2. 浮点型输入
    float b = 1.14514f;
    cin >> b;
    cout << b <<endl;
//3. 字符型输入
    char c = 'minecraft';
    cin >> c;
    cout << c <<endl;
//4. 字符串型输入
    string d = "hello";
    cin >> d;
    cout << d <<endl;


//5。布尔类型输入
    bool e=true;
    cin>>e;
    cout << e << endl;


return 0;
}
```







# 3. 运算符

**作用：**用于执行代码的运算

**分类：**

| 运算符类型 | 作用                                   |
| ---------- | -------------------------------------- |
| 算术运算符 | 用于处理四则运算                       |
| 赋值运算符 | 用于将表达式的值赋给变量               |
| 比较运算符 | 用于表达式的比较，并返回一个真值或假值 |
| 逻辑运算符 | 用于根据表达式的值返回真值或假值       |



## 3.1 算数运算符

**作用：**用于处理四则运算

| 运算符 | 术语     | 示例       | 示例结果 |
| ------ | -------- | ---------- | -------- |
| +      | 正号     | +1         | 1        |
| -      | 负号     | -1         | -1       |
| +      | 加       | 1+1        | 2        |
| -      | 减       | 1-1        | 0        |
| *      | 乘       | 2*2        | 4        |
| /      | 除       | 10/5       | 2        |
| %      | 取余     | 10%3       | 1        |
| ++     | 前置递增 | a=2,b=++a; | a=3,b=3; |
| ++     | 前置递减 | a=2,b=a++; | a=3,b=2; |
| --     | 前置递减 | a=2,b=--a; | a=1,b=1; |
| --     | 后置递减 | a=2,b=a--; | a=1,b=2  |



> 1. 加减乘除运算中，整数和整数相除结果为整数，小数部分舍去。
>
> 2. 除数分母不能为0。
>
> 3. 两小数可以相除，结果也可以是小数。
>
> 4. 取模运算中，不可以用两个小数进行运算。
>
>    



递增递减示例：

```c++
#include <iostream>
using  namespace std;
//前置递增与后置递增的区别

//前置递增先进行递增再运算
int main()
{
int a = 1;
int b = ++a*3;
cout << b << endl;//输出b结果为6

//后置递增先进行运算后递增
int c = 1;
int d = c++*3; 
cout << d << endl;//输出d结果为3

return 0;
}
```







## 3.2 赋值运算符

**作用：**用于将表达式的值赋给变量

赋值运算符包括以下几个符号：

| 运算符 | 术语   | 示例     | 结果   |
| ------ | ------ | -------- | ------ |
| =      | 赋值   | a=2;b=3  | a=;b=3 |
| +=     | 加等于 | a=0;a+=2 | a=2    |
| -=     | 减等于 | a=5;a-=3 | a=2    |
| *=     | 乘等于 | a=2;a*=2 | a=4    |
| /=     | 除等于 | a=4;a/=2 | a=2    |
| %=     | 模等于 | a=3;a%2  | a=1    |

```c++
#include <iostream>
using  namespace std;
int main()
{
int a = 1;
a+=1；
cout << a <<endl;//a的结果为2
return 0;
}
```







## 3.3 比较运算符

**作用：**用于表达式的比较，并返回一个真值（1）或一个假值（0）

| 运算符 | 术语     | 示例 | 结果 |
| ------ | -------- | ---- | ---- |
| ==     | 相等于   | 1==2 | 0    |
| !=     | 不等于   | 4!=3 | 1    |
| <      | 小于     | 2<1  | 0    |
| >      | 大于     | 1>3  | 0    |
| <=     | 小于等于 | 1<=2 | 1    |
| >=     | 大于等于 | 3>=1 | 1    |



**示例：**

```c++
#include <iostream>
using  namespace std;
int main()
{
int a = 1;
int b = 2;
cout << (b>=a) <<endl;//返回结果为真（1）
return 0;
    
}
```







## 3.4 逻辑运算符

**作用：**根据一定逻辑和表达式的值来返回真值或假值



| 运算符 | 术语 | 示例   | 结果                                               |
| ------ | ---- | ------ | -------------------------------------------------- |
| !      | 非   | !a     | 如果a为假，则!a为真：如果a为真，则!a为假。         |
| &&     | 与   | a&&b   | 如果a和b都为真，则结果为真，否则为假。             |
| \|\|   | 或   | a\|\|b | 如果a和b有一个为真则结果为真，若全为假则结果为假。 |



**示例：**

```c++
#include <iostream>
using  namespace std;

int main(){

    //逻辑运算符<非>
    int a = 1；
    //在C++中，除0以外都为真
    cout << !a <<endl;//输出假（0）
    
    //逻辑运算符<与>
    int b = 1;
    int c = 1;    
    cout << a && b << endl;//此时a和b均为真，输出真（1）
    
    b-=1
    cout<< a && b <<endl;//此时b为假，结果输出为假（0）
    
   //逻辑运算符<或>
    int d = 1;
    int e = 1;
    cout << d||e << endl;//都为真，结果为真   
    cout << b||d << endl;//有一个假，但结果依然为真
    int f = 0;
    cout << b||f <<endl;//都为假，结果输出为假。
    
    
return 0;
}
```







# 4. 程序流程结构

C/C++支持最基本的三种程序运行结构：**顺序结构，选择结构，循环结构。**

- **顺序结构：**程序按照顺序执行，不发生跳转
- **选择结构：**依据条件是否满足，有选择的执行相应功能
- **循环结构：**依据条件是否满足，循环多次执行某段代码



## 4.1 选择结构



### 4.1.1 if语句

**作用：**执行满足条件的语句

if语句的三种形式

- 单行格式if语句
- 多行格式if语句
- 多条件的if语句



**1.单行格式if语句：**`if（条件）{条件满足执行的语句}`

**举例：**根据分数判断胜利与否

```c++
#include <iostream>
using  namespace std;
int main(){

cout << "输入你的分数:" << endl;
float point = 0;
cin >> point;
//if后面不加分号！！
if(point>=10)
{
cout << "you win!"<<endl;

}
if(point<10)
{
cout << "you lost!" << endl;

}


return 0;
}
```





**2.多行格式if语句：**`if(条件){条件成立执行的代码}else{不成立时执行的代码}`

上一个例子可用多行格式改为：

```c++
#include <iostream>
using  namespace std;
int main(){

cout << "输入你的分数:" << endl;
float point = 0;
cin >> point;
//if后面不加分号！！
if(point>=10)
{
cout << "you win!"<<endl;
}
else{
cout <<"you lost!" << endl;
}

return 0;
}
```





**3.多条件的if语句：**`if(条件1){相应执行代码}else if(条件2){相应执行代码}else if......else{全不满足执行的代码}`

**示例：**

```c++
#include <iostream>
using  namespace std;
int main(){

cout << "输入你的分数:" << endl;
float point = 0;
cin >> point;
//if后面不加分号！！
if(point>=10)
{
 cout << "you are 1th!" << endl;}//10上是第一
    else if(point>5)
    {
     cout << "you are 2th!"<< endl;   //5分到10分为第二
    }      
   else{cout <<"loser" << endl;}//剩下的是失败者
return 0;
}
```





**4.嵌套if语句：**在if语句中，可以嵌套使用if语句，达到更精确的条件判断

**示例：**

```c++
#include <iostream>
using  namespace std;
int main(){

cout << "输入你的分数:" << endl;
float point = 0;
cin >> point;
//if后面不加分号！！
if(point>=10)
{ cout << "you win!" << endl;
 //10~15分胜利，且为第一梯队
  if（point<=15） {cout << "you are the number one!" << endl;} 
}
 else{cout <<"you lost" << endl;}
return 0;
}
```





### 4.1.2 三目运算符

**作用：**通过三目运算符实现简单的判断

**语法：**`表达式1?表达式2：表达式3`

**解释：**

如果表达式1的值为真，执行表达式2，并返回表达式2的结果；

如果表达式1的值为假，执行表达式3，并返回表达式3的结果。

**示例：**

```c++
#include <iostream>
using  namespace std;
int main(){
    int a = 0;
    int b = 1;
    int c = 2;
    int d = 3;
    int e = 4;
   d=a ? b : c;//此时d等于c等于2
   e=d ? b : c;//此时e等于b等于1          
return 0;
}
```







### 4.1.3 switch语句

**作用：**执行多条件分支语句

**语法：**

```c++
switch(表达式)
{
    case 结果1：执行语句;break;
    case 结果2：执行语句;break;
    
    ......
 
    default:执行语句;break;

}
```



**示例：**

```c++
#include <iostream>
using  namespace std;
int main(){
int point=0;
cout <<"请给进击的巨人完结篇后篇打一个分（1~5）" << endl;
cin >> point;
cout << "您为进击的巨人完结篇后篇的打分为:" << point << endl;
switch(point)
{
    case 5:
        cout <<"您认为这是一个完美的结局" << endl;break;
    case 4:
        cout <<"您认为这是一个优秀的结局" << endl;break;
    case 3:
        cout <<"您认为这是一个一般的结局" << endl;break;
    case 2:
        cout <<"您认为这是一个较差的结局" << endl;break;
    case 1:
        cout <<"您认为这是一个糟糕的结局" << endl;break;
        
} 
    return 0;
}
```







## 4.2 循环结构



### 4.2.1 whlle循环语句

**作用：**满足循环条件，执行循环语句

**语法：**`while（循环条件）{循环语句}`

**解释：**只要循环条件结果为真，就不断地执行循环语句



**示例：**

```c++
#include <iostream>
using  namespace std;
int main(){
//在屏幕中完成0~9整数的打印
int a=0;
while(a<10)
{
 cout << a << endl;
    a++;
}
return 0;
}
```





### 4.2.2 do...while循环语句

**作用：**满足循环条件，执行循环语句

**语法：**```do{ 循环语句 } while(循环条件):```

> **注意：**while与do...while的区别是do...while会<u>先执行一次循环语句，再判断循环条件。</u>



**示例：**

```c++
#include <iostream>
using  namespace std;
int main()
{
int a = 0;
int b = 0;
do{
a++;
cout << a << endl;
}while(a);//因为先进行了相加，a为真，因此循环将无限进行

while(b)
{
b++;
cout << b << endl;//一开始进行条件判定，b为假，因此循环从头就无法进行
}

    return 0;
}
```





### 4.2.3 for循环语句

**作用：**满足循环条件，执行循环语句

**语法：**`for（起始表达式;条件表达式;末尾循环体）{循环语句}`



**示例：**

```c++
int main()
{
  for (int i = 0);i<10;i++)
  {
    cout << i << endl;  
  } 
   
    system("pause");
    
    return 0;
}
```





### 4.2.4 嵌套循环

**作用：**在循环体中再嵌套一层循环，解决一些实际问题。



**示例：**

```c++
#include <iostream>
using  namespace std;
int main()
{
  for(int a = 0;a<10 ;a++)  
  { for(int i=0;i<10;i++)
   {
    cout << "1" ;
   }
    cout << endl;//打印一个10x10大小矩阵的数字1
  }
    return 0;
}
```







## 4.3 跳转语句

 

### 4.3.1 break语句

**作用：**用于跳出**<u>选择结构</u>**或者**<u>循环结构</u>**

break使用的时机：

- 出现在<u>switch条件语句</u>中用于终止case并跳出switch
- 出现在<u>循环语句</u>中，作用是跳出当前循环语句
- 出现在<u>嵌套循环</u>中，跳出最近的内层循环语句

**示例1：**

```c++
#include <iostream>
using  namespace std;
int main(){
int point=0;
cout <<"请给进击的巨人完结篇后篇打一个分（1~5）" << endl;
cin >> point;
cout << "您为进击的巨人完结篇后篇的打分为:" << point << endl;
switch(point)
{
    case 5:
        cout <<"您认为这是一个完美的结局" << endl;break;
        //若无break,将会将所有评价一次性都打印出来
    case 4:
        cout <<"您认为这是一个优秀的结局" << endl;break;
    case 3:
        cout <<"您认为这是一个一般的结局" << endl;break;
    case 2:
        cout <<"您认为这是一个较差的结局" << endl;break;
    case 1:
        cout <<"您认为这是一个糟糕的结局" << endl;break;
        
} 
    return 0;
}
```

**示例2：**

```c++
#include <iostream>
using  namespace std;
int main(){
int a=0;
while(a<10)
{
 cout << a << endl;
    a++;
    break;//循环被打破，只会打印一个0
}
return 0;
}
```

**示例3**：

```c++
#include <iostream>
using  namespace std;
int main()
{
  for(int a = 0;a<10 ;a++)  
  { for(int i=0;i<10;i++)
   {
    cout << "1" ;
   }
    cout << endl;break;//此时不再是10x10的1，而是10个1
  }
    return 0;
}
```





### 4.3.2 continue语句

**作用：**在**<u>循环语句</u>**中，跳过剩下未执行部分语句，直接执行下一次循环

**示例：**

```c++
#include <iostream>
using  namespace std;
int main()
{
  for(int i = 0;i<10; i++)
{
if(i % 2 == 0)
{
continue;//如果输出结果是偶数，则不接着打印直接跳入下一循环。
}
cout << i << endl;


}
    return 0;
}//最后输出结果为1到10之间的奇数
```





### 4.3.3 goto语句

**作用：**可以像艾伦一样自♂由地跳转语句

**语法：**

```c++
goto 标记;

...
    
标记:    
```



**示例：**

```c++
#include <iostream>
using  namespace std;
int main()
{ cout << "1" << endl;
 goto MYSELF;
  cout << "2" << endl;
  cout << "3" << endl;
 MYSELF:
  cout << "4" << endl;
    return 0;
}//只输出结果1和4
```







# 5. 数组



## 5.1 数组的概述

所谓数组，就是一个集合，里面存放了相同类型的数据元素

- **特点1**：数组中的每个数据元素都是**<u>相同的数据类型</u>**

- **特点2**：数组是由**<u>连续的内存</u>**位置组成的





## 5.2 一维数组

### 5.2.1 一维数组的定义方式

一维数组定义的三种方式：

- `数据类型 数组名[数组长度];`
- `数据类型 数组名[数组长度] = {值1，值2，值3......};`

- `数据类型 数组名[] = {值1，值2，值3......};`

**示例：**

```c++
int main()
{
  //第1种定义方式，数据类型 数组名[数组长度];
    int score[3];
  //利用下标赋值
  for(int i = 0;i<3;i++)
  { int score[i] =i;
}
  //利用下标输出
   for(int a = 0; a < 3; a++)
   {
     cout << score[a] << endl;
   }
    
    
  
   //第2种定义方式，数据类型 数组名[数组长度] = {值1，值2，值3......};
    //如果{}内不足数据，则会用0补全
   int minecraft[2] = {1,2,3};
    
    //第3种定义方式，数据类型 数组名[] = {值1，值2，值3......};
    int player[]={1,2,3,4,5,6};
    //此时数组会自动检测元素数量。
```



### 5.2.2 一维数组数组名

**一维数组名称的用途：**

- 1.可以统计整个数组在内存中的长度

- 2.可以获取数组在内存中的首地址

**示例：**

```c++
#include <iostream>
using  namespace std;
int main(){
//数组名用途
//1.可以获取整个数组占用内存空间的大小
int arr[] ={1,2,3};
    cout <<"整个数组所占内存空间为：" << sizeof(arr) <<endl;
    cout <<"第一个元素所占内存空间为：" << sizeof(arr[0]) <<endl;
    
//2.可以通过数组名获取到数组首地址
cout <<"数组首地址为：" <<(arr) <<endl;
return 0;
}

```

 



### 5.2.3 冒泡排序

**作用：**最常见的排序算法，对数组内元素进行排序

1.比较相邻的元素。如果第一个比第二个大，就交换他们两个。

2.对每一对相邻元素做同样的工作，执行完毕后，找到第一个最大值。

3.重复以上步骤，每次比较次数-1，直到不需要比较



**示例：**将数组{4,2,8,0,5,7,1,3,9}进行升序排序

```c++
#include <iostream>
using  namespace std;
int main(){
int arr[] ={4,2,8,0,5,7,1,3,9};
for(int i =0;i<9;i++)
{
cout <<arr[i] <<"";
}
//开始冒泡排序
//总排序轮数为 元素个数-1
for (int i =0;i<9-1;i++)
   {
//内层循环对比 次数=元素个数-当前轮数-1
for(int j=0;j<9-i-1;j++)
      {
        //如果第一个数字比第二个数字大。交换两个数字
        if(arr[j]>arr[j+1])
          {
            int temp = arr[j];
            arr[j] = arr[j+1];
            arr[j+1] = temp;

          }
      }
   }

   cout<<"排序后：" ;
   for(int i =0;i<9;i++)
{
cout <<arr[i] <<"";
}
return 0;
}
//排序并输出完成
```





## 5.3 二维数组

二维数组就是在一维数组的基础上<u>增加一个维度</u>。



### 5.3.1 二维数组的定义方式

**二维数组定义的四种方式**

1.`数据类型 数组名[ 行数 ][ 列数 ];`

2.`数据类型 数组名[ 行数 ][ 列数 ] ={{数据1，数据2} , {数据3，数据4}};`

3.`数据类型 数组名[ 行数 ][ 列数 ] ={数据1,数据2,数据3,数据4}；`

4.`数据类型 数组名[ ][ 列数 ] = {数据1,数据2,数据3,数据4;}`

> 建议：以上四种方式，<u>利用第二种方式更加直观，提高代码的可读性</u>

**示例：**

```c++
#include <iostream>
using  namespace std;
int main(){
//1.数据类型 数组名 [行数][列数]；
int arr[1][1];
    arr[0][0]=1;
    arr[0][1]=2;
    arr[1][0]=3;
    arr[1][1]=4;
//2.数据类型 数组名[ 行数 ][ 列数 ] ={{数据1，数据2} , {数据3，数据4}};
 int arr2[2][3] ={{1,2,3},{4,5,6}};
//3.数据类型 数组名[ 行数 ][ 列数 ] ={数据1,数据2,数据3,数据4}；
int arr3[2][3] ={{1,2,3,4,5,6};//系统能区分，但不直观
//4数据类型 数组名[ ][ 列数 ] = {数据1,数据2,数据3,数据4;}
int arr4[][3] ={1,2,3,4,5,6};//系统自动识别列数
return 0;
}
```





### 5.3.2 二维数组数组名

- 查看二维数组所占内存空间
- 获取二维数组的首地址

**示例：**

```c++
int main(){
 //二维数组数组名  
    int arr[2][3]={{1,2,3},{4,5,6}};
    cout <<"二维数组大小： " << sizeof(arr) <<endl;
    cout <<"二维数组一行大小："<< sizeof(arr[0])<<endl;
    cout <<"二维数组元素大小：" <<sizeof(arr[0][0])<<endl;
 //获取二维数组首地址
    cout << "二维数组首地址" <<arr <<endl;
    return 0;
}
```







# 6. 函数



## 6.1 概述

**作用：**将一段经常使用的代码封装起来，减少重复代码

一个较大的程序，一般分为若干个程序块，每个模块实现特定的功能。







## 6.2 函数的定义

函数的定义一般有5个步骤

- 返回值类型
- 函数名
- 参数表列
- 函数体语句
- return表达式

**语法：**

```c++
返回值类型 函数名 （参数列表）
{
    
    函数体语句
    
    return表达式
}
```

**示例：**

```c++
//加法函数，实现两个整形的相加，并且将相加的结果进行返回
int add(int num1, int num2)
{
   int sum = num1+num2;
   return sum;
    
}
```







## 6.3 函数的调用

**功能：**使用定义好的函数

**语法：**`函数名(参数)`

**示例：**

```c++
//创建函数时，num1，num2不是真实的数据，只是形式上的参数，简称形参
int add(int num1, int num2)
{
   int sum = num1+num2;
   return sum;
    
}
int main(){
    //main函数中调用add函数
    int a =10;
    int b =20;
    //语法：函数名称(参数)
    //a和b称为 实际参数，简称实参
    //当调用函数的时候，实参的值会传递给形参
    add(a,b);
    return 0;
}
```





## 6.4 值传递

- 所谓值传递，就是函数调用时实参将数值传入给形参
- 值传递时，**如果形参发生改变，并不会影响实参**

**示例：**

```c++
//如果函数不需要返回值，声明的时候可以写void
void swap(int num1,int num2)
{
    cout <<"交换前：" <<endl;
    cout <<"num1 =" <<num1 <<endl;
    cout <<"num2 =" <<num2 <<endl;
    int temp =num1;
        num1 = num2;
        num2 = temp;
    cout <<"交换后：" <<endl;
    cout <<"num1 =" <<num1 <<endl;
    cout <<"num2 =" <<num2 <<endl;
}
 int main(){
     int a =10;
     int b =20;
     cout <<"a= "<< a <<endl;
     cout <<"b= "<< b <<endl;
     //当我们做值传递的时候，函数的形参发生改变时并不会影响实参
     swap (a,b)
     cout <<"a= "<< a <<endl;
     cout <<"b= "<< b <<endl;
     //此时a和b输出结果不变
 }
```





## 6.5 函数的常见样式

常见的函数样式有4种

- 无参无返
- 有参无返
- 无参有返
- 有参有返

**示例：**

```c++
//函数的常见形式
//1.无参无返
void test01()
{
 cout <<"这是test01" << endl;
 //test01();函数调用
}

//2。 有参无返
void test02(int a)
{
 cout <<"这是test02" << endl;
}

//3,无参有返
int  test03()
{
 cout << "这是test03" << endl;   
 return 0;
}
//4.有参有返
int test04(int b)
{
    cout << "这是test04" << endl;
    return 0;
}

int main(){
test01();
    
test02(100);
    
int num1 = test03()
    cout <<"num1 =" <<num1 << endl;
    
int num2 = test04(10000);
    cout << "num2 = "<<num2 << endl;
}
```





## 6.6 函数的声明

**作用：**告诉编译器函数名称以及如何调用函数。函数的实际主体可以单独定义。

- 函数的声明可以多次，但是函数的**<u>定义只能有一次</u>**

**示例：**

```c++
#include<iostream>
using namespace std;
//提前告诉编译器函数的存在，可以利用函数的声明
//函数的声明
int max(int a;int b);

int main()
{
    int a = 10;
    int b = 20;
    
    cout << max(a,b) <<endl;
    return 0;
}

int max(int a,int b)
{
    return a > b ? a : b;
}

```





## 6.7 函数的分文件编写

**作用：**让代码结构更加清晰

函数分文件编写一般有**<u>4个步骤</u>**

- 1.创建后缀名为h.的头文件

- 2.创建后缀名为.cpp的源文件

- 3.在头文件中写函数的声明

- 4.在源文件中写函数的定义







# 7. 指针



## 7.1 指针的基本概念

**指针的作用：**可以通过指针间接访问内存



- 内存编号是从0开始记录的，一般用十六进制的数字表示
- 可以利用指针变量保存地址





## 7.2 指针变量的定义和使用

指针变量定义语法：`数据类型 * 变量名；`

**示例：**

```c++
int main()
{
  //1.定义指针
    int a = 10;
  //指针定义的语法：数据类型 * 指针变量
    int * p;
  //让指针记录变量a的地址
    p = &a;
    cout << "a的地址为： " << &a <<endl;
    cout <<"指针p为： " << p <<endl;
    //2.使用指针
    //可以通过解引用的方式来找到指针指向的内存
    //指针前加*代表解引用，找到指针指向的内存中的数据
    *p = 1000;
    cout <<"a = " << a <<endl;
    cout <<" *p = " << *p <<endl;
    system("pause");
    
    return 0;
}
```







## 7.3 指针所占内存空间

**示例：**

```c++
include<iostream>
using namespace std;
int main(){
int a = 10;
int * p = &a;
    //32位系统占4字节内存，64位系统8字节内存，不管是哪种数据类型
cout <<"sizeof int *p =" << sizeof(int *)<<endl;
cout <<"sizeof int *p =" << sizeof(float *)<<endl;
cout <<"sizeof int *p =" << sizeof(double *)<<endl;
cout <<"sizeof int *p =" << sizeof(char *)<<endl;
 
    system("pause");
    
    return 0;
}
```







## 7.4 空指针和野指针

**空指针：**指针变量指向内存中编号为0的空间

**用途：**初始化指针变量

**注意：**空指针指向的内存是不可以访问的

**示例1：空指针**

```c++
include<iostream>
using namespace std;
int main(){
//空指针
//1.空指针用于给指针变量进行初始化
int * p = NULL;
//2.空指针是不可以进行访问的
//内存编号0~255为系统占用内存，不允许用户访问
*p = 100;
system("pause");
    
return 0;
}
```



**野指针：**指针变量指向非法的内存空间

**示例2：野指针**

```c++
include<iostream>
using namespace std;
int main(){
//指针变量指向内存地址编号为0x1100的空间
int *p =(int *)0x1100;
    
//访问野指针报错
 cout <<*p<<endl;
    
system("pause");
    
return 0;
}
```





## 7.5 const修饰指针

const修饰指针有三种情况：

- const修饰指针 ----常量指针
- const修饰常量 ----指针常量 
- const即修饰指针，又修饰常量

**示例：**

```c++
int main(){
    int a = 10;
    int b = 10;

 //const修饰的是指针，指针指向可以改，指针指向的值不能改
    const int * p1 =&a;
    p1 = &b;//正确
    //*p1 = 100;报错
    
 //const修饰的常量，指针指向不可以改，指针指向的值可以更改
    int * const p2 = &a;
    //p2 = &b;错误
    *p2 =100;//正确
 //const修饰指针和常量，指向和值都不可以改
   const int * const p3 = &a;
     //p3 = &b;错误
     // *p3 =100;错误
    system("pause");
    
    
}
```







## 7.6 指针和数组

**作用：**利用指针访问数组中的元素

**示例：**

```c++
int main(){
 int arr[] = {1,2,3,4,5,6,7,8,9,10}; 
}
```

