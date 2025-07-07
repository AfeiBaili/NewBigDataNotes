- # <a href="#java">Java</a>
    - ## <a href="#java-初出茅庐">初出茅庐</a>
        - ### <a href="#java-环境搭建">环境搭建</a>
        - ### <a href="#java-首次运行">首次运行</a>
        - ### <a href="#java-注释">注释</a>
        - ### <a href="#java-关键字">关键字</a>
        - ### <a href="#java-标识符">标识符</a>
    - ## <a href="#java-渐入佳境">渐入佳境</a>
        - ### <a href="#java-变量">变量</a>
        - ### <a href="#java-数据类型">数据类型</a>
        - ### <a href="#java-运算符">运算符</a>
        - ### <a href="#java-流程控制">流程控制</a>
        - ### <a href="#java-数组">数组</a>
    - ## <a href="#java-炉火纯青">炉火纯青</a>
        - ### <a href="#java-面向对象">面向对象</a>
        - ### <a href="#java-方法">方法</a>
        - ### <a href="#java-属性">属性</a>
        - ### <a href="#java-构造器">构造器</a>
        - ### <a href="#java-封装">封装</a>
        - ### <a href="#java-this关键字">this关键字</a>
        - ### <a href="#java-继承">继承</a>
        - ### <a href="#java-super关键字">super关键字</a>
        - ### <a href="#java-多态">多态</a>
        - ### <a href="#java-object类">Object类</a>
        - ### <a href="#java-static关键字">static关键字</a>
        - ### <a href="#java-代码块">代码块</a>
        - ### <a href="#java-final关键字">final关键字</a>
    - ## <a href="#java-登峰造极">登峰造极</a>
        - ### <a href="#java-抽象类">抽象类</a>
        - ### <a href="#java-接口">接口</a>
        - ### <a href="#java-内部类">内部类</a>
        - ### <a href="#java-枚举类">枚举类</a>
        - ### <a href="#java-注解">注解</a>
        - ### <a href="#java-包装类">包装类</a>
        - ### <a href="#java-异常处理">异常处理</a>
        - ### <a href="#java-多线程">多线程</a>
        - ### <a href="#java-常用类">常用类</a>
            - ### <a href="#java-string类">String类</a>
            - ### <a href="#java-stringbuilder和stringbuffer">StringBuilder和StringBuffer</a>
            - ### <a href="#java-时间类">时间类</a>
            - ### <a href="#java-比较器">比较器</a>
            - ### <a href="#java-其他常用类">其他常用类</a>
        - ### <a href="#java-泛型">泛型</a>
        - ### <a href="#java-集合框架">集合框架</a>
        - ### <a href="#java-io">IO</a>
            - ### <a href="#java-常用流">常用流</a>
            - ### <a href="#java-网络编程">网络编程</a>
        - ### <a href="#java-反射">反射</a>

# <div id="java">Java</div>

Java是Sun公司开发的一门**面向对象**语言，Java不仅继承了C++的优点，还抛弃了C语言中的指针等概念。
Java可以做到灵活简单功能强大，极好地实现了面向对象等理论

Java的优点有跨平台性（可以在多个操作系统中运行一样的代码）、面向对象（是一种程序设计技术，适合大型软件的设计和开发，让程序更好地达到高内聚、低耦合的标准）、
安全性高（适合于网络/分布式环境，可以分配不同的命名空间防止同类名）

## <div id="java-初出茅庐">初出茅庐</div>

## <div id="java-环境搭建">环境搭建</div>

在开始之前要先下载Java的开发工具包即**JDK**推荐使用**JDK17**和**JDK8**
JDK下载地址**https://adoptium.net/zh-CN/**

压缩包的格式下载完之后需要配置环境变量，拿到其中的压缩包解压，找到本机中的***环境变量**配置 >
找到系统变量 > 找到并点击Path > 点击新建 > 进入JDK解压目录 > 找到bin目录 > 复制bin的所在目录 >
添加到新建*中即可完成Java的环境变量配置

打开控制台终端输入`java -version`如果打印出你安装的版本号即表示安装成功

## <div id="java-首次运行">首次运行</div>

使用Java编写 HelloWorld 让Java语言打印出一串字符串

```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello World");
    }
}
```

其中被高亮的词代表着这是一个关键字。
关键字解释，在开始的阶段不理解其中的意思也无关紧要，只需留下一个初步的印象

| 关键字    | 解释    |
|--------|-------|
| public | 公开的   |
| class  | 类的声明  |
| static | 静态的   |
| void   | 返回值为空 |

## <div id="java-注释">注释</div>

其中在编程语言中注释代表着代码的解释，是由开发者本人编写，用于解释代码的意思。
注释又分为单行注释和多行注释

单行注释顾名思义只在一行中的注释使用`//`进行表示这是一个单行注释

```java
//这是单行注释，Java不会执行此行代码
int i = 0; //前面的代码会被执行，斜杠后面的文字不会被执行
```

多行注释可跨越多行，其功能和单行注释一样只是用于解释代码

```java
/*多行注释
可以跨越多行*/
int i = 0;
/*也可以这样写*/
```

其中Java文档注释也是属于多行注释，但是可以被javadoc（bin目录下的工具）工具解析成Javadoc文档

```java
/**
 * Javadoc注释常常用于解释类的、方法的、变量的功能，
 *
 * @param args 运行时传入的参数
 */
//此方法为main方法是Java程序的入口，如果没有main方法Java程序将无法运行
public static void main(String[] args) {

}
```

## <div id="java-关键字">关键字</div>

在Java关键字的作用至关重要，被Java语言赋予了特殊含义，用做专门用途的单词。
在HelloWorld案例中出现的关键字有class、public、static、void等，这些单词是Java定义好的。
关键字的特点就是全部都是小写的，关键字较多，不要死记硬背，用到哪里写到哪里即可

## <div id="java-标识符">标识符</div>

在Java中变量名、方法名、类名、形参名等要素命名时使用的字符序列成为**标识符**，可以记为自己在写代码中需要自己起名字的地方就叫标识符

> Java标识符的命名规范：
>
> 1. 由26个英文字母、0-9的数字、_下划线和$刀乐符组成组成
> 2. 不能以数字开头
> 3. 不能使用Java的关键字，但是可以包含关键字
> 4. 不能包含空格
> 5. 使用时严格区分大小写，长度无限制

## <div id="java-渐入佳境">渐入佳境</div>

## <div id="java-变量">变量</div>

变量是在内存的一个存储区域，相同的值类型可以此变量不断的变化，其中Java中有多个类型，
常见的类型有**字符串**、**数字**、**浮点数**类型

变量的的组成有**数据类型**、**变量名**、**存储的值**，他的作用是在内存中保存数据，
他存储的值是可以更改的

```java
//以下创建了一个变量

//声明类型为int类型，变量名为a，使用等号赋值，存储的值为10
int a = 10;
```

以下是更详细的示例

```java
public class Demo {
    public static void main(String[] args) {
        //声明一个变量为a
        int a = 1;
        //打印的值为1
        System.out.println("打印的值为：" + a);
        int a = 25; //此行报错，不能在一个作用域声明相同的变量名，可以理解为一个大括号为一个作用域
        //将变量a的值从1变成了25
        a = 30;
        //打印的值为30，因为更改了a的变量值
        System.out.println("打印的值为：" + a);
        //声明一个类型为字符串的类型，值为Hello World
        String b = "Hello World";
    }
}
```

## <div id="java-数据类型">数据类型</div>

Java是一个严格类型判断语言，它的数据类型至关重要，其中分为两大类，基本数据类型、引用数据类型

基本数据类型有：

- 整形：byte \ short \ int \ long
- 浮点型：float \ double
- 字符型：char
- 布尔型：boolean

引用数据类型有：

- 类（class）
- 数组（array）
- 接口（interface）
- 枚举（enum）
- 注解（annotation）
- 记录（record）

为什么要有这么多整形呢？我们带着这个疑问想到，在Java中不同的整形类型的内存占用大小是不太一样的，通过下表表示

| 类型    | 占用空间 | 范围                               |
|-------|------|----------------------------------|
| byte  | 1字节  | -128~127                         |
| short | 2字节  | -2<sup>15</sup>~2<sup>15-1</sup> |
| int   | 4字节  | -2<sup>31</sup>~2<sup>31-1</sup> |
| long  | 8字节  | -2<sup>63</sup>~2<sup>63-1</sup> |

其中声明long类型的时候要在数字最后加一个L或者l来标识这是一个long类型，这是Java的规定

```java
//声明一个long类型
long a = 123456789L;
```

> 在Java中默认的数字类型是int类型

浮点类型有两种，分别是float和double其中float为单精度类型，double为双精度类型。
声明float类型时要在数字后添加f或者F代表这是一个float类型

```java
//需要浮点数后添加f
float a = 1.0f;
//不需要添加后缀
double b = 1.0;
```

| 类型     | 占用空间 | 范围                   |
|--------|------|----------------------|
| float  | 4字节  | -3.403E38~3.403E38   |
| double | 8字节  | -1.798E308~1.798E308 |

float的尾数可以精确到7位有效数字。double是float的两倍，虽然double已经表示很多位数了，
但是还是会有误差，可以使用**BigDecimal**类做到零误差

char类型用来表示一个字符，占用两个字节。Java中所有字符都是使用的Unicode编码，
所以一个字符可以存储一个字母、一个汉字等等。通常使用单引号来表示一个chat类型`char a = 'a'`，
也可以使用Unicode值来表示char类型`char a = '\uxxxx'`，
最重要的是使用转义字符例如`char a = '\n'`代表一个换行符，
也可以使用数字来表示解析字符`chat a = 90'`

布尔类型通常是用于判断逻辑中，在流程控制语句中比较常见，boolean类型只有两个值，为true和false，
下面是一个布尔类型的示例

```java
public static void main(String[] args) {
    boolean isTrue = true;
    if (isTrue) {
        System.out.println("isTrue是真的");
    } else {
        System.out.println("isTrue是假的");
    }
}
```

在Java中做基本的类型运算时会有基本数据类型运算问题， 一个基本数据类型和另一个较高的数据类型运算时，结果自动转换为容量大的数据类型。
可以使用强制类型转换进行低精度转换

```java
int a = 1;
//将int类型a转换为byte类型b，会有精度丢失问题，因为他们的存储字节大小不一致
byte b = (btye) a; 
```

在Java中String是一个类，并不是基本数据类型，而是引用数据类型。使用`""`双引号进行表示字符串，
且String类型只能使用以`+`运算符进行连接，即拼在一起为新的字符串

```java
public static void main(String[] args) {
    boolean a = true;
    String b = "你好";
    System.out.println(a + b);//结果为：true你好
}
```

> 由于字符串类型十分的常用所以Java把字符串的赋值特意简化了

## <div id="java-运算符">运算符</div>

运算符是一种特殊的符号，用于表示数据的运算、比较、赋值等

运算符的分类：

| 类别        | 运算符                                      |
|-----------|------------------------------------------|
| 算术运算符     | +、-、*、/、%、++、--                          |
| 赋值运算符     | =、+=、-=、*=、/=、%=、>>=、<<=、>>>=、&=、 \|=、^= |
| 比较运算符     | \>、>=、<、<=、==、!=                         |
| 逻辑运算符     | &、&&、\|、\| \|、^、!                        |
| 位运算符      | &、\|、^、~、>>、<<、>>>                       |
| 三元运算符     | (条件表达式)?结果a:结果b                          |
| Lambda运算符 | ->                                       |

运算符的使用：

| 运算符        | 解释                 | 示例                      | 结果    |
|------------|--------------------|-------------------------|-------|
| +          | 加法运算               | 1+1                     | 2     |
| -          | 减法运算               | 1-1                     | 0     |
| *          | 乘法运算               | 2*2                     | 4     |
| /          | 除法运算               | 1/1                     | 1     |
| %          | 取余运算               | 3*2                     | 1     |
| +          | 字符串拼接              | "早"+1                   | 早1    |
| ++         | 自增运算（自增1，同 1 += 1） | ++1                     | 2     |
| --         | 自减运算（自减1，同 1 -= 1） | --1                     | 0     |
| =          | 赋值运算               | a = 1                   | 1     |
| +=         | 相加并赋值（其中a=1）       | a += 1                  | 2     |
| -=         | 相减并赋值（其中a=1）       | a -= 1                  | 0     |
| *=         | 相乘并赋值（其中a=1）       | a *= 1                  | 1     |
| /=         | 相除并赋值（其中a=1）       | a /= 1                  | 1     |
| %=         | 取余并赋值（其中a=1）       | a %= 1                  | 0     |
| ==         | 等于                 | 1 == 1                  | true  |
| !=         | 不等于                | 1 != 1                  | false |
| \>         | 大于                 | 1 > 1                   | false |
| <          | 小于                 | 1 < 1                   | false |
| \>=        | 大于等于               | 1 >= 1                  | true  |
| <=         | 小于等于               | 1 <= 1                  | true  |
| instanceof | 判断实例是否匹配类类型        | "str" instanceof String | true  |

> 其中`++`运算又分为前++和后++，前++是先+=1再进行运算，后++是先运算后+=1，`--`同理，**注意`++`和`--`只能在变量上使用**
> ```java
> public static void main(String[] args){
>   int a = 2;
>   System.out.println(2 * ++a);    //打印6
>   a = 2;                          //重置
>   System.out.println(2 * a++);    //打印4
> }
> ```
> `=`运算符也可以进行连续运算符例如`a = b = 20;`

位运算是难点，但是想要成功优秀的程序员就要学会使用位运算，平时使用可以了解，部分地方使用位运算可以提高代码的性能但提升的性能是微乎其微，
对于一个会使用位运算的程序员，会不会感到很酷哈哈。位运算是操作二进制进行运算，操作涉及二进制

位运算解释：

- <<：向左移一位，空位补零，高位丢弃。例如：**0001**四个bit位的二进制表示1，左移一位变成**0010**的二进制表示2
- \>>：向右移一位，高位为一，高位补一，为零补零。例如：**0001**四个bit位的二进制表示1，右移一位变成**0000**的二进制表示0
- \>>>：向右移一位，无论如何都补零，无符号代表不包含负数，所以高位一直为零
- &：比较每个位，都是1补1如果一个为0就为0，0110和0010做&运算结果为0010，因为只有一个位全都是1
- |：比较每个位，如果一个位为1就为1
- ^：比较每个位，如果一个位和另一个位不相同就为1反之为0
- ~：取反这个数的每个位1为0，0为1

> 在编程中int类型代表四个字节一个字节又是八个bit位，如下：00000000 00000000 00000000 00000001，表示十进制的1。
> 其中在左边首个bit位如果为1就代表这个数为负数

逻辑运算符解释：

- &、&&：逻辑与，表示且关系，需要两边都为真结果才为真，&&运算符中其中第一个就是false就不会判断之后值，但是&会全部运算
- |、||：逻辑或，表示或关系，有一个为真结果就为真，|即使第一个为真，后面的也要计算，||如果第一个为真后面将不再计算
- ！：逻辑非，表示相反，值如果为真结果为假，值为假结果为真
- ^：逻辑异或，两边结果不同才为真，相同为假

逻辑运算符示例：

| a     | b     | a&b   | a&&b  | a\|b  | a\|\|b | !a    | a^b   |
|-------|-------|-------|-------|-------|--------|-------|-------|
| true  | true  | true  | true  | true  | true   | false | false |
| true  | false | false | false | true  | true   | false | true  |
| false | true  | false | false | true  | true   | true  | true  |
| false | false | false | false | false | false  | true  | false |

三元运算符相比就比较简单了，就像一个简单的if判断一样`布尔表达式 ? 值1 : 值2`

```java
public static void main(String[] args) {
    //判断1是否大于2如歌大于就返回第一个值
    String string = 1 > 2 ? "是的1大于2" : "不是的1不大于2";
    System.out.println(string);
}
```

## <div id="java-流程控制">流程控制</div>

流程控制语句是指，控制代码流程的语句。代码是依次向下执行的，可以使用分支语句达到代码的分支切换，使用循环语句循环处理逻辑和值

分支语句含有if else表达式，和switch case语句。其中if的用法为`if(条件表达式（结果为布尔值）) {执行语句}`，
也可以加上else进行分支`if(条件表达式（结果为布尔值）) {执行语句} else {执行语句}`

```java
public static void main(String[] args) {
    //使用if判断是否为真
    if (1 > 2) {
        //如果达到条件执行此括号语句...
    }
    //使用if判断是否为真
    if (1 > 2) {
        //如果达到条件执行此括号语句...
    } else {
        //如果if的结果为假执行此括号语句，即if判断加上else进行二选一
    }
    //如果大括号代码只有一行，可以省略大括号
    if (1 > 2) System.out.println("一大于二");
    else System.out.println("一不大于二");
}
```

使用switch进行多分支，switch表达式中需要传入一个值，然后代码会根据值来查找相应的case语句，
其中break关键字代表着终止流程控制语句，使其跳出语句

```java
public static void main(String[] args) {
    int a = 1;
    //判断今天星期几
    switch (a) {
        case 1:
            System.out.println("今天星期一");
            break;
        case 2:
            System.out.println("今天星期二");
            break;
        //.....
        default://如果以上的值都没有命中就执行以下语句
            System.out.println("不知道今天星期几");
    }
}
```

循环语句有for循环、while循环、do while循环，指的是在某些条件下反复执行的语句

for循环可以在声明的时候初始化一个值，使用方法为`for(初始化语句;条件判断;更新语句) {//执行语句}`

```java
public static void main(String[] args) {
    //从0开始，判断1是否大于10，如果条件达成执行语句，最后再走更新语句
    for (int i = 0; i < 10; i++) {
        System.out.println("i当前是：" + i);
    }
    //在for循环语句嵌套其他语句，例如嵌套for循环
    for (int i = 0; i < 10; i++) {
        //以下循环十次
        for (int j = 0; j < 10; j++) { //其中i已经在这个作用域赋值过了，变量名不能重复
            //执行语句，执行十次
        }
    }
}
```

while循环只有一个条件判断，相比for循环少了初始化语句和更新语句，但是可以在while循环外写初始化语句，
在执行语句中写更新语句，更加自由和简单。

do while和while不同的是，while是先判断再执行，而do while可以先执行一次再判断

```java
public static void main(String[] args) {
    int a = 0;
    while (a < 10) {
        a++;
        //执行语句
    }
    //也可以把++写道while的条件表达式中
    while (a++ < 10) {
        //执行语句
    }

    //do while使用
    do {
        //先执行后判断，如果条件不成立就不执行
    } while (a++ < 10);
}
```

在流程控制中关键词字**break**的作用是跳出此流程控制，**continue**关键字可以跳过此循环进行下一次循环，而break是跳出循环、结束循环

## <div id="java-数组">数组</div>

数组（array）是指的是多个相同类型的集合，并只用一个变量名命名，通过下标的方式进行取值，方便集中管理。在数组中下标用于获取值的位置，
元素指的是数组中的值，可以根据数组的长度获取到每一个元素。下标的数值是从0开始。

数组可以为引用数据类型也可以为基本数据类型，其中变量名引用数组的内存位置，数组中所有的元素都是在内存中紧紧挨着的。

一个用表格表示的数组：

| 值1  | 值2  | 值3  | 值4  | 值...  |
|-----|-----|-----|-----|-------|
| 下标0 | 下标1 | 下标2 | 下标3 | 下标... |

```java
//声明一个数组并初始化值，也叫做静态初始化
int[] arrayInt = new int[]{1, 2, 3, 4, 5, 6};
//也可以使用基本类型推断来声明一个数组
int[] arrayInt2 = {1, 2, 3, 4, 5, 6};
//声明一个长度为10的空数组，也叫做动态初始化
int[] arrayInt3 = new int[10];
//声明一个String类型的数组并初始化
String[] strings = new String[]{"Hi", "Hello", "你好"};

//通过下标获取数组的值
String string = strings[0];     //拿到下标为零的元素，为 Hi
String string2 = strings[1];    //拿到 Hello
String string3 = strings[2];    //拿到 你好

//获取数组长度，使用数组自带的属性“.length”
int arrayLength = strings.length; //长度为 3
```

我们拿到数组的长度就可以使用循环遍历数组

```java
public static void main(String[] args) {
    String[] strings = new String[]{"Hi", "Hello", "你好"};

    for (int i = 0; i < strings.length; i++) {
        //将此次循环的i值赋给到数组的下标，在i开始时为0对应着下标0
        System.out.println(strings[i]);
    }

    //如果在使用数组时访问超出下标的范围就会报出数组下标越界异常
    //使用throw关键字抛出一个异常，格式throw [异常对象]
    throw new IndexOutOfBoundsException();
}
```

> 为什么数组的下标要从零开始？因为数组的结构是放在内存的堆空间中紧密排列的是一块连续的内存空间，每个元素对应着第一个元素的偏移量，
> 因为第一个元素的偏移量为0，所以下标从0开始

建议要学会冒泡算法，冒泡算法是最简单的排序算法之一，学会此算法可以锻炼你的空间能力、逻辑编程能力。下方是代码，
看不懂没有关系，不好理解的可以去查资料，问老师问同学。

```java
public static void main(String[] args) {
    //创建一个无序列表
    int[] arr = {6, 9, 4, 1, 3, 2, 4, 9, 5, 6, 2, 1};
    //使用Arrays类打印此数组（暂未学到）
    System.out.println(Arrays.toString(arr));

    //双重for循环
    for (int i = 0; i < arr.length; i++) {
        for (int j = i + 1; j < arr.length; j++) {
            //判断前方的值是否大于后方的值
            if (arr[i] > arr[j]) {
                //如果大于值就交换
                int temp = arr[i];
                arr[i] = arr[j];
                arr[j] = temp;
            }
        }
    }

    //使用Arrays类打印此数组（暂未学到）
    System.out.println(Arrays.toString(arr));
}
```

一维数组就像是一排数据，而二维数组就像是一张表，也就是多排数据，当然也还有三维四维...

声明一个二维数组：

```java
int[][] arrayInt = {{1, 2, 3}, {4, 5, 6}, {7, 8, 9}};
//更直观的声明
int[][] arrayInt2 = {
        {1, 2, 3},
        {4, 5, 6},
        {7, 8, 9}
};
//使用下标访问 arrayInt[0][1] 拿到元素2
//动态初始化长度为3的数组，元素中的数组也为3的数组
int[][] arrayInt3 = new int[3][3];  
```

数组工具类（Arrays），在`java.util`中有个Arrays类，此类有许多静态方法，用于数组的方法，静态方法可以直接调用。

使用`import java.util.Arrays;`导入此类，import关键词是导入用的关键字，用于导入包、类、静态字段。

```java
public static void main(String[] args) {
    //判断两个数组是否相等，比较的是每一个值是否相等，长度是否相同
    int[] arr = {1, 2, 3, 4, 5, 6};
    int[] arr2 = {1, 2, 3, 4, 5, 6};

    System.out.println(Arrays.equals(arr, arr2));

    //使指定的值填充到数组内，填充每一个数组
    Arrays.fill(arr, 1);
    System.out.println(Arrays.toString(arr));

    //使用快速排序算法进行排序
    arr = new int[]{6, 9, 4, 1, 3, 6, 4};
    Arrays.sort(arr);
    System.out.println(Arrays.toString(arr));

    //二分查找，前提数组是有序的，返回一个数值的索引下标
    System.out.println(Arrays.binarySearch(arr, 6));
}
```

## <div id="java-炉火纯青">炉火纯青</div>

## <div id="java-面向对象">面向对象</div>

Java之所以受高端应用青睐，离不开的是Java的面向对象，对于Java来说面向对象是它的心脏，也是Java中较难理解的地方

对象是类的实例也就是类的对象，一个类的成员都有**属性、方法、构造器、代码块、内部类**。
面向对象三大特征：**封装、继承、多态**。
面向对象常用关键字：**new、this、super、import、package，static、final、interface、abstract...**

面向对象是软件开发中的编程风格、开发范式。除了**面向对象**、还有面向过程、指令式编程、**函数式编程**。
早期先有的面向过程，随着应用逻辑的复杂化，面向过程已经不能解决这个问题之后出现了面向对象思想并成为主流编程方式。

面向对象的主要成分是类和对象；   
类：具有相同特征的事物的抽象描述，是抽象的，概念上的定义  
对象：实际存在的该事物的每个个体，是具体的，因此也被称为实例  
可以理解为，类=对某一个人的描述、对象=就在眼前的一个人。

```java
//声明一个Cat类
class Cat {
    //喵咪身上的属性
    int age; //它的年龄
    int weight; //它的体重

    //此方法是静态的所以它和Cat类并没有太大的关系，放在这里只是方便调试
    public static void main(String[] args) {
        //使用new关键字给对象开辟一块内存空间，也是创建一个对象的方法
        Cat cat = new Cat();
        //创建好对象可以通过对象调用里面的方法。
        cat.eat();

        //也可以更改猫咪身上的属性，每个对象中的属性是不相关我更改第二个猫咪对象，第一个猫咪对象没有变化
        Cat cat2 = new Cat();
        //更改猫咪的体重
        cat2.weight = 20;

        //同时打印两种猫咪的体重
        System.out.println("cat的体重是：" + cat.weight);
        System.out.println("cat2的体重是：" + cat2.weight);

        //调用带参数的方法
        cat2.sleep(30);
    }

    //猫咪身上的方法
    public void eat() { //猫咪吃东西的方法
        System.out.println("猫咪正在吃东西！"); //具体实现
    }

    public void birthday() { //猫咪过生日的方法
        this.age++;
        System.out.println("猫咪今天过生日");
    }

    public void sleep(int minutes) { //猫咪睡觉的方法，其中形参里面有个minutes的参数
        System.out.println("猫咪睡了" + minutes + "分钟");
    }
}
```

面向对象完成具体实现功能的三步操作

1. 创建类，并设计类（内部结构）
2. 创建类的对象（例如：`Cat cat = new Cat();`）
3. 通过对象调用里面的方法和属性

> 类和数组都属于引用数据类型，他们和普通的值类型并不相同，值类型重新赋值不影响赋值的值，
> 但是引用数据类型赋值的是引用地址，而不是里面的数据，如果将一个地址分给两个变量，其中一个变量更改，另一个拿到的变量也会被更改

## <div id="java-方法">方法</div>

方法是类或对象的行为，用来执行重复的代码，避免重复代码、减少冗余、简化代码。**方法在别的编程语言中也被称为函数或过程**。
Java中方法不能独立存在，需要放在类里，其中加上**static**关键字的方法可以不用创建对象调用方法，可以使用类.方法进行调用

```java
public static void main(String[] args) {
    //常见的方法
    //获取一个int类型的随机数
    Random random = new Random();
    random.nextInt();

    //获取键盘输入
    Scanner scanner = new Scanner(System.in);
    scanner.nextLine();

    //判断两个数的大小
    int max = Math.max(2, 1);

    //打印字符串到控制台
    System.out.println("Hi");
}
```

方法声明的格式：  
权限修饰符 返回值类型 方法名(方法参数，又被称为形参列表）) {  
}

```java
//权限修饰符（后面会写到） 返回值类型（是否有返回值，返回值的类型是什么） 方法名 形参列表（要传入的参数）
public void printlnName(String name) {
    //方法体
    System.out.println(name);
}
```

方法的重载，我们可以使用一个“方法”来传入不同的类型，使用重载时需要在类里创建多个**不同形参类型**相同方法名的方法，
参数列表不同、参数个数不同、参数类型不同、方法名相同，权限修饰符和返回值不同和这个没有关系。这就是方法的重载

```java
public class Cat {
    public static void main(String[] args) {
        Cat cat = new Cat();
        cat.move(5, 5);   //调用了第一个方法
        cat.move(5);    //调用了第二个方法
    }

    public void move(int x, int y) {
        System.out.println("Cat moved at " + x + ", " + y);
    }

    public void move(int distance) {
        System.out.println("Cat moved " + distance);
    }
}
```

> 方法的重载用在很多地方，比如Arrays中的方法用到了大量的重载。判断是否重载就看方法名是否一致，形参是否不同即可


方法不光可以放固定的参数，也可以放可变的参数，这统称为**可变形参**。要在形参中用，用法`int ... numbers`。
其中可变形参可以传入**0到任何数**，参数也变成了一个数组，但和数组并不相同，如果参数数组是要传入一个数组，
而可变形参是多个元素集合为一个数组

```java
//print(1,2,3,5,6,4,8,9) /可以传入任何数

public void print(int... numbers) {
    System.out.println(Arrays.toString(numbers));
}

//不能和相同方法名且传入相同类型的方法共存，这样编译器会以为这是一个方法，虽然传入的值不同
public void print(int[] numbers) {
    System.out.println(Arrays.toString(numbers));
}
```

如果一个方法形参是两个形参类型，一个是可变形参，方法调用传入了两个形参，java会默认使用合适的方法，即两个形参类型的方法

方法可以在方法中调用自己的方法导致循环，这叫方法的**递归**。可以在递归中加些判断，防止死循环，如果死循环栈的内存就会溢出，
报出栈内存错误，递归的开销也比循环大，如果不能用递归尽量不要用递归，递归有时可以简单的完成复杂循环，请务必在合适的位置使用

因为调用完函数才能弹栈，使用一直在调用一直不能弹栈，导致栈内存溢出错误

```java
//如果调用此循环将抛出错误
public static void add() {
    add();
}
```

使用递归拿到从零到n的合，如果看不明白也很正常，可以先往后看看，等你的写的代码经验变多自然就能看懂了

```java
public static int recursion(int n) {
    if (n == 1) return 1;
    return recu(n - 1) + n;
}
```

## <div id="java-属性">属性</div>

类中不光有方法还有属性，对象还有个特性，不共同性（静态的除外）修改对象1的属性，对象2的属性不会更改，
每个对象的行为和属性都是独立的

每个属性都有默认值，如果不给属性赋值属性就会有一个默认值，整数类型的默认值都是0、浮点型默认值是0.0、
布尔类型为false、引用类型是null

创建对象时，每次使用new关键词创建的都是一个新对象

```java
public class Cat {
    String name;
    int age;

    public static void main(String[] args) {
        Cat cat = new Cat();
        cat.name = "猫咪";
        cat.age = 3;

        System.out.println(cat.name);   //打印猫咪
        System.out.println(cat.age);    //打印3

        //如果不给他们赋值使用的就是属性的默认值
        Cat cat1 = new Cat();

        System.out.println(cat1.name);  //打印null
        System.out.println(cat1.age);   //打印0
    }
}

```

我们认识了一下类，就可以把类和数组结合起来，之前是基本类型的数组，现在是引用类型的数组

```java
public static void main(String[] args) {
    //创建一个Cat类数组，长度为3
    Cat[] cats = new Cat[3];

    //循环数组，不超过数组的长度就循环一次
    for (int i = 0; i < cats.length; i++) {
        //创建一个Cat对象
        Cat cat = new Cat();
        //设置对象的名字
        cat.name = "cat" + i;
        //设置对象的年龄
        cat.age = i;
        //赋值到数组中
        cats[i] = cat;
    }

    //打印数组中的所有对象（打印的是引用地址，需要重写toString才可以打印内容）
    System.out.println(Arrays.toString(cats));
}
```

## <div id="java-构造器">构造器</div>

构造器是一个常用的结构，常用到每个类都有一个构造器，不光Java有构造器，所有对象类语言都有构造器。
我们使用`new Cat()`来创建一个对象，其中Cat()就是一个构造方法，但是我们并没有写构造器，
哪来的构造器，Java中如果没有写构造器，就会默认生成一个没有参数的构造器，那我不想让他们调用构造器怎么办，
你可以显式声明一个私有化的构造器

默认生成的构造器是public的，使用private私有化构造器

```java
public class Cat {
    String name;
    int age;

    //注意构造器不是方法，他并没有返回值
    private Cat() {

    }
}
```

构造器还可以通过形参列表来给对象的属性赋值，当然你可以通过构造器来传入任何东西，和方法的形参列表无异

```java
public class Cat {
    String name;
    int age;

    //当自己编写了一个构造器，就不会生成空参构造器了
    public Cat(String name, int age) {
        this.name = name;
        this.age = age;
    }
}

```

## <div id="java-封装">封装</div>

面向对象不可缺少的三大特征：**封装、继承、多态**

学习封装之前我们要先认识两个关键字，**package**、**import**，这两个关键字让Java的安全性和封闭性非常的高

- package：翻译过来就是包的意思，用于指明文件中的类、接口、等机构所在的包
- import：导入，导入不同的到到本类文件中，用于使用非本文件的类

包的格式为`package 包名`，此声明必须放到文件的第一行的代码，放到其他位置会报错

使用其他包的类就需要使用import导入类，import关键字要声明在类和包声明之间，
通常使用其他包的类开发工具会自动帮你导入

```java
package com.afeibaili; //声明包

import java.util.Arrays; //导入Arrays的类

public class Cat {
    public static void main(String[] args) {
        System.out.println(Arrays.toString(args));
    }
}
```

我们也可以只导入静态方法和属性，也可以导入包里的全部类

```java
import java.util.*; //导入util下的全部类

import static java.lang.System.out; //导入静态变量
```

可以在不同的包写同名的类，一个包不可以写相同的类

> 包名通常是顶级域名开始、域名、项目名、功能名...  
> 且不能命名java开头的包名，程序会报出安全异常

包可以让代码的耦合度变低，增加开发效率更好维护代码

例如**MVC设计模式**，MVC将整个程序分为三个层次：视图模型（viewer）、控制器模型（controller）、数据模型（model）

- 视图层：显示数据为用户提供界面，与用户直接交互
    - 视图工具类 view.utils
    - UI类 view.ui
- 控制层：解析用户的请求，处理业务逻辑
    - 应用界面相关 controller.activity
    - 适配器 controller.adapter
    - 服务相关 controller.service
    - 抽取的基类 controller.base
- 模型层：主要承载数据、处理数据
    - 数据对象的封装 model.bean
    - 数据库操作 model.dao
    - 数据库 model.db

随着我们的程序越来越复杂，类会越来越多，类与类的关系要明确好，不要一坨东西都放到一个类里，
写代码的开发原则就是**高内聚、低耦合**

封装可以比作一台电脑，电脑用户只需要敲键盘动鼠标就行了，而底层就需要调用cpu、gpu、内存等操作，
电脑给你用并不是让你调内存、走cpu的，因为电脑已经给你**封装**好了键盘和鼠标，所以你只需要动键盘和鼠标就好了

高内聚：指的是模块中元素各个之间的紧密程度，类的内部数据细节自己操作，不允许外部操作。  
低耦合：指的是不同模块之间的紧密程度，仅暴露必要的方法，方便外部操作。

内聚意味着重用和独立，耦合意味着牵动一发动全身

如何实现数据的封装？使用权限修饰符可以让其他包的类访问不到此类

Java有四种权限修饰符，分别是:**private、默认（缺省）、protected、public**。
我们可以用这四种来修饰类的内部成员，指定谁可以访问谁不能访问

```java
class Cat {
    //其他文件中的类无法访问此属性
    private String name;

    //任何类都可以访问
    public String getName() {
        return this.name; //this关键字代表当前对象，当前对象调用此方法会放回调用对象的name
    }

    //任何类都可以调用
    public void setName(String name) {
        this.name = name;
    }
}
```

| 修饰符       | 本类内部 | 本包内 | 其他包子类 | 其他包非子类 |
|-----------|------|-----|-------|--------|
| private   | √    | ×   | ×     | ×      |
| 缺省        | √    | √   | ×     | ×      |
| protected | √    | √   | √     | ×      |
| public    | √    | √   | √     | √      |

类只能使用缺省和public，如果用private和protected编译会报错，加上也没有什么意义

最常见的私有化修饰就是getter和setter，用get和set来访问和更改对象的属性值

```java
public class Cat {
    private String name;
    private int age;

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        this.age = age;
    }
}
```

## <div id="java-this关键字">this关键字</div>

this通常代表在类的结构中，代表使用此方法的对象，在构造器使用就是初始化的对象，在方法中使用，就是操作此方法的对象，
在属性中使用就是此对象的属性值

```java
public class Cat {
    String name;
    int age;

    public Cat(String name, int age) {
        //当前的对象属性
        this.name = name;
        this.age = age;
        //如果不使用this，name是形参中的变量，就会原地赋值且和对象中的name不沾任何关系
        name = name;
        //当然你可以让你的形参名叫做其他的名字，只要它们不一致，jvm会自动找到对象中的name进行赋值例如
        //name = nameA; //nameA假如是形参中的变量名
    }

    public void setName(String name) {
        //将对象属性中的name设置为传进来的name
        this.name = name;
    }
}
```

this不光可以执行对象的属性，还可以指向对象的构造器来调用其他的构造器，我们可以使用`this(//传参)`来进行代码的复用

```java
public class Cat {
    String name;
    int age;

    //空参构造器
    public Cat() {
        //一堆代码
    }

    //使用这个构造器会因为this()调用空参构造器
    public Cat(String name) {
        this();
        this.name = name;
    }

    public Cat(String name, int age) {
        this(name);
        this.age = age;
    }
}
```

## <div id="java-继承">继承</div>

面向对象的第二个特征，继承性

继承指的是一个类向另一个类继承属性和方法，通常一个属性很基础的父类，和几个在此基础上的子类。比如人和工人、学生的关系，
人都有年龄，而工人也有年龄，工人不光有年龄还有薪资，而学生也有年龄，没有薪资，但是有作业。

我们可以写一个人类来定义一个父类

```java
class Person {
    String name;
    int age;

    public void info() {
        //加不加this无所谓，因为只有一个name（如果形参中有name变量就需要加this了）
        System.out.println(this.name);
    }
}
```

我们可以使用`extents`关键字来继承一个父类，我们继承Person类之后会继承它所有的属性和方法（私有方法和属性无法访问）

```java
class Worker extends Person {
    double salary;

    public static void main(String[] args) {
        Worker worker = new Worker();
        //可以获取到父类的属性
        worker.name = "Bob";
        //调用父类的属性
        worker.info();
    }
}
```

继承的出现减少了代码冗余，提高了代码复用性，且更有利于拓展功能。
继承中的父类通常叫做父类、superClass、超类、基类，子类叫做子类、subClass、派生类

在Java中声明的类，默认继承Java.lang.Object类，即使你显式继承其他类，其他类也会继承Object类，
Object类中也有许多方法，所有声明的类有没有声明过的方法，很有可能就是Object中生命的方法，例如`toString()`

Java也可以进行多继承，继承之后还可以被其他类继承，其他类也可以被其他类继承...

子类继承父类的方法，但父类的方法可能并不适用于子类，例如Animal的方法叫做吃食物，而Cat的方法可以为吃鱼，
这就不太适合子类的方法，我们可以使用**重写**来覆盖父类的方法，使用`@Override`注解可以让编译器在编译阶段判断此方法是否重写父类方法，
如果没有重写将报错，使用注解也可以让你的代码更加易读和优雅

```java
class Animal {
    public void eat() {
        System.out.println("动物在吃东西");
    }
}

class Cat extends Animal {
    //重写父类方法
    @Override
    public void eat() {
        System.out.println("猫在吃鱼");
    }
}
```

重写应当遵循的规则，权限修饰符、返回值类型、方法名、throws异常类型。子类不能重写private的方法

## <div id="java-super关键字">super关键字</div>

super和this类似，this代表对象的，super代表父类的，子类在重写父类的方法还可以使用super关键字进行父类方法、属性的调用。
如果父类的属性和子类的属性一致，例如两个id属性（id不能被覆盖），可以使用super关键字来调用父类的属性，super和this一样也可以调用构造器，
不过调用的是父类的构造器

```java
class Animal {
    String name;

    public void eat() {
        System.out.println("动物在吃东西");
    }
}

class Cat extends Animal {
    //重写父类方法
    @Override
    public void eat() {
        System.out.println("猫在吃鱼");
        //打印父类的属性 
        System.out.println(super.name);
        //调用父类的方法
        super.eat();
    }
}
```

如果调用super()和this()必须要放在构造器的**首行**，否则程序将报错，且super()和this()只能二选一，
如果this()和super()都没有调用将会隐式调用super()构造器，如果父类没有空参构造器，必须要显示调用super有参构造器了

> 要记住至少有一个构造器会调用父类的构造器

## <div id="java-多态">多态</div>

多态性是面向对象的第三的特性，可以理解为一个事物的多态性，我们可以假如有一个人类，然后再创建一个员工类、一个医生类，
它们都继承人类，其中人类中有个方法叫做`work`。员工类和子类分别重写work方法，然后我们创建两个对象员工类和医生类，
将它们的类型全部写为人类的类型，因为员工类和医生类都是继承并重写work的方法，所以可以用人类作为接收类型，
虽然隐藏了具体类型，但是它们都有重写work方法所以都能调用到work,当一个对象调用work时候，
打印的是当时创建的对象示例。编译时是左边声明的方法，调用时是具体实例的方法

```java
//创建人类
public class Person {
    //人类中的方法
    public void work() {
        System.out.println("人在工作");
    }
}

//创建工人类，继承并重写work方法
class Worker extends Person {

    @Override
    public void work() {
        System.out.println("工人在工作");
    }
}

//创建医生类，继承并重写work方法
class Doctor extends Person {

    @Override
    public void work() {
        System.out.println("医生在救人");
    }
}

//运行测试类
class Main {
    public static void main(String[] args) {
        //创建工人的实例但是声明人类
        Person p1 = new Worker();
        //创建医生的实例但是声明人类
        Person p2 = new Doctor();

        p1.work();

        //这样体现的可能不好理解多态性，接下来使用方法来解释多态性
        //假如云端传过来两个对象一个员工的对象和一个医生的对象，我们都需要让他们工作，
        //由于多态的存在，我们不可能为每个类都写一个方法，
        //我们可以让他调用一个方法进行工作，那就是doWork方法
        //这样避免了使用两个方法例如doWorkerWork和doDoctorWork方法

        doWork(p1);
        doWork(p2);
    }

    //声一个做工作方法，传入一个Person对象，进行work调用
    public static void doWork(Person person) {
        person.work();
    }

    //不用多态时调用的方法
    public static void doWorkerWork(Worker worker) {
        worker.work();
    }

    public static void doDoctorWork(Doctor doctor) {
        doctor.work();
    }
}
```

我们调用时发现是父类的类型，子类的方法就不能调用了，可以使用类型的向下转换，来转换类型，
转换类型的方法为`Worker w = (Worker) p1;`使用强制类型转换进行转换，将父类的Person类型转换为它的子类型Worker，
需要注意的是如果p1的实例是Doctor而不是Worker的实例那么就会报出类型转换异常，在类型转换之前最好进行类型判断，
判断p1是否是对应类型

```java
public void conversionType(Person person) {
    //类型判断
    if (person instanceof Workder) {
        //向下转型
        Worker worker = (Worker) person;

        System.out.println("person类型是worker类型");
    }
}
```

## <div id="java-object类">Object类</div>

在Java中默认继承的类就是Object类，即使你显示继承了其他类，其他类也会继承Object类，在java.lang包中Object类。
其中java.lang包默认导入，所以不需要显式导入，Object类也被称为Java的根父类，在Object类中并没有属性为子类继承，
但是有很多方法被子类继承，常用的方法有`toString()`、`equals()`，还有其他的方法`clone()`、`finalize()`、
`getClass()`、`hashCode()`、`notify()`、`notifyAll()`、`wait()`

clone方法是将一个对象克隆出另一个对象，其中值不变，但是引用地址改变，我们都知道如果直接用`=`赋值对象的话，
赋值的只是引用地址，而不是具体的值，但使用clone就可以克隆出一个全新的对象，
**注意：使用克隆必须先在要克隆的类上实现`Cloneable`接口**

```java
//实现Cloneable接口
public class O1 implements Cloneable {
    //throws CloneNotSupportedException是抛出一个异常
    public void executeCode() throws CloneNotSupportedException {
        //创建一个对象
        O1 o1 = new O1();
        //克隆新的对象
        O1 clone = (O1) o1.clone();
    }
}
```

在Java内部方法中可能**native**关键字，然后并没有方法体，这是因为这个操作并不是使用Java实现的，Java借助外部调用资源从而实现的

```java
protected native Object clone() throws CloneNotSupportedException;
```

重写finalize方法之后当对象即将被垃圾回收器（GC）销毁时调用此方法，可以在对象销毁时做出某些操作，
如果在finalize中执行循环等操作，会导致此对象迟迟不能回收，所以这个方法是**被弃用的**

```java
class O2 {
    //重写finalize方法
    @Override
    protected void finalize() throws Throwable {
        System.out.println("我被销毁了");
    }
}

public class Main {
    public static void main(String[] args) throws InterruptedException {
        //创建并销毁测试
        O2 o2 = new O2();
        //设置为null即o2的实例不在被任何变量指向
        o2 = null;
        //调用GC垃圾回收器
        System.gc();
        //防止对象在没销毁就结束了，延迟进程一秒
        Thread.sleep(1000);
    }
}
```

在Object类中有一个重要的方法就是equals方法，作用是对比两个元素是否正确，判断的逻辑由开发者写。
假如我有两个对象，两个对象的name属性值都是bob，使用==得到的结果是false，如果不重写equals使用equals判断的话也是false，
我们都知道这两个对象的属性都是相同的但得到的答案却不是我们想要的，我们可以重写equals方法根据name值是否相同来返回true和false，
这样equals就可以根据我们想要的属性值进行判断，从而实现两个对象是否相等

```java
class O2 {
    String name;

    //重写equals方法
    @Override
    public boolean equals(Object obj) {
        //需要注意Object.equals中的类型是Object最好判断一下另一个值是否是O2
        //判断类型相等使用逻辑与进行String的equals判断，因为String是引用数据类型，
        //并且String已经重写了equals方法
        return obj instanceof O2 && name.equals(((O2) obj).name);
    }

    public static void main(String[] args) {
        //创建两个属性值相同的对象
        O2 o = new O2();
        o.name = "bob";
        O2 o2 = new O2();
        o2.name = "bob";

        //使用equals判断是否相等
        System.out.println(o.equals(o2)); //打印true
    }
}
```

> 如果不重写equals默认判断的是引用地址是否相等

在Object类中还有一个至关重要的方法就是toString方法，代码演示

```java
//创建一个类
public class O3 {
    String name;

    //运行方法
    public static void main(String[] args) {
        O3 o3 = new O3();
        o3.name = "O3";

        //尝试打印一个对象，打印的结果为java生成的“引用地址”
        System.out.println(o3);             //打印结果为：O3@6d311334
        //使用toString方法打印的结果和直接打印对象的结果一致
        System.out.println(o3.toString());  //打印结果为：O3@6d311334
    }
}
```

可以看到直接打印o3和o3调用toString方法的结果是一致的，因为println中方法会调用传入属性的toString方法，
所以即使你不调用，println也帮你调，我们可以重写toString方法让打印的结果自定义

```java
public class O3 {
    String name;

    public static void main(String[] args) {
        O3 o3 = new O3();
        o3.name = "O3";

        System.out.println(o3);             //打印结果为：O3 [name=O3]
    }

    //重写toString方法
    @Override
    public String toString() {
        return "O3 [name=" + name + "]";
    }
}
```

> 当然Object还有一些方法，但不能现在演示

## <div id="java-static关键字">static关键字</div>

我们都知道一个对象的属性值是不能和其他对象所共享的，**如果想让所有对象共享这个属性值，就使用static关键字**，
被修饰的属性、方法也被称为**静态方法，静态属性**，这些静态成员都是唯一的，**类加载后静态成员只存在一份**，
静态成员和对象无关。静态成员的调用方式和对象的调用方式不一样，对象方法调用使用**对象.方法**，而静态成员调用方法为
**类名.方法**，属性也是如此

static可以修饰的结构：属性、方法、代码块、内部类

| 功能   | 静态变量                           | 实例变量               |
|------|--------------------------------|--------------------|
| 个数   | 在内存空间只有一份                      | 类的每一个对象（实例）保存着一份变量 |
| 内存位置 | jdk6及之前：静态变量存放在方法区，jdk7以后存在堆内存 | 存放在堆空间的对象实体中       |
| 加载时机 | 随着类的加载而加载，因为类只能加载一份，所以只有一份变量   |                    |
| 调用者  | 被类调用，也可以被实例变量调用                | 只能被实例调用            |
| 消亡时机 | 随着类的消亡而消亡                      | 随着实例的消亡而消亡         |

```java
public class Person {
    //创建静态属性
    static String company;
    //创建实例属性
    String name;

    //静态方法
    public static void printPersonInfo(Person person) {
        //不能在静态方法使用this，会报错我们也都知道this是当前对象，
        //而使用类名调用方法是没有对象的，因为是类调用而不是对象调用，
        //所以this在static中会报错
        //this
        System.out.println(company);
    }

    //测试入口
    public static void main(String[] args) {
        Person person1 = new Person();
        Person person2 = new Person();
        person1.company = null; //可以用对象调用
        Person.company = "暗影公司";

        person1.printCompany();
        System.out.println(person2.company);
    }

    //实例方法
    public void printCompany() {
        System.out.println(company);
    }
}
```

借助static关键字我们可以实现单例模式，一个应用程序中只有一个对象，这对某些场景下很重要，
下方单例模式只能从Message中的INSTANCE（中文翻译：实例）获取对象代码为`Message.INSTANCE`，
我们可以想想它的实际用途，一台计算机是不是只能有一个系统进程，如果一台计算机有多个系统实例岂不是很多系统进程，
那么究竟是谁才能管理系统？我们就可以把系统设置为单例模式，只能存在一个“系统实例”

```java
//创建单例模式
class Message {
    //只能使用此属性进行获取Message因为构建器私有化了
    public static final Message INSTANCE = new Message();

    //私有化构建器
    private Message() {
    }


    //实例中的方法...
    public void createMessage() {

    }

    public void createStream() {

    }
}
```

## <div id="java-代码块">代码块</div>

代码块有两种分别是：静态代码块、实例代码块，静态代码块只会加载一次，而实例代码块会随着对象的创建而加载，
每创建一个对象就会运行一次代码块。操作和普通方法类似，就像是一个不能调用但总会执行的方法

代码块可以用来初始化类（对象）的信息，如果有多个代码块执行顺序是从上到下，静态代码块不能调用对象之类的属性和方法，
因为它不属于任何一个实例，当然实例代码块可以调用静态的结构，也可以调用对象中的属性，因为就是为了对象创建而加载的

```java
public class Dome {
    //静态代码块
    static {
        System.out.println("我是静态代码块");
    }

    String testName;

    //代码块（实例代码块）
    {
        this.testName = "张三";
        System.out.println("我是实例代码块");
    }

    public static void main(String[] args) {
        //走到这里已经加载了Dome类，所以首先打印：我是静态代码块
        //接下来创建两个对象，并在代码块中进行赋值，所以打印两次：我是实例代码块
        Dome d = new Dome();
        Dome d2 = new Dome();
        System.out.println(d2.testName); //打印为：张三
    }
}
```

## <div id="java-final关键字">final关键字</div>

final的理解可以是：最终的、不可变的。final可以修饰：类、方法、变量

被final修饰的类，表示这是最终的类，你不要继承了，在Java中的String类就是被final修饰的最终类，
如果你继承了String类你在编译阶段就会报错，因为这是最终的不可变的类

```java
public class Dome extends String { //编译报错 无法继承String因为是最终的
}

final class Dome2 { //声明不可变的类
}
```

被final修饰的方法，将不能被重写，例如Object中的getClass()

```java
class Dome {
    public final void doSomething() {
        //此方法不可被子类重写
    }
}
```

被final修饰的变量，不管是成员变量还是局部变量都可以修饰。此时的变量已经变成了**常量**，
声明为常量之后，此“变量”就不能被更改

声明常量需要赋值，如果在类中必须显示赋值，如果没有显示赋值可以用代码块赋值，
如果没有代码块赋值就只能用构造器赋值了

```java
final String NAME = "Bob"; //显式赋值
```

```java
class Dome {
    final String NAME;

    //代码块赋值
    {
        this.NAME = "Bob";
    }
}
```

```java
class Dome {
    final String NAME;

    Dome() {
        this.NAME = "Bob";
    }
}
```

当然静态常量也可以使用代码块赋值

```java
class Dome {
    public static final String NAME;

    static {
        NAME = "Bob";
    }
}
```

final和static修饰后就是全局常量，全局只有一份且不可更改，例如Math中的PI属性

变量被修饰为全局常量之后其属性名要大写表示这是一个全局常量，这是代码规范

## <div id="java-登峰造极">登峰造极</div>

## <div id="java-抽象类">抽象类</div>

随着继承子类一个个定义增加，类的设计也应该保证和子类能够共享特征，有时将一个父类设计的非常抽象，
以至于它都没有具体的实例，这样的类叫做抽象类（关键字**abstract**）

简而言之就是子类的共同父类，但是这个父类在抽象层次，不需要实例化。例如一个人类，它有很多子类：
员工类、医生类、学生类、平民类，我们可以把这些子类的基本属性都写在抽象的人类中

抽象类可以声明抽象方法，抽象方法不能有方法体即`{}`抽象方法的作用主要是让子类进行重写实现，强制让子类重写，
不然会报错。没有声明abstract的方法将不是抽象方法，可以写方法体和具体的逻辑也不强制子类实现

```java
//创建一个抽象类
public abstract class Person {
    //定义一个属性
    String name;

    //声明一个抽象方法，抽象方法只能被重写不能在抽象类中写方法体
    public abstract void sayHello();

    //普通方法
    public void sayMyName() {
        System.out.println(name);
    }
}

//继承Person类
class Worker extends Person {

    //必须重写抽象方法不不然编译会报错
    @Override
    public void sayHello() {

    }
}
```

```java
public void execute() {
    //会报错，因为抽象类不能实例化
    //Person person = new Person();
    //可以实例化，具体的实现类
    Worker worker = new Worker();
}
```

抽象类中是包含构造器的，因为子类对象实例化需要直接或间接调用父类的构造器

## <div id="java-接口">接口</div>

接口（interface），在Java中的接口就像是现实生活中的USB接口类似，通过USB接口来连接不同的USB硬件，
不管是什么USB硬件都遵循了USB**接口规范**，但是硬件的公司，生产日期是我们不关心的，
我们只关心这个USB硬件可以连接我的电脑，USB接口就是厂家公司实现的规范，假如你要生产USB硬件，
那么你就要遵守USB规范

接口就像是规范一样，定义的是一组规则，如果继承是是不是的关系，那么接口就是能不能的关系

假如我又一个人类，工人类继承人类，医生类继承人类，它们都是继承关系那我们创建一个英语的接口，
这个英语接口可以给任何类实现，那么工人类可以实现英语接口，医生类都可以选择是否实现英语接口

```text
英语  人类
⁞    /   \
⁞   /     \
工人类    医生类
```

接口的本质就是契约、标准、规范，接口是不可实例化的，因为它是**规范**

接口中的属性只能使用public static final修饰，在接口中创建一个属性默认被**public static final**修饰。
声明方法：jdk8之前声明抽象方法，修饰为public abstract、jdk8声明静态方法，默认方法，jdk9：声明私有化方法，
接口中默认声明方法默认修饰为**public abstract**。接口中不能声明构造器和代码块，它并不是一个类

一个类可以实现多个接口，和继承不一致，继承只可以单继承，而接口可以多实现，接口不能实现接口，但是接口可以继承接口

```java
//声明一个可飞行的接口
interface Fly {
    //创建全局常量，下方代码等价为：public static final int MAX_SPEED = 999;
    int MAX_SPEED = 999;
    int MIN_SPEED = 1;

    //创建方法，默认为：public abstract
    void fly();
}

//声明一个可游泳的接口
interface Swim {
    //声明一个方法
    void swim();
}

//如果不声明为abstract就必须实现接口里的方法，因为方法默认为abstract
public abstract class Dome implements Fly, Swim {
}
```

```java
//实现Fly和Swim接口
class Bullet implements Fly, Swim {

    //重写抽象方法
    @Override
    public void fly() {

    }

    //重写抽象方法
    @Override
    public void swim() {

    }
}
```

当然也可以实现上面的Dome抽象类，因为它实现了Fly和Swim接口

```java
//继承Dome抽象类，此抽象类实现Fly和Swim接口
class Bullet extends Dome {

    //重写抽象方法
    @Override
    public void fly() {

    }

    //重写抽象方法
    @Override
    public void swim() {

    }
}
```

一个类只能继承一个类但是可以实现多个接口

```java
class Bullet extends Dome implements Fly, Swim {

    //重写抽象方法
    @Override
    public void fly() {

    }

    //重写抽象方法
    @Override
    public void swim() {

    }
}
```

在上方代码中，Bullet相较于Dome类我们可以称为子类，Bullet相较于Fly称为实现类

接口可以作为声明类型，例如`Fly bullet = new Bullet();`这叫接口的多态性

> 抽象类和接口的共性有很多，比如都可以声明声明抽象方法、都不能实例化，不同点为：
> 抽象类有构造器，而接口没有构造器、抽象类与类之间是是继承关系，与接口是实现关系，
> 接口与类不能继承和实现，接口与接口是继承关系

| 区别点    | 抽象类                  | 接口                       |
|--------|----------------------|--------------------------|
| 定义     | 可以包含抽象方法的类           | 主要是抽象方法和全局常量的集合          |
| 组成     | 构造方法、抽象方法、普通方法、常量、变量 | 常量、抽象方法、（jdk8：默认方法、静态方法） |
| 使用     | 子类继承抽象类（extends）     | 子类实现接口（implement）        |
| 关系     | 抽象类可以实现多个接口          | 接口不能继承抽象类，但允许继承多个接口      |
| 常见设计模式 | 模板方法                 | 简单工厂、工厂方法、代理模式           |
| 局限     | 抽象类单继承的局限            | 接口没有继承的局限                |
| 实际     | 作为一个模板               | 是作为一个标准或是一种能力            |

> 如果不知道如何选择，一个类往下的子类比较多就用抽象类，创建某种功能或某种能力选接口

在接口中还有两种方法：静态方法和默认方法。静态方法通过接口名进行调用，而默认方法通过接口的实现类进行调用，
定义的静态方法和默认方法必须要有方法体

```java
//定义接口
interface Fly {
    //声明静态方法
    static int getMaxSpeed() {
        return 999;
    }

    //声明默认方法
    default void printString(String string) {
        System.out.println(string);
    }
}

//Fly的实现类
public class Dome implements Fly {
    public static void main(String[] args) {
        //通过接口名调用静态方法
        System.out.println(Fly.getMaxSpeed());
        //通过实例名调用静态方法
        Dome dome = new Dome();
        dome.printString("Hello World");
    }

    //当然可以重写接口的方法
    @Override
    public void printString(String string) {
        Fly.super.printString(string);
    }
}
```

需要注意一点，如果一个类实现了两个接口并且有相同的默认方法，不实现此方法会报错，
而且需要指定调用哪一个类中的方法

两个接口有相同方法就会造成【钻石问题】，当子类访问接口的方法时候，不知道该选择哪个接口的方法，
Java中添加了一种语法来指定选择哪一个接口，在重写的方法中写`接口名.super.方法`来指定哪一个方法

```java
//定义接口
interface Fly {
    //定义与另一个接口冲突的默认方法
    default void doSomething(String string) {
        System.out.println(string);
    }
}

//定义接口
interface Swim {
    //定义与另一个接口冲突的默认方法
    default void doSomething(String string) {
        System.out.println(string);
    }
}

//一个类同时实现Fly和Swim接口，需要重写doSomething方法，否则会报错
public class Dome implements Fly, Swim {
    public static void main(String[] args) {
        Dome dome = new Dome();
        dome.doSomething("Hello World");
    }

    @Override
    public void doSomething(String string) {
        //调用Swim接口的doSomething方法，当然你也可以自己重写它的方法
        Swim.super.doSomething(string);
    }
}
```

在jdk9接口中可以定义私有方法，私有静态方法，主要是给默认方法和静态方法封装复用逻辑

```java
//接口
interface Dome {
    //静态方法
    static void sayStatic() {
        baseStatic();
        System.out.println("Hello");
    }

    //复用逻辑
    private static void baseStatic() {
    }

    //默认方法
    default void say() {
        base();
        System.out.println("Hello");
    }

    //复用逻辑
    private void base() {

    }
}
```

## <div id="java-内部类">内部类</div>

将一个类A定义到另一个类B里面，这个里面的A类就被称为内部类。内部类出现的需求，
当一个A类还需要一个完整的部分B类进行描述，而这个完整B类又只为外部事物的A类提供服务，不在其他地方使用，
那么整个完整的结构就是将B设为内部类，内部类也分为成员内部类，声明在成员内部、局部内部类，声明在代码块内部。
其中成员内部类又分为静态的和非静态的，局部内部类分为匿名的局部内部类和非匿名的局部内部类

成员内部类也可以被权限修饰符修饰

```java
class Person {
    //静态内部类
    static class Tool {

    }

    //非静态内部类
    class Info {

    }
}
```

创建成员内部类的实例

```java
public void test() {
    //创建静态内部类
    Peroson.Tool tool = new Peroson.Tool();
    //创建非静态内部类
    Person person = new Person();
    Info info = person.new Info();
}
```

内部类调用外部类，可以通过外部类.this.方法来来实现内部类调用外部类的结构

```java
public class Person {
    public static void main(String[] args) {
        //声明内部类对象
        Person person = new Person();
        Tool tool = person.new Tool();
        //调用内部类
        tool.show();
    }

    //外部类方法
    public void show() {
        System.out.println("显示人");
    }

    //声明内部类
    class Tool {
        //内部类方法
        public void show() {
            System.out.println("显示工具");
            //调用外部方法
            Person.this.show();
        }
    }
}
```

局部内部类，可以借助多态来返回一个实现接口（抽象类）的类，首先先要写一个局部内部类

```java
//一个普通的接口
interface Info {
    void show();
}

//一个普通的类
public class Person {
    //测试方法
    public static void main(String[] args) {
        //获取info对象
        Info info = getInfo();
        //调用info对象
        info.show();
    }

    //一个静态方法
    public static Info getInfo() {
        //一个局部内部类，实现了Info接口的方法
        class MyInfo implements Info {
            @Override
            public void show() {
                System.out.println("我的信息");
            }
        }
        //返回局部内部类的对象
        return new MyInfo();
    }

    //除了以上可以返回一个内部类对象，我们还可以实现一个匿名的内部类
    public static Info getInfoByAnonymous() {
        //我们并不关心类的名字，可以使用这种语法来匿名实现一个内部类
        Info info = new Info() {
            @Override
            public void show() {
                System.out.println("我的信息");
            }
        };

        //甚至还可以使用lambda表达式简化，后面会提到lambda
        Info info1 = () -> System.out.println("我的信息");
        //info1等价于info
        return info;
    }
}
```

## <div id="java-枚举类">枚举类</div>

枚举类本质上也是类，这不过这个类的对象时有限的、固定的几个，且不能让用户创建，
假如我们要把星期一到星期五设置为对象，我们使用时还要创建，但是使用枚举类我们可以提前把对象放到里面，
相当于一个不可变的对象常量

简而言之我们针对每个类的对象时确定个数的，则推荐使用枚举类。
举例，颜色RED("红色")、YELLOW("黄色")、BLUE("蓝色")

jdk5.0之前常量类都是开发者自己定义，之后Java支持了**enum**关键字来定义枚举类

使用普通类来实现一个枚举类

```java
public class Color {
    //创建后的常量
    public static final Color RED = new Color("红色");
    public static final Color YELLOW = new Color("黄色");
    public static final Color BLUE = new Color("蓝色");
    //类属性
    private String describe;

    //私有化构造器
    private Color(String describe) {

    }

    //测试方法
    public static void main(String[] args) {
        System.out.println(Color.RED);
    }

    //get和set
    public String getDescribe() {
        return describe;
    }

    public void setDescribe(String describe) {
        this.describe = describe;
    }

    //重写toString
    @Override
    public String toString() {
        return "Color{" +
                "describe='" + describe + '\'' +
                '}';
    }
}
```

使用enum关键字来创建枚举类，使用枚举类，省略了很多关键字，例如public static final，
枚举常量之间用逗号分割，最后一个元素用分号结尾，且构造器默认私有化

```java
public enum Color {
    RED("红色"),
    YELLOW("黄色"),
    BLUE("蓝色");

    private String describe;

    //默认私有化构造器
    Color(String describe) {

    }

    public String getDescribe() {
        return describe;
    }

    public void setDescribe(String describe) {
        this.describe = describe;
    }

    @Override
    public String toString() {
        return "Color{" +
                "describe='" + describe + '\'' +
                '}';
    }
}
```

枚举类**默认继承Enum类**而Enum类继承Object类，其中Enum类中有一些方法供我们调用

```java
public static void main(String[] args) {
    //默认实现toString方法，打印常量的名字即“RED”
    System.out.println(RED.toString());
    //打印常量的名字即“RED”
    System.out.println(RED.name());
    //拿到Color枚举类所有的常量
    //此方法是编译器生成的并不是源代码编写的
    Color[] values = Color.values();
}
```

## <div id="java-注解">注解</div>

注解（Annotation）从jdk5.0引入以 **@注解名** 在代码中存在例如`@Override`

注解可以像修饰符一样修饰包、类、构造器、方法、成员变量、参数局部变量的声明，还可以添加一些参数值。
注解可以在类编译、运行时加载，体现不同的功能

注解在宽泛的定义可以看做一种注释，通过使用Annotation，程序员可以在不改变原有逻辑的，在源文件中嵌入一些补充信息，
对于单行注释和多行注释是给程序员看的，而注解是可以被编译器或其他程序读取的。程序还可以根据注解的不同，做出相应的处理

注解是十分重要的，注解的目的很简单，例如标记过时的，忽略警告等，而在JavaEE/Android中注解占据了更重要的角色，
例如配置应用程序的任何切面，代替JavaEE旧版中所遗留的

常见注释（Javadoc）相关的注解

- @author 标明开发改模块的作者，多个作者用“,”分割
- @version 标明该模块的版本
- @see 参考转向，相关内容
- @since 从那个版本开始增加的
- @param 对某个参数的说明
- @return 对返回值进行说明
- exception 对可能抛出的异常进行说明

我们在重写方法时，经常看见`@Override`注解，这个注解的功能可以让编译器检查是否可以重写方法。
我们后面认识的框架都依赖于注解进行配置可以理解为 框架=注解+反射+设计模式

我们可以参照@Override来自定义一个注解，首先我们看@Override的注解，我们看到@Override被@Target和@Retention，
修饰，@Target内部注解含有一个数组，代表此注解可以被哪些结构修饰，下方的METHOD就代表只能修饰方法，
如果自定义注解要传多个参数可以这样写`@Target({类型、类型})`下方的Retention就代表此注解保留到哪个生命周期，
其中SOURCE类型就代表此注解只保留在源码中，字节码和运行时是不存在的，当然还有保留到字节码和运行时中

```java

@Target(ElementType.METHOD)
@Retention(RetentionPolicy.SOURCE)
public @interface Override {
}
```

定义注解使用`@interface`声明一个注解

```java
//声明一个工具注解
@Target(ElementType.METHOD) //此注解只能在方法中声明
@Retention(RetentionPolicy.CLASS) //此注解可保留在字节码文件中
public @interface Tool {
    //注解中的信息，类似类中的属性
    String toolName() default "null";
}

//声明一个被自定义注解的类
//如果toolName属性名为value可以省略toolName = 直接写参数"usbTool"
@Tool(toolName = "usbTool")
class UsbTool {

}
```

## <div id="java-包装类">包装类</div>

Java提供了两个类型系统，基本数据类型和引用数据类型。使用基本数据类型在于效率，而要是针对面向对象涉及又该怎么办呢？
使用包装类使得基本数据类型也能有引用数据的特征例如封装、继承、多态还有值为null

假如我们调用一个对象的equals方法可以看到里面传入的是一个Object对象而不是基本数据类型

```java
public void testEquals() {
    Object object = new Object();
    int a = 1;
    boolean equals = object.equals(a);//实际上会将a变量包装成一个类
}
```

需要包装类还有一个地方就是泛型，一个泛型的集合无法放入一个基本数据类型，只能放引用数据类型，
那么包装类就可在泛型中使用

而包装类就是基本数据类型以引用数据类型的方式出现，Java针对八种基本数据类型定义了相应的引用类型

| 基本数据类型  | 包装类       |
|---------|-----------|
| byte    | Byte      |
| short   | Short     |
| int     | Integer   |
| long    | Long      |
| float   | Float     |
| double  | Double    |
| boolean | Boolean   |
| char    | Character |

其中Byte、Short、Integer、Long、Float、Double继承了Number类

创建一个包装类对象，虽然可以用new来创建一个包装类对象，但是对于现在来说已经是被弃用的了

```java
//自jdk9以来此方法被标记为已删除了
Integer i = new Integer(1);

//推荐的方法
Integer i2 = Integer.valueOf(1);

//可以使用xxxValue来拿到基本数据类型
int intValue = i2.intValue();
```

在jdk5.0时可以自动装箱和拆箱，基本数据类型、引用数据类型互相转换没有这么麻烦了，可以直接进行调用

```java
int a = 1; //基本数据类型
Integer i = a; //自动进行装箱，调用valueOf
int j = i;  //自动拆箱，调用xxxValue
```

封装之后的内存对比，num的值是放在栈帧中随着方法的消失而消散，而objNum的值放在堆内存中

```java
public static void main(String[] args) {
    int num = 520;
    Integer objNum = 520;
}
```

基本数据类型、包装类对String类型进行转换，我们可以使用`String.valueOf(参数)`进行转换String类型。
当然我们也可以使用字符串拼接进行转换字符串`String i = 1 + ""`如果将字符串类型转换为包装类可以使用包装类
`parseXxx(字符串)`进行转换包装类，例如`Integer i = Integer.parseInt("1")`如果转换失败例如传入了字母，
就会报出类型转换异常

## <div id="java-异常处理">异常处理</div>

在代码运行中出现意外即为异常，对于异常我们要做相应的处理，例如现实中你在上班的途中遇到堵车这种意外，
你可以选择换路或者等待，那么换路和等待就可以视为异常的处理

常见的代码异常例如字符串转数值型，需要用户传入数字类型，奈何用户非要传入abc那么转换时就会抛出类型转换异常，
还有例如读取文件发现文件不存在，网络断开连接等等

异常：指的是程序在执行过程中，出现非正常情况，如果不处理最终会导致JVM非正常停止

对于异常地出现，一般有两种解决办法：一是遇到错误就终止程序的运行。
另一种方法是程序员在编写代码时充分考虑可能出现的异常和错误，极力预防和避免。
实在无法避免的要编写相应的代码进行异常的检测、及异常地处理，保证代码的健壮性

Java异常体系，在类**java.lang.Throwable**是异常的根父类，虽然是根父类但类的根永远是Object。
在Throwable中的常用方法有printStackTrace()：打印异常出现的详情信息、getMessage()：获取错误消息

在Throwable中可分两大类，Error和Exception。分别对应着**java.lang.Error**和**java.lang.Exception**两个类。  
Error：Java虚拟机无法解决的问题。如JVM内部错误、资源耗尽等严重情况。一般不编写针对性代码进行处理。例如：StackOverflowError
（栈内存溢出）和OutOfMemoryError（堆内存溢出简称OOM）  
Exception：其他因为编程错误或偶然的外在因素导致的一般性问题，需要使用针对性代码进行处理，使程序继续运行。
否则一旦发生异常，程序也会挂掉。例如：空指针异常、试图访问不存在的图片

一个空指针异常（NullPointerException）

```text
Exception in thread "main" java.lang.NullPointerException: Cannot invoke "String.toString()" because "str" is null
	at com.afeibaili.pack2.Test1.main(Test.java:11)
```

> 在运行中报出此样的代码就是异常，如果后缀是Exception那就是异常是代码可以处理，如果是Error则是错误，
> 是JVM无法处理的

Exception异常又分为编译时异常和运行时异常，编译时指的是在编译的时候报出的异常，而运行时异常就是只在运行时出现的异常

- 编译时异常：即受检异常、check异常，在代码编译阶段，编译器就能明确当前可能发生的异常，并督促程序员编写处理它的代码，
  如果程序员没有编写对应的异常处理，则编译器就会直接判定编译失败，从而不能生成字节码文件
- 运行时异常：即runtime异常、unchecked异常、非受检异常，在代码编译阶段，编译器都是无法感知的，
  只有代码运行中出现异常并报出它才能被发现。通常，这类异常是程序员编写不当导致的，只要稍加判断和细心检查就会避免。
  **java.lang.RuntimeException**类及它的子类都是运行时异常。比如：ArrayIndexOutOfBoundsException
  数组下标越界异常

```text
Java源代码 javac.exe-> 字节码文件 java.exe-> 在内存中加载、运行类、运行中
```

一个空指针异常

```java
public static void main(String[] args) {
    String str = null;
    str.toString(); //报出空指针异常，因为str是null
}
```

两种异常处理机制：try-catch-finally、throws 抛出异常

try-catch-finally（捕捉异常）：程序在执行的过程中一旦此处发生异常，程序就会创建一个异常对象并将此对象抛出。
一旦抛出不处理程序就终止运行。此时一旦抛出异常被try捕捉到，抛出的异常就不会终止程序，由try捕捉并到catch中处理，
代码继续执行。`try { //可能产生的代码 } catch(异常类型 变量名) { //捕捉后处理 }`，如果try中代码抛出异常，
该段代码会自动抛出一个异常对象，使用try捕捉catch进行处理

```java
public void catching() {
    try {
        String str = null;
        str.toString(); //引发空指针抛出异常给catch处理
        //抛出异常下面的代码不运行
    } catch (NullPointerException e) { //获取异常对象
        //捕捉空指针异常，空指针异常继承运行时异常

        System.out.println(e.getMessage()); //异常处理
    } catch (RuntimeException e) { //获取异常对象
        // 捕捉运行时异常，如果把运行时异常放到空指针异常上面，空指针异常将永远无法执行，
        // 因为空指针异常继承运行时异常，异常处理从上往下进行判断，运行时异常是父类所以
        // 包含空指针异常，捕捉运行时异常，但你真的把运行时异常放上面下面的空指针异常
        // 将会报错，因为这是无法达到的代码

        System.out.println(e.getMessage()); //异常处理
    }
}
```

非运行时异常需要显式处理否则编译不通过

```java
public void catching() {
    try {
        //需要写try-catch进行显式处理否则编译不通过
        FileWriter fw = new FileWriter("config.json");
    } catch (IOException e) {
        System.out.println(e.getMessage());
    }
}
```

finally写在catch后面，代表不管有没有抛出异常这段代码必须执行，`System.exit(0)`除外，这段代码会终止jvm
导致还没处理finally jvm就终止了

```java
public void catching() {
    try {
        String str = null;
        str.toString();
    } catch (NullPointerException e) {
        //异常处理
        System.out.println(e.getMessage());
        //再次抛出异常，下面代码没有异常处理所以会报错到JVM
        System.out.println(10 / 0);
    } finally {
        // 如果不写finally执行以下代码，在10 / 0处就会报错终止程序从而无法执行以下代码
        // 如果写了finally此段代码不管怎样都会执行

        System.out.println("程序执行");
    }
}
```

> 在使用流操作或者网络操作时必须手动关闭连接，因为这些类型被其他引用指向gc无法处理并回收这些对象，
> 导致资源泄漏（程序已经结束了，但是资源还在被占用），需要手动搭配finally进行关闭

throws（抛出异常）：在方法声明出编写`throws 异常类型,异常类型`

```java
class ThrowsTest {
    public void method2() throws IOException { //再次抛出
        method(); //调用method，如果不写try-catch或throws编译报错
    }

    public void method() throws FileNotFoundException, IOException { //向上抛
        FileWriter fileWriter = new FileWriter("config.txt"); //抛出异常
    }
}
```

如果代码执行成功将不抛出，如果执行失败抛出异常将向上抛出如果不处理main方法也抛出，
错误将抛出到JVM从而终止JVM，从这种角度看throws方式不算是真正意义上的处理异常

> 如果继承的接口方法抛出异常，你抛出的异常不能比重写方法的异常更大

使用**throw**手动抛出异常，注意：throws是向上抛出异常，而throw是手动抛出一个异常对象，
在实际开发中假如你要对一个网络传过来的数据进行操作，可是数据的id为-1，在我们的程序中是不允许这样的，
虽然Java可以允许-1存在，但是我们的程序不允许-1的存在，如果直接写处理方法可能差点意思，
那么我们就可以抛出一个异常或者一个自定义异常，如果你正在编写外部库，那么自定义异常和手动抛出异常是很重要的

```java
public static void main(String[] args) {
    int dataId = -1;
    //使用throw new 异常类型抛出一个异常
    if (dataId < 0) throw new RuntimeException("无效的数据ID");
}
```

在我们编写代码时如果 ，自定义一个异常的话需要继承Exception或RuntimeException类，
编译自定义异常的主要原因是为了通过异常的名称，就能具体判断出现什么问题

```java
//创建一个自定义异常类
public class IdInvalidException extends RuntimeException {

    //一个序列化号，用于序列化一个类，序列化号可以随便写
    @java.io.Serial
    static final long serialVersionUID = -2411718391L;


    public IdInvalidException() {

    }

    public IdInvalidException(String message) {
        super(message);
    }
}
```

> 为什么会有序列化？因为Throwable实现了Serializable接口，而Throwable又是Exception的父类

手动抛出一个自定义异常

```java
public static void main(String[] args) {
    String id = "-1";
    int idInt = Integer.parseInt(id);
    if (idInt < 0) {
        throw new IdInvalidException("无效的ID");
    }
}
```

异常打印

```text
Exception in thread "main" com.afeibaili.pack3.IdInvalidException: 无效的ID
	at com.afeibaili.pack3.Main.main(Main.java:8)
```

## <div id="java-多线程">多线程</div>

如果想让一个程序分别进行操作，比如一条线进行获取网络信息，获取到信息另一条线进行数据分割并处理，
如果不用多线程那么需要处理完数据才能获取下一条信息，但是有了多线程可以多条线程一起工作

一个代码项目或者一个应用程序可以称作程序，一个运行中的聊天软件就是一个程序，而**进程**可以理解为程序开始到结束的过程。
每个进程在电脑中都有一个独立的内存空间，而一个进程可以细分为多个**线程**，线程是程序内部执行的一条路径，
一个程序至少有一个线程，如果一个进程同一时间执行多个线程，那么这个进程就是多线程的

多个线程不同的分配有多个调度：**分时调度**，所有线程轮流访问CPU每个线程平均获取时间、**抢占式调度**：
让优先级高的线程以较大的概率抢占CPU如果优先级相同及随机选择一个（Java使用抢占式调度）

多线程的优点：提高应用程序的响应。对图形化更重要，增强用户体验、提高计算机系统从利用率、改善程序结构，
将复杂的程序进程分为多个线程，利于理解和修改

并行和并发：**并行**是指多个事件在同一时刻发生，例如多个人做不同的事、**并发**：
指两个或多个事在同一时间段内发生，即在一段时间内，有多条指令单个CPU轮流执行、交替、轮换，
使得在宏观上具有多个进程在同时执行

使用**Thread**类创建一个线程，每个Thread类的实例就相当于一个线程，
重写Thread的run方法并调用start即开始执行此线程

使用继承重写的方式

```java
public class Main {
    public static void main(String[] args) {
        Stream stream = new Stream();
        //开启线程的执行
        stream.start();
    }
}

class Stream extends Thread {
    @Override
    public void run() {
        //要给此线程做的事情
    }
}

```

使用匿名实现类的方式

```java
public static void main(String[] args) {
    new Thread() {
        @Override
        public void run() {
            //此线程要做的事情
        }
    }.start(); //直接调用运行不返回线程对象
}
```

上面代码可以用lambda表达式简化为

```java
public static void main(String[] args) {
    //传入一个Runnable函数式接口并简化为lambda
    new Thread(() -> {
        //此线程要做的事情
    }).start(); //直接调用运行不返回线程对象
}
```

多线程的直观展示

```java
public class Main {
    public static void main(String[] args) {
        new Thread(() -> {
            for (int i = 0; i < 100; i++) {
                System.out.println("thread:" + i);
            }
        }).start();
        for (int i = 0; i < 100; i++) {
            System.out.println("main:" + i);
        }
    }
}

/* 结果打印为：
main:0
main:1
main:2
thread:0
thread:1
thread:2
thread:3
main:3
...
 */
```

在Thread构造方法中，可以传入一个Runnable接口，此接口的run方法就是Thread要执行的方法，
还可以传入一个String类型的name即是线程的名称

Thread中常用的方法

| 方法              | 功能             |
|-----------------|----------------|
| start()         | 启动一个线程         |
| run()           | 线程要执行的操作       |
| currentThread() | 获取当前执行的线程（静态的） |
| getName()       | 获取线程名          |
| setName()       | 设置线程名          |
| sleep()         | 让线程基于毫秒睡眠（静态的） |
| yield()         | 让出线程的执行权（静态的）  |
| join()          | 等待线程执行完        |
| isAlive()       | 线程是否存活         |
| stop()          | 强行结束线程（过时的）    |
| suspend()       | 暂停此线程（过时的）     |
| resume()        | 恢复此线程（过时的）     |
| getPriority()   | 获取线程优先级        |
| setPriority()   | 设置线程优先级范围1-10  |

> join方法在a线程中通过b调用join那么a线程将阻塞等待b线程执行完毕。stop过时是因为，
> 强行结束一个线程会导致线程中的任务无法完成或一些清理工作得不到完成，不建议使用，
> 可以使用`interrupt()`方法标记是否中断，然后在run方法中做出判断让线程内部执行完。
> suspend/resume必须成对出现，suspend会导致线程暂停，但不会释放任何锁资源，
> 导致其他线程都无法访问它被占用的锁，直到调用resume，不建议使用，
> 可以使用Object类中的**wait()**方法，线程暂停会让出锁，
> 使用notify进行唤醒，notifyAll唤醒全部等待的线程

线程安全问题，在我们使用多个线程访问同一资源时，若多线程只有读线程那么将不会出现线程安全问题，
如果多个线程有读和写的操作就容易出现线程安全问，例如你的银行账户有3000块钱，
你和你媳妇同时取出2000，那么会减两次2000

如果多个线程访问并修改一个变量，会导致变量内容不准确。以下例子，定义了一个变量票数，
三个线程轮流取票导致可能出现重票和错票，这是我们不希望出现的，出现问题是因为进入到if判断之后有一些逻辑操作，
在处理操作时其他线程也进入if判断获取到没有修改后的变量，这样会导致第一个修改完毕， 而第二个根据修改后的又修改一次，
导致出现错误。

```java
package com.afeibaili.pack3;

public class Main {
    //定义票数
    public static int ticket = 10;

    //方法入口
    public static void main(String[] args) throws InterruptedException {
        //定义线程1
        Thread thread1 = new Thread(() -> {
            while (ticket > 0) {
                //假如做一些操作
                try {
                    Thread.sleep(10);
                } catch (InterruptedException e) {
                    throw new RuntimeException(e);
                }
                //售出的票
                System.out.println("售票处1卖出去了一张票，当前票：" + --ticket);
            }
        });
        thread1.start();
        //定义线程2
        Thread thread2 = new Thread(() -> {
            while (ticket > 0) {
                //假如做一些操作
                try {
                    Thread.sleep(10);
                } catch (InterruptedException e) {
                    throw new RuntimeException(e);
                }
                //售出的票
                System.out.println("售票处2卖出去了一张票，当前票：" + --ticket);
            }
        });
        thread2.start();
        //定义线程3
        Thread thread3 = new Thread(() -> {
            while (ticket > 0) {
                //假如做一些操作
                try {
                    Thread.sleep(10);
                } catch (InterruptedException e) {
                    throw new RuntimeException(e);
                }
                //售出的票
                System.out.println("售票处3卖出去了一张票，当前票：" + --ticket);
            }
        });
        thread3.start();
        
        /* 打印结果为：
            售票处1卖出去了一张票，当前票：9
            售票处2卖出去了一张票，当前票：8
            售票处3卖出去了一张票，当前票：7
            售票处1卖出去了一张票，当前票：6
            售票处3卖出去了一张票，当前票：4
            售票处2卖出去了一张票，当前票：5
            售票处3卖出去了一张票，当前票：3
            售票处1卖出去了一张票，当前票：2
            售票处2卖出去了一张票，当前票：1
            售票处3卖出去了一张票，当前票：0
            售票处1卖出去了一张票，当前票：-1
            售票处2卖出去了一张票，当前票：-2
        */
    }
}
```

解决方式为：必须保证一个线程在处理变量时其他线程必须等待直到线程对变量操作完毕，
在Java中可以使用同步代码块或者同步方法

- **同步代码块（synchronized）**：编写需要同步的代码逻辑，即操作共享数据的代码。
  被synchronized包裹的部分就使得一个线程在里面进行处理，其他线程只能等待，同步监视器，
  俗称锁，哪个线程获取了锁，哪个线程就能执行需要同步的代码，可以用任意类当作同步监视器，
  但是多个线程必须使用一个同步监视器

  使用`synchronized (object) { //代码块 }`创建一个同步代码块，object需要传入一个对象，
  让参与同步的代码块都要传入此对象


- **同步方法**：我们可以将操作共享数据的代码放到一个方法里可以让多个线程调用此方法，
  并且不需要写同步监视器，使用同步监视器是因为多个代码块用到一个同步监视器，而同步方法只有一段代码，
  所以同步监视器是this，如果是静态即使类本神

  使用`public synchronized static void syncMethod() { //方法体 }`创建一个同步方法，
  在修饰符后面声明synchronized关键字

synchronized解决了线程安全问题，但是操作共享数据时，多线程又变成了串行了

我们使用同步解决了安全问题但是会引发另一个问题，那就是**死锁**，两个线程占用不同的锁，
而两个线程需要对方的锁才能继续执行，而释放锁又需要对方的锁，这样就导致握着锁不放又需要对方的锁

在编写代码时要注意不要给代码写成死锁，也要判断代码是否会写成死锁，注意不要达成互斥条件、占用锁且等待锁

一个死锁例子，线程1在占用锁1还要等待锁2释放，而线程2占用锁2等待锁1释放，导致死锁

```java
public class Main {
    public static void main(String[] args) {
        Object lock1 = new Object();
        Object lock2 = new Object();


        new Thread(() -> {

            synchronized (lock1) {
                try {
                    Thread.sleep(100);
                } catch (InterruptedException e) {
                    throw new RuntimeException(e);
                }
                synchronized (lock2) {
                    System.out.println("线程1操作");
                }
            }

        }).start();

        new Thread(() -> {

            synchronized (lock2) {
                try {
                    Thread.sleep(100);
                } catch (InterruptedException e) {
                    throw new RuntimeException(e);
                }
                synchronized (lock1) {
                    System.out.println("线程2操作");
                }
            }

        }).start();
    }
}
```

使用Lock类来进行锁操作，对比synchronized来说Lock只需要两个方法，创建一个ReentrantLock类，
在操作共享变量前调用ReentrantLock实例的lock方法，在操作共享变量后调用unlock方法

```java
public static void main(String[] args) {
    //多个线程必须用一个Lock实例
    ReentrantLock reentrantLock = new ReentrantLock();

    new Thread(() -> {


        //操作前调用lock方法
        reentrantLock.lock();
        while (ticket > 0) {

            try {
                Thread.sleep(10);
            } catch (InterruptedException e) {
                throw new RuntimeException(e);
            }

            System.out.println("线程1：" + --ticket);
        }
        //操作后调用
        reentrantLock.unlock();

    }).start();
    new Thread(() -> {

        //操作前调用lock方法
        reentrantLock.lock();
        while (ticket > 0) {

            try {
                Thread.sleep(10);
            } catch (InterruptedException e) {
                throw new RuntimeException(e);
            }


            System.out.println("线程2：" + --ticket);
        }
        //操作后调用
        reentrantLock.unlock();

    }).start();
}
```

suspend方法暂停线程而不释放锁，所以这是一个过时的方法，可以使用wait方法来代替suspend，
wait可以暂停线程并释放锁，resume唤醒suspend后的线程，那么可以用notify来唤醒wait的线程，
也可以使用notifyAll唤醒全部线程，注意如果有多个线程wait notify会唤醒线程优先级最高的那个，
如果相同优先级就会随机唤醒一个，被唤醒的线程紧接着wait后的位置继续执行

注意使用wait和notify/notifyAll要在synchronized中，如果是Lock类需获取并使用Condition类

> wait和notify/notifyAll在Object类中所以每个对象都可以调

使用Callable、FutureTask、Thread来实现一个有返回值的线程

```java
public static void main(String[] args) throws ExecutionException, InterruptedException {
    FutureTask<Integer> task = new FutureTask<>(() -> {
        //run方法的操作逻辑，可有返回值
        return 42;
    });
    //启动运行线程
    new Thread(task).start();
    //等待线程运行完并打印
    System.out.println(task.get());
}
```

> 多线程还可以使用线程池，使用`Executors`类创建线程池相关操作

## <div id="java-常用类">常用类</div>

### <div id="java-string类">String类</div>

String类也是我们常用的类了，翻开String源码后看到String是final修饰的，代表着这个类不可继承的，
String还实现了Serializable接口，此接口代表此对象可以序列化的，序列化指的是可以把此对象序列化一串二进制，
使用反序列化将序列化的二进制串反序列化为对象，String还实现了Comparable接口，凡是实现此接口的类，
其对象可以比较大小

在jdk8中存入的字符串以char类型数组进行存储，而jdk9及以后使用字节数组（byte[]）进行存储，
使用byte将节省一部分内存空间

声明的字符串`String str = "Hello";`都放在字符串常量池中，字符串常量池中不允许两个两个相同的字符串，
所以再创建一个字符串其值还为Hello那么使用“==”比较其返回值为true，因为字符串常量池不允许两个相同的字符串，
所以返回了相同字符串的内存地址，jdk7之前：字符串常量池放在方法区，jdk7及以后放在堆空间中

String还可以使用`new String("Hello")`来创建一个字符串，需要注意的是，创建String对象和直接写字符串常量，
它们的引用地址不是一样的，我们都知道两个String类型使用字符串常量声明相同的字符串常量它们的引用地址是相同的，
因为它们都是在字符串常量池中获取的引用地址，而使用new String()会导致先在堆内存中创建地址，
再引用到字符串常量池里面的字符串，所以`String s1 = new String("Hello")`和`String s2 = "Hello"`，
判断它们的相等性`==`结果并不相等

如果在使用字符串拼接是其中一方包含变量，那么底层字节码文件并不会直接拼接这两个字符串，
但如果是两个字符串常量会直接拼接为一个字符串常量，但那个变量被常量修饰符（final）
修饰后就和普通字符串常量一致了

```java
public void equals() {
    String s1 = "hello";
    final String s2 = "world";

    String s3 = "helloworld";
    String s4 = "hello" + "world";
    //通过查看字节码文件发现调用了StringBuilder的toString()
    String s5 = s1 + "world";
    //由于s2被常量修饰符修饰，所以s3和s4个s6地址都是一致的
    String s6 = "hello" + s2;
    String s7 = s1 + s2;
}
```

字符串还可以使用`getBytes()`用指定的字符集进行字符串解码，当然还可以在创建字符串使用构造函数中指定字符集进行编码

```java
public static void main(String[] args) throws UnsupportedEncodingException {
    //一个包含中文的字符串
    String s1 = "abc你好";
    //将字符串以gbk解码为字节数组
    byte[] gbk = s1.getBytes("gbk");

    //将上面的字节数组以utf-8编码打印为：abc���
    System.out.println(new String(gbk, "utf-8"));
    //将上面的字节数组以gbk编码打印为：abc你好
    System.out.println(new String(gbk, "gbk"));
}
```

String常用方法

`intern()`返回字符串常量池中的字符串

```java
public void internTest() {
    String str = "嘿嘿嘿哈";
    String intern = str.intern();
    System.out.println(str == intern); //true
}
```

`isEmpty()`判断字符串是否为空

```java
public void isEmptyTest() {
    String str = "";
    String str1 = "hi";
    System.out.println(str.isEmpty()); //true
    System.out.println(str1.isEmpty()); //true
}
```

`length()`返回字符串的长度

```java
public void lengthTest() {
    String str = "早安";
    System.out.println(str.length()); //2
}
```

`concat()`拼接字符串

```java
public void concatTest() {
    String str = "早";
    String str1 = "安";
    System.out.println(str.concat(str1)); //早安
}
```

`equals()`判断两个字符串内容是否相等

```java
public void equalsTest() {
    String str = "午安";
    String str1 = new String("午安");
    System.out.println(str.equals(str1)); //true
}
```

`equalsIgnoreCase()`判断两个字符串是否相等，不区分大小写

```java
public void equalsIgnoreCaseTest() {
    String str = "abc";
    String str1 = "ABC";
    System.out.println(str.equalsIgnoreCase(str1)); //true
}
```

`compareTo()`比较字符串大小，根据Unicode编码值比较

```java
public void compareToTest() {
    String str = "a";
    String str1 = "b";
    //相同为0，大于为1小于为-1
    System.out.println(str.compareTo(str1)); //-1
}
```

`compareToIgnoreCase()`比较字符串大小，根据Unicode编码值比较，不区分大小写

```java
public void compareToIgnoreCaseTest() {
    String str = "a";
    String str1 = "A";
    //相同为0，大于为1小于为-1
    System.out.println(str.compareToIgnoreCase(str1)); //0
}
```

`trim()`去掉字符串前后的空白符

```java
public void trimTest() {
    String str = "\na   ";
    System.out.println(str.trim()); //a
}
```

`toUpperCase()`将字符串的小写转为大写

```java
public void toUpperCaseTest() {
    String str = "abc";
    System.out.println(str.toUpperCase()); //ABC
}
```

`toLowerCase()`将字符串的大写转为小写

```java
public void toLowerCaseTest() {
    String str = "ABC";
    System.out.println(str.toLowerCase()); //abc
}
```

`contains()`是否包含某字符串

```java
public void containsTest() {
    String str = "hello";
    System.out.println(str.contains("llo")); //true
}
```

`indexOf()`查找某字符串的位置

```java
public void indexOfTest() {
    String str = "hello";
    //没有找到为-1
    System.out.println(str.indexOf("llo")); //2
    //从指定位置往后寻找
    System.out.println(str.indexOf("l", 3)); //3
}
```

`lastIndexOf()`从后查找某字符串的位置

```java
public void lastIndexOfTest() {
    String str = "hello";
    //没有找到为-1
    System.out.println(str.lastIndexOf("llo")); //2
    //从指定位置往前寻找
    System.out.println(str.lastIndexOf("l", 3)); //3
}
```

`substring()`截取并返回一个新的字符串

```java
public void substringTest() {
    String str = "hello world";
    //从下标6往后截取
    System.out.println(str.substring(6)); //world
    //从下标6往后截取直到下标8
    System.out.println(str.substring(6, 8)); //wo
}
```

`chatAt()`返回指定下标的字符

```java
public void charAtTest() {
    String str = "hello";
    System.out.println(str.charAt(4)); //o
}
```

`valueOf`静态方法，将某类型转为String类型

```java
public void valueOfTest() {
    System.out.println(String.valueOf(3.5)); //3.5
    System.out.println(String.valueOf(new char[]{'h', 'i'})); //hi
}
```

`copyValueOf`静态方法，根据偏移量和长度截取字符数组中的字符

```java
public void copyValueOfTest() {
    char[] chars = {'h', 'i'};
    System.out.println(String.copyValueOf(chars, 1, 1)); //i
}
```

`startsWith()`是否以某字符串开头

```java
public void startsWithTest() {
    String str = "//hello";
    System.out.println(str.startsWith("//")); //true
}
```

`endsWith()`是否以某字符串结尾

```java
public void endsWithTest() {
    String str = "//hello";
    System.out.println(str.endsWith("//")); //false
}
```

`replace()`替换字符串内容

```java
public void replaceTest() {
    String str = "hewwo";
    System.out.println(str.replace('w', 'l')); //hello
    //替换字符串
    System.out.println(str.replace("hewwo", "world")); //world
}
```

`replaceAll()`根据正则表达式替换字符串

```java
public void replaceAllTest() {
    String str = "username123456";
    //将所有的数组转换为空字符串，正则中\d代表数字
    System.out.println(str.replaceAll("\\d", "")); //username
}
```

`replaceFirst()`根据正则表达式替换第一个字符串

```java
public void replaceFirstTest() {
    String str = "username123456";
    //只替换第一个正则
    System.out.println(str.replaceFirst("\\d", "")); //username
}
```

### <div id="java-stringbuilder和stringbuffer">StringBuilder和StringBuffer</div>

String是不可变字符序列，而StringBuilder和StringBuffer都是可变字符序列，
StringBuilder是线程不安全的jdk5.0声明效率高，而StringBuffer是线程安全的jdk1.0声明效率低

StringBuilder和StringBuffer操作字符串相比于String效率会更高

它们的方法和功能都是类似的我们针对于StringBuilder来说，创建一个StringBuilder默认有16个字符容量，
`StringBuilder sb = new StringBuilder()`默认内部容量为16，
如果默认传入一个字符串那么默认容量就会变为默认的16容量加上字符串的长度，一旦字符串添加的长度不够用，
就会扩容内部的字符数组

StringBuilder常用方法

`append()`追加字符串

```java
public void stringBuilderTest() {
    StringBuilder sb = new StringBuilder();
    //append的返回值是this，就是当前对象本身，所有可以链式调用此方法
    sb.append("hello").append(" ").append("world");
    System.out.println(sb.toString()); //hello world
}
```

`delete()`删除指定位置的字符串

```java
public void deleteTest() {
    StringBuilder sb = new StringBuilder("hello");
    sb.delete(2, 5);
    //可以省略toString调用默认println内部方法调用toString
    System.out.println(sb.toString()); //he
}
```

`deleteCharAt()`删除指定位置的字符

```java
public void deleteCharAtTest() {
    StringBuilder sb = new StringBuilder("hello");
    sb.deleteCharAt(1);
    System.out.println(sb.toString()); //hllo
}
```

`replace()`替换指定位置的字符串

```java
public void replaceTest() {
    StringBuilder sb = new StringBuilder("hewwo");
    sb.replace(2, 4, "ll");
    System.out.println(sb); //hello
}
```

`setCharAt()`替换指定位置的字符

```java
public void setCharAtTest() {
    StringBuilder sb = new StringBuilder("hewlo");
    sb.setCharAt(2, 'l');
    System.out.println(sb); //hello
}
```

`charAt()`获取指定位置的字符

```java
public void charAtTest() {
    StringBuilder sb = new StringBuilder("hello");
    char charAt = sb.charAt(0);
    System.out.println(charAt); //h
}
```

`insert()`在指定位置插入字符串

```java
public void insertTest() {
    StringBuilder sb = new StringBuilder("hello");
    sb.insert(5, " world");
    System.out.println(sb); //hello world
}
```

`length()`返回字符串长度

```java
public void lengthTest() {
    StringBuilder sb = new StringBuilder("hello");
    System.out.println(sb.length()); //5
}
```

`reverse()`反转字符串

```java
public void reverseTest() {
    StringBuilder sb = new StringBuilder("hello");
    System.out.println(sb.reverse()); //olleh
}
```

`setLength()`设置字符串长度，并删除后面的字符串

```java
public void setLengthTest() {
    StringBuilder sb = new StringBuilder("hello");
    sb.setLength(2);
    System.out.println(sb); //he
}
```

当然StringBuilder还有String一些常用的api例如indexOf、substring等等方法，功能和String中一样的

### <div id="java-时间类">时间类</div>

获取时间最简单的方式可以使用`System.currentTimeMillis()`获取当前的毫秒值，叫做时间戳，
从1970年1月1日开始计算的毫秒值

#### jdk8之前

使用Date类，创建一个基于当前系统时间的Date实例`new Date()`，注意是java.util包下的。
Date类中也可以传入一个时间戳，根据时间戳来获取时间

在java.sql包下也有个Date类，是为了对应数据库的时间信息，使用`new Date(long l)`传入一个时间戳来获取时间

```java
public void dateTest() {
    System.out.println(new java.util.Date()); //Fri May 09 17:48:24 CST 2025
    System.out.println(new java.sql.Date(System.currentTimeMillis())); //2025-05-09
}
```

使用SimpleDateFormat类，SimpleDateFormat可以进行格式化将日期转为文本，也可以将文本解析为日期

将日期格式为字符串，将字符串解析为日期

```java
public void dateTest() throws ParseException {
    Date date = new Date();
    SimpleDateFormat sdf = new SimpleDateFormat();
    //date对象toString
    System.out.println(date); //Fri May 09 18:01:43 CST 2025
    //date的默认格式化
    System.out.println(sdf.format(date)); //2025/5/9 下午6:01
    //将字符串解析为日期，可能会抛出解析异常
    Date parse = sdf.parse("2025/5/9 下午6:01");
    System.out.println(parse); //Fri May 09 18:01:00 CST 2025
}
```

SimpleDateFormat类的主要作用还是格式化，在构造方法中传入要格式化的字符串，接着调用格式化方法

api中对应的格式为字母

| 字母 | 日期或时间         | 介绍          | 示例                                    |
|----|---------------|-------------|---------------------------------------|
| G  | 年号（纪元指示符）     | 文本          | AD                                    |
| y  | 年             | 年           | 1996; 96                              |
| Y  | 年             | 年           | 2009; 09                              |
| M  | 一年中的月份（上下文相关） | 月           | July; Jul; 07                         |
| L  | 一年中的月份（独立形式）  | 月           | July; Jul; 07                         |
| w  | 一年中的周         | 周           | 27                                    |
| W  | 每月的周          | 周           | 2                                     |
| D  | 一年中的天         | 数           | 189                                   |
| d  | 月中的天          | 数           | 10                                    |
| F  | 当月的星期几        | 数           | 2                                     |
| E  | 星期名称          | 文本          | Tuesday; Tue                          |
| u  | 星期数           | 数           | 1                                     |
| a  | 上午或下午         | 文本          | PM                                    |
| H  | 一天中的小时（0-23）  | 数           | 0                                     |
| k  | 一天中的小时（1-24）  | 数           | 24                                    |
| K  | 上午 / 下午（0-11） | 数           | 0                                     |
| h  | 上午 / 下午（1-12） | 数           | 12                                    |
| m  | 当前小时的分钟       | 数           | 30                                    |
| s  | 当前分钟的秒        | 数           | 55                                    |
| S  | 当前秒的毫秒        | 数           | 978                                   |
| z  | 时区            | 通用时区        | Pacific Standard Time; PST; GMT-08:00 |
| Z  | 时区            | RFC 822 时区  | -0800                                 |
| X  | 时区            | ISO 8601 时区 | -08; -0800; -08:00                    |

一个常见的格式化

```java
public void dateFormateTest() {
    SimpleDateFormat sdf = new SimpleDateFormat("yyyy-MM-dd HH:mm:ss");
    System.out.println(sdf.format(new Date())); //2025-05-11 12:53:35
}
```

现在Date中大量的勾构造方法和方法已经被标记为已弃用的了，API推荐使用**Calendar**类。
由于Calendar是一个抽象类通过Calendar.getInstance()获取日历类的实例，获取某一信息，
通过get(Calendar.字段名)来获取，当然还有set设置、add增加等操作

```java
public void calendarTest() {
    Calendar calendar = Calendar.getInstance();
    //获取毫秒数
    System.out.println(calendar.get(Calendar.MILLISECOND));
    //获取秒数
    System.out.println(calendar.get(Calendar.SECOND));
    //获取分钟数
    System.out.println(calendar.get(Calendar.MINUTE));
    //获取24小时数
    System.out.println(calendar.get(Calendar.HOUR_OF_DAY));
}
```

#### jdk8及之后

LocalDate获取日期、LocalTime获取时间、LocalDateTime获取时间和日期、Instant获取时间错、
DateTimeFormatter时间日期格式化，这些类都是jdk8及以后的类

虽然我们已经有了Calendar类，但Calendar并没有比Date类好多少，时间和日期这样的类应该是不可变的
（不更改原来的数值）、Date中年份是1900开始的，而月份都是从0开始、格式化只对Date有用，
Calendar则不行，此外它们都是线程不安全的、不能处理闰秒等

> 闰秒，是指为保持协调世界时接近于世界时时刻，由国际计量局统一规定在年底或年中（也可能在季末）
> 对协调世界时增加或减少1秒的调整。由于地球自转的不均匀和长期变慢性（主要由潮汐摩擦引起的），
> 会使世界时（民用时）和原子时之间相差超过到±0.9秒时，就把协调世界时向前拨1秒（负闰秒，最后一分钟为59秒）
> 或向后拨动1秒（正闰秒，最后一分钟为61秒）；闰秒一般加在公历年末或公历六月末。  
> 目前，全球已经进行了27次闰秒，均为正闰秒

本地日期时间：LocalDate、LocalTime、LocalDateTime，获取当前时间都是使用`now()`静态方法来获取当前时间，
使用`of()`静态方法来根据指定日期/时间创建对象

```java
public void localDateTimeTest() {
    System.out.println(LocalDate.now()); //2025-05-11
    System.out.println(LocalTime.now()); //13:37:48.328746600
    System.out.println(LocalDateTime.now()); //2025-05-11T13:37:48.328746600
    //指定时间日期
    LocalDateTime localDateTime = LocalDateTime.of(2005, 5, 16, 0, 0);
    System.out.println(localDateTime); //2005-05-16T00:00
}
```

还可以使用getDayOfMonth()/getDayOfYear()获取月份天数/获取年份天数、getDayOfWeek()获取星期几等等。
使用`withXxx()`设置日期，使用`plusXxx()`添加时间或日期、`minusXxx()`减去时间或日期

本地日期时间的不可变性

```java
public void localDateTimeTest() {
    //指定时间日期
    LocalDateTime localDateTime = LocalDateTime.of(2005, 5, 16, 0, 0);
    System.out.println(localDateTime); //2005-05-16T00:00
    //添加日期并返回新日期
    System.out.println(localDateTime.plusDays(5)); //2005-05-21T00:00
    //并没有更改原来的日期
    System.out.println(localDateTime); //2005-05-16T00:00
}
```

使用`isAfter()`方法判断是否在此时间之后，使用`isBefore()`方法判断是否在此时间之前

```java
public void isAfterAndIsBefore() {
    LocalDateTime localDateTime = LocalDateTime.of(2005, 5, 16, 0, 0);
    LocalDateTime plus5Day = localDateTime.plusDays(5);
    LocalDateTime minus5Day = localDateTime.minusDays(5);
    //判断本地时间是否在它之后
    System.out.println(localDateTime.isAfter(plus5Day)); //false
    System.out.println(localDateTime.isAfter(minus5Day)); //true
    //判断本地时间是否在它之前
    System.out.println(localDateTime.isBefore(plus5Day)); //true
    System.out.println(localDateTime.isBefore(minus5Day)); //false
}
```

还可以用`isLeapYear()`判断是否是闰年

使用Instant获取瞬时，时间线上的一个瞬间点。这可能被用来记录应用程序中的事件时间戳：
时间戳是指格林威治时间1970年01月01日00时00分00秒（北京时间提前8小时）起至现在的总秒数

使用`now()`静态方法来创建一个默认UTC时区的Instant对象，
使用`toEpochMilli()`返回1970-01-01 00:00:00到当前的毫秒数，即时间戳

由于Instant是UTC时区，所以使用atOffset()来进行一个偏移

```java
public void instantTest() {
    Instant instant = Instant.now();
    System.out.println(instant); //2025-05-11T06:08:20.101422400Z
    //设置偏移量八个小时，北京时间在UTC的基础上+8小时
    System.out.println(instant.atOffset(ZoneOffset.ofHours(8))); //2025-05-11T14:10:17.623691100+08:00
}
```

DateTimeFormatter可以格式化LocalDate、LocalTime、LocalDateTime，类似SimpleDateFormat

DateTimeFormatter提供了三种格式化方法：预定义的标准格式、本地化相关的格式、自定义格式。
当然可以根据格式解析

```java
public void dateTimeFormatterTest() {
    //预定义的
    DateTimeFormatter predefined = DateTimeFormatter.ISO_DATE_TIME;
    System.out.println(predefined.format(LocalDateTime.now())); //2025-05-11T14:24:12.3794375

    //本地化相关的
    DateTimeFormatter localizedDate = DateTimeFormatter.ofLocalizedDate(FormatStyle.FULL);
    System.out.println(localizedDate.format(LocalDateTime.now())); //2025年5月11日星期日

    //自定义的
    DateTimeFormatter ofPattern = DateTimeFormatter.ofPattern("yyyy-MM-dd HH:mm:ss");
    System.out.println(ofPattern.format(LocalDateTime.now())); //2025-05-11 14:25:36

    //解析
    DateTimeFormatter ofPattern1 = DateTimeFormatter.ofPattern("yyyy-MM-dd HH:mm:ss");
    //返回的是一个LocalDateTime的接口实现
    TemporalAccessor temporalAccessor = ofPattern1.parse("2025-05-11 14:25:36");
    //可以使用from方法来获取LocalDateTime对象
    LocalDateTime localDateTime = LocalDateTime.from(temporalAccessor);
    System.out.println(localDateTime); //2025-05-11T14:25:36
}
```

关于日期时间的还有一些类：关于时区的ZoneId和ZonedDateTime、关于日期和时间的Duration和Period

与传统日期类的转换

| 类                               | 到遗留类                                  | 从遗留类                        |
|---------------------------------|---------------------------------------|-----------------------------|
| Instant/Date（util下）             | Date.from(instant)                    | date.toInstant()            |
| Instant/Timestamp               | Timestamp.from(instant)               | timestamp.toInstant()       |
| ZonedDateTime/GregorianCalendar | GregorianCalendar.from(zonedDateTime) | cal.toZonedDateTime()       |
| LocalDate/Time（sql下）            | Date.valueOf(localDate)               | date.toLocalDate()          |
| LocalTime/Time（sql下）            | Date.valueOf(localTime)               | date.toLocalTime()          |
| LocalDateTime/Timestamp（sql下）   | Timestamp.valueOf(localDateTime)      | timestamp.toLocalDateTime() |
| ZoneId/TimeZone                 | TimeZone.getTimeZone(id)              | timeZone.toZoneId()         |
| DateTimeFormatter/DateFormat    | formatter.toFormat                    | 无                           |

### <div id="java-比较器">比较器</div>

Java中很多都是以对象的形式存在的，对象之间可以用equals判断是否相等，但是无法比较对象之间的大小，
我们可以使用Java中的两个接口来实现比较大小**Comparable自然排序**/**Comparator定制排序**，
用比较器来进行排序、自定义排序

一个对象排序

前置类

```java
class Worker {
    String name;
    int age;

    public Worker(String name, int age) {
        this.name = name;
        this.age = age;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        this.age = age;
    }

    @Override
    public String toString() {
        return "Worker{" +
                "name='" + name + '\'' +
                ", age=" + age +
                '}';
    }
}
```

使用**Arrays.sort()**进行排序

```java
public class ComparableTest {
    public static void main(String[] args) {
        Worker[] workers = new Worker[5];
        workers[0] = new Worker("张三", 18);
        workers[1] = new Worker("李四", 19);
        workers[2] = new Worker("王五", 20);
        workers[3] = new Worker("赵六", 19);
        workers[4] = new Worker("周七", 21);
        System.out.println(Arrays.toString(workers));
        Arrays.sort(workers);
        System.out.println(Arrays.toString(workers));
    }
}
```

报错，可以看到报出了ClassCastException异常，因为没有实现Comparable接口

```text
[Worker{name='张三', age=18}, Worker{name='李四', age=19}, Worker{name='王五', age=20}, Worker{name='赵六', age=19}, Worker{name='周七', age=21}, null, null, null, null, null]
Exception in thread "main" java.lang.ClassCastException: class com.afeibaili.pack3.Worker cannot be cast to class java.lang.Comparable (com.afeibaili.pack3.Worker is in unnamed module of loader 'app'; java.lang.Comparable is in module java.base of loader 'bootstrap')
	at java.base/java.util.ComparableTimSort.countRunAndMakeAscending(ComparableTimSort.java:320)
	at java.base/java.util.ComparableTimSort.sort(ComparableTimSort.java:188)
	at java.base/java.util.Arrays.sort(Arrays.java:1041)
```

实现Comparable接口并实现方法，**Comparable比较大小的方式是根据实现方法中对象返回的数值**，如果为正数当前对象大，
如果为负数就是当前对象小，为零就是等于

```java
//实现Comparable接口，泛型为本类型，可以假装泛型不存在
class Worker implements Comparable<Worker> {
    String name;
    int age;

    //实现方法
    @Override
    public int compareTo(Worker o) {
        //判断当前对象的年龄是否大于比较对象
        return this.age - o.age;
    }

    //省略 getter 和 setter 还有 toString
}
```

打印结果

```text
[Worker{name='张三', age=18}, Worker{name='李四', age=19}, Worker{name='王五', age=20}, Worker{name='赵六', age=19}, Worker{name='周七', age=21}]
[Worker{name='张三', age=18}, Worker{name='李四', age=19}, Worker{name='赵六', age=19}, Worker{name='王五', age=20}, Worker{name='周七', age=21}]
```

虽然Comparable可以实现让对象进行比较，但是Comparable有一个缺点，就是不能比较别人写的类，
当元素没有实现Comparable且不方便修改代码，还有一种情况就是别人实现了Comparable接口但是我不想使用它的排序方式，
那么可以使用**Comparator**接口，强行对多个对象进行比较，Comparator是一个接口，
通常是在方法中以实现类的方式传入Comparator中有个`compare(Object o1, Object o2)`方法传入两个对象进行比较

```java
public static void main(String[] args) {
    Worker[] workers = new Worker[5];
    workers[0] = new Worker("张三", 18);
    workers[1] = new Worker("李四", 19);
    workers[2] = new Worker("王五", 20);
    workers[3] = new Worker("赵六", 19);
    workers[4] = new Worker("周七", 21);
    System.out.println(Arrays.toString(workers));
    //传入一个Comparator匿名实现类并实现方法
    Arrays.sort(workers, new Comparator<Worker>() {
        @Override
        public int compare(Worker o1, Worker o2) {
            return o1.getAge() - o2.getAge();
        }
    });
    System.out.println(Arrays.toString(workers));
}
```

两种排序方式对比：自然排序，单一的唯一的；定制排序，灵活的多样的。
从另一种角度来看自然排序是一劳永逸的而定制排序是临时的

### <div id="java-其他常用类">其他常用类</div>

System类，System通常我们用来打印信息，除了打印信息System中还有很多方法属性，
System内部包含in、out、err三个成员变量，分别为标准输入流，标准输出流，错误输出流，
控制台输入输出都在System类中，之前使用Scanner类中传入的System.in就代表这是一个控制台输入

`currentTimeMillis()`静态方法，获取当前系统的时间戳（不含时区）

```java
public void currentTimeMillisTest() {
    long timeMillis = System.currentTimeMillis();
    System.out.println(timeMillis); //1747022150566
}
```

System类中有一个退出的方法，结束JVM进程就是`System.exit()`方法。
exit方法可以传入一个int值代表结束代码

`System.gc()`此方法作用请求系统进行垃圾回收。至于系统是否立刻回收，
则取决于系统中垃圾回收算法的实现以及系统执行时的情况

`System.getProperty()`此方法的作用是获得系统中名为key的属性对应的值

| 属性名          | 属性说明        |
|--------------|-------------|
| java.version | Java运行时环境版本 |
| os.name      | 操作系统名称      |
| user.dir     | 用户的当前目录     |

可以使用`System.getPropertys()`获取所有属性

```java
public void getPropertyTest() {
    System.getProperties().forEach((k, v) -> {
        System.out.println(k + "=" + v);
    });
}
```

Runtime类：每个Java应用程序都有一个Runtime类实例，使应用程序能够与其运行的环境相连接。
Runtime中有一个静态属性即Runtime的唯一实例，使用`getRuntime()`方法返回当前运行时对象

Runtime中有`totalMemory()`方法，返回Java虚拟机中初始时的内存总量。
此方法返回的值可能随着时间的推移而变化，这取决于主机环境。默认为物理电脑内存的1/64

`maxMemory()`方法返回Java虚拟机中最大程度能使用的内存总量。默认为物理电脑内存的1/4

`freeMemory()`方法返回Java虚拟机空闲内存量。调用gc方法可能使得freeMemory返回值增加

```java
public void runtimeTest() {
    Runtime runtime = Runtime.getRuntime();
    System.out.println(runtime.totalMemory() / 1024 / 1024 + "MB");
    System.out.println(runtime.freeMemory() / 1024 / 1024 + "MB");
    System.out.println(runtime.maxMemory() / 1024 / 1024 + "MB");
}
```

**Math**类凡是数学运算相关的操作，都可以查看Math类的方法

`Math.abs(-5)`结果为5；取绝对值

`Math.ceil(3.3)`结果为4；向上取整

`Math.floor(3.3)`结果为3；向下取整

`Math.round(3.3)`结果为3；四舍五入

`Math.random()`结果为0-1的随机值

`Math.pow(double a, double b)`返回a的b次幂

`Math.sqrt(double a)`返回a的平方根

`Math.PI`返回圆周率

等等还有一些对于数学的方法

BigInteger、BigDecimal类不管是int还是long类型它们存储的值都是有限的，
如果要使用很大的数或小数就使用BigInteger或BigDecimal，
因为大到连数值类型都放不下了所以运算操作都是以方法存在的，返回值也是BigInteger、BigDecimal类

```java
public void bigNumberTest() {
    BigInteger b1 = new BigInteger("1321685464891321313");
    BigInteger b2 = new BigInteger("1321685464891321303");
    //加
    System.out.println(b1.add(b2)); //2643370929782642616
    //减
    System.out.println(b1.subtract(b2)); //10
    //乘
    System.out.println(b1.multiply(b2)); //1746852468104988129868587498094830839
    //除
    System.out.println(b1.divide(b2)); //1
    //取余
    System.out.println(b1.mod(b2)); //10
}
```

Random类用于产生随机数，里面有许多方法获取随机的int、byte、float...等等类型

```java
public void randomTest() {
    Random random = new Random();
    System.out.println(random.nextInt()); //1548607685
    System.out.println(random.nextLong()); //1786862586748623907
    System.out.println(random.nextDouble()); //0.2514538801269194
    System.out.println(random.nextFloat()); //0.23771548
    System.out.println(random.nextBoolean()); //true
    //指定范围
    System.out.println(random.nextInt(10)); //4
}
```

## <div id="java-泛型">泛型</div>

泛型就像是很多抽屉外面的标签，代表这个抽屉是存放哪种物品的。

在Java中我们声明方法时，当完成方法功能时如果有未知的数据需要参与，这些未知的数据是不确定的，
所以利用泛型将未知数据的类型传入，就知道数据是哪种类型了。泛型即为参数类型，
这个类型参数在声明它的类、接口、方法中代表某种未知的通用类型

例如Comparable中的泛型，我们无需在意这是什么类型，因为任何类型都可以使用

```java
public interface Comparable<T> {
    int compareTo(T o);
}
```

<T>就是泛型，而T只是个标识符，可以并非为一个字母，也可以写整个单词例如<Type>

泛型的使用，例如集合中的泛型

```java
public void genericsTest() {
    //声明此数组列表的类型为String，add方法只能存放String类型
    //因为声明时指定类型了，在创建的时候可以不写指定类型
    ArrayList<String> list = new ArrayList<>();
    list.add("a");
    list.add("b");
    //编译报错，类型不符合
    //list.add(1);
}
```

如果在创建泛型类的时候没有传入泛型就默认为Object类，其实想想也知道，
编译器不知道这是什么类型那么只能为所有对象的父类也就是Object

创建一个泛型类，需要在类名后面写一个尖括号<>尖括号中写入类型的标识符

```java
//声明为泛型类，泛型名为Type
public class Tool<Type> {
    //一个泛型属性
    Type type;

    //构造函数，传入一个泛型类型
    public Tool(Type type) {
        this.type = type;
    }

    //返回泛型类型的对象
    public Type get() {
        return type;
    }
}
```

创建并获取泛型类的实例，注意泛型是无法放入基本数据类型的

```java
public static void main(String[] args) {
    Tool<String> tool = new Tool<>("Hello");
    //报错，泛型类型不能为基本数据类型，可以使用包装类型
    //Tool<int> tool = new Tool<>(1);
    String string = tool.get();
}
```

如果父类有泛型，可以指定声明泛型类型、从声明子类泛型并传入父类，
如果子类不指定父类泛型类型那么父类的泛型为Object

声明父类

```java
public class SupperClas<T> {
}
```

子类如果不声明泛型类型可以指定类型

```java
class SubClass extends SupperClas<Integer> {
}
```

子类声明泛型类型

```java
class SubClass<T> extends SupperClas<T> {
}
```

**泛型类型可以声明多个**，多个类型之间以逗号分割

```java
//声明多个泛型，并传入父类一个类型
class SubClass<InType, OutType, ShowType> extends SupperClas<ShowType> {
}
```

声明完泛型之后可以在类的内部使用泛型（属性、方法、构造器），创建自定义泛型类对象时，可以指明泛型参数类型。  
一旦指明内部凡是使用类的泛型参数的位置都具体化为指定的泛型类型，如果创建自定义泛型类对象时，
没有指明泛型类型，那么泛型将被擦除，泛型对应的类型都将按照Object类处理。  
泛型最好要么一路都用，要么一路都不用。  
泛型指定的泛型必须为引用数据类型，不能为基本数据类型，此时可以用包装类。  
除创建泛型外，子类继承泛型类时， 实现类实现泛型接口时，也可以确定泛型中的泛型结构。  
如果我们在给泛型类提供子类时，子类也不确定泛型的类型，则可以继续使用泛型参数。  
我们还可以在现有的父类的泛型参数的基础上，新增泛型参数

注意不能使用`new E[]`但是可以`E[] e = (E[])new Object[capacity]`

可以不使用泛型类，但是可以声明泛型方法，泛型方法的泛型参数通常会出现在形参列表和返回值类型中

```java
//声明一个静态的泛型方法，在返回值前方声明泛型
public static <T> T getTool(T tool) {
    return tool;
}
``` 

格式

```text
权限修饰符 <T> 返回值类型 方法名(形参列表) {
}
```

使用泛型方法需要注意的是，泛型类型要放在调用的方法名前面

```java
String s = Tool.<String>getTool("Hi Tool");
```

泛型在继承上的使用，需要注意的是假设我有两个对象分别是`Class<Object> o1`和`Class<String> s1`，
`o1 = s1 //报错`o1是不能让s1赋值的，尽管它们存在子父类的关系，但是s1并不能赋值给o1，假如允许存在这种操作s1赋值成功了，
那么s1适用的方法到Object都没有了

```java
public void objectTest() {
    ArrayList<Object> list = new ArrayList<>();
    ArrayList<String> list1 = new ArrayList<>();
    //泛型类型可以添加子类型的值
    list.add("hello");
    //但是无法赋值不同类型的泛型，报错
    //list = list1
    //如果进行赋值那么s1就不是一个String类型了，
    //也就是说内部调用可以传入一个Integer类型，
    //这很明显不是ArrayList<String>对象要干的事
}
```

如果要对泛型进行通用操作可以使用通配符&lt;?&gt;

```java
public void objectTest() {
    ArrayList<?> list = new ArrayList<>();
    ArrayList<String> list1 = new ArrayList<>();
    list1.add("one");
    //可以进行赋值
    list = list1;
    //可以读取但是无法写入（null是个例外），如果可以写入那和Object有什么区别
    //list.add("hello");
    System.out.println(list.get(0));
    list.add(null);
}
```

> 注意带?的泛型只能读取不能写入

通配符：?，使用举例：ArrayList&lt;?&gt;。Class&lt;?&gt;可以看作Class&lt;?&gt;的父类，
即可以将Class&lt;?&gt;的对象赋值给Class&lt;?&gt;类型的引用或变量

带限制条件的通配符的使用：extends和super

前置类

```java
class A {

}

class B extends A {

}
```

extends的使用

```java
public void extendsAndSuperTest() {
    ArrayList<? extends A> list = new ArrayList<>();
    ArrayList<A> list1 = new ArrayList<>();
    ArrayList<B> list2 = new ArrayList<>();
    ArrayList<Object> list3 = new ArrayList<>();
    //可以将A和A的子类赋值给<? extends A>
    list = list1;
    list2.add(new B());
    list = list2;
    //报错，不允许比A大的类
    //list = list3;
    //可以读取
    System.out.println(list.get(0));
    //但是无法写入，原因和通配符的原因一致
    //list.add(new A());
    //list.add(new B());
    //list.add(new Object());
    //如果将B传入给? extends A写入那么List不光可以写入B类型还可以写入A类型
    //所以这是错误的
}
```

super的使用

```java
public void extendsAndSuperTest() {
    ArrayList<? super A> list = new ArrayList<>();
    ArrayList<A> list1 = new ArrayList<>();
    ArrayList<B> list2 = new ArrayList<>();
    ArrayList<Object> list3 = new ArrayList<>();
    list = list1;
    //无法将子类放入，报错
    //list = list2;
    list3.add(new B());
    list = list3;
    //可读的，由于上界可以为Object所以读出来是Object的
    System.out.println(list.get(0));
    //可以写入A及子类
    list.add(new A());
    list.add(new B());
    //因为最大支持的类就是A，所以A的子类也可以存入
    //不可以写入父类，报错
    //list.add(new Object());
}
```

> 在代码编写时遇见extends和super，看见extends就不要写入数据，而看见super可以写入泛型参数的子类

## <div id="java-集合框架">集合框架</div>

面向对象语言对事物的体现都是以对象的形式，为了方便对多个对象的操作，就要对对象进行存储，
如果使用数组存储对象方面就会有一些弊端，而Java集合就像一种容器，可以动态的把多个对象的引用放如容器中

数组的特点和缺点

- 数组一旦初始化，其长度就是确定的
- 数组中多个元素是紧密排列的、有序的、可重复的
- 数组一旦确定类型，就不可放入其他类型
- 元素可以是基本数据类型也可以是引用数据类型

缺点

- 数组一旦初始化长度是不可变的
- 数组对于无序的不可重复的场景的多个数据就无能为力了
- 数组的方法属性极少。具体的需求都需要自己组织相关代码
- 数组的删除插入性能较差

Java集合框架体系

- java.util.Collection：存储一个一个的数据
    - 子接口：List：存储有序的、可重复的
        - ArrayList、LinkedList、Vector
    - 子接口：Set：存储无序的、不可重复的数据
        - HashSet、LinkedHashSet、TreeSet
- java.util.Map：存储一对一对的数据
    - HashMap、LinkedHashMap、TreeMap、Hashtable、Properties

Collection中的方法

```java
public void collectionTest() {
    Collection<String> collection = new ArrayList<String>();
    //添加元素
    collection.add("张三");
    //允许存放相同的元素
    collection.add("张三");
    //清空元素
    collection.clear();
    //移除元素
    boolean removed = collection.remove("张三");
    //转成数组
    Object[] array = collection.toArray();
    //是否包含此元素
    boolean contains = collection.contains("张三");
    //...
}
```

Collection中还可以使用allAll方法来添加一个集合的元素，
Collection还有一些常见的方法，例如是否为空等等

集合可以调用toArray()来转为数组，而集合可以使用Arrays.asList()静态方法来转为集合

迭代器（Iterator），在集合中所有实现类都实现了迭代器对象。
可以使用`collection.iterator()`创建一个迭代器对象，使用`iterator.next()`方法来获取下一个对象

```java
public void collectionTest() {
    Collection<String> collection = new ArrayList<String>();
    collection.add("张三");
    collection.add("李四");
    collection.add("王五");
    //获取迭代器对象
    Iterator<String> iterator = collection.iterator();
    System.out.println(iterator.next()); //张三
    System.out.println(iterator.next()); //李四
    System.out.println(iterator.next()); //王五
}
```

利用`hasNext()`方法来判断是否还有下一个

```java
public void collectionTest() {
    Collection<String> collection = new ArrayList<String>();
    collection.add("张三");
    collection.add("李四");
    collection.add("王五");
    //获取迭代器对象
    Iterator<String> iterator = collection.iterator();
    while (iterator.hasNext()) {
        System.out.println(iterator.next());
    }

    //当然也可以使用循环for，不推荐
    for (int i = 0; i < collection.size(); i++) {
        System.out.println(iterator.next());
    }
}
```

实现过Iterator接口可以发现，hasNext判断下一个元素是否存在或是否为空，
next方法获取元素并删除或更新索引在迭代器的元素

可以使用增强for循环（foreach循环）jdk5.0引入，来循环迭代器，不光可以遍历集合还可以遍历数组

```java
public void collectionTest() {
    Collection<String> collection = new ArrayList<String>();
    collection.add("张三");
    collection.add("李四");
    collection.add("王五");
    //获取迭代器
    Iterator<String> iterator = collection.iterator();
    //使用增强for循环（foreach）
    for (String s : collection) {
        System.out.println(s);
    }
}
```

使用foreach遍历数组

```java
public void foreachTest() {
    String[] strings = {"bob", "alis", "jeb"};
    for (String s : strings) {
        System.out.println(s);
    }
}
```

foreach格式

```text
for(要遍历的集合或数组的类型 临时变量 : 要遍历的集合或数组){
    //操作临时变量
}
```

需要注意的是，临时变量的更改不会影响到原来数组中的变量，但是可以更改变量引用地址内的变量

> 针对于集合来讲foreach底层还是使用的迭代器进行遍历，只是写法更简洁了

#### List

List作为子接口有一些方法是Collection没有的方法

```java
public void listTest() {
    List<String> list = new ArrayList<String>();
    list.add("张三");
    list.add("李四");
    list.add("王五");
    //根据索引获取元素
    String s = list.get(0);
    //根据元素获取索引
    int indexOf = list.indexOf("张三");
    //在指定位置添加元素
    list.add(1, "周三点五");
    //list默认实现了toString方法
    System.out.println(list); //[张三, 周三点五, 李四, 王五]
    //在指定位置添加集合中的元素
    list.addAll(2, list);
    System.out.println(list); //[张三, 周三点五, 张三, 周三点五, 李四, 王五, 李四, 王五]
    //添加集合中的元素
    list.addAll(list);
    //删除指定索引的元素
    list.remove(0);
}
```

ArrayList是List中主要的实现类，于它对应的还有Vector实现类和LinkedList实现类

Vector是一个古老的实现类在jdk1.0版本就存在了，是线程安全的，而ArrayList是线程不安全的，
因为是线程安全的所以Vector效率低一些，ArrayList和Vector底层都是使用的数组进行存储的

LinkedList底层使用的**双向链表**来存储数据，LinkedList还有一些特有方法，都是从头和尾部操作的，
删除头元素、添加头元素、获取头元素、添加尾元素等等

使用数组删除、添加指定位置效率较低但是查询较高，而链表删除、添加指定位置效率高，查询较低，
链表底层使用的引用地址进行连接下一个元素，内存间隔也不是相连的，如果删除一个元素前后元素的索引位置将重新进行指定，
不影响其他元素，如果为数组删除会牵动到后方的元素效率较低

#### Set

Set的主要的实现类是HashSet而LinkedHashSet是HashSet的子类 而HashSet底层使用的是HashMap。

HashMap底层使用**数组+单向链表+红黑树**结构进行存储，LinkedHashSet在现有的基础之上又添加了一组双向链表，
用于记录添加元素的先后顺序。即我们可以根据添加元素的循序进行遍历

```java
public void setTest() {
    HashSet<String> strings = new HashSet<>();
    strings.add("张三");
    strings.add("李四");
    strings.add("王五");
    strings.add("王五");
    //由于Set是无序的、不可重复的，所以打印的循序和添加的循序不一致
    System.out.println(strings); //[李四, 张三, 王五]
}
```

使用LinkedHashSet

```java
public void setTest() {
    LinkedHashSet<String> strings = new LinkedHashSet<>();
    strings.add("张三");
    strings.add("李四");
    strings.add("王五");
    strings.add("王五");
    //由于LinkedHashSet底层维护了一层双向链表，使用可以根据添加的循序进行打印
    System.out.println(strings); //[李四, 张三, 王五]
}
```

需要注意在Object中有一个方法叫做hashCode，此方法用于生成哈希值，
根据对象生成的哈希值放到哈希表（Map底层实现）中，这就是随机性的体现。根据hashCode来决定存放位置，
新增元素时，如果hashCode相同，判断之后发现equals不同可以进入，如果equals也相同那这个元素就不能进去了，
HashMap避免了添加一个元素还要对比所有元素是否相同

```java
class Person {
    String name;
    int age;

    @Override
    public boolean equals(Object o) {
        if (!(o instanceof Person person)) return false;
        return age == person.age && Objects.equals(name, person.name);
    }

    @Override
    public int hashCode() {
        return Objects.hash(name, age);
    }
}
```

LinkedHashSet维护了一对双向链表，虽然数据无序，但是可以根据添加的循序来放入双向链表的索引中，
所以可以根据添加的顺序进行遍历

所以比较的标准就是判断hashCode和equals

如果不重写hashCode和equals会导致元素判断不存在

没有重写hashCode和equals

```java
class Person {
    String name;
    int age;

    public Person(String name, int age) {
        this.name = name;
        this.age = age;
    }
}
```

Set打印

```java
public void setTest() {
    LinkedHashSet<Person> strings = new LinkedHashSet<Person>();
    strings.add(new Person("张三", 3));
    strings.add(new Person("张三", 3));
    //因为没有重写hashCode和equals导致无法判断是否相同
    System.out.println(strings); //[张三 3, 张三 3]
}
```

如果只存在hashCode不存在equals那么两个元素判断Object的equals方法发现引用地址不同还是会放进Set中，
所以两个都要写

```java
class Person {
    String name;
    int age;

    public Person(String name, int age) {
        this.name = name;
        this.age = age;
    }

    @Override
    public String toString() {
        return this.name + " " + this.age;
    }

    @Override
    public boolean equals(Object o) {
        if (!(o instanceof Person person)) return false;
        return age == person.age && Objects.equals(name, person.name);
    }

    @Override
    public int hashCode() {
        return Objects.hash(name, age);
    }
}
```

再次添加打印

```java
public void setTest() {
    LinkedHashSet<Person> strings = new LinkedHashSet<Person>();
    strings.add(new Person("张三", 3));
    strings.add(new Person("张三", 3));
    //因为重写hashCode和equals可以判断两个对象相同
    System.out.println(strings); //[张三 3]
}
```

看源码可以看到HashSet底层是new了一个HashMap所以可以证明Set底层使用HashMap

```java
/**
 * Constructs a new, empty set; the backing {@code HashMap} instance has
 * default initial capacity (16) and load factor (0.75).
 */
public HashSet() {
    map = new HashMap<>();
}
```

TreeSet底层使用红黑树，通过比较大小的方式进行存储

前置对象结构

```java
//没有声明Comparable
class User {
    String name;
    int age;

    public User(String name, int age) {
        this.name = name;
        this.age = age;
    }
}
```

```java
public void treeSeTest() {
    TreeSet<User> users = new TreeSet<>();
    users.add(new User("bob", 19));
}
```

由于没有声明Comparable实现所以无法比较大小，报出**ClassCastException**移除

实现Comparable并根据年龄比较

```java
class User implements Comparable<User> {
    String name;
    int age;

    public User(String name, int age) {
        this.name = name;
        this.age = age;
    }

    @Override
    public int compareTo(User o) {
        return this.age - o.age;
    }

    @Override
    public String toString() {
        return "[name=" + name + ", age=" + age + "]";
    }
}
```

再次运行

```java
public void treeSeTest() {
    TreeSet<User> users = new TreeSet<>();
    users.add(new User("bob", 19));
    users.add(new User("alis", 12));
    users.add(new User("white", 23));
    users.add(new User("jessie", 31));
    //此条不会被添加，由于Set的不可重复性
    users.add(new User("jack", 31));
    System.out.println(users);
    //[[name=alis, age=12], [name=bob, age=19], [name=white, age=23], [name=jessie, age=31]]
}
```

TreeSet不再是考虑hashCode和equals方法了，而是使用Comparable接口

#### Map

HashMap是Map主要的实现类，Hashtable是Map古老的实现类但是是线程安全的

HashMap底层使用数组+单向链表+红黑树结构存储（jdk8更改为红黑树），
而Hashtable使用数组+单向链表结构存储，
**LinkedHashMap继承HashMap**在底层维护了一个双线链表，这样就会根据添加的顺序进行遍历。
TreeMap底层使用红黑树，可以根据元素的属性的大小顺序进行遍历。
Properties的key和value都是String类型，常用来处理属性文件

```text
Key  Value
 AA = 90
 BB = 90
 CC = 61
 DD = 99
```

Map中的key是不可重复的，唯一的，所以HashSet底层使用HashMap。value是可以重复的

Map中的常用方法

添加元素：`put(key, value)`添加一个键值对

移除元素：`remove(key)`根据key移除元素

修改元素：`put(key, value)`修改元素也可以根据put方法来修改，根据key修改

获取元素：`get(key)`根据key获取value

获取长度：`size()`获取map长度

遍历，可以获取这些Key：keySet()、value：values()、entry entrySet()

```java
public void hashMapTest() {
    HashMap<Integer, String> map = new HashMap<>();
    //添加元素
    map.put(1, "bob");
    map.put(2, "alice");
    map.put(3, "jerry");
    //修改元素
    map.put(3, "jack");
    System.out.println(map); //{1=bob, 2=alice, 3=jack}
    //删除元素
    map.remove(1);
    System.out.println(map); //{2=alice, 3=jack}
    //根据key获取元素
    System.out.println(map.get(2)); //alice
    //获取长度
    System.out.println(map.size()); //2
    //遍历entry
    //循环遍历1（lambda）
    map.forEach((k, v) -> System.out.println(k + ": " + v));
    //循环遍历2（增强for）
    for (Map.Entry<Integer, String> entry : map.entrySet()) {
        System.out.println(entry.getKey() + ": " + entry.getValue());
    }
}
```

> HashMap中有一个Entry类，类中有Key和Value属性，entrySet返回就是键值对的对象

TreeMap根据Key的大小进行顺序排序

```java
public void treeMapTest() {
    TreeMap<Integer, String> map = new TreeMap<>();
    map.put(3, "three");
    map.put(1, "one");
    map.put(2, "two");
    System.out.println(map); //{1=one, 2=two, 3=three}
}
```

TreeSet和TreeMap都可以在构造方法中传入一个Comparator用来排序

Properties类是Hashtable的子类此类的主要用法就是存放配置文件信息

像这样的的键值对配置可以放到properties文件中给Properties读取

```properties
name=bob
password=123456
```

Properties类中传入一个文件流，Properties会自动获取配置文件中的Key和Value

```java
public void propertiesTest() throws IOException {
    Properties prop = new Properties();
    //创建文件读取，并抛出异常
    //传入路径
    FileReader fileReader = new FileReader("config.properties");
    prop.load(fileReader);
    prop.forEach((k, v) -> System.out.println(k + "=" + v));
}
```

**Collections**工具类，它是一个操作Set、List、Map等集合的工具类

常用方法

`reverse()`反转List中的元素顺序

```java
public void reverseTest() {
    List<Integer> list = Arrays.asList(1, 2, 3, 4, 5);
    Collections.reverse(list);
    System.out.println(list); //[5, 4, 3, 2, 1]
}
```

`shuffle()`对List集合元素进行随机排序

```java
public void shuffleTest() {
    List<Integer> list = Arrays.asList(1, 2, 3, 4, 5);
    Collections.shuffle(list);
    System.out.println(list); //[1, 5, 4, 2, 3]
}
```

`sort()`排序，使用自然排序或传入一个定制排序

```java
public void sortTest() {
    List<Integer> list = Arrays.asList(3, 5, 2, 1);
    Collections.sort(list);
    System.out.println(list); //[1, 2, 3, 5]
    //使用定制排序（lambda）
    Collections.sort(list, (o1, o2) -> o2 - o1);
    System.out.println(list); //[5, 3, 2, 1]
}
```

`swap()`交换两处元素位置

```java
public void swapTest() {
    List<Integer> list = Arrays.asList(1, 2, 3, 4);
    //交换下标2和3的位置
    Collections.swap(list, 2, 3);
    System.out.println(list); //[1, 2, 4, 3]
}
```

`max()`根据自然或定制排序获取最大值

```java
public void maxTest() {
    List<Integer> list = Arrays.asList(1, 2, 3, 4);
    System.out.println(Collections.max(list)); //4
}
```

`min()`根据自然或定制排序获取最小值

```java
public void minTest() {
    List<Integer> list = Arrays.asList(1, 2, 3, 4);
    System.out.println(Collections.min(list)); //1
}
```

`binarySearch()`在List集合中查找某个元素的下标

```java
public void binarySearchTest() {
    List<Integer> list = Arrays.asList(1, 2, 3, 4);
    //查找元素2的下标
    System.out.println(Collections.binarySearch(list, 2)); //1
}
```

`frequency()`返回指定元素在集合中出现的次数

```java
public void frequencyTest() {
    List<Integer> list = Arrays.asList(1, 2, 3, 4, 1);
    System.out.println(Collections.frequency(list, 1)); //2
}
```

`copy()`赋值集合1到集合2中

```java
public void copyTest() {
    List<Integer> src = Arrays.asList(1, 2, 3, 4);
    List<Integer> dest = Arrays.asList(0, 0, 0, 0);
    Collections.copy(dest, src);
    System.out.println(dest); //[1, 2, 3, 4]
    //注意copy的源数组不能大于目标数组否则会报错
    ArrayList<Integer> dest2 = new ArrayList<>();
    //抛出异常：java.lang.IndexOutOfBoundsException: Source does not fit in dest
    //Collections.copy(dest2, src);
    //System.out.println(dest2);
    //可以使用Arrays.asList(new Integer[10])来初始化容量
    List<Integer> dest3 = Arrays.asList(new Integer[10]);
    Collections.copy(dest3, src);
    System.out.println(dest3); //[1, 2, 3, 4, null, null, null, null, null, null]
}
```

`replaceAll()`使用新值替换List中的旧值

```java
public void replaceAllTest() {
    List<Integer> list = Arrays.asList(1, 2, 3, 4, 100);
    Collections.replaceAll(list, 100, 0);
    System.out.println(list); //[1, 2, 3, 4, 0]
}
```

`unmodifiableXxx()`返回一个不可修改的集合

```java
public void unmodifiableTest() {
    List<Integer> list = Arrays.asList(1, 2, 3, 4, 100);
    List<Integer> unmodifiableList = Collections.unmodifiableList(list);
}
```

`synchronizedList()`返回一个线程安全的集合

```java
public void synchronizedListTest() {
    List<Integer> list = Arrays.asList(1, 2, 3, 4, 100);
    List<Integer> synchronizedList = Collections.synchronizedList(list);
}
```

## <div id="java-io">IO</div>

讲IO之前先讲一下文件类（File），File类位于java.io包下，
File对象对应着操作系统的一个文件或目录

创建一个File

```java
public void fileTest() {
    File file = new File("test.txt");
    //第二种构造器，一个参数为父路径，第二个为子路径
    File file = new File("./", "test.txt");
}
```

在File的构造器中，可以传入一个**相对路径和绝对路径**

相对路径：相对当前文件夹的路径

绝对路径：从操作系统的根路径到文件的路径

> 单元测试方法的相对路径为模块下，main方法的相对路径为项目下

File常见方法

`getName()`获取名称

```java
public void getNameTest() {
    File file = new File("test.txt");
    String name = file.getName();
    System.out.println(name); //test.txt
}
```

`getPath()`获取路径

```java
public void getPathTest() {
    File file = new File("test.txt");
    String path = file.getPath();
    //由于传入的相对路径所以打印的就是传入的路径
    System.out.println(path); //test.txt
}
```

`getAbsolutePath()`获取绝对路径

```java
public void getAbsolutePathTest() {
    File file = new File("test.txt");
    String path = file.getAbsolutePath();
    System.out.println(path); //B:\Java\Afei\JavaTest\test.txt
}
```

`getAbsoluteFile()`获取绝对路径的文件

```java
public void getAbsoluteFileTest() {
    File file = new File("test.txt");
    File file1 = file.getAbsoluteFile();
    System.out.println(file1.getPath()); //B:\Java\Afei\JavaTest\test.txt
}
```

`getParent()`获取上层目录文件

```java
public void getParentTest() {
    File file = new File("test.txt");
    String fileString = file.getParent();
    //由于是相对路径所以为null
    System.out.println(fileString); //null
    //使用getAbsoluteFile
    System.out.println(file.getAbsoluteFile().getParent()); //B:\Java\Afei\JavaTest
}
```

`length()`获取文件大小（字节数）

```java
public void lengthTest() {
    File file = new File("test.txt");
    //文件内容为“hi txt”
    System.out.println(file.length()); //6
}
```

`lastModified()`获取文件最后修改的时间

```java
public void lastModifiedTest() {
    File file = new File("test.txt");
    long lastModified = file.lastModified();
    System.out.println(lastModified); //1747795017188

    Instant instant = Instant.ofEpochMilli(lastModified);
    LocalDateTime from = LocalDateTime.ofInstant(instant, ZoneId.systemDefault());
    System.out.println(DateTimeFormatter.ofLocalizedDate(FormatStyle.FULL).format(from)); //2025年5月21日星期三
}
```

`renameTo()`启动重命名文件；`mkdir()`创建文件夹（目录）

```java
public void renameToTest() {
    //必须存在
    File file = new File("test2.txt");
    //必须不存在
    //创建文件夹
    System.out.println(new File("data").mkdir()); //true
    //必须不存在
    boolean isRenameTo = file.renameTo(new File("data/test.txt"));
    System.out.println(isRenameTo); //true
}
```

`list()`返回当前file目录所有的文件或目录

```java
public void listTest() {
    File file = new File("data");
    for (String s : file.list()) {
        System.out.print(s + ";"); //config.cfg;resource;test.txt;
    }
}
```

`listFiles()`返回当前file目录所有的文件或目录的file对象

```java
public void listFilesTest() {
    File file = new File("data");
    for (File f : file.listFiles()) {
        System.out.print(f + ";"); //data\config.cfg;data\resource;data\test.txt;
    }
}
```

`exists()`判断此文件或目录是否存在

```java
public void existsTest() {
    File file = new File("data/null.txt");
    boolean exists = file.exists();
    System.out.println(exists); //false
}
```

`isDirectory()`判断此File是否是目录

```java
public void isDirectoryTest() {
    File file = new File("data");
    File file1 = new File("data/test.txt");
    System.out.println(file.isDirectory()); //true
    System.out.println(file1.isDirectory()); //false
}
```

`isFile()`判断此File是否是文件

```java
public void isFileTest() {
    File file = new File("data");
    File file1 = new File("data/test.txt");
    System.out.println(file.isFile()); //false
    System.out.println(file1.isFile()); //true
}
```

`canRead()`判断此File是否可写

```java
public void canReadTest() {
    File file = new File("data/test.txt");
    System.out.println(file.canRead()); //true
}
```

`canWrite()`判断此File是否可读

```java
public void canWriteTest() {
    File file = new File("data/test.txt");
    System.out.println(file.canWrite()); //true
}
```

`canExecute()`判断此File是否可执行（Linux系统中文件可以为可执行）

```java
public void canExecuteTest() {
    File file = new File("data/test.txt");
    System.out.println(file.canExecute()); //true
}
```

`isHidden()`判断此File是否隐藏

```java
public void isHiddenTest() {
    File file = new File("data/test.txt");
    System.out.println(file.isHidden()); //false
}
```

`createNewFile()`创建文件，若文件存在返回false

```java
public void createNewFileTest() throws IOException {
    File file = new File("data/hello.txt");
    System.out.println(file.createNewFile()); //true
}
```

`mkdir()`创建目录，若目录存在返回false，若目录父路径不存在也返回false

```java
public void mkdirTest() {
    File file = new File("data/test");
    System.out.println(file.mkdir()); //true
}
```

`mkdirs()`创建目录，若目录父路径不存在，一并创建

```java
public void mkdirsTest() {
    File file = new File("data/test/test1/test2/test3");
    System.out.println(file.mkdirs()); //true
}
```

`delete()`删除文件或目录，删除后的文件不走回收站，删除文件夹时文件夹内不能包含文件或目录

### <div id="java-常用流">常用流</div>

```java
public void deleteTest() {
    File file = new File("data/hello.txt");
    System.out.println(file.delete()); //true
}
```

I/O（Input/Output），IO技术时非常实用的技术，用于设备之间的数据传输。如读/写文件，网络通讯等

input：将外部数据（磁盘，网络等）读取到程序的内存中，

output：将程序（内存）中的数据输出到外部（磁盘，网络等）

```text
       01011001 00011011 00111001
{程序} --<--<------<----<--<----- {外部数据}
```

IO流不光传输字节，还可以传输字符。传输字节叫字节流，传输字符叫字符流，字符流以Writer和Read结尾

流还分为节点流和处理流：

节点流：直接从数据源或目的地读写数据

处理流：不直接连接到数据源或目的地，而是连接已存在的流（进行包装），对数据的处理提供更强大地读写功能

Java的IO流涉及几十个类，命名上十分规则，都是从以下的抽象基类派生的

| 抽象基类/流 | 输入流         | 输出流          |
|--------|-------------|--------------|
| 字节流    | InputStream | OutputStream |
| 字符流    | Reader      | Writer       |

由这四个类派生出来的子类名称都是以其父类名作为子类后缀名

| 分类    | 字节输入流                | 字节输出流                 | 字符输入流             | 字符输出流              |
|-------|----------------------|-----------------------|-------------------|--------------------|
| 抽象基类  | InputStream          | OutputStream          | Reader            | Writer             |
| 访问文件  | FileInputStream      | FileOutputStream      | FileReader        | FileWriter         |
| 访问数组  | ByteArrayInputStream | ByteArrayOutputStream | CharArrayReader   | CharArrayWriter    |
| 访问管道  | PipedInputStream     | PipedOutputStream     | PipedReader       | PipedWriter        |
| 访问字符串 |                      |                       | StringReader      | StringWriter       |
| 缓冲流   | BufferedInputStream  | BufferedOutputStream  | BufferedReader    | BufferedWriter     |
| 转换流   |                      |                       | InputStreamReader | OutputStreamWriter |
| 对象流   | ObjectInputStream    | ObjectOutputStream    |                   |                    |
| 装饰器流  | FilterInputStream    | FilterOutputStream    | FilterReader      | FilterWriter       |
| 打印流   |                      | PrintStream           |                   | PrintWriter        |
| 退回输入流 | PushbackInputStream  |                       | PushbackReader    |                    |
| 特殊流   | DataInputStream      | DataOutputStream      |                   |                    |

文件流的使用FileReader/FileWriter

```text
hi txt
```

```java
//异常处理：抛出异常
public void fileTest() throws IOException {
    //创建一个流
    FileReader fileReader = new FileReader("data/test.txt");
    //读出来的是int类型使用强制类型转换转换类型
    System.out.println((char) fileReader.read()); //h
    System.out.println((char) fileReader.read()); //i
    System.out.println((char) fileReader.read()); //
    System.out.println((char) fileReader.read()); //t
    System.out.println((char) fileReader.read()); //x
    System.out.println((char) fileReader.read()); //t
    //流用完需要关闭操作，否则导致流的内存泄露
    fileReader.close();
}
```

read方法的文档中写“读取字符，如果到达流的末尾则返回-1”  
**The character read, or -1 if the end of the stream has been reached**  
如果达到文件末尾则返回-1，可以根据返回值进行判断是否读取文件末尾

```java
public void fileTest() throws IOException {
    //创建一个流
    FileReader fileReader = new FileReader("data/test.txt");
    int c;
    while ((c = fileReader.read()) != -1) {
        //使用不换行打印
        System.out.print((char) c); //hi txt
    }
    //流用完需要关闭操作，否则导致流的内存泄露
    fileReader.close();
}
```

在项目中通常不会使用上面的写法，上面并没有做异常处理且每次与磁盘交互只交互一个字节，
导致性能底下。交互时传入一个数组，read方法会返回读取数组的长度

```java
public void fileTest() throws IOException {
    FileReader fileReader = null;
    //read后读取的长度
    int length;
    //声明数组长度（可以称为数组缓存长度）
    char[] buffer = new char[1024];
    try {
        fileReader = new FileReader("data/test.txt");
        //只要数组大于0就代表还有内容
        while ((length = fileReader.read(buffer)) > 0) {
            //打印
            for (int i = 0; i < length; i++) {
                System.out.print(buffer[i]);
            } //hi txt
        }
    } catch (IOException e) {
        System.out.println(e.getMessage());
    } finally { //将close放入finally保证成功或者失败都会执行
        //文件可能不存在所以要判断是否为null
        if (fileReader != null) fileReader.close();
    }
}
```

输出流和输入流类似，输出流可以不需要文件的存在

```java
public void fileTest() throws IOException {
    //初始化流
    FileWriter fileWriter = null;
    try {
        //如果文件不存在将会创建文件
        fileWriter = new FileWriter("data/test2.txt");
        //可指定文件是否追，默认不追加，覆盖之前的内容
        //fileWriter = new FileWriter("data/test2.txt", true);
        //写出一行字
        fileWriter.write("Hello World\n");
        fileWriter.write("你好吗\n");
        fileWriter.write("最近怎么样\n");
    } catch (IOException e) {//异常处理
        System.out.println(e.getMessage());
    } finally {
        //close处理
        if (fileWriter != null) fileWriter.close();
    }
}
```

FileReader / FileWriter 使用的执行步骤：  
创建读取或写出的File类的对象，创建输入流和输出流，具体的写入写出过程，关闭流操作防止资源泄露

字节流的使用 FileInputStream / FileOutputStream

在电脑上每1个bit等于1位，8个bit等于一个字节，所有的文件都是以字节存储的，
不光可以操作文本，还可以操作图片、视频、安装包等等，可以实现复制和传输操作

操作一张图片，复制到另一个路径中

```java
public void imgTest() {
    //创建文件输入流和输出流
    FileInputStream fileInputStream = null;
    FileOutputStream fileOutputStream = null;

    try {
        //创建对象
        fileInputStream = new FileInputStream("data/image/img.png");
        fileOutputStream = new FileOutputStream("data/resource/img-copy.png");

        //声明每次交互的容量
        byte[] buffer = new byte[1024];
        //声明每次读取的长度
        int length;
        //循环操作
        while ((length = fileInputStream.read(buffer)) > 0) {
            //写出操作
            fileOutputStream.write(buffer, 0, length);
        }
        System.out.println("复制成功");

    } catch (Exception e) {
        //异常处理
        System.out.println(e.getMessage());
    } finally {
        //关闭操作
        try {
            if (fileInputStream != null) fileInputStream.close();
        } catch (IOException e) {
            System.out.println(e.getMessage());
        }
        try {
            if (fileOutputStream != null) fileOutputStream.close();
        } catch (IOException e) {
            System.out.println(e.getMessage());
        }
    }
}
```

**编程技巧**：看到这么多异常处理结构可读性会直线下降，可以封装一个异常处理方法进行异常处理

```java
//try块的函数
interface CatchInterface {
    void invoke() throws Exception;
}

//catch块的函数
interface ErrorInterface {
    void invoke(Exception e);
}

//finally块的函数
interface FinallyInterface {
    void invoke();

}

//字段，用于lambda表达式中的更改属性
class Field<T> {
    public T field;
}


public class CatchingTest {
    //包含finally的try-catch
    static void catchingFinally(CatchInterface c, ErrorInterface e, FinallyInterface f) {
        try {
            c.invoke();
        } catch (Exception exception) {
            e.invoke(exception);
        } finally {
            f.invoke();
        }
    }

    //不包含finally的try-catch
    static void catching(CatchInterface c, ErrorInterface e) {
        try {
            c.invoke();
        } catch (Exception exception) {
            e.invoke(exception);
        }
    }
}
```

使用封装的catting类

```java
public void testCatting() {
    Field<FileInputStream> fileInputStreamField = new Field<>();
    Field<FileOutputStream> fileOutputStreamField = new Field<>();

    catchingFinally(() -> {
        fileInputStreamField.field = new FileInputStream("data/image/img.png");
        fileOutputStreamField.field = new FileOutputStream("data/resource/img-copy.png");

        byte[] buffer = new byte[1024];
        int length;

        while ((length = fileInputStreamField.field.read(buffer)) > 0) {
            fileOutputStreamField.field.write(buffer, 0, length);
        }

        System.out.println("操作成功");
    }, e -> System.out.println(e.getMessage()), () -> {
        catching(() -> {
            if (fileOutputStreamField.field != null) fileOutputStreamField.field.close();
        }, e -> System.out.println(e.getMessage()));

        catching(() -> {
            if (fileInputStreamField.field != null) fileInputStreamField.field.close();
        }, e -> System.out.println(e.getMessage()));
    });
}
```

> 相比之前的try-catch封装的catching语法更简洁，操作更优雅，需要使用此方法需要一些lambda表达式知识  
> 这种封装在需要大量重复异常处理逻辑的项目中会很有用，但也要注意不要过度封装，因为Java本身的异常处理机制已经很清晰了


节点流，（文件流）FileWriter、FileInputStream...可以使用四个处理流进行包装（缓冲流）BufferedInputStream、BufferWriter...

缓冲流的作用：提升文件的读写效率，例如BufferReader可以一次读一行

BufferInputStream / BufferInputStream 中里面有一个默认的缓存其大小为8192字节，
如果你给传输中的buffer字节数组分配的大小为8192其实和BufferInputStream是差不多的

使用 BufferReader

```text
hi txt
hello Java
hi Scala
hello Kotlin
```

```java
public void bufferTest() {
    Field<FileReader> fileReaderField = new Field<>();
    Field<BufferedReader> bufferedReaderField = new Field<>();

    catchingFinally(() -> {
        fileReaderField.field = new FileReader("data/test.txt");
        bufferedReaderField.field = new BufferedReader(fileReaderField.field);

        String line;
        while ((line = bufferedReaderField.field.readLine()) != null) {
            System.out.println(line);
            // hi txt
            // hello Java
            // hi Scala
            // hello Kotlin
        }

    }, e -> System.out.println(e.getMessage()), () -> {
        //先关闭外部流
        catching(() -> {
            if (bufferedReaderField.field != null) bufferedReaderField.field.close();
        }, e -> System.out.println(e.getMessage()));
        //再关闭内部流
        catching(() -> {
            if (fileReaderField.field != null) fileReaderField.field.close();
        }, e -> System.out.println(e.getMessage()));
    });
}
```

读取文本文件时，不同的编码语言可能会导致乱码，可以在Reader的第二个参数指定字符编码

`new FileReader("data/test.txt", StandardCharsets.UTF_8);`

处理流：转换流，将字节流和字符流进行转换

使用InputStreamReader，将字节流转成字符流，OutputStreamWriter将一个输出的字节流转成字符流

```java
public void streamTest() {
    Field<FileInputStream> fileInputStreamField = new Field<>();
    Field<InputStreamReader> inputStreamReaderField = new Field<>();
    catchingFinally(() -> {
        fileInputStreamField.field = new FileInputStream("data/test2.txt");
        //第二个参数还可以指定字符集
        inputStreamReaderField.field = new InputStreamReader(fileInputStreamField.field, StandardCharsets.UTF_8);
        char[] buffer = new char[1024];
        int len;
        while ((len = inputStreamReaderField.field.read(buffer)) != -1) {
            System.out.print(new String(buffer, 0, len));
        }

    }, e -> System.out.println(e.getMessage()), () -> {
        catching(() -> {
            if (fileInputStreamField.field != null) fileInputStreamField.field.close();
        }, e -> System.out.println(e.getMessage()));
        catching(() -> {
            if (inputStreamReaderField.field != null) inputStreamReaderField.field.close();
        }, e -> System.out.println(e.getMessage()));
    });
}
```

OutputStreamWriter流的使用

```java
public void streamTest() {
    Field<FileOutputStream> fileOutputStreamField = new Field<>();
    Field<OutputStreamWriter> outputStreamWriterField = new Field<>();
    catchingFinally(() -> {
        fileOutputStreamField.field = new FileOutputStream("data/test2.txt");
        outputStreamWriterField.field = new OutputStreamWriter(fileOutputStreamField.field, StandardCharsets.UTF_8);

        outputStreamWriterField.field.write("你还在吗？\n");
        outputStreamWriterField.field.write("下午好呀\n");
        outputStreamWriterField.field.write("hi!\n");
        //刷新操作
        outputStreamWriterField.field.flush();
    }, e -> System.out.println(e.getMessage()), () -> {
        catching(() -> {
            if (fileOutputStreamField.field != null) fileOutputStreamField.field.close();
        }, e -> System.out.println(e.getMessage()));
        catching(() -> {
            if (outputStreamWriterField.field != null) outputStreamWriterField.field.close();
        }, e -> System.out.println(e.getMessage()));
    });
}
```

对象流的使用以及对象的序列化机制，如果要将一个对象进行存储，那么应该怎么办呢。我们可以将一个对象的数据拆开来进行存储，
我们也可以对对象进行序列化操作，序列化就像是一个物品分解成积木一样，到使用的时候还能还原出来，还原的过程叫做反序列化

Java提供了数据流和对象流来处理数据，数据流对象只能处理基本数据类型 DataInputStream / DataOutputStream

对象流：ObjectInputStream / ObjectOutputStream ，要使用对象流的对象必须实现序列化接口，否则无法进行序列化

```java
//没有实现序列化接口
class Pen {
    String color;
    int length;
    Boolean hasEraser;

    public Pen(String color, int length, Boolean hasEraser) {
        this.color = color;
        this.length = length;
        this.hasEraser = hasEraser;
    }
}
```

使用ObjectOutputStream

```java
//没有进行异常处理
public void ObjectStreamTest() throws IOException {
    //创建对象
    Pen pen = new Pen("red", 10, true);
    ObjectOutputStream objectOutputStream = new ObjectOutputStream(System.out);
    objectOutputStream.writeObject(pen); //报错NotSerializableException，没有实现序列化接口
    objectOutputStream.flush();
    objectOutputStream.close();
}
```

实现序列化接口

```java
class Pen implements java.io.Serializable {

    // 实现序列化必须声明一个变量名为 serialVersionUID 的全局常量，
    // 此long值代表此对象的版本号，如果序列化和反序列化的版本号不正常,
    // 会导致前后结果不一致
    @Serial
    private static final long serialVersionUID = 1L;


    String color;
    int length;
    Boolean hasEraser;

    public Pen(String color, int length, Boolean hasEraser) {
        this.color = color;
        this.length = length;
        this.hasEraser = hasEraser;
    }
}
```

再次打印序列化结果

```java
public void ObjectStreamTest() {
    //创建对象
    Pen pen = new Pen("red", 10, true);
    Field<ObjectOutputStream> objectOutputStreamField = new Field<>();
    catchingFinally(() -> {
        //传入一个终端作为输出流
        objectOutputStreamField.field = new ObjectOutputStream(System.out);
        //写入到System.out流中，也就是控制台中
        objectOutputStreamField.field.writeObject(pen);
        //刷新写入数据
        objectOutputStreamField.field.flush();
    }, e -> System.out.println(e.getMessage()), () -> {
        catching(() -> {
            // 注意：此流会关闭控制台的流，导致无法接受到终端的打印
            // 处理流会关闭节点流，但是为了安全起见，通常建议先关闭外流再关闭内流
            if (objectOutputStreamField.field != null) objectOutputStreamField.field.close();
        }, e -> System.out.println(e.getMessage()));
    });
}
```

序列化并反序列化

```java
public void ObjectStreamTest() {
    //创建对象
    Pen pen = new Pen("red", 10, true);
    //创建输出流（序列化）
    Field<FileOutputStream> fileOutputStreamField = new Field<>();
    Field<ObjectOutputStream> objectOutputStreamField = new Field<>();

    catchingFinally(() -> {
        fileOutputStreamField.field = new FileOutputStream("data/pen1.txt");
        objectOutputStreamField.field = new ObjectOutputStream(fileOutputStreamField.field);

        objectOutputStreamField.field.writeObject(pen);
    }, e -> System.out.println(e.getMessage()), () -> {
        catching(() -> {
            if (objectOutputStreamField.field != null) objectOutputStreamField.field.close();
        }, e -> System.out.println(e.getMessage()));
        catching(() -> {
            if (fileOutputStreamField.field != null) fileOutputStreamField.field.close();
        }, e -> System.out.println(e.getMessage()));
    });

    //创建输入流（反序列化）
    Field<FileInputStream> fileInputStreamField = new Field<>();
    Field<ObjectInputStream> objectInputStreamField = new Field<>();

    catchingFinally(() -> {
        fileInputStreamField.field = new FileInputStream("data/pen1.txt");
        objectInputStreamField.field = new ObjectInputStream(fileInputStreamField.field);

        //进行类型转换
        Pen pen1 = (Pen) objectInputStreamField.field.readObject();

        System.out.println(pen1.color);
    }, e -> System.out.println(e.getMessage()), () -> {
        catching(() -> {
            if (fileInputStreamField.field != null) fileInputStreamField.field.close();
        }, e -> System.out.println(e.getMessage()));
        catching(() -> {
            if (objectInputStreamField.field != null) objectInputStreamField.field.close();
        }, e -> System.out.println(e.getMessage()));
    });
}
```

> 如果序列化的值和反序列化的值不一致会报出异常

其他流的使用：

System.in：标准的键盘输入流（控制台输入的字符都会进这个流）
System.out：标准的输出流（控制台输出的数据就是这个流写出的数据）
System.err：输出错误的内容到控制台

在System中可以设置这些流，分别为setIn()、setOut()、setErr()

打印流的使用

```java
public void systemTest() {
    Field<FileOutputStream> fileOutputStreamField = new Field<>();
    Field<PrintStream> printStreamField = new Field<>();

    //拿到控制台输出流（为了之后使用控制台）
    PrintStream console = System.out;

    catchingFinally(() -> {
        fileOutputStreamField.field = new FileOutputStream("data/print.txt");
        printStreamField.field = new PrintStream(fileOutputStreamField.field);
        //设置系统的输出流
        System.setOut(printStreamField.field);

        //下方内容输出到文件中
        System.out.println("你好哈哈！");
        //下方输出到控制台
        console.println("在吗？");
    }, e -> console.println(e.getMessage()), () -> {
        catching(() -> {
            if (printStreamField.field != null) printStreamField.field.close();
        }, e -> console.println(e.getMessage()));
        catching(() -> {
            if (fileOutputStreamField.field != null) fileOutputStreamField.field.close();
        }, e -> console.println(e.getMessage()));
    });
}
```

### <div id="java-网络编程">网络编程</div>

Java是Internet上的语言，它从语言上提供了对网络应用程序的支持，程序员能够很容易开发常见的网络应用程序

Java提供的的网络类库，可以实现无痛的网络连接，联网的底层细节被隐藏在Java的本机安装系统里，由JVM进行控制。
并且Java实现了一个跨平台的网络库，程序员面对的是一个统一的网络编程环境

C/S架构：全称为Client/Server结构，是指客户端结构和服务端结构

B/S架构：全称为Browser/Server结构，是指浏览器喝服务端结构

这些都是通过网络实现的，实现网络传输的三个要素：

使用IP地址，精准定位网络上的主机、使用端口号，精准定位主机上特定的应用程序、规范网络通信协议

IP地址：指的是互联网协议地址（Internet Protocol Address），俗称IP。
IP地址用来给网络中的一台计算机设备做唯一的编号

> 假如我们把个人电脑比作“电话”的话，那么IP地址就相当于“电话号码”

IPv4：是一个32位的二进制数，通常被分为4个字节，表示成**b1.b2.b3.b4**的形式，每个字节以十进制表示，
例如192.168.65.100。其中b1.b2.b3.b4都是0~255之间的十进制整数。万维网还分为两类地址：
公网地址和局域网地址（通常以192.168开头），其中127.0.0.1还代表本机地址

便捷地记录IP地址：域名，例如www.baidu.com域名就是包装后的IP地址，其中引用的还是IP地址

通信要素2：端口号

网络的通信，本质上是两个进程的通信。每台计算机有很多进程，那么在网络通信中可以使用端口号就可以标识设备中唯一的进程。
不同的进程，只能设置不同的端口号

端口的取值范围为0~65535，端口分为三类端口分别为：

- 公认端口：0~1023。被预先定义的服务通信占用，如HTTP的80、FTP的21、SSH的22、Telnet的23
- 注册端口：1024~49151。分配给用户进程或应用程序。如Tomcat的8080，MySQL的3306、Oracle的1521
- 动态端口：49152~65535。

通信要素3：网络通信协议

通过计算机网络可以使多台计算机实现连接，位于同一个网络中的的计算机在进行连接和通信是需要遵守一定的规则，
好比汽车在道路行驶中的规则

网络通信协议：在计算机网络中，这些连接和通信的规则被称为网络通信协议，
它对数据的传输格式、速率、步骤、出错控制等做了统一规定，通信双方必须同时遵守才能完成数据交换

网络参考模型
OSI参考模型：将网络分为7层，过于理想化，没有实施起来  
TCP/IP参考模型：将网络分为4层：应用层、传输层、网络层、物理+数据链路层。事实上使用的标准

InetAddress：一个InetAddress对象代表一个IP地址

Socket（套接字）是IP地址和端口一起构成唯一能识别的标识符套接字（Socket）。
通信的两端都要有Socket，是两台机器通信的端点。
Socket允许程序把网络连接当成一个流，数据在两个Socket间通过IO传输。
Socket分为ServerSocket（此类实现TCP服务器套接字）和Socket（此类实现客户端套接字）。
数据报套接字（DatagramSocket此类实现UDP数据报包的套接字）

TCP协议：

- TCP协议进行通信的两个应用程序：客户端、服务端
- 使用TCP协议前，须先建立TCP连接，形成基于字节流的传输数据通道
- 传输前，采用“三次握手”方式，点对点通信，是可靠的，TCP一方发送一个消息给另一个通信实体后，需要收到另一个通信实体确认信息，如果没收到就会重发信息
- 在连接中可进行大数据量的传输
- 传输完毕，需释放已建立的连接，效率低

> 流程：服务端开启ServerSocket -> 客户端连接服务端的Socket -> 此时服务端和客户端都可以获取对方的流

```java
public class SocketTest {
    @Test
    public void server() {
        ServerSocket serverSocket = null;
        InputStreamReader inputStreamReader = null;
        BufferedReader bufferedReader = null;

        try {
            //创建Socket服务器对象
            serverSocket = new ServerSocket(33393);
            //此方法会阻塞线程等待连接此Socket并返回一个Socket对象（即连接方的对象）
            Socket socket = serverSocket.accept();
            System.out.println("已有远程地址连接此服务器：" + socket.getRemoteSocketAddress());
            //获取连接方发送的信息并转为String
            inputStreamReader = new InputStreamReader(socket.getInputStream());
            bufferedReader = new BufferedReader(inputStreamReader);
            //打印消息
            System.out.println("连接方发送的消息：" + bufferedReader.readLine());

            //异常处理与流的关闭
        } catch (IOException e) {
            throw new RuntimeException(e);
        } finally {
            try {
                if (serverSocket != null) serverSocket.close();
            } catch (IOException ignored) {
            }
            try {
                if (bufferedReader != null) bufferedReader.close();
            } catch (IOException ignored) {
            }
            try {
                if (inputStreamReader != null) inputStreamReader.close();
            } catch (IOException ignored) {
            }
        }
    }

    @Test
    public void client() {
        Socket socket = null;
        OutputStreamWriter outputStreamWriter = null;
        //打印流（此流发送的是字符串）
        PrintWriter printWriter = null;

        try {
            //创建客户端对象连接服务端地址
            //可以直接传入端口和地址，也可以创建InetAddress对象传入
            socket = new Socket("127.0.0.1", 33393);
            //获取输出流
            outputStreamWriter = new OutputStreamWriter(socket.getOutputStream());
            //包装成打印流
            printWriter = new PrintWriter(outputStreamWriter);
            //发送一行消息
            printWriter.println("你好呀");
            //刷新流，直接发送
            printWriter.flush();
        } catch (Exception e) {
            throw new RuntimeException(e);
        } finally {
            try {
                if (socket != null)
                    socket.close();
            } catch (IOException ignored) {
            }
            try {
                if (outputStreamWriter != null)
                    outputStreamWriter.close();
            } catch (IOException ignored) {
            }
            if (printWriter != null)
                printWriter.close();
        }
    }
}
```

UDP协议：

- UDP协议进行通信的两个应用程序：发送端、接收端
- 将数据、源、目的封装成数据包（基本的传输单位），不需要建立连接
- 发送方不管对方是否准备好，接收方收到也不确认，不能保证数据的完整性，故是不可靠的
- 每个数据报??的大小限制64k内
- 发送数据报结束时无法释放资源，开销小，通信效率高，可靠性差
- 适用场景：音频视频和普通的数据的传输。例如视频会议

```java
public class DataSocketTest {
    @Test
    public void receiver() {
        DatagramSocket socket = null;
        try {
            //创建接收对象
            socket = new DatagramSocket(33393);
            //一个用来接收的数据报
            DatagramPacket packet = new DatagramPacket(new byte[1024 * 64], 1024 * 64);
            //等待接收，会阻塞线程
            socket.receive(packet);
            //接收之后将字节数组打印为字符串
            System.out.println(new String(packet.getData(), 0, packet.getLength()));

            //异常处理
        } catch (IOException e) {
            throw new RuntimeException(e);
        } finally {
            if (socket != null) socket.close();
        }
    }

    @Test
    public void sender() {
        DatagramSocket socket = null;
        try {
            //创建发送对象
            socket = new DatagramSocket();
            //一个用来发送的数据报，并将字符串传入进去
            byte[] bytes = "你好UDP".getBytes();
            DatagramPacket packet = new DatagramPacket(
                    bytes,
                    bytes.length,
                    InetAddress.getByName("127.0.0.1"),
                    33393);
            //发送数据报
            socket.send(packet);
            //接收之后将字节数组打印为字符串

            //异常处理
        } catch (IOException e) {
            throw new RuntimeException(e);
        } finally {
            if (socket != null) socket.close();
        }
    }
}
```

URL（Uniform Resource Locator）：统一资源操作符

URL是互联网上一个资源的地址，格式为：

```text
http://xxxxxxxxxxxxxx:8080/xxxxxxx/index.html?name=tom
应用层协议 IP地址或者域名 端口  资源地址     资源和参数
```

URL类的使用

```java
//异常处理：向上抛出
public void urlTest() throws IOException {
    URL url = new URL("http://www.bilibili.com");
    //获取连接
    URLConnection urlConnection = url.openConnection();
    //包装连接流
    BufferedReader bufferedReader = new BufferedReader(new InputStreamReader(urlConnection.getInputStream()));
    //打印消息
    String line;
    while ((line = bufferedReader.readLine()) != null) {
        System.out.println(line);
    }
}
```

## <div id="java-反射">反射</div>

Java程序中，所有对象都有两种类型：编译时类型和运行时类型，而很多时候对象的编译时类型和运行时类型不一致

反射（Reflection）是被视为动态语言的关键，反射机制允许程序在运行期间借助于ReflectionAPI取得任何类的内部信息，
并能直接操作任意对象的内部属性及方法

在加载完类之后，在堆内存的方法区中就产生了一个Class类型的对象（一个类只有一个Class对象），
这个对象就包含了完整的类的结构信息。这个对象就像一面镜子，透过这个镜子看到类的结构，所以，我们形象的称之为：反射

反射的基本用法：

前置对象

```java
class Person {
    //对象的两个字段
    private String name;
    private int age;

    //私有构造器
    private Person() {

    }

    public Person(String name, int age) {
        this.name = name;
        this.age = age;
    }

    public void show() {
        System.out.println("你好我是：" + name + "，我的年龄是：" + age);
    }

    //私有的方法
    private void sayHello(String name2) {
        System.out.println("你好我是：" + name + "。你好，" + name2);
    }

    @Override
    public String toString() {
        return "Person{" +
                "name='" + name + '\'' +
                ", age=" + age +
                '}';
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        this.age = age;
    }
}
```

使用反射：

使用声明的构造器创建对象：

```java
public void constructorTest() throws NoSuchMethodException, InvocationTargetException, InstantiationException, IllegalAccessException {
    //获取Person类
    Class<Person> personClass = Person.class;

    //获取到空参的构造器
    Constructor<Person> declaredConstructor = personClass.getDeclaredConstructor();
    //由于空参构造器是私有的需要设置访问权限
    declaredConstructor.setAccessible(true);
    //创建对象
    Person person = declaredConstructor.newInstance();
    System.out.println(person); //Person{name='null', age=0}

    //使用有参构造函数，需要传入形参类型
    Constructor<Person> declaredConstructor1 = personClass.getDeclaredConstructor(String.class, int.class);
    //由于是公开的所以不用设置访问权限
    //创建对象
    Person person1 = declaredConstructor1.newInstance("bob", 18);
    System.out.println(person1); //Person{name='bob', age=18}
}
```

获取对象并使用反射赋值：

```java
public void fieldTest() throws NoSuchFieldException, IllegalAccessException {
    //一个对象
    Person person = new Person("alice", 18);
    //获取Person类
    Class<Person> personClass = Person.class;
    //获取声明的字段
    Field field = personClass.getDeclaredField("age");
    //设置字段的访问权限
    field.setAccessible(true);
    //设置对象值
    field.set(person, 30);
    System.out.println(person); //Person{name='alice', age=30}
}
```

获取对象并调用声明的方法：

```java
public void MethodTest() throws NoSuchMethodException, InvocationTargetException, IllegalAccessException {
    //一个对象
    Person person = new Person("alice", 18);
    //获取Person类
    Class<Person> personClass = Person.class;
    //获取声明的方法
    Method showMethod = personClass.getDeclaredMethod("show");
    //调用
    showMethod.invoke(person); //你好我是：alice，我的年龄是：18

    //调用私有有参方法
    Method sayHelloMethod = personClass.getDeclaredMethod("sayHello", String.class);
    //设置访问权限
    sayHelloMethod.setAccessible(true);
    //调用方法，并传入值
    sayHelloMethod.invoke(person, "Bob"); //你好我是：alice。你好，Bob
}
```

> 你可能会像，我为什么不直接调用呢？反射更多适用于框架和高度自定义的系统中，使用反射会让你的开发效率高不少。
> 例如之后学习的dao层，对数据库操作的dao层很适合用反射来写

反射体现了动态性，可以在运行时动态的获取对象所属的类，动态的调用相关方法。所以在设计框架时会使用大量的反射