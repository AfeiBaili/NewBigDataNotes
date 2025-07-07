- # <a href="#scala">Scala</a>
    - ## <a href="#scala-初出茅庐">初出茅庐</a>
        - ### <a href="#scala-环境搭建">环境搭建</a>
        - ### <a href="#scala-首次运行">首次运行</a>
        - ### <a href="#scala-变量">变量</a>
        - ### <a href="#scala-标识符">标识符</a>
        - ### <a href="#scala-关键字">关键字</a>
        - ### <a href="#scala-字符串">字符串</a>
        - ### <a href="#scala-常用类">常用类</a>
    - ## <a href="#scala-渐入佳境">渐入佳境</a>
        - ### <a href="#scala-数据类型">数据类型</a>
        - ### <a href="#scala-运算符">运算符</a>
        - ### <a href="#scala-流程控制">流程控制</a>
        - ### <a href="#scala-函数式编程">函数式编程</a>
    - ## <a href="#scala-炉火纯青">炉火纯青</a>
        - ### <a href="#scala-高阶函数">高阶函数</a>
        - ### <a href="#scala-闭包与柯里化">闭包与柯里化</a>
        - ### <a href="#scala-递归">递归</a>
        - ### <a href="#scala-包">包</a>
        - ### <a href="#scala-类">类</a>
        - ### <a href="#scala-继承">继承</a>
        - ### <a href="#scala-抽象类">抽象类</a>
        - ### <a href="#scala-单例对象">单例对象</a>
        - ### <a href="#scala-apply">apply</a>
        - ### <a href="#scala-特质">特质</a>
        - ### <a href="#scala-类型检查和转换">类型检查和转换</a>
        - ### <a href="#scala-枚举类和应用类">枚举类和应用类</a>
    - ## <a href="#scala-登峰造极">登峰造极</a>
        - ### <a href="#scala-集合">集合</a>
            - ### <a href="#scala-数组">数组</a>
            - ### <a href="#scala-列表">列表</a>
            - ### <a href="#scala-集">集</a>
            - ### <a href="#scala-映射">映射</a>
        - ### <a href="#scala-元组">元组</a>
        - ### <a href="#scala-集合函数">集合函数</a>
        - ### <a href="#scala-队列">队列</a>
        - ### <a href="#scala-模式匹配">模式匹配</a>
        - ### <a href="#scala-异常处理">异常处理</a>
        - ### <a href="#scala-隐式转换">隐式转换</a>
        - ### <a href="#scala-泛型">泛型</a>

# <div id="scala">Scala</div>

学习大数据离不开的一个框架就是Spark，Spark是新一代内存级大数据计算框架，是大数据的重要内容。
Spark是由Scala，学习Spark要先学习Scala

Scala的历史，联邦理工学院的马丁·奥德斯基（Martin Odersky）于2001年开始设计Scala。
他是编程狂热爱好者，长时间的编程后，希望发明一种语言，能够让写程序这样的基础工作变得高效且简单。
当他接触到Java后，对Java这门便携式、运行在JVM且存在垃圾回收的语言产生了极大的兴趣，
所以决定将函数式编程语言的特点融合到Java中，由此发明了两种语言（Pizza和Scala）。
Pizza和Scala极大的推动了java编程语言的发展，JDK5.0的泛型、增强for循环、自动类型转换等，都是从Pizza引入的新特性。
JDK8.0的类型判断、Lambda表达式是从Scala中引入的特性。

## <div id="scala-初出茅庐">初出茅庐</div>

编写Java代码时候我们的引入的JDK类库，使用javac对源代码进行编译然后再到JVM运行。而Scala的运行逻辑是，
先引入JDK类库 -> 引入Scala类库 -> 使用scalac编译Scala源代码 -> 运行在JVM中。

## <div id="scala-环境搭建">环境搭建</div>

scala的Sdk要先保证电脑上存在Jdk，可以从[Scala](https://www.scala-lang.org/download/all.html)的官网上下载建议下载版本2.12.11版本，
2.12版本是众多框架使用的版本

下载Zip格式的文件需要将Scala解压然后复制Scala里的目录，在环境变量处新建一条，变量名为**SCALA_HOME**，
然后点击**Path**在里面也新建一条，为**%SCALA_HOME%\bin**，这样就配置好了，
你也可以为你的电脑配置一个JAVA_HOME推荐配置一下，配置完之后打开命令终端输入scala以检查是否配置成功

## <div id="scala-首次运行">首次运行</div>

如果在idea中编写Scala语言需要下载一个Scala插件，在scala中文件声明一个伴生对象名叫`object`然后跟上办上对象的名字和括号就是它的作用域，
声明一个方法的关键字为`def`然后跟上方法名（函数名，在Scala中函数比方法更合适），方法名后面跟上形参列表，Scala中声明类型是先声明变量名，
再声明类型，关于这个原因我听到的是，在阅读代码中，把变量名放到较前的位置更好观察和查找，参数名声明之后跟上`Array`
类型，在Scala中是没有基本数据类型的，
因为Scala是一个全部面向对象的语言，在Array类型后面要跟上泛型用方括号表示泛型类型`[]`泛型里面填入String代表一个String类型的数组，
在括号后面跟上一个冒号表示此函数的返回值类型，main方法不需要返回值，所以返回值类型为`Unit`代表返回值为空，类型后面跟上一个等号，
此等号就像是数学中的函数一样，等号后面就是此函数的作用域了，**如果此函数只有一行代码，大括号也可以省略**

```scala
object Main {
    def main(args: Array[String]): Unit = {
        println("hello world")
    }

    //也可以这样写
    def main(args: Array[String]): Unit = println("hello world")
}
```

> object声明出的是伴生对象，那它与谁相伴相生呢？答案是与class相伴相生

> Scala的分号也可以省略，可以少敲一个字

声明一个class和object，object像是一个单例模式，里面的内容都是静态的，内存中也只有一份

```scala
//声明类
class Student(name: String, age: Int) {
    def printlnInfo(): Unit = println(this.name + "=" + this.age + ":" + Student.school)
}

//声明伴生类
object Student {
    val school: String = "shanfu";

    def main(args: Array[String]): Unit = {
        val bob = new Student("bob", 18)
        val alex = new Student("alex", 19)

        bob.printlnInfo()
        alex.printlnInfo()
    }
}

```

## <div id="scala-注释">注释</div>

在Scala中注释和Java完全一致推荐查看<a href="#java-注释">Java的注释笔记</a>

## <div id="scala-变量">变量</div>

在Scala中声明一个常量和变量是用两个不同的关键字，而不是像Java一样声明了一个变量还要加一个final来表示这是一个常量，
Scala的思想是常量和变量应该是同级的，声明常量的关键词叫`val`对应着英文value，变量的关键字叫`var`对应着英文的variable

```scala
object Demo {
    val a: Int = 10

    //如果变量的值可以推断就可以省略声明类型
    val a = 10

    //声明var变量
    var b = 10
}
```

> 如果可以使用常量就不要使用变量，因为在函数式编程中，你从数学的意义上定义了一个值`a = 10`那么它的值就不应该随意更改

## <div id="scala-标识符">标识符</div>

Scala中很多东西都是Java中存在的，使用标识符的声明也和Java差不多，但还是有些区别的要不然这段话也不会出现

1. 以字母和下划线开头，后接字母、数字、下划线
2. 以操作符开头，且只能包含操作符号（Scala经常使用+-*/作为函数名）
3. 使用反引号``可以包含关键字

## <div id="scala-关键字">关键字</div>

很多关键字都和Java相同，但有多出来的关键字是Java中没有的，也会有被替换名字但是意思大致相同的关键字，我会列出来Scala常用关键字及对应的介绍

| 关键字       | 功能                 |
|-----------|--------------------|
| package   | 声明包位置              |
| import    | 导入包                |
| class     | 声明类                |
| object    | 声明伴生对象             |
| trait     | 同Java接口，声明一个特征     |
| extends   | 继承                 |
| with      | 类似implement，但有部分区别 |
| type      | 给类型声明一个别名          |
| for       | 声明for循环            |
| yield     | 返回for的集合           |
| private   | 权限修饰符，私有的          |
| protected | 权限修饰符，可被子类继承访问     |
| abstract  | 声明抽象类              |
| final     | 修饰类和方法，最终的         |
| implicit  | 隐式的                |
| overwrite | 重写方法               |
| try       | 异常处理，捕捉            |
| catch     | 异常处理，捕捉异常          |
| finally   | 异常处理，必须执行的         |
| throw     | 抛出异常               |
| if        | 条件判断               |
| else      | 分支处理               |
| match     | 模式匹配               |
| do        | 配合while            |
| while     | while循环            |
| return    | 返回值                |
| def       | 定义方法（函数）           |
| val       | 声明常量               |
| var       | 声明变量               |
| this      | 本对象                |
| super     | 父类对象               |
| new       | 创建一个对象             |
| true      | 布尔类型，真             |
| false     | 布尔类型，假             |
| null      | 空                  |
| lazy      | 惰性加载               |

## <div id="scala-字符串">字符串</div>

Scala的字符串相比Java多出了很多实用方法，可以大大加快编程效率

```scala
//继承App可以直接在伴生对象中运行
object Test extends App {
    val age = 0
    val name = "bob"
    val double = 1.0

    //常见字符串用法
    println("age = " + age + "; name = " + name)

    //格式化输出
    printf("age = %d; name = %s" + "\n", age, name)

    //模板字符串输出，如果只有一个值可以省略大括号，加上大括号可以写运算表达式
    println(s"age = $age; name = ${name * 3}")

    //格式化模板字符串
    println(f"age = $age; name = ${name}; double = ${double}%2.3f")

    //模板原始字符串
    println(raw"\")
}
```

> “*”运算符输出此字符串的次数（\*是一个方法名，且name.\*(3)在Scala中可以写成name * 3）

## <div id="scala-常用类">常用类</div>

我们知道了字符串用法之后，键盘输入和文件读取也是我们常用的类，我们不常用也要知道怎么用Scala实现相关代码

```scala
object Test2 extends App {
    //获取键盘输入返回Int如果无法格式化将报出NumberFormatException异常
    StdIn.readInt()

    //获取字符串
    StdIn.readLine()

    //当然也有更多类型
    //...
}
```

文件读取

```scala
object Test3 {
    //创建文件输出流
    val writer = new PrintWriter(new File(System.getProperty("user.dir") + "\\a.txt"))
    writer.write("hello" + "\n");
    writer.write("java" + "\n");
    writer.write("scala" + "\n");
    writer.write("hive" + "\n");
    writer.write("spark" + "\n");
    writer.close()

    //文件输入流
    val source = Source.fromFile(new File(System.getProperty("user.dir") + "\\a.txt"))

    //使用lambda表达式传入print函数，由于foreach里的参数是一个函数所以传入print
    //foreach中函数中类型为char让print打印每一个char即可实现打印一行的效果，如果不理解可以查看源代码
    source.foreach(print)
}
```

## <div id="scala-渐入佳境">渐入佳境</div>

## <div id="scala-数据类型">数据类型</div>

学习Scala数据类型前，我们先回顾Java的数据类型。在Java中分有两大类数据类型，分别是**基本数据类型**、**引用数据类型**，
其中引用数据类型就是对象类型，但是基本数据类型并不是一个真正的对象，虽然Java有包装类，但是基本数据类型并不是真正的对象。

而在Scala中抛弃了Java中的基本数据类型，Scala中一切数据都是对象，都是Any的子类，Scala中数据类型分为两大类：
数值类型**AnyVal**、引用类型**AnyRef**，不管是值类型还是引用数据类型都是对象。Scala数据类型仍然遵守，低精度的值自动转换高精度类型（隐式转换），
其中Scala的String类型有个增强版，叫StringOps，它还有一个空类型叫做**Unit**对应Java的void，Unit也是一个数据类型，Null也是一个类型，
它是所有AnyRef类型的的子类。

它们的继承关系，"-->"直接继承，"~~>"隐式转换

```text
Any --> AnyVal --> Double (Double继承AnyVal)
               --> Double ~~> Float (Float继承AnyVal隐式继承Double)
               --> Float ~~> Long
               --> Long ~~> Int
               --> Int ~~> Short
               --> Short ~~> Byte
               --> Unit
               --> StringOps
               --> Int ~~> Char

    --> AnyRef --> (Scala collections)
               --> (All java classes)
               --> (Other Scala classes) --> Null (继承以上三个)

               --> Nothing (继承所有)
```

> 所有的Java类、Scala类、Scala集合类型都继承AnyRef类型，Nothing代表什么都没有，没有返回值，没有引用类型
> 在Java中使用强制类型转换是这种方式`byte a = (byte) 200`，而Scala中是`val a: Byte = 200.toByte`调用方法的形式进行转换

Null、Nothing、Unit的使用：

```scala
object Test3 extends App {

    def a(): Unit = {
        return 1
    }

    println(a()) //返回Unit的实例值 () 空括号

    def b: Null = {
        val a: Null = null
        return a
    }

    println(a()) //返回Null的实例值 null

    def c: Nothing = {
        //什么也不返回会报错
        //返回任何类型也会报错，因为Nothing是任何类型的子类
        //抛出异常不报错
        throw new RuntimeException()
    }

    def d(number: Int): Int = {
        //通常这样使用Nothing
        if (number == 0) throw new RuntimeException()
        else number
    }

}
```

String转数值类型，Scala中使用调方法的方式来进行数值数据转换，而在Java中使用`Integer.parseInt("12")`进行转换，
而Scala更加简单方便

```scala
val int: Int = "12".toInt
val double: Double = "12.3".toDouble
val toInt: Int = "12.3".toInt //会报错，因为不能将小数转换为Int类型
val toDoubleToInt: Int = "12.3".toDouble.toInt //进行两次转换就可以了
```

## <div id="scala-运算符">运算符</div>

Scala运算符与Java运算符相同，注意Scala的运算符都是方法，关于Java运算符请看<a href="#java-运算符">Java运算符</a>

在集合中有大量的操作集合的运算符（方法），集合方法到后面集合篇可以找到

> 需要注意的是在Java中使用`==`对比字符串会是false，因为Java对比的是引用地址，而不是string的具体内容
> ```java
>   String a = "hello";
>   String b = new String("hello");
>   //引用地址不相等，equals相等
> ```
> 但是在Scala中所有运算符都是方法（函数），Scala使用`==`的时候判断的不是地址，而是实实在在的内容
>```scala
>  val a = "hello"
>  val b = new String("hello")
>  println(a.==(b))      //等价于 a == b（Scala运算符的本质），打印true
>  println(a.equals(b))  //等价于 a equals b，打印true
>  println(a.eq(b))      //等价于 a eq b，打印false
>```

## <div id="scala-流程控制">流程控制</div>

经典的if语句使用，`if(布尔表达式){代码块}`，当为true时执行代码块，
还有else`if(布尔表达式){代码块}else{代码块}`，当为false时执行else代码块，
还有有if else if`if(布尔表达式){代码块}else if(布尔表达式){代码块}`，
如果第一个为true执行第一个if，如果为false判断第二个布尔表达式是否为true如果true执行else if中的代码块，
如果为false 且有else（这个例子没有else）执行else 下的代码块

需要注意的是，在Java中的三元运算符，在Scala中是没有的，在Scala中要使用这样的方式：

```scala
//在Scala中每一行都有一个返回值，只是那个返回值值我们不能"处理（指的是Unit）"，所以我们还可以这样做
val a: Int = if (a != 0) 1 else 2

//当然也可以这样做
val b: Int = if (b != 0) {
    //代码块
    123
} else {
    //代码块
    456
}
//在使用时把三元换成 if else 就可以了，还要记得每一行都是一个表达式就可以，或者记住if可以返回值
```

当然if分支也可以嵌套的

```scala
if (true) {
    if (true) {
        //代码块
    } else {
        //代码块
    }
}
```

在Java中的for循环是较为复杂的，`for(int i = 0; i < 10; i++) {//代码块}`，虽然相对于foreach就简单多了。
而Scala的for的语法更加简介`for(i <- 1 to 10){//i为1~10（包含）}`

```scala
for (i <- 1 to 10) {
    //i为1到10
}
```

我们发现to在编辑器中并没有关键词高亮，其实to并不是一个关键词，而是一个方法`1 to 10`等价于`1.to(10)`。
点开to的源码发现to是RichInt类里的方法，可是1不是一个int类型吗，其实在Scala中有隐式转换，
如果对象调用的方法并没有实现就会找到，但是我们并没有声明隐式转换，其实隐式转换在**Predef.scala**文件中，
*Predef 对象提供可在所有 Scala 编译单元中访问的定义，而无需显式限定 ---Predef原话*，所以Predef是Scala默认加载的类。

其中隐式转换就在这里

```scala
implicit def byteWrapper(x: Byte): Byte = new runtime.RichByte(x)
implicit def shortWrapper(x: Short): Short = new runtime.RichShort(x)
//传入一个Int并包装成RichInt
implicit def intWrapper(x: Int): Int = new runtime.RichInt(x)
implicit def charWrapper(c: Char): Char = new runtime.RichChar(c)
implicit def longWrapper(x: Long): Long = new runtime.RichLong(x)
implicit def floatWrapper(x: Float): Float = new runtime.RichFloat(x)
implicit def doubleWrapper(x: Double): Double = new runtime.RichDouble(x)
implicit def booleanWrapper(x: Boolean): Boolean = new runtime.RichBoolean(x)
```

使用`1 to 10`方法时发现to方法是**包含1和10**的，如果不想让它包含10就需要使用Range类或者使用until方法

```scala
  //使用Range类打印1-9
for (i <- Range(1, 10)) {
    println(s"$i，Range")
}
//使用until打印1-9
for (i <- 1 until 10) {
    println(s"$i，until")
}
```

当然也可以使用for遍历集合

```scala
val arr: Array[Int] = Array(1, 2, 3, 4, 5, 6, 7)
for (i <- arr) {
    println(i)
}
```

在Scala的for循环中还有一个语法，叫做循环守卫，也叫做循环保护式，在for表达式中编写if语句，
还需要注意的一点就是Scala**删除了continue和break**，可以在循环守卫中先判断是否应该跳过此次循环，代替了continue

```scala
//在表达式中添加了if判断是否执行此次循环
for (i <- 1 to 10 if i != 5) {
    println(s"$i，to if")
}
```

Scala还有一个方法，就是可以设置步长，`if(i <- 1 to 10 by 2){//代码块}`，从1到10每次+2而不是+1，看到这里会有个疑虑，
这个by方法哪来的，by方法其实是1调用to10后返回的Range类，Range类中的by方法

```scala
for (i <- 1 to 10 by 5) println(s"$i,to by") //打印出1、6
//如果我们把步长设为负数，经过我们的思考1 + -1永远达不到10，所以什么也不会运行，但是循环会结束
for (i <- 1 to 10 by -1) println(s"$i,to by")
//我们可以把10放在前面，步长还是设为-1
for (i <- 10 to 1 by -1) println(s"$i,to by") //打印出来的将是倒序
//如果我们把步长设置为0，将会抛出IllegalArgumentException的step cannot be 0异常，步长不能为0异常
for (i <- 10 to 1 by 0) println(s"Exception")
//当然也可以使用to的设置步长的方法进行实现步长
for (i <- 1.to(10, 2)) println(s"$i,to by") //但是需要.进行来调用了
```

Scala还有一种嵌套的简写语法，虽然是简写，看起来更难理解了hha

```scala
//这是平常的嵌套for循环
for (i <- 1 to 3) {
    for (j <- 3 until 6) println(s"$j = j")
    println(i)
}
//这是简写语法
for (i <- 1 to 3; j <- 3 until 6) { //将两个for写到了一起
    println(s"$j = j")
    if (j == 5) println(i)
}
```

for还有一个引入变量的写法，就是在后面引入一个或多个变量

```scala
for (i <- 1 to 10; j = 10 - i; l = 10 + i) {
    println(s"$j = j、$i = i、$l = l")
}
//如果代码过长也可以把圆括号换成大括号
for {i <- 1 to 10
     j = 10 - i
     l = 10 + i} {
    println(s"$j = j、$i = i、$l = l")
}
```

是的，Scala每行都有返回值，就连for循环都有返回值，我们思考for循环是返回什么值？第一个值？最后一个值？
其实都不是，默认for循环返回的Unit值，就是一个空值。返回值应该是每个值才对，我们可以利用一个关键字来**返回一个集合**，
那就是`yield`关键字

```scala
val arr = for (i <- 1 to 10) yield i * i
println(arr) //返回值为：Vector(1, 4, 9, 16, 25, 36, 49, 64, 81, 100)的集合数组
```

当然Scala中也是有while循环的，用法和Java一样，do-while也是一样的，虽然Scala有while但不推荐使用while。
因为while循环没有办法像for一样那么强大，也没有yield将值返回为集合，只会返回一个Unit

之前我们提到，Scala**删除了continue和break**所以我们想要中断循环就要用另一种方式了，使用try-catch

```scala
//使用try-catch进行break终止循环
try {
    for (i <- 1 to 10) {
        if (i == 5) throw new RuntimeException("this is break")
        println(i)
    }
} catch {
    case e: RuntimeException => //nothing
}
//可以看到本来就一个break的事情，却有这么多行代码，很显然这不是我们想要的
//Scala封装了一个类，我们可以用Breaks类进行操作需要break的语句
Breaks.breakable(for (i <- 1 to 10) {
    if (i == 5) Breaks.break()
    println(i)
})
```

我们知道Java导入此类的所有方法和属性是用的*号，而Scala使用的是_下划线

```scala
//导入Breaks中的所有方法和属性

import scala.util.control.Breaks._
```

> _下划线在Scala中还有更多用法，比如占位符等等...之后会提到

## <div id="scala-函数式编程">函数式编程</div>

Scala不光是完全面向对象语言，也是一门函数式编程语言，本质就是把数据和行为封装成函数，这也是Scala和Java区别最大的地方。

定义一个函数需要**def关键字，用来定义函数的关键字、一个函数名、参数名、参数类型、返回值类型、函数体**

```scala
//def代表定义一个函数
//show代表函数名
//message代表形参名
//String代表形参类型
//Unit代表返回值类型
//大括号内容代表函数体
def show(message: String): Unit = {

}

//如果函数体一行可以省略大括号
def send(message: String): Unit = println(message)
```

> 注意在Scala中是不能更改形参的值的，因为默认形参是用val进行声明。在函数式编程中也不推荐使用变量，
> 如果要达到变量的效果可以使用函数进行封装
`def changeVar(variable: Int, n: Int)(func: (Int, Int) => Int) = func(variable, n)`，
> 这个changeVar函数使用了柯里化，到后面会提到

这是Java的方法（函数）

```java
public void send(String message) {
    System.out.println(message);
}
```

在Java中方法中不能声明方法，但是Scala可以，因为Scala是函数式编程语言它可以把函数写在函数中

```scala
def a(x: Int): Unit = {
    def b(n: Int): Unit = {

    }
}
```

> 值得一提的是，方法和函数还有另一种不同的意思，在类的函数称为方法，而在类外定义的叫函数，
> 因为Java的函数只能写在类里，所以叫方法，而Scala当然也可以把函数写在类里，所以写在类里的叫做方法，类体外叫做函数

Scala也有可变参数，用法和Java也是一致的，需要注意的是在Scala中通过下标获取一个集合的元素，
用的是圆括号，而Java是用的方括号，使用圆括号其实是apply方法。apply方法可以让你在调用时，
可以直接跟上圆括号而不是 `instance.apply(0)` 当然你也可以这么做，不加apply只是省略了而已

```scala
def a(message: String*): Unit = {
    println(message(0))
    println(message(1))
}

a("111", "hello")
```

Scala函数中还有默认参数，在形参类型后面赋上一个值就代表这是默认形参

```scala
def a(age: Int = 0): Unit = {
    println(age)
}

a() //不传参数打印0，传参打印参数
```

如果一个以上的参数都是默认传参，你可以使用形参名赋值进行指定传参

```scala
def a(name: String = "bob", age: Int = 18) = println(s"name=$name,age=$age")

a("alice", 19)
a(age = 17) //如果只想传后面的参数，可以根据函数参数名进行指定传参
a(age = 20, name = "张三") //这是调换形参前后位置的传参
```

函数至简原则，能省则省

1. return可以省略，Scala会使用函数的**最后一行作为返回值**
2. 如果函数体只有一行代码，可**省略大括号**
3. 返回值类型如果可以推断出来，可以**省略返回值**
4. 如果有return，则不能省略返回值类型
5. 如果函数明确声明了Unit，那么return将不起作用
6. Scala如果是无返回值类型，可以省略等号，（没有等号就代表过程，就不是数学上的映射了）
7. 如果**函数无参**，在调用时小括号可加可不加
8. 如果**函数没有参数列表**，小括号可以省略但是在调用时**必须省略**

> 匿名参数通常是作为函数进行返回，或者作为参数进行传入

```scala
//一个普通的匿名参数、lambda表达式
() => println("aaa")
//如果要调用或者赋值，就需要声明一个变量，类型为 () => Unit 然后等号赋值 () => println("aaa")
val function: () => Unit = () => println("aaa")
function() //调用
```

## <div id="scala-炉火纯青">炉火纯青</div>

## <div id="scala-高阶函数">高阶函数</div>

函数的高阶用法，函数传参，返回函数，柯里化都是函数的高阶用法

定义一个函数，把函数作为参数传入

```scala
def f(function: String => Unit): Unit = {
    function("hello")
}
f(x => println(x))
//如果函数只有一个形参可以用_代表参数
f(println(_))
//还可以再省略为
f(println)
```

定义一个函数，但是传入的函数是无参函数

```scala
def f(function: () => Unit) = {
    function()
}
f(() => {
    println("啊啊")
    println("啊啊")
    println("啊啊")
    println("啊啊")
})
```

定义一个两个形参的函数参数，Scala的简写方式很抽象，建议遵守能省则省的原则

```scala
def f(fun: (Int, Int) => Int) = println(fun(1, 1))

f((x1, x2) => x1 + x2)
//可以简化为，因为这两个形参变量只用了一次w
f(_ + _)
```

将函数作为值传递，将f函数赋值给f1。f1的类型为`() => Unit`无参无返回值

```scala
def f(): Unit = println("function")

val f1: () => Unit = f
f1()
```

将函数作为返回值，返回一个函数

```scala
//创建一个f的函数，返回一个函数，返回值为((Int,Int) => Int) => Int
def f(a: Int, b: Int): ((Int, Int) => Int) => Int = {
    //传入一个匿名函数，返回结果
    def f1(operation: (Int, Int) => Int): Int = {
        operation(a, b)
    }

    f1
}
//传入ab参数，返回过来的函数再次调用，并返回结果
println(f(1, 2)(_ + _))
``` 

可以使用柯里化进行简化，柯里化就是`f(a: Int, b: Int)(f: (Int, Int) => Int)`中的`(f: (Int, Int) => Int)`部分，
可以看到柯里化直接将返回函数的形参作为了一个形参表示，使用柯里化让返回返回值更加易读和简介

```scala
def f(a: Int, b: Int)(f: (Int, Int) => Int) = f(a, b)

println(f(1, 2)(_ + _))
```

> 在大数据中处理一个集合，你需要处理集合并要集合的结果，处理集合是一步一步进行的，
> 你要做的是，将每一步的逻辑都抽象出来

拓展：将每个数组中的元素相加拿到总和

传入一个数组和一个操作，并将结果使用foreach循环返回

```scala
val array: Array[Int] = Array[Int](2, 3, 4)

def f(array: Array[Int], op: (Int, Int) => Int): Int = {
    var int = 0
    array.foreach(element => int = op(element, int))
    int
}

println(f(array, _ + _))
```

在Scala源码中，Scala作者用了一种精妙的方式进行数组操作

作者使用类进行巧妙的操作

```scala
def foldLeft[B](z: B)(op: (B, A) => B): B = {
    //avoid the LazyRef as we don't have an @eager object
    class folder extends AbstractFunction1[A, Unit] {
        var result = z

        override def apply(v1: A): Unit = result = op(result, v1)
    }
    val folder = new folder
    this foreach folder
    folder.result
}
 ```

进行简化作为函数返回值的函数

```scala
//首先我们先写一个没简化的版本，在函数中嵌套了一个函数
def f(string: String): Int => Boolean = {
    def _f(int: Int): Boolean = {
        if (string == "" || int == 0) true else false
    }

    _f
}

//我们知道_f的名字在这里是不重要的，我们可以省略_f为匿名函数
def f1(string: String) = {
    //声明形参类型可以不用声明返回值
    (i: Int) => if (string == "" || i == 0) true else false
}

//当然可以再省略大括号，还有(i: Int)中的小括号和形参类型，因为我们在返回值中声明过了
def f2(string: String): Int => Boolean = i => if (string == "" || i == 0) true else false
```

## <div id="scala-闭包与柯里化">闭包与柯里化</div>

如果一个函数，访问到了它局部变量以外的值，那么这个函数和环境就被称为**闭包**，每一个**函数式编程语言**都是支持闭包的，
在Java8之后引入了lambda表达式也开始真正实现了闭包，在Java8之前都是使用匿名类麻烦的实现方法，
使用闭包可能会造成内存泄露，谨慎使用

这是一个简单的函数套函数，当我们调用addByA函数，返回add函数，其中我们的a变量即使addByA结束了add也能调用到a变量

```scala
def addByA(a: Int): Int => Int = {
    def add(b: Int): Int = {
        a + b
    }

    add
}

//调用addByA的方法将4传入到形参a
val addByFour: Int => Int = addByA(4)
//这里addByA的方法已经结束，我们都知道，变量都是随着变量作用域
//当addByA虽然栈中已经结束，但是堆内存中还有这addByA的实例，所以可以调用到形参a
println(addByFour(3))
```

> 在JVM（Java虚拟机：Java程序都是在Java虚拟机中运行）中，调用的方法会放到一个名叫栈的区域，还有一个堆区。
> 其中栈区是用来放置调用的方法，而堆是用来防止对象的实例，这也是引用数据类型引用的地方。
> 栈有个特性，就是先进先出，方法1调用之后会进入栈区，如果在方法1中调用方法2就会压栈，只有方法2结束调用才能结束调用方法1
>
> 而Scala在用一个方法时，也会压栈，但是在堆内存中会有一个方法的实例，虽然方法在栈区被弹出但是堆内存中还存在着实例，
> 这样也就为了闭包方法中提供了引用变量地址

“**柯里化**将一个形参列变成了多个形参列表”，在写嵌套函数时通常都是这样写的

这个例子我们将一个函数作为返回值，声明了返回值类型是一个函数

```scala
//这是上一个函数的简写
def addByA(a: Int): Int => Int = a + _
```

我们可以使用柯里化的方式来清晰地编写嵌套函数

```scala
//我们将返回值的函数的形参加到了第一个函数的形参旁边，一个形参列表变成了多个形参列表篇
//这就是柯里化
def addByA(a: Int)(b: Int): Int = a + b
```

## <div id="scala-递归">递归</div>

递归指的是，调用一个函数之后函数本身又调用函数本身，递归必须要达到一个条件跳出循环，否则会报出栈内存溢出异常。
几乎所有编程语言都有递归。

递归也可以实现循环，我们在之前提到过栈区，在认识递归之前需要理解它的底层原理，当有第一个函数调用就会进入到栈区，
其中函数在栈区中叫做**栈帧**这个操作被称为压栈，只要函数调用没有结束就会一直在栈中，
栈的结构为先进先出，先调用的方法先进去如果方法没有结束而调用其它的方法就会压栈，先进去的必须等待后进去的出来

利用递归来相加1-9，这种递归使用了上一个递归的变量也就是`fact(n-1)+n`的 +n 部分

```scala
//可能有点不好理解，如果不好理解就去调试一行一行去看
def fact(n: Int): Int = {
    if (n == 1) return 1
    fact(n - 1) + n
}

println(fact(10))
```

可以看到上个例子由于使用了上个栈帧的变量（指的是+n）Scala不能弹出上一个栈，如果把+n放到函数的形参中，
这样结果就不引用函数变量，Scala会自动弹出上一个栈，这叫**尾递归**。Java中并没有尾递归

```scala
def fact(n: Int, c: Int): Int = {
    if (n == 0) return c
    fact(n - 1, c + n)
}

println(fact(10, 0))
```

可以使用`@tailrec`注解来判断是否是尾递归，如果不是就会报错

```scala
@tailrec
def fact(n: Int, c: Int): Int = {
    if (n == 0) return c
    fact(n - 1, c + n)
}
```

Scala支持**惰性加载**，惰性加载要用到一个关键字`lazy`声明在变量和常量前面，表示变量虽然赋值，
但是变量值并没有加载，只在值使用的时候才会加载函数中的内容

```scala
def sum(a: Int, b: Int): Int = {
    println("sum被调用")
    a + b
}

lazy val value = sum(1, 1)
println("Hello lazy")
println(value)
println(value)

/* 打印为
Hello lazy
sum被调用
2
2
 */
```

## <div id="scala-包">包</div>

基本语法：package 包名

包的三大作用：

1. 区分相同名字的类
2. 当类很多时，可以方便管理类
3. 控制访问权限

包的命名规则，只能包含数字、字母、下划线，但不能以数字开头，也不要使用关键字

命名规范，一般是小写字母

```text
package com.example.demo
```

所有Scala包都可以定义一个包对象。包对象，包对象要和包同名

创建一个包对象

```scala
package object test {
    val name = "包对象"
}
```

包对象里面的属性方法类，此包下的所有结构都可以**访问包对象里的属性和方法**

Scala导包和Java导包类似，可以顶部使用**import**导入，在这个文件中的所有类都可以使用，
Scala还可以进行局部导入，在其作用域进行访问

可以使用`_`通配符导入导入所有包下的类

```scala
//顶部导入

import test._

object Obj {
    def main(args: Array[String]): Unit = {
        import scala.util._
    }
}
```

使用 **{类名 => 别名}** 给导入的类起别名

```scala
import com.example.{Demo => D}

object demo {
    private val demo = D()
}
```

导入相同包下的类可以使用 **{类1,类2}**

屏蔽类使用 `import com.example.{Demo => _,_}`：
Demo是被屏蔽的类，第一个_代表Demo被屏蔽，第二个代表所有类。  
所以屏蔽多个类可以使用`import com.example.{Demo => _,Test => _,_}`

## <div id="scala-类">类</div>

在Scala中，一个文件可以写多个类

创建一个类的基本语法：

```text
[修饰符] class 类名 {
    类体
}
```

定义一个类

```scala
class Student {
    //var可变变量
    var name = "小王"
    //val不可变值
    val age = "18"
    //如果不想给一个默认属性默认值，可以使用_
    //但是要使用var
    var school: String = _
}
```

将数据封装起来，并设置访问权限，防止数据被修改

访问权限：

1. Scala没有public修饰符，但是默认是public
2. private为私有权限，只能本类访问
3. protected为保护权限，只能同类和子类访问
4. private\[包名\]为包权限，包名下的所有类可以访问

构造器的基本语法

```text
class 类名(参数列表) { //主构造器
    def this(参数列表) { //次构造器
        this() //调用主构造器
    }
    
    def this(参数列表) { //次构造器
        this() //调用其他构造器，但是最终必须指向主构造器
    }
}
```

主构造器的形参列表可以使用三种方式修饰：

1. 什么也不用，仅仅代表这是一个参数，不是对象属性
2. var，可以修改的属性
3. val，不可以修改的属性

```scala
class ClassStudy(name: String, var age: Int, val gender: String) {
}

object ClassStudy {
    def main(args: Array[String]): Unit = {
        val study = new ClassStudy("bob", 18, "male")
        //只能访问var和val属性
        println(study.age)
        println(study.gender)
    }
}
```

## <div id="scala-继承">继承</div>

继承的语法：`class 子类名 extends 父类名 { 类体 }`

子类会继承父类的属性和方法

一个继承的示例

```scala
//继承并重写属性
class Worder(override val name: String, var age: Int) extends Person(name) {
    //重写方法
    override def sayHello(): Unit = println(s"你好我叫$name, 我今年$age")
}

//父类
class Person(val name: String) {
    def sayHello(): Unit = println(s"你好我叫，$name")
}
```

## <div id="scala-抽象类">抽象类</div>

对于抽象类是和Java中抽象类是一致的，但是语法会有些不同

1. 定义抽象类：`abstract class 类名`
2. 定义抽象类属性：`val或者var name: String`
3. 定义抽象方法：`def hello(): String`

继承和重写

1. 如果父类为抽象类，那么子类就要重写属性和方法，否则子类就要声明为抽象类
2. 重写抽象方法可以不加override
3. 子类调用父类的方法要用super关键字
4. 子类对抽象属性进行实现，父类抽象属性可以用var

子类对非抽象属性重写，父类非抽象属性只支持val类型，而不支持var。
因为var修饰的为可变变量，子类继承可以直接使用，没有必要重写

当然也可以使用匿名子类来实现一个类

```scala
//继承并重写属性
class Worder(name: String) extends Person(name) {

    override def say(): Unit = {
        println("I'm " + name)
    }

}

//父类
abstract class Person(var name: String) {
    def say(): Unit

    def sayHello(): Unit = {
        println("hello")
    }
}

object ClassStudy {
    def main(args: Array[String]): Unit = {
        //匿名子类
        new Person("bob") {
            override def say(): Unit = {
                println(s"hi，my name is $name")
            }
        }
    }
}
```

## <div id="scala-单例对象">单例对象</div>

单例对象也叫做伴生对象，Scala是一门完全面向对象的语言，所以它没有静态从操作。  
即使Scala没有静态概念，但是Scala可以使用单例对象来模拟静态的概念

伴生对象里面的方法和属性和静态方法和静态属性一致，全局只有一份（因为只有一个对象）

单例对象可以和普通的类对象重名

使用object定义一个伴生对象（单例对象）基本语法：

```text
object 类名 {
    val school = "某某大学"
}
```

一个类对象与伴生对象

```scala
class Student(val name: String, val age: Int) {

}

object Student {
    val school = "某某大学"
}

object Main {
    def main(args: Array[String]): Unit = {
        //调用伴生对象属性，通过伴生对象名调用
        println(Student.school)
    }
}
```

## <div id="scala-apply">apply</div>

在普通的类对象还有单例对象中创建一种特殊的方法，叫做apply方法

```scala
class Student(val name: String, val age: Int) {
    def apply(): Unit = println("做操作")
}

object Student {
    def apply(name: String, age: Int): Student = new Student(name, age)
}

object Main {
    def main(args: Array[String]): Unit = {
        //apply可以不写apply的方法名，直接使用圆括号调用apply
        //使用apply创建一个对象
        val student = Student("张三", 18)
        //当然普通的类也有apply使用对象调用
        student()
    }
}
```

## <div id="scala-特质">特质</div>

在Scala中使用特质（特征）来代替接口的概念，也就是说，多个类具有相同的“特征”时，
就可以将这个“特征”独立出来，采用**trait**声明

trait中可以有抽象属性和方法，也可以有具体的属性和方法，一个类可以“混入（mixin）”多个特质

基本语法：

```text
trait 特质名 {
    trait主体
}
```

使用特质时使用的也是**extends**，如果有多个特质使用**with**关键字连接

例如：`class 类名 extends 父类|特质 with 特质 [with 特质]... `

使用混入

```scala
//程序入口
object Main {
    def main(args: Array[String]): Unit = {
        new Person("张三", 18).activity()
    }
}

//特质一
trait Young {
    var age: Int

    def activity(): Unit
}

//特质二
trait Hobby {
    var hobby: String
}

//在主构造器中实现var
class Person(var name: String, var age: Int) extends Young with Hobby {

    //实现hobby属性
    override var hobby: String = "编码"

    //实现activity方法
    override def activity(): Unit = println("活动！")
}
```

动态进行混入

```scala
package notes

object Main {
    def main(args: Array[String]): Unit = {
        //动态混入Hobby特质
        val person = new Person("bob") with Hobby {
            override val hobby: String = "football"

            override def showHobby(): Unit = println(s"$name like $hobby")
        }

        //调用实现方法
        person.showHobby()
    }
}

trait Hobby {
    val hobby: String

    def showHobby(): Unit
}

class Person(var name: String)
```

多继承的钻石问题

如果多个特质含有相同的方法，子类调用特质的非抽象方法时，会发生冲突（虽然使用super访问的是最后一个特质的方法）

但是我们可以使用`super[特质]`指定进行调用哪个特质的方法

```scala
trait Hobby {
    val hobby: String

    def showHobby(): Unit = {
        println("hobby1")
    }
}

trait Hobby2 {
    val hobby: String

    def showHobby(): Unit = {
        println("hobby2")
    }
}

class Person(var name: String) extends Hobby with Hobby2 {
    override val hobby: String = "basketball"

    //通过super[特质]来指定方法
    override def showHobby(): Unit = super[Hobby2].showHobby()
}
```

在Scala中继承具有叠加循序，继承根据继承的顺序来确定要调用的顺序，顺序为从后往前

假如`super[Hobby2].showHobby()`不指定特质，那么将调用最后一个特质中的方法

### 如何选择抽象类和特质呢

1. 抽象级别较高使用特质，建议多使用特质
2. 一个类可以只能实现一个抽象类，但是可以继承多个特质
3. 可以先编写特质，然后被抽象类做通用的继承和实现，再被子类继承
4. 如果需要构造函数参数就使用抽象类，因为特质不能声明构造函数

### 特质自身类型

可以让自身类型实现依赖注入的功能

像是在接口中定义一个属性

```scala
object Main {
    def main(args: Array[String]): Unit = {
        new Registry("bob").insert() //插入了一个用户：bob
    }
}

class User(var name: String)

trait Dao {
    //创建自身类型，其中_为通配符，例如使用user作为自身类型参数的话
    //就要通过user.name来获取name了
    _: User =>

    def insert(): Unit = {
        println(s"插入了一个用户：$name")
    }
}

//如果不继承User，Dao特质就会报错，编译失败
class Registry(name: String) extends User(name) with Dao
```

## <div id="scala-类型检查和转换">类型检查和转换</div>

1. `obj.isInstanceOf[T]`：判断obj是否是T类型
2. `obj.asInstanceOf[T]`：将obj转换为T类型
3. `classOf`：获取对象的类名

在判断是否是此类型时，使用父类作为类型时也会返回true

```scala
object Main {
    def main(args: Array[String]): Unit = {
        val worder = new Worder("bob")
        //声明是为Person，赋值时为Student
        val student: Person = new Student("alice")

        //判断Worder对象是否为Person
        println(worder.isInstanceOf[Person]) //true
        //判断Student是否时Worder类型
        println(student.isInstanceOf[Worder]) //false
        //强制转换为Student
        println(student.asInstanceOf[Student])

        //打印类信息
        println(classOf[Student]) //class notes.Student
    }
}

class Person(var name: String)

class Worder(name: String) extends Person(name)

class Student(name: String) extends Person(name)
```

## <div id="scala-枚举类和应用类">枚举类和应用类</div>

定义一个枚举类要使用`object`伴生对象，然后继承**Enumeration**类

应用类指的是，可以直接运行的类，不需要写main方法，但是需要继承**APP**类

```scala
//枚举类，需要继承Enumeration
object WordDay extends Enumeration {
    //定义枚举值
    val MONDAY, WEEK_ONE = Value(1, "周一")
    val TUESDAY = Value(2, "周二")
}


//应用类，可以直接运行，App类中包含一个main方法所以可以直接运行
object Main extends App {
    println(WordDay(1)) //周一
    println(WordDay.TUESDAY) //周二
}
```

枚举类的其他写法

- 直接继承Value

```scala
object WordDay extends Enumeration {
    val Monday, Tuesday, Wednesday, Thursday, Friday = Value
}


object Main extends App {
    //输出枚举值的常量名
    WordDay.values.foreach(println)
}
```

- 自定义枚举值

```scala
object Color extends Enumeration {
    //枚举值
    val Red = ColorValue(255, 0, 0, "red")
    val Green = ColorValue(0, 255, 0, "green")
    val Blue = ColorValue(0, 0, 255, "blue")

    //继承Enumeration中的Val类
    protected case class ColorValue(red: Int, green: Int, blue: Int, describe: String) extends Val {
        def printInfo(): Unit = println(s"R:$red, G:$green, B:$blue, describe:$describe")
    }

    //隐式转换Value为ColorValue，让Color可以调用printInfo方法
    implicit def valueToColorValue(x: Value): ColorValue = x.asInstanceOf[ColorValue]
}


object Main extends App {
    //可以打印信息
    Color.values.foreach(_.printInfo())
}
```

> 在Enumeration中其枚举值必须为Value的子类，
> 而Val继承Value，ColorValue继承Val，所以在Color.values中可以访问到枚举值

## <div id="scala-登峰造极">登峰造极</div>

## <div id="scala-集合">集合</div>

Scala中的集合有三大类：**Seq（序列）、Set（集）、Map（映射）**，所有的集合都扩展自Iterable特质

对于所有的集合类，Scala都同时提供了可变和不可变的版本，分别在：

- 不可变集合位于：scala.collection.immutable
- 可变集合位于：scala.collection.mutable

Scala不可变集合指的是集合中的数据不可修改，每次修改返回的是一个新对象，不会对源数据更改

可变集合就是这个集合可以直接更改集合里的数据，而不会返回新对象

不可变集合继承图

```text
Traversable --> Iterable --> Seq --> IndexedSeq --> Vector
                                                --> NumericRange
                                                --> Range
                                                ~~> Array
                                                ~~> String
                                                
                                 --> LinearSeq --> List
                                               --> Stream
                                               --> Queue
                                               --> Stack
                                               
                         --> Set --> HashSet
                                 --> SortedSet --> TreeSet
                                 --> BitSet
                                 --> ListSet
                                 
                         --> Map --> HashMap
                                 --> SortedMap --> TreeMap
                                 --> ListMap
```

可变集合继承图

```text
Traversable --> Iterable --> Seq --> IndexedSeq --> ArraySeq
                                                --> StringBuffer
                                                --> ArrayBuffer
                                                
                                 --> LinearSeq --> MutableList --> Queue --> SynchronizedQueue
                                               --> LinkedList
                                               --> DoubleLinkedList
                                               
                                 --> Buffer --> ArrayBuffer
                                            --> ListBuffer
                                            --> ObservableBuffer
                                            --> SynchronizedBuffer
                                        
                                 --> Stack --> SynchronizedStack
                                 --> ArrayStack
                                 --> PriorityQueue --> SynchronizedPriorityQueue  
                                 
                         --> Set --> HashSet
                                 --> BitSet
                                 --> ObservableSet
                                 --> SynchronizedSet
                                 --> ImmutableSetAdaptor
                                 --> LinkedHashSet
                                 
                         --> Map --> HashMap
                                 --> WeakHashMap
                                 --> OpenHashMap
                                 --> LinkedHashMap
                                 --> ObservableMap
                                 --> SynchronizedMap
                                 --> ImmutableMapAdaptor
                                 --> ListMap
```

### <div id="scala-数组">数组</div>

定义一个数组：`val arr = Array[Int](1, 2, 3)`

也可以使用apply来创建一个数组`Array(1, 2, 3)`

Array为一个数组，方括号代表泛型，括号中为传入的元素

Array是不可变的，所以不能改变数组的长度，但是可以改变数组的元素（仅限Array可变）

访问元素

```scala
val arr = Array(1, 2, 3)
//通过apply方法访问
println(arr(0)) //1
```

使用update方法更改一个元素 **arr(0) = 10 等价于 arr.update(0, 10)**

```scala
object Main extends App {
    val arr = Array(1, 2, 3)

    //其实是调用了update方法，类似apply
    arr(0) = 10


    val person = new Person("bob")
    person() = "aa"
}


class Person(var name: String) {
    def update(name: String): Unit = {
        println(name) //aa  
    }
}
```

数组的循环 使用范围对象（隐式转换的）中的until来 指定范围

```scala
for (a <- 0 until arr.length) {
    println(arr(a))
}
```

也可以直接使用arr中的indices方法来获取所有下标

```scala
for (a <- arr.indices) {
    println(arr(a))
}
```

也可以直接使用arr来获取arr中的值

```scala
for (a <- arr) {
    println(a)
}
```

当然还有foreach`arr.foreach(println)`

还有一种更方便的方式，可以让数组根据字符串来分割并返回一个数组

```scala
println(arr.mkString("，")) //1，2，3
```

添加一个元素，因为是不可变集合，所以返回的是一个新对象

```scala
val arr = Array(1, 2, 3)
var temp: Array[Int] = Array.empty

//使用:+方法来添加一个元素，注意:+方法是经过隐式转换的
//我们可以省略点和括号 arr.:+(4) 等价于 arr :+ 4
temp = arr :+ 4
println(temp.mkString(", ")) //1, 2, 3, 4

//Scala还有前相加 arr.+:(0) 等价于 0 +: arr
//注意以冒号结尾的方法不能放在后面
temp = 0 +: arr
println(temp.mkString(", ")) //0, 1, 2, 3
```

混在一起

```scala
//当然可以混一起
temp = -1 +: 0 +: arr :+ 4 :+ 5 :+ 6 :+ 7
println(temp.mkString(", ")) //-1, 0, 1, 2, 3, 4, 5, 6, 7
```

> 可以让你快速记住的方法，把冒号想象为数组本身，冒号的加号在哪边就把方法写在哪边

创建一个可变数组

```scala
val arr = ArrayBuffer(1, 2, 3)
//创建一个带初始化大小的数组
val arr2 = new ArrayBuffer[Int](20)
```

添加元素

```scala
val arr = ArrayBuffer(1, 2, 3)

//需要注意的是，使用:+只适用于不可变集合
//使用:+返回的还是一个新的对象
//val ints = arr :+ 4

//使用+=来添加一个元素
arr += 4
println(arr.mkString(", ")) //1, 2, 3, 4

//当然也有前添加，使用+=:进行前添加
0 +=: arr
println(arr.mkString(", ")) //0, 1, 2, 3, 4

//推荐可变集合使用方法进行添加删除操作
arr.append(5)
arr.prepend(-1)
println(arr.mkString(", ")) //-1, 0, 1, 2, 3, 4, 5

//还可以根据指定位置添加
arr.insert(2, 1)
println(arr.mkString(", ")) //-1, 0, 1, 2, 3, 4, 5

//还可以添加一整个数组的元素
arr.appendAll(Array(6, 7))
//注意-2和-3的位置
arr.prependAll(Array(-3, -2))
println(arr.mkString(", ")) //-3, -2, -1, 0, 1, 2, 3, 4, 5, 6, 7
```

删除元素

```scala
val arr = ArrayBuffer(1, 2, 3, 4, 5, 6, 7, 8, 9)

arr.remove(0)
//删除指定下标的数
println(arr.mkString(", ")) //2, 3, 4, 5, 6, 7, 8, 9

//删除根据数量删除下标后的数
arr.remove(0, 2)
println(arr.mkString(", ")) //4, 5, 6, 7, 8, 9

//还可以根据-=来减去集合中的一个元素
//如果找到就减去。找不到就不做任何事
arr -= 4
println(arr.mkString(", ")) //5, 6, 7, 8, 9
```

可变与不可变数组之间的转换

```scala
val arr: Array[Int] = Array(1, 2, 3)

//将可变转化为不可变
val buffer: mutable.Buffer[Int] = arr.toBuffer

buffer.append(4)

//将不可变转化为可变
val array: Array[Int] = buffer.toArray

println(array.mkString(", ")) //1, 2, 3, 4
println(arr.mkString(", ")) //1, 2, 3
```

多维数组

```scala
//使用数组自带的方法
//一个三行三列的数组
//需要指定泛型，否则为Noting
val array3 = Array.ofDim[Int](3, 3)
array3(0) = Array(1, 2, 3)

//使用for打印输出
for (i <- array3.indices; j <- array3(i).indices) {
    print(s"${array3(i)(j)}; ")
}
//1; 2; 3; 0; 0; 0; 0; 0; 0;


//使用另一种方式定义二维数组
val array = Array(Array(1, 2, 3), Array(4, 5, 6), Array(7, 8, 9))

println
println("---")
//使用foreach打印输出
array.foreach(_.foreach(x => print(s"$x; ")))
//1; 2; 3; 4; 5; 6; 7; 8; 9;

println
println("---")
//也可以这样
array.foreach(x => println(x.mkString(", ")))
//1, 2, 3
//4, 5, 6
//7, 8, 9
```

### <div id="scala-列表">列表</div>

列表默认为不可变集合

创建一个List：`val list = List(1, 2, 3, 4, 5)`

虽然List是线性的，但是也可以根据下标来访问元素

```scala
println(list(1)) //2
```

由于是不可变所以无法使用update方法：`list(2) = 5`

添加元素

```scala
//私用+:方法来添加元素
val list3 = -1 +: 0 +: list
println(list3) //List(-1, 0, 1, 2, 3, 4, 5)
```

在List.scala文件中有一个空的List对象，可以作为List的初始值叫做**Nil**

List中有一个方法叫做 **::** 用来向列表前方添加一个元素

使用Nil加上::方法可以让创建一个List的可读性更强，
由于使用::中缀方法（就是不加点和括号）冒号在方法后，Scala不让中缀方法中冒号再后所以需要放在Nil前面

```scala
val list = List(1, 2, 3, 4, 5)

//::其实等价与+:但是 :: 只适用于List，而 +: 适用于所有Seq
//推荐在List中使用::
val list2 = -3 :: -2 :: -1 :: 0 :: list
println(list2) //List(-3, -2, -1, 0, 1, 2, 3, 4, 5)

//使用Nil来创建一个新集合
val list3 = 1 :: 2 :: 3 :: 4 :: 5 :: Nil
println(list3) //List(1, 2, 3, 4, 5)
```

添加整个集合

```scala
val list = List(1, 2, 3, 4, 5)
val list2 = list.map(_ * 2)

//在list2列表前添加list列表，但是将list作为一个元素来添加
val list3: List[Any] = list :: list2
println(list3) //List(List(1, 2, 3, 4, 5), 2, 4, 6, 8, 10)

//但是可以使用:::来添加list中的所有元素
val list4 = list ::: list2
println(list4) //List(1, 2, 3, 4, 5, 2, 4, 6, 8, 10)
```

创建一个可变列表

```scala
//推荐使用伴生对象中的apply方法创建对象
val list = ListBuffer(1, 2, 3)
val list2 = new ListBuffer[Int]()
```

添加或修改元素

```scala
val list = ListBuffer(1, 2, 3)

//往前后个追加一个元素，和数组操作一致
0 +=: list += 4
println(list) //ListBuffer(0, 1, 2, 3, 4)

//删除一个元素 注意是使用的不是-=，使用-的话会返回一个新对象
val list2 = list - 4
//list不变
println(list) //ListBuffer(0, 1, 2, 3, 4)

//使用 ++= 添加一个列表中的多个元素
list ++= List(5, 6, 7)
println(list) //ListBuffer(0, 1, 2, 3, 4, 5, 6, 7)

//当然也有 ++=: 往前追加
List(-3, -2, -1) ++=: list
println(list) //ListBuffer(-3, -2, -1, 0, 1, 2, 3, 4, 5, 6, 7)

//使用update修改元素
list(0) = -4
println(list) //ListBuffer(-4, -2, -1, 0, 1, 2, 3, 4, 5, 6, 7)

//使用remove或-=删除元素
list -= -4
list.remove(0, 5)
println(list) //ListBuffer(3, 4, 5, 6, 7)
```

### <div id="scala-集">集</div>

默认情况下，Scala使用的都是不可变集合，如果想要使用可变集合，需要导入scala.collection.mutable包

Set默认是不可变集合，数据无序且不可重复

操作Set

```scala
val set = Set(1, 2, 3, 15, 61, 3, 1235)

//添加一个元素，由于Set是无序的所以添加元素时不用在意添加前还是后
//使用 + 添加元素
val set2 = set + 4
println(set2) //Set(61, 1, 2, 3, 1235, 4, 15)

//使用 ++ 来添加整个Set中的元素
val set3 = set ++ Set(5, 6)
println(set3) //Set(5, 61, 1, 6, 2, 3, 1235, 15)

//删除元素
val set4: Set[Int] = set - 1
println(set4) //Set(61, 2, 3, 1235, 15)

//删除一个集合中的元素
val set5 = set -- Set(1, 2, 3)
println(set5) //Set(61, 1235, 15)
```

创建一个可变Set

```scala
//创建可变Set
val set = mutable.Set(1)

//使用+=添加元素
set += 2
println(set) //Set(1, 2)

//使+返回新集合
val set2 = set + 3
println(set) //Set(1, 2)
println(set2) //Set(1, 2, 3)

//使用-=删除元素
set -= 2
println(set) //Set(1)

//使用++=添加两个集合
set ++= set2
println(set) //Set(1, 2, 3)
```

### <div id="scala-映射">映射</div>

Scala中的Map和Java中的Map类似，也是一个散列表，它存储的内容也是键值对

创建一个Map

```scala
//创建一个Map
val map = Map("1" -> "one", "2" -> "two")
println(map) //Map(1 -> one, 2 -> two)

//遍历每个元素
for ((key, value) <- map) {
    println(s"key: $key, value: $value")
}

map.foreach(println)
//(1,one)
//(2,two)

//当然也可以只拿到key或者value
for (key <- map.keys) {
    println(s"key: $key")
}

for (value <- map.values) {
    println(s"value: $value")
}

//添加元素
val map1 = map + ("3" -> "three")
//也可以这样
val map1 = map + (("3", "three"))
println(map1) //Map(1 -> one, 2 -> two, 3 -> three)

//添加集合中的元素
val map3 = map ++ Map("4" -> "four", "5" -> "five")
println(map3) //Map(1 -> one, 2 -> two, 4 -> four, 5 -> five)

//获取到某个值
println(map3("1")) //one
```

创建一个可变的Map

```scala
//可以使用值别名，来指定可变Map
val Map = scala.collection.mutable.Map

//创建一个可变Map
val map = Map(1 -> "one", 2 -> "two", 3 -> "three")

//添加元素
map += (4 -> "four")
println(map) //Map(2 -> two, 4 -> four, 1 -> one, 3 -> three)

//更新一个元素
map(4) = "四"
println(map) //Map(2 -> two, 4 -> 四, 1 -> one, 3 -> three)

//删除一个元素
map -= 4
//或者
map.remove(3)
println(map) //Map(2 -> two, 1 -> one)
```

## <div id="scala-元组">元组</div>

元组可以理解为一个容器，可以存放各种相同或不同类型的数据。说的简单点，就是将多个无关的数据封装为一个整体，
称为元组

元组最大只有22个元素

声明元素的方式：`(元素1, 元素2, ...)`

```scala
//声明一个元组
val tuple: (String, Int, Double, Boolean, String) = ("hi", 123, 0.1, true, "scala")
```

元组的底层就是一个类名为Tuple，最多有22个Tuple（除非自己写一个）

```scala
val tuple1: Tuple2[String, Int] = ("one", 1)
```

访问元组中的元素，通过下划线然后跟上第几个元素

```scala
//声明一个元组
val tuple: (String, Int, Double, Boolean, String) = ("hi", 123, 0.1, true, "scala")

//打印整个元组
println(tuple) //(hi,123,0.1,true,scala)
//打印元组中的第1个元素
println(tuple._1) //hi
```

还可以根据下标来访问元素

```scala
println(tuple.productElement(0)) //hi
```

遍历整个元组

```scala
for (i <- tuple.productIterator) {
    print(i + ";")
}
//hi;123;0.1;true;scala;
```

元组也可以嵌套元组

```scala
val tuple: ((Int, String), String) = ((1, "one"), "tuple")
println(tuple._1._2) //one
```

## <div id="scala-集合函数">集合函数</div>

在Scala集合中有许多强大的函数，如map、fold等等

集合一些通用的属性和方法

前置对象

```scala
val seq = Seq(1, 2, 3)
val list = List(1, 2, 3)
val set = Set(1, 2, 3)
val map = Map(1 -> "one", 2 -> "two", 3 -> "three")
```

获取集合的长度或者大小

```scala
//序列和列表用length
seq.length
list.length
//集和映射用size
set.size
map.size
```

遍历与迭代器

```scala
//都可以使用foreach
seq.foreach(println)
list.foreach(println)
set.foreach(println)
map.foreach(println)

//都可以使用迭代器
seq.iterator
list.iterator
set.iterator
map.iterator
```

判断是否包含

```scala
seq.contains(1)
list.contains(1)
set.contains(1)
map.contains(1)
```

### 衍生集合方法

获取集合的头和尾，通常来获取序列和列表中的首尾元素

```scala
//获取元素的第一个元素
println(list.head)
println(seq.head)
println(set.head)
println(map.head)

//获取除了头的元素
println(list.tail)
println(seq.tail)
println(set.tail)
println(map.tail)

//获取最后一个元素
println(list.last)
println(seq.last)
println(set.last)
println(map.last)

//获取除了尾的元素
println(seq.init)
println(list.init)
println(set.init)
println(map.init)
```

反转集合

```scala
println(seq.reverse)
println(list.reverse)
//注意set和map没有反转
println(set.toSeq.reverse)
println(map.toSeq.reverse)
```

获取/去掉集合前或后的n个元素

```scala
//获取前两个元素
seq.take(2)
list.take(2)
set.take(2)
map.take(2)

//获取后两个元素
seq.drop(2)
list.drop(2)
set.drop(2)
map.drop(2)

//丢弃前两个元素
seq.drop(2)
list.drop(2)
set.drop(2)
map.drop(2)

//丢弃后两个元素
seq.dropRight(2)
list.dropRight(2)
set.dropRight(2)
map.dropRight(2)
```

并集；将两个集合并在一起，当然Set会去重

```scala
seq.union(seq)
//其他集合（除了Map）...
```

交集：两个集合相交的放在一起

```scala
val seq2 = Seq(0, -1, 3)
seq.intersect(seq2)
//其他集合（除了Map）...
```

差集：两个元素中互相不存在的元素

```scala
val seq2 = Seq(0, -1, 3)
seq.diff(seq2)
//其他集合（除了Map）...
```

拉链：将两个集合交叉放在一个元组中

```scala
val seq2 = Seq(0, -1, 3, 4, 5, 6)
println(seq.zip(seq2)) //List((1,0), (2,-1), (3,3))
```

滑窗：将元素以n个放在一起，返回一个迭代器，默认步长为1

```scala
val seq2 = Seq(0, -1, 3, 4, 5, 6)
seq2.sliding(3).foreach(x => print(s"$x;"))
//List(0, -1, 3);List(-1, 3, 4);List(3, 4, 5);List(4, 5, 6);
```

### 集合简单函数

求和

```scala
seq.sum
list.sum
set.sum
map.keys.sum
```

求乘积

```scala
seq.product
list.product
set.product
map.keys.product
```

最大值

```scala
seq.max
list.max
set.max
map.keys.max

//maxBy根据参数的指定字段进行获取最大值
map.toSeq.maxBy(_._1)
```

最小值

```scala
seq.min
list.min
set.min
map.keys.min

//maxBy根据参数的指定字段进行获取最大值
map.toSeq.minBy(_._1)
```

排序

```scala
//shuffle打乱集合
val seq2 = Random.shuffle(seq ++ Seq(4, 5, 6) ++ seq)
println(seq2) //List(6, 1, 4, 3, 1, 2, 3, 5, 2)
//使用sorted排序
println(seq2.sorted) //List(1, 1, 2, 2, 3, 3, 4, 5, 6)
//sorted方法内部隐式传参，可以使用sorted进行倒叙
println(seq2.sorted(Ordering[Int].reverse))

val seq3 = Random.shuffle(Seq(("a", 1), ("b", 2), ("c", 3), ("d", 4), ("e", 5)))
println(seq3) //List((a,1), (c,3), (e,5), (b,2), (d,4))
//使用sortBy排序
println(seq3.sortBy(_._2)) //List((a,1), (b,2), (c,3), (d,4), (e,5))

//使用sortWith排序，sortWith传入一个函数自定义排序规则
println(seq3.sortWith((x, y) => x._2 > y._2)) //List((e,5), (d,4), (c,3), (b,2), (a,1))
//可简化函数表达式
println(seq3.sortWith(_._2 > _._2)) //List((e,5), (d,4), (c,3), (b,2), (a,1))
```

前置对象

```scala
val seq = Seq(1, 3, 94, 12, 64, 5, 6, 7, 8, 9, 10)
val map = Map("one" -> 1, "four" -> 4, "two" -> 2, "three" -> 3)
```

过滤

```scala
//过滤出偶数
println(seq.filter(_ % 2 == 0)) //List(94, 12, 64, 6, 8, 10)

//没有简化函数
seq.filter((x) => x % 2 == 0)

//再复杂化
def filterEvenNumbers(x: Int): Boolean = {
    x % 2 == 0
}
seq.filter(filterEvenNumbers)
```

映射（将元素变成另一种类型的元素）

```scala
//将每个值乘2
println(seq.map(_ * 2))
//List(2, 6, 188, 24, 128, 10, 12, 14, 16, 18, 20)

//将值变为字符串
println(seq.map(_.toString))
//List(1, 3, 94, 12, 64, 5, 6, 7, 8, 9, 10)

//将值乘二并变为元组
println(seq.map(x => (x, x * 2)))
//List((1,2), (3,6), (94,188), (12,24), (64,128), (5,10), (6,12), (7,14), (8,16), (9,18), (10,20))
```

扁平化（将嵌套集合变为一个集合）

```scala
val seq1 = Seq(List(1, 2, 3), Seq(9, 10, 11))
//扁平化
println(seq1.flatten)
//List(1, 2, 3, 9, 10, 11)
```

扁平化+映射

```scala
val strings = Seq("hello scala", "hi big date", "how are you")
//将一组字符串按空格分开
val stringSeq = strings.map(_.split(" "))
println(stringSeq) //List([Ljava.lang.String;@1f28c152, [Ljava.lang.String;@6325a3ee, [Ljava.lang.String;@1d16f93d)
//使用扁平化将Array分成一个一个的元素
println(stringSeq.flatten)
//List(hello, scala, hi, big, date, how, are, you)

//可以直接使用flatMap进行映射加扁平化
println(strings.flatMap(_.split(" ")))
//List(hello, scala, hi, big, date, how, are, you)
```

分组（将数据分组）

```scala
//根据奇偶将数据分组，分组的Key是函数的返回值
//因为要么是0，要么是1
println(seq.groupBy(_ % 2))
//需要注意分组会将数据变成Map
//Map(1 -> List(1, 3, 5, 7, 9), 0 -> List(94, 12, 64, 6, 8, 10))

//Key可以为任何类型
println(seq.groupBy(x => if (x % 2 == 0) "偶数" else "奇数"))
//Map(奇数 -> List(1, 3, 5, 7, 9), 偶数 -> List(94, 12, 64, 6, 8, 10))
```

归约（将集合元素聚合为单个元素）

```scala
//看源码来如何使用
//传入一个函数，里面要两个参数，并返回一个相同类型的值
//第一次执行将集合中的第一二个数进行处理，并返回值
//将返回的值与集合中下一个数进行相同处理，最终返回一个值
def reduce[A1 >: A](op: (A1, A1) => A1): A1 = reduceLeft(op)
```

使用

```scala
//将所有数拿出来相乘
println(seq.reduce(_ * _)) //-1613447168（超出Int最大值）

//将所有数拿出来相加
println(seq.reduce(_ + _)) //219

//将map中的字符串拼接起来
println(map.toSeq.map(_._1).reduce(_ + ";" + _)) //one;four;two;three
```

折叠（传入一个值和一个操作，将所有操作折叠到值中）

```scala
//将初始值设置为0，将每个数与值相加
println(seq.fold(0)((x, y) => x + y)) //219
```

> fold还有两个相关的方法，分别是foldLeft和foldRight

大数据经典题目（word count）

统计字符串中的单词，并按照出现的次数排序

```scala
//字符串集合
val strings = Seq(
    "hello scala",
    "hi kotlin",
    "i like kotlin",
    "i like scala",
    "hi hadoop",
    "hello hbase",
    "hello spark",
    "hello kotlin",
    "Scala is a powerful programming language"
)

//将字符串按照空白字符进行切分
println(strings.flatMap(_.split("\\s"))
    //分组
    .groupBy(_.toLowerCase)
    //转换Seq更好的操作
    .toSeq
    //统计个数
    .map(x => (x._1, x._2.size))
    //排序
    .sortBy(-_._2))
//Vector((hello,4), (scala,3), (kotlin,3)...)
```

### 并行集合

将集合元素分为多线程操作，这个也让Scala走向了大数据的方向

```scala
//将1到10的数字进行并行处理
println((1 to 10)
    .par
    //获取处理程序的线程名
    .map(_ => Thread.currentThread().getId))
//ParVector(38, 38, 40, 40, 40, 39, 39, 41, 41, 41)
```

## <div id="scala-队列">队列</div>

队列具有**先进先出**的原则，在一些操作时可能会用到队列

```scala
//可变队列
val mutableQueue = mutable.Queue(1, 2, 3)

//传入一个元素
mutableQueue.enqueue(5)

//取出元素
println(mutableQueue.dequeue) //1
println(mutableQueue.dequeue) //2
println(mutableQueue.dequeue) //3
//只剩下后来传入的元素了
println(mutableQueue) //Queue(5)


//不可变队列
val immutableQueue = Queue(1, 2, 3)
//传入一个元素
var queue = immutableQueue.enqueue(5)

//不可变队列使用dequeue取出元素，并返回一个新集合，返回值是一个队列
```

## <div id="scala-模式匹配">模式匹配</div>

模式匹配对应于Java的switch分支语句。在模式匹配的语法中，
每个分支采用 case 关键字进行声明，如果匹配成功就会进入对应的逻辑代码，
如果都不匹配那么会执行case _分支类似于Java的default语句

基本语法：

```text
返回值 变量 match {
    case 匹配条件 => 匹配成功执行的逻辑代码
    case 匹配条件 => 匹配成功执行的逻辑代码
    case _ => 匹配失败执行的逻辑代码
}
```

```scala
val result = 1 match {
    case 1 => "one"
    case 2 => "one"
    case _ => "other"
}

println(result) //one
```

还可以将匹配模式作用于方法中

```scala
def result(x: Int): String = x match {
    case 1 => "one"
    case 2 => "one"
    case _ => "other"
}

println(result(1)) //one
```

需要注意的是，如果没有case _作为兜底，且元素匹配的值不在范围内，会报出MatchError

模式守卫，可以在case后跟上条件判断变量是否满足条件

```scala
def result(x: Int): String = x match {
    case x if x < 1 => "less than one"
    case 2 => "one"
    case _ => "other"
}

println(result(-1)) //less than one
```

匹配常量

```scala
val result = 1 match {
    case 1 => "one"
    case 2 => "one"
    case _ => "other"
}

println(result) //one
```

匹配类型

```scala
val result = 0 match {
    case d: Double => "is double"
    case i: Int => "is int"
    case _ => "other"
}

println(result) //is int
```

匹配数组

```scala
val str = Array("hi") match {
    case Array("hi") => "hi"
    case Array("hi", "你好") => "两个元素相等"
    case Array(x, y) => s"匹配两个元素分别是 $x, $y"
    case Array("hello", _*) => "以hello开头的数组"
    case Array(x, "hi", y) => "中间是hi的三位数数组"
    case _ => "other"
}

println(str) //hi
```

序列也行

```scala
val str = Seq("", "hi", "") match {
    case Seq("hi") => "hi"
    case Seq("hi", "你好") => "两个元素相等"
    case Seq(x, y) => s"匹配两个元素分别是 $x, $y"
    case Seq("hello", _*) => "以hello开头的数组"
    case Seq(x, "hi", y) => "中间是hi的三位数数组"
    case _ => "other"
}

println(str) //中间是hi的三位数数组
```

列表特殊写法

```scala
val result = List(1, 3, 5, 6, 7) match {
    case one :: two :: list => s"这是$list"
    case _ => "other"
}

//其中list是列表，元素可能是0和n个，但是one和two只能只能是各占一个
//所以one是1，two是2，list是5,6,7
println(result) //这是List(5, 6, 7)
```

元组匹配

```scala
val result = (1, "hi", true) match {
    case (x, y, z: Boolean) => "匹配三个元素，且最后一个元素类型为布尔"
    case (1, a, _) => s"匹配三个元素中第一个元素为1的元素: $a"
    case _ => "other"
}

println(result) //匹配三个元素，且最后一个元素类型为布尔
```

在变量声明时匹配

```scala
//元组变量赋值
val (x, y) = (1, 2)
println("x=" + x + ", y=" + y)

//将变量也分为List，值转移给变量中
val List(first, second, _*) = List(1, 3, 5, 6)
println("first=" + first + " and second=" + second)

//List变量赋值
val fir :: sec :: rest = List(1, 2, 3, 4, 5)
println("fir=" + fir + " and second=" + sec + " and rest=" + rest)
```

for推导式中的变量

```scala
val tuple = List((1, "hi"), (1, "你好"), (1, "こんにちは"), (1, "안녕하세요"), (1, "Здравствуйте"))

for ((_, v) <- tuple) {
    println(v)
}
```

对象模式匹配

```scala
//定义运行类
object Main extends App {
    //定义两个对象
    val bob = Person("bob", 18)
    val alice = Person("alice", 18)

    //创建匹配模式方法
    def matchPerson(person: Person): String = person match {
        case Person(name, 18) => s"$name 18 years old"
    }

    //调用打印
    println(matchPerson(bob)) //bob 18 years old
    println(matchPerson(alice)) //alice 18 years old
}

//Person对象
class Person(val name: String, val age: Int)

//Person伴生对象
object Person {
    def apply(name: String, age: Int): Person = new Person(name, age)

    //解构方法
    def unapply(p: Person): Option[(String, Int)] = Some((p.name, p.age))
}
```

定义样例类，里面包含unapply和apply自动封装的方法

```scala
object Main extends App {
    val bob = Person("bob", 18)
    val alice = Person("alice", 18)

    def matchPerson(person: Person): String = person match {
        case Person(name, 18) => s"$name 18 years old"
    }

    println(matchPerson(bob)) //bob 18 years old
    println(matchPerson(alice)) //alice 18 years old
}

case class Person(name: String, age: Int)
```

### 偏函数

偏函数也是函数的一种，通过偏函数我们可以方便的对输入参数做更精准的检查

```text
val 偏函数名 : 偏函数类型[参数类型 , 返回值类型] = {
    case语句
}
```

使用偏函数在lambda中，可以想想偏函数是match中的一小段case语句

```scala
val tuples = Seq(("a", 1), ("b", 2), ("c", 3), ("d", 4), ("e", 5))

println(tuples.map {
    //使用偏函数（想象这是match中的一个case语句）
    case (a, b) => (a, b - 1)
}) //List((a,0), (b,1), (c,2), (d,3), (e,4))
```

偏函数的应用

```scala
//偏函数的定义
val isString: PartialFunction[Any, Option[Boolean]] = {
    case s: String => Some(true)
}

//偏函数的定义
val isInt: PartialFunction[Any, Option[Boolean]] = {
    case i: Int => Some(true)
}

//偏函数的定义
val none: PartialFunction[Any, Option[Boolean]] = {
    case _ => None
}

//组合在一起并打印
//判断“aa”是否是String、Int、什么也不是
println(isString.orElse(isInt).orElse(none)("aa").get) //true
//判断0f是否是String、Int、什么也不是
println(isString.orElse(isInt).orElse(none)(0f)) //None
```

> 偏函数就像是多个部分函数组成一个函数

## <div id="scala-异常处理">异常处理</div>

Scala中的异常处理和Java类似

基本语法

```text
try {
    要进行捕捉的代码
} catch {
    case 异常变量名 : 异常类型 => { 异常处理代码块 }
    case 异常变量名 : 异常类型 => { 异常处理代码块 }
    ...
} finally {
    finally代码块
}
```

我们将可疑代码装在try块中，之后使用catch捕捉异常  
需要注意的是Scala工作机制和Java一致，但是**Scala没有编译期异常**  
catch是按照声明顺序从上往下，当然最好把具体的异常放在前面，普遍的异常放在后面  
finally和Java中一致，不管有没有异常都有进行处理  
可以使用throw抛出一个异常对象，因为Noting是所有类型的子类型，所以可以这样写

```scala
val none: Nothing = throw new RuntimeException("第一个异常")

def nothing(): Nothing = throw new RuntimeException("第二个异常")

nothing() //不会执行，第一个异常已经抛出
println("Hello, world!") //无法打印这句话
```

异常处理

```scala
val string: String = try {
    val i = 1 / 0
    "执行成功"
} catch {
    case e: ArithmeticException => s"算术异常: ${e.getMessage}"
    case e: RuntimeException => s"通用异常: ${e.getMessage}"
} finally {
    println("执行完成") //执行完成
}

println(string) //算术异常: / by zero
```

## <div id="scala-隐式转换">隐式转换</div>

当编译器第一次编译失败的时候，会在当前的环境中查找能让代码编译通过的方法，用于将类型进行转换，实现二次编译

**隐式转换是一个强大且危险的功能**，隐式转换可以在不需改任何代码的情况下，扩展某个类的功能

> Scala编译时间长的原因找到了！

Scala的隐式成员有：隐式方法，隐式传参，隐式值，隐式类

隐式方法

```scala
implicit def intToString(x: Int): String = x.toString

//使用Int调用其他对象方法，调用String中的indexOf方法
val i: Int = 123111.indexOf("2")
//2的下标1
println(i) //1
```

隐式传参，隐式值

```scala
def sayHi(implicit s: String): Unit = println(s"Hi! $s")

//使用隐式参数需要隐式值，否则隐式参数找不到值
implicit var name: String = "bob"

//如果带上小括号会报错
sayHi //Hi! bob
name = "alice"
sayHi //Hi! alice
```

隐式参数在Scala底层，它是一种柯里化的表达，如果想在sayHi调用时加上小括号，
如果不加小括号底层默认认为你是一个无括号的函数（无括号函数调用时无法加上小括号）

```scala
//添加一个小括号
def sayHi()(implicit s: String): Unit = println(s"Hi! $s")

implicit var name: String = "bob"

//加上小括号不会报错
sayHi() //Hi! bob
```

需要注意的是，传入隐式值是根据类型来进行传入的，如果有两个类型相同的隐式值，
隐式传参就不知道该传哪个了，导致报错

隐式传参还可以和默认传参一起写

```scala
implicit var name: String = "bob"

def sayHi(implicit s: String = "alice"): Unit = println(s"Hi! $s")
//加上默认传参可以加上小括号
//隐式值的优先级要大于（覆盖）默认传参
sayHi() //Hi! alice
```

隐式传参的简便写法

```scala
implicit var name: String = "bob"

//直接通过implicitly[类型]来查找调用隐式值
def sayHello(): Unit = println(s"Hi! ${implicitly[String]}")

sayHello() //Hi! bob
```

## <div id="scala-泛型">泛型</div>

泛型在Java中使用`<>`表示而Scala使用`[]`表示

泛型的协变和逆变

基本语法：

```text
class 类名[+T] {} //协变
class 类名[-T] {} //逆变
class 类名[T] {} //不变
```

代码声明

```scala
//在不变的情况下：[T]
// 成功
val collection: CollectionClass1[Person] = new CollectionClass1[Person]
// 报错，因为声明时和实际的泛型不一致
// val collection1: CollectionClass[Person] = new CollectionClass[Child]
// 报错，因为声明时和实际的泛型不一致
// val collection2: CollectionClass[Child] = new CollectionClass[Person]

//在协变的情况下：[+T]
// 成功，允许子类声明时为父类发泛型
val collection3: CollectionClass2[Person] = new CollectionClass2[Child]

//在逆变的情况下
// 成功，允许父类声明时为子类泛型
val collection4: CollectionClass3[Child] = new CollectionClass3[Person]

//声明两个类并实现继承关系
case class Person()

case class Child() extends Person()

//创建集合类
class CollectionClass1[T]

class CollectionClass2[+T]

class CollectionClass3[-T]
```

泛型的上下限

基本语法：

```text
class 类名[T <: Person] {} //泛型上限
class 类名[T >: Person] {} //泛型下限
```

泛型的上下限的作用是对传入的泛型进行限定

```scala
//继承Person类的可以传入
new CollectionClass1[Child](Class[Child]).print()
//Child类的父类可以传入
new CollectionClass2[Person](Class[Person]).print()

//声明两个类并实现继承关系
case class Person()

case class Child() extends Person()

//创建集合类
class CollectionClass1[T <: Person](val clazz: Class[T]) {
    def print(): Unit = println(clazz.getName)
}

class CollectionClass2[T >: Child](val clazz: Class[T]) {
    def print(): Unit = println(clazz.getName)
}
```

上下文限定

基本语法：

```text
def f[A : B](a: A) = println //等同于 def f[A](a: A)(implicit arg:B[A]) = println(a)
```

上下文限定是将泛型和隐式转换的结合产物，简化隐式参数的传递，强调"某个存在的能力"，
通过implicitly获取隐式实例

```scala
//定义隐式参数
implicit val printerInt: Printer[Int] = (t: Int) => println(t)
// (t: Int) => println(t) 等价于 println
implicit val printerString: Printer[String] = println

//通过隐式参数处理方法
def print[T: Printer](t: T): Unit = {
    implicitly[Printer[T]].show(t)
}

print(55) //55
print("Hello") //Hello
```