---
title: Java基础
date: 2021-01-09 14:31:19
tags:
typora-root-url: ..\img
---
<!-- toc -->
# 基础概念

## java与其他语言

- java与C#甚至有90%的重叠 两者都对c++的一些地方做了修正，例如宏替换，两者都是单继承多接口

- python解释型语言  
## java语言运行机制

  Java 源程序与编译型运行区别

![image](https://www.runoob.com/wp-content/uploads/2013/12/ZSSDMld.png)

## 编译型语言和解释型语言

编译型语言是指使用专门的编译器 针对特定平台翻译成机器码在特定平台上运行

现有的c，c++，objectc，pascal都是编译型语言

解释型语言是指使用特定的解释器解释成特定的机器码并立即运行的语言。

可以认为解释型语言每次执行都需要进行一次编译因此效率极低而且不能脱离解释器独立运行。但解释性语言哭泣平台比较容易，只要提供特定平台的解释器即可

除此之外还有一种伪编译型语言vb。

## jvm

- 指令集

- 寄存器

- 类文件的格式

- 栈

- 垃圾回收堆

- 存储区

  ​						

## 程序的三种结构

  - 顺序
  - 选择
  - 循环
## 面向对象的特征
###  封装

将对象的实现细节隐藏起来，通过一些公共方法来暴露对象的功能

###  继承

实现软件复用的重要手段，通过继承获得父类的属性和方法（行为）

在 Java 中，一个类可以由其他类派生。如果你要创建一个类，而且已经存在一个类具有你所需要的属性或方法，那么你可以将新创建的类继承该类。

利用继承的方法，可以重用已存在类的方法和属性，而不用重写这些代码。被继承的类称为超类（super class），派生类称为子类（subclass）。

继承是描述 is a的关系。

###  多态

指子类对象可以直接赋给父类变量，但运行时依然表现出**子类的行为特征**，这意味着同一个类型的对象在执行同一个方法时，可能表现出多种行为特征

### 抽象

抽象就是忽略一个主题中与当前目标无关的那些方面，以便更充分地注意与当前目标有关的方面

## 对象
 对象是类的一个实例，他有状态和行为。

### 基于对象和面向对象

基于没有继承的概念，例如js，只是封装好对象你使用，但你不能派生出新的对象

## 类
  类是一个模板，他描述一类对象的行为和状态



## 方法
方法就是行为，一个类可以有很多方法
## 实例变量
每个对象都有独特的实例变量，对象的状态由这些实例状态的值决定

## 软件设计的步骤

OOA---OOD——OOP

# 基本语法
- 大小写敏感
- 类名：类的首字母大写，如果有多个单词组成，每个单词首字母都应该大写
- 方法名 ：起始字母小写，其他单词首字母大写
- 源文件名 ：应与类名相同
- 主方法入口：
```java
//所有使用java语言的都是
public static void main(String[] args){}
```
## 基本数据类型

- 整型
  - byte  8位  -128-127
  - short 16 
  - long 64
  - int 32
  - http://www.360doc.com/content/20/0513/00/69475900_911880617.shtml

   0正1负

计算机都是用补码表示的，补码-1取反（除符号位），很奇妙可以组成一个闭环，例如127+1=-128，

反之亦然，因为溢出了。

ob 或0B  二进制

0   8进制

0x  16进制

可以使用下划线分割数据1_000 java7之后自动分辨





## java运算符

[<<<] [>>>] 无符号左移右移

## java 循环结构

- while 循环

``` 
  while（true）{}
```

- do…while 循环
  对于 while 语句而言，如果不满足条件，则不能进入循环。但有时候我们需要即使不满足条件，也至少执行一次。

do…while 循环和 while 循环相似，不同的是，do…while 循环至少会执行一次。

- for循环
  虽然所有循环结构都可以用 while 或者 do...while表示，但 Java 提供了另一种语句 —— for 循环，使一些循环结构变得更加简单。

for循环执行的次数是在执行前就确定的。语法格式如下：

for(初始化; 布尔表达式; 更新) {
    //代码语句
}

- Java 增强 for 循环
  Java5 引入了一种主要用于数组的增强型 for 循环。

Java 增强 for 循环语法格式如下:

for(声明语句 : 表达式)
{
   //代码句子
}

- break 关键字
  break 主要用在循环语句或者 switch 语句中，用来跳出整个语句块。

break 跳出最里层的循环，并且继续执行该循环下面的语句。

语法
break 的用法很简单，就是循环结构中的一条语句：

break;

- continue 关键字
  continue 适用于任何循环控制结构中。作用是让程序立刻跳转到下一次循环的迭代。
  ==在 for 循环中，continue 语句使程序立即跳转到更新语句。==

==在 while 或者 do…while 循环中，程序立即跳转到布尔表达式的判断语句==。

## java标识符

Java 所有的组成部分都需要名字。==类名、变量名以及方法名都被称为标识符==。
- 所有的标识符都应该以字母（A-Z 或者 a-z）,美元符（$）、或者下划线（_）开始
- 首字符之后可以是字母（A-Z 或者 a-z）,美元符（$）、下划线（_）或数字的任何字符组合
- 关键字不能用作标识符
- 标识符是大小写敏感的
合法标识符举例：age、$salary、_value、__1_value
非法标识符举例：123abc、-salary

总结起来 就是三个 字母美元下划线开头，后面可以跟数字

### 不用数字开头的原因
 标示符（ID_entifier）是指用来标识某个实体的一个符号。在不同的应用环境下有不同的含义。比如，在日常生活中，某人的姓名；在数学解方程时，用到这样或那样的变量名或函数名；在编程语言中，标识符是为变量、常量、函数、等起的名字。所有这些，统统称为标识符。标识符可能是字母、符号，或由上述元素构成的组合。
多种语言表示数值的方法，第一个字符要求一定要是数字字符，尽管后面的字符可能不一定是数字字符。
下列JAVA代码声明不同类型数值的标识符(左边：变量类型 标识符)，并以相应的数值初始化(右边：变量数值)。
为了有效区别"数字值"与其"标识符"，必须对标识符有所约束。
比如下列 Java 代码的第一个声明，若取数字字符'0'为 这个 8 进制数值变量的标识符，即
int 0 = 0321；
那么，赋值操作符 '=' 两边的符号均为数字字符，两者无法区分。

所以，Java 语言规定，标识符的第一个字符不允许是数字字符，但第一个字符可以是下划线'_'。于是，下列Java代码的标识符的第一个字符只要取为下划线'_', 第二个字符是什么数字字符都无妨了。

再比如，下列 Java 代码的最后一个声明:
double e = 3e3;
如果标识符允许第一个字符为数字字符的话，那么 3e3 既可表示标识符(变量名)，亦可表示数值：3*10^3, 编译时会显示二义性。

为了避免上述弊端，多种编程语言对标识符的命名法，均做出严格规定：标识符不能以数字字符开头。

## java修饰符
像其他语言一样，Java可以使用修饰符来修饰类中方法和属性。主要有两类修饰符：

访问控制修饰符 : default, public , protected, private
非访问控制修饰符 : final, abstract, static, synchronized
## java变量
 局部变量
 静态变量又称类变量
 成员变量（非静态变量）
 ## Java 数组
 数组是储存在堆上的对象，可以保存多个同类型变量
 ## Java 枚举
 Java 5.0引入了枚举，枚举限制变量只能是预先设定好的值。使用枚举可以减少代码中的 bug。
 ## java 关键字
<table class="reference">
<tbody><tr>
<th>类别</th>
<th>关键字</th>
<th>说明</th>
</tr>
<tr>
<td rowspan="3" align="center">访问控制</td>
<td>private</td>
<td>私有的</td>
</tr>
<tr>
<td>protected</td>
<td>受保护的</td>
</tr>
<tr>
<td>public</td>
<td>公共的</td>
</tr>
<tr>
<td rowspan="13" align="center">类、方法和变量修饰符</td>
<td>abstract</td>
<td>声明抽象</td>
</tr>
<tr>
<td>class</td>
<td>类</td>
</tr>
<tr>
<td>extends</td>
<td>扩充,继承</td>
</tr>
<tr>
<td>final</td>
<td>最终值,不可改变的</td>
</tr>
<tr>
<td>implements</td>
<td>实现（接口）</td>
</tr>
<tr>
<td>interface</td>
<td>接口</td>
</tr>
<tr>
<td>native</td>
<td>本地，原生方法（非 Java 实现）</td>
</tr>
<tr>
<td>new</td>
<td>新,创建</td>
</tr>
<tr>
<td>static</td>
<td>静态</td>
</tr>
<tr>
<td>strictfp</td>
<td>严格,精准</td>
</tr>
<tr>
<td>synchronized</td>
<td>线程,同步</td>
</tr>
<tr>
<td>transient</td>
<td>短暂</td>
</tr>
<tr>
<td>volatile</td>
<td>易失</td>
</tr>
<tr>
<td rowspan="12" align="center">程序控制语句</td>
<td>break</td>
<td>跳出循环</td>
</tr>
<tr>
<td>case</td>
<td>定义一个值以供 switch 选择</td>
</tr>
<tr>
<td>continue</td>
<td>继续</td>
</tr>
<tr>
<td>default</td>
<td>默认</td>
</tr>
<tr>
<td>do</td>
<td>运行</td>
</tr>
<tr>
<td>else</td>
<td>否则</td>
</tr>
<tr>
<td>for</td>
<td>循环</td>
</tr>
<tr>
<td>if</td>
<td>如果</td>
</tr>
<tr>
<td>instanceof</td>
<td>实例</td>
</tr>
<tr>
<td>return</td>
<td>返回</td>
</tr>
<tr>
<td>switch</td>
<td>根据值选择执行</td>
</tr>
<tr>
<td>while</td>
<td>循环</td>
</tr>
<tr>
<td rowspan="6" align="center">错误处理</td>
<td>assert</td>
<td>断言表达式是否为真</td>
</tr>
<tr>
<td>catch</td>
<td>捕捉异常</td>
</tr>
<tr>
<td>finally</td>
<td>有没有异常都执行</td>
</tr>
<tr>
<td>throw</td>
<td>抛出一个异常对象</td>
</tr>
<tr>
<td>throws</td>
<td>声明一个异常可能被抛出</td>
</tr>
<tr>
<td>try</td>
<td>捕获异常</td>
</tr>
<tr>
<td rowspan="2" align="center">包相关</td>
<td>import</td>
<td>引入</td>
</tr>
<tr>
<td>package</td>
<td>包</td>
</tr>
<tr>
<td rowspan="8" align="center">基本类型</td>
<td>boolean</td>
<td>布尔型</td>
</tr>
<tr>
<td>byte</td>
<td>字节型</td>
</tr>
<tr>
<td>char</td>
<td>字符型</td>
</tr>
<tr>
<td>double</td>
<td>双精度浮点</td>
</tr>
<tr>
<td>float</td>
<td>单精度浮点</td>
</tr>
<tr>
<td>int</td>
<td>整型</td>
</tr>
<tr>
<td>long</td>
<td>长整型</td>
</tr>
<tr>
<td>short</td>
<td>短整型</td>
</tr>
<tr>
<td rowspan="3" align="center">变量引用</td>
<td>super</td>
<td>父类,超类</td>
</tr>
<tr>
<td>this</td>
<td>本类</td>
</tr>
<tr>
<td>void</td>
<td>无返回值</td>
</tr>
<tr>
<td rowspan="3" align="center">保留关键字</td>
<td>goto</td>
<td>是关键字，但不能使用</td>
</tr>
<tr>
<td>const</td>
<td>是关键字，但不能使用</td>
</tr>
<tr>
<td>null</td>
<td>空</td>
</tr>
</tbody></table>





------



## Java注释
三种

单行注释，多行注释，文档注释



## 接口
在 Java 中，接口可理解为对象间相互通信的协议。接口在继承中扮演着很重要的角色。

接口只定义派生要用到的方法，但是方法的具体实现完全取决于派生类。



## 对象与垃圾回收

- 垃圾回收机制只会回收堆里的对象，其他物理资源不回收，例如物理资源数据库链接
- 回收无法精确进行 对象永久失去引用后
- 调用finilize（） 该方法可能使对象复活
## 对象的软弱虚引用
- 强
- 软 需要通过SoftReferececence类来使用，当系统内存空间不足时，系统可能会回收它 
- 弱 弱引用级别更低  WeakREference 当系统垃圾回收机制开始时，不管内存是否足够，都会回收
- 虚 PhanotmReference  相当于没有引用，主要是用来跟踪对象被垃圾回收的状态，必须和引用队列ReferenceQenue一起使用
# Java的基础类库

## 与用户互动

- Scanner 
## 系统相关

- System类 代表当前的运行平台 ，提供了标准输入标准输出错误输出的类变量，并提供了一些方法访问环境变量，系统属性的方法，加载动态连接库
- runtime类代表java运行时环境 可以gc，执行操作系统的一个命令 runtime.exec("dfdsf.exe")
## 常用类
- Object   当定义一个类没有使用extends关键字指定父类，默认继承object类。

​           Class<?> getClass（）获取运行时类

​            int hashcode（）返回hashcode值，即对象的地址值，与identifyhashcode计算结果相同，但是很多已经重写，不在返回地址值

​         toString（）返回运行时类@16进制hashcode值

​        clone（） 只是复制了一份副本

- Objects类

   工具类（java 的工具类名称一般都是s结尾）

  Objects.requireNonNull 校验空，抛出异常或者返回参数本身

- String StringBuffer StringBuilder

  - String

  String并不是基本数据类型，而是一个对象，并且是不可变的对象。查看源码就会发现String类为final型的（当然也不可被继承），而且通过查看JDK文档会发现几乎每一个修改String对象的操作，实际上都是创建了一个全新的String对象

  字符串为对象，那么在初始化之前，它的值为null，到这里就有必要提下””、null、new String()三者的区别。null 表示string还没有new ，也就是说对象的引用还没有创建，也没有分配内存空间给他，而””、new String()则说明了已经new了，只不过内部为空，但是它创建了对象的引用，是需要分配内存空间的。打个比方：一个空玻璃杯，你不能说它里面什么都没有，因为里面有空气，当然也可以把它弄成真空，null与" "、new String()的区别就象真空与空气一样。

   在字符串中存在一个非常特殊的地方，那就是字符串池。每当我们创建一个字符串对象时，首先就会检查字符串池中是否存在面值相等的字符串，如果有，则不再创建，直接放回字符串池中对该对象的引用，若没有则创建然后放入到字符串池中并且返回新建对象的引用。这个机制是非常有用的，因为可以提高效率，减少了内存空间的占用。所以在使用字符串的过程中，推荐使用直接赋值（即String s=”aa”），除非有必要才会新建一个String对象（即String s = new String(”aa”)）。

  String直接赋值和使用new的区别

  String str1 = “ABC”;可能创建一个或者不创建对象，如果”ABC”这个字符串在java String池里不存在，会在java String池里创建一个创建一个String对象(“ABC”)，然后str1指向这个内存地址，无论以后用这种方式创建多少个值为”ABC”的字符串对象，始终只有一个内存地址被分配，之后的都是String的拷贝，Java中称为“字符串驻留”，所有的字符串常量都会在编译之后自动地驻留。

  String str2 = new String(“ABC”);至少创建一个对象，也可能两个。因为用到new关键字，肯定会在heap中创建一个str2的String对象，它的value是“ABC”。同时如果这个字符串再java String池里不存在，会在java池里创建这个String对象“ABC”。

  在JVM里，考虑到垃圾回收（Garbage Collection）的方便，将heap(堆)划分为三部分：young generation(新生代)、tenured generation （old generation）（旧生代）、permanent generation（永生代）。

  字符串为了解决字符串重复问题，生命周期长，存于pergment中。

  JVM中，相应的类被加载运行后，常量池对应的映射到JVM运行时的常量池中

  建议在平时的使用中，尽量使用String = “abcd”;这种方式来创建字符串，而不是String = new String(“abcd”);这种形式，因为使用new构造器创建字符串对象一定会开辟一个新的heap空间，而双引号则是采用了String interning(**字符串驻留**)进行了优化，效率比构造器高

  - StringBuffer

    StringBuffer和String一样都是用来存储字符串的，只不过由于他们内部的实现方式不同，导致他们所使用的范围不同，对于StringBuffer而言，他在处理字符串时，若是对其进行修改操作，它并不会产生一个新的字符串对象，所以说在内存使用方面它是优于String的。

      其实在使用方法，StringBuffer的许多方法和String类都差不多，所表示的功能几乎一模一样，只不过在修改时StringBuffer都是修改自身，而String类则是产生一个新的对象，这是他们之间最大的区别。

      同时StringBuffer是不能使用=进行初始化的，它必须要产生StringBuffer实例，也就是说你必须通过它的构造方法进行初始化。

      在StringBuffer的使用方面，它更加侧重于对字符串的变化，例如追加、修改、删除，相对应的方法：

      1、append()：追加指定内容到当前StringBuffer对象的末尾，类似于字符串的连接，这里StringBuffer对象的内容会发生改变。

      2、insert：该类方法主要是在StringBuffer对象中插入内容。

      3、delete：该类方法主要用于移除StringBuffer对象中的内容。

  - 

  - StringBuilder

   StringBuilder也是一个可变的字符串对象，他与StringBuffer不同之处就在于它是线程不安全的，基于这点，它的速度一般都比StringBuffer快。与StringBuffer一样，StringBuider的主要操作也是append与insert方法。这两个方法都能有效地将给定的数据转换成字符串，然后将该字符串的字符添加或插入到字符串生成器中。

  - 如何正确使用

    ![20131226204829250](\Java 基础\20131226204829250.png)

    

    

    1、String：在字符串不经常变化的场景中可以使用String类，如：常量的声明、少量的变量运算等。

    ​     2、StringBuffer：在频繁进行字符串的运算（拼接、替换、删除等），并且运行在多线程的环境中，则可以考虑使用StringBuffer，例如XML解析、HTTP参数解析和封装等。

    ​     3、StringBuilder：在频繁进行字符串的运算（拼接、替换、删除等），并且运行在多线程的环境中，则可以考虑使用StringBuffer，如SQL语句的拼装、JSON封装等（貌似这两个我也是使用|StringBuffer）。

- Math
- ThreadLocalRandom  与Random   前者是后者为了减少多线程竞争的类
- BigDecimal 使用string作为参数可以减少精度损失
- Date类 过时不推荐使用
- Calendar类
- DateFormat  NumberFormat  MessageFormat

## 使用序列化实现对象的拷贝

- 浅拷贝

    1、 基本类型

  ​     如果变量是基本很类型，则拷贝其值，比如int、float等。

     2、 对象

  ​     如果变量是一个实例对象，则**拷贝其地址引用**，也就是说此时新对象与原来对象是公用该实例变量。

     3、 String字符串

  ​     若变量为String字符串，则拷贝其地址引用。但是在修改时，它会从字符串池中重新生成一个新的字符串，原有对象保持不变

- 深拷贝

  内存中通过字节流的拷贝是比较容易实现的。把母对象写入到一个字节流中，再从字节流中将其读出来，这样就可以创建一个新的对象了，并且该新对象与母对象之间并不存在引用共享的问题，真正实现对象的深拷贝

  ```java
  public class CloneUtils {
      @SuppressWarnings("unchecked")
      public static <T extends Serializable> T clone(T obj){
          T cloneObj = null;
          try {
              //写入字节流
              ByteArrayOutputStream out = new ByteArrayOutputStream();
              ObjectOutputStream obs = new ObjectOutputStream(out);
              obs.writeObject(obj);
              obs.close();
             
              //分配内存，写入原始对象，生成新对象
              ByteArrayInputStream ios = new ByteArrayInputStream(out.toByteArray());
              ObjectInputStream ois = new ObjectInputStream(ios);
              //返回生成的新对象
              cloneObj = (T) ois.readObject();
              ois.close();
          } catch (Exception e) {
              e.printStackTrace();
          }
          return cloneObj;
      }
  }
  ```

  使用该工具类的对象必须要实现Serializable接口，否则是没有办法实现克隆的

## 基本数据类型的取值范围
[先了解下补码](https://www.cnblogs.com/tuojunjie/p/6383624.html)
Java语言提供了八种基本类型。六种数字类型（四个整数型，两个浮点型），一种字符类型，还有一种布尔型。

- byte：

byte 数据类型是8位、有符号的，以二进制补码表示的整数；
最小值是 -128（-2^7）；
最大值是 127（2^7-1）；
默认值是 0；
byte 类型用在大型数组中节约空间，主要代替整数，因为 byte 变量占用的空间只有 int 类型的四分之一；
例子：byte a = 100，byte b = -50。
- short：

short 数据类型是 16 位、有符号的以二进制补码表示的整数
最小值是 -32768（-2^15）；
最大值是 32767（2^15 - 1）；
Short 数据类型也可以像 byte 那样节省空间。一个short变量是int型变量所占空间的二分之一；
默认值是 0；
例子：short s = 1000，short r = -20000。
- int：

int 数据类型是32位、有符号的以二进制补码表示的整数；
最小值是 -2,147,483,648（-2^31）；
最大值是 2,147,483,647（2^31 - 1）；
一般地整型变量默认为 int 类型；
默认值是 0 ；
例子：int a = 100000, int b = -200000。
long：

- long 数据类型是 64 位、有符号的以二进制补码表示的整数；
最小值是 -9,223,372,036,854,775,808（-2^63）；
最大值是 9,223,372,036,854,775,807（2^63 -1）；
这种类型主要使用在需要比较大整数的系统上；
默认值是 0L；
例子： long a = 100000L，Long b = -200000L。
"L"理论上不分大小写，但是若写成"l"容易与数字"1"混淆，不容易分辩。所以最好大写。
- float：

float 数据类型是单精度、32位、符合IEEE 754标准的浮点数；
float 在储存大型浮点数组的时候可节省内存空间；
默认值是 0.0f；
浮点数不能用来表示精确的值，如货币；
例子：float f1 = 234.5f。
- double：

double 数据类型是双精度、64 位、符合IEEE 754标准的浮点数；
浮点数的默认类型为double类型；
double类型同样不能表示精确的值，如货币；
默认值是 0.0d；
例子：double d1 = 123.4。
- boolean：

boolean数据类型表示一位的信息；
只有两个取值：true 和 false；
这种类型只作为一种标志来记录 true/false 情况；
==默认值是 false==；
例子：boolean one = true。
- char：

char类型是一个单一的 16 位 Unicode 字符；
最小值是 \u0000（即为0）；
最大值是 \uffff（即为65,535）；
char 数据类型可以储存任何字符；
例子：char letter = 'A';

## 引用类型
## 访问控制修饰符
<table class="reference">
<caption style="font-weight: bold;font-size:16px;font-weight: bold;" id="accesscontrol-levels">访问控制</caption>
<tbody><tr>
<th>修饰符</th>
<th>当前类</th>
<th>同一包内</th>
<th>子孙类(同一包)</th>
<th>子孙类(不同包)</th>
<th>其他包</th>
</tr>
<tr>
<td headers="h1"><code>public</code></td>
<td headers="h2">Y</td>
<td headers="h3">Y</td>
<td headers="h4">Y</td>
<td headers="h5">Y</td>
<td headers="h6">Y</td>
</tr>
<tr>
<td headers="h1"><code>protected</code></td>
<td headers="h2">Y</td>
<td headers="h3">Y</td>
<td headers="h4">Y</td>
<td headers="h5">Y/N（<a href="#protected-desc">说明</a>）</td>
<td headers="h6">N</td>
</tr>
<tr>
<td headers="h1"><code>default</code></td>
<td headers="h2">Y</td>
<td headers="h3">Y</td>
<td headers="h4">Y</td>
<td headers="h5">N</td>
<td headers="h6">N</td>
</tr>
<tr>
<td headers="h1"><code>private</code></td>
<td headers="h2">Y</td>
<td headers="h3">N</td>
<td headers="h4">N</td>
<td headers="h5">N</td>
<td headers="h6">N</td>
</tr>
</tbody></table>
默认访问修饰符-不使用任何关键字
使用默认访问修饰符声明的变量和方法，对同一个包内的类是可见的。接口里的变量都隐式声明为 public static final,而接口里的方法默认情况下访问权限为 public。


- ==受保护的访问修饰符-protected
protected== 需要从以下两个点来分析说明：

子类与基类在同一包中：被声明为 protected 的变量、方法和构造器能被同一个包中的任何其他类访问；

子类与基类不在同一包中：那么在子类中，子类实例可以访问其从基类继承而来的 protected 方法，而不能访问基类实例的protected方法。

## 非访问控制修饰符
为了实现一些其他的功能，Java 也提供了许多非访问修饰符。

static 修饰符，用来修饰类方法和类变量。 属于类不属于某一个实例变量，或者说被说有实例共享，所以this不能使用，只能访问静态变量静态方法

final 修饰符，用来修饰类、方法和变量，final 修饰的类不能够被继承，修饰的方法不能被继承类重新定义，修饰的变量为常量，是不可修改的。

abstract 修饰符，用来创建抽象类和抽象方法。

synchronized 和 volatile 修饰符，主要用于线程的编程。

static 修饰符
静态变量：

static 关键字用来声明独立于对象的静态变量，无论一个类实例化多少对象，它的静态变量只有一份拷贝。 静态变量也被称为类变量。局部变量不能被声明为 static 变量。

静态方法：

static 关键字用来声明独立于对象的静态方法。静态方法不能使用类的非静态变量。静态方法从参数列表得到数据，然后计算这些数据

synchronized 修饰符
synchronized 关键字声明的方法同一时间只能被一个线程访问。synchronized 修饰符可以应用于四个访问修饰符

transient 修饰符
序列化的对象包含被 transient 修饰的实例变量时，java 虚拟机(JVM)跳过该特定的变量。

该修饰符包含在定义变量的语句中，用来预处理类和变量的数据类型。

volatile 修饰符
volatile 修饰的成员变量在每次被线程访问时，都强制从共享内存中重新读取该成员变量的值。而且，当成员变量发生变化时，会强制线程将变化值回写到共享内存。这样在任何时刻，两个不同的线程总是看到某个成员变量的同一个值。

一个 volatile 对象引用可能是 null。



# 面向对象

- java里的引用就是c语言的指针封装起来方便使用

- java里 参数传递方法只有值传递，也就是将实际参数值的副本传过去，参数本身不会受到影响

## 内部类

### 成员内部类

第一：成员内部类中不能存在任何static的变量和方法；

​         Static 不用实例化就能加载进内存

　　而内部类需要外部类实例化后才能加载进内存。这就间接造成static需要实例化了。与static不需要实例化语义矛盾

第二：成员内部类是依附于外围类的，所以只有先创建了外围类才能够创建内部类

```java
public class OuterClass {
    private String str;
    
    public void outerDisplay(){
        System.out.println("outerClass...");
    }
    
    public class InnerClass{
        public void innerDisplay(){
            //使用外围内的属性
            str = "chenssy...";
            System.out.println(str);
            //使用外围内的方法
            outerDisplay();
        }
    }
    
    /*推荐使用getxxx()来获取成员内部类，尤其是该内部类的构造函数无参数时 */
    public InnerClass getInnerClass(){
        return new InnerClass();
    }
    
    public static void main(String[] args) {
        OuterClass outer = new OuterClass();
        OuterClass.InnerClass inner = outer.getInnerClass();
        inner.innerDisplay();
    }
}
--------------------
chenssy...
outerClass...
```



### 局部内部类 

有这样一种内部类，它是嵌套在方法和作用于内的，对于这个类的使用主要是应用与解决比较复杂的问题，想创建一个类来辅助我们的解决方案，到那时又不希望这个类是公共可用的，所以就产生了局部内部类，局部内部类和成员内部类一样被编译，只是它的作用域发生了改变，它只能在该方法和属性中被使用，出了该方法和属性就会失效。



定义在方法里

```java
public class Parcel5 {
    public Destionation destionation(String str){
        class PDestionation implements Destionation{
            private String label;
            private PDestionation(String whereTo){
                label = whereTo;
            }
            public String readLabel(){
                return label;
            }
        }
        return new PDestionation(str);
    }
    
    public static void main(String[] args) {
        Parcel5 parcel5 = new Parcel5();
        Destionation d = parcel5.destionation("chenssy");
    }
}
```

 定义在作用域内:

```java
public class Parcel6 {
    private void internalTracking(boolean b){
        if(b){
            class TrackingSlip{
                private String id;
                TrackingSlip(String s) {
                    id = s;
                }
                String getSlip(){
                    return id;
                }
            }
            TrackingSlip ts = new TrackingSlip("chenssy");
            String string = ts.getSlip();
        }
    }
    
    public void track(){
        internalTracking(true);
    }
    
    public static void main(String[] args) {
        Parcel6 parcel6 = new Parcel6();
        parcel6.track();
    }
}
```







### 匿名内部类

  1 匿名内部类是没有访问修饰符的。

  2 new 匿名内部类，这个类首先是要存在的。如果我们将那个InnerClass接口注释掉，就会出现编译出错。

  3 注意getInnerClass()方法的形参，第一个形参是用final修饰的，而第二个却没有。同时我们也发现第二个形参在匿名内部类中没有使用过，所以当所在方法的形参需要被匿名内部类使用，那么这个形参就必须为final。

 4 匿名内部类是没有构造方法的。因为它连名字都没有何来构造方法。



## final使用

 我们给匿名内部类传递参数的时候，若该形参在内部类中需要被使用，那么该形参必须要为final。也就是说：**当所在的方法的形参需要被内部类里面使用时，该形参必须为final。**

   为什么必须要为final呢？

   首先我们知道在内部类编译成功后，它会产生一个class文件，该class文件与外部类并不是同一class文件，仅仅只保留对外部类的引用。当外部类传入的参数需要被内部类调用时，从java程序的角度来看是直接被调用

```java
public class OuterClass {
    public void display(final String name,String age){
        class InnerClass{
            void display(){
                System.out.println(name);
            }
        }
    }
}
```

 从上面代码中看好像name参数应该是被内部类直接调用？其实不然，在java编译之后实际的操作如下：

```java
public class OuterClass$InnerClass {
    public InnerClass(String name,String age){
        this.InnerClass$name = name;
        this.InnerClass$age = age;
    }
    
    
    public void display(){
        System.out.println(this.InnerClass$name + "----" + this.InnerClass$age );
    }
}
```

 所以从上面代码来看，内部类并不是直接调用方法传递的参数，而是利用自身的构造器对传入的参数进行备份，自己内部方法调用的实际上时自己的属性而不是外部方法传递进来的参数。

​    直到这里还没有解释为什么是final？在内部类中的属性和外部方法的参数两者从外表上看是同一个东西，但实际上却不是，所以他们两者是可以任意变化的，也就是说在内部类中我对属性的改变并不会影响到外部的形参，而然这从程序员的角度来看这是不可行的，毕竟站在程序的角度来看这两个根本就是同一个，如果内部类该变了，而外部方法的形参却没有改变这是难以理解和不可接受的，所以为了保持参数的一致性，就规定使用final来避免形参的不改变。

   简单理解就是，拷贝引用，为了避免引用值发生改变，例如被外部类的方法修改等，而导致内部类得到的值不一致，于是用final来让该引用不可改变。

   ***故如果定义了一个匿名内部类，并且希望它使用一个其外部定义的参数，那么编译器会要求该参数引用是final的。***

 ## 静态内部类

不能引用外部非static的变量或方法

 它的创建是不需要依赖于外围类的



## instanceof与getClass的区别

instanceof进行类型检查规则是:你属于该类吗？或者你属于该类的派生类吗？而通过getClass获得类型信息采用==来进行检查是否相等的操作是严格的判断。不会存在继承方面的考虑；

- 

  

  # 异常体系

  ***不论程序是否发生异常，finally代码块总是会执行。所以finally一般用来关闭资源。***

  ```java
/** 自定义异常 继承Exception类 **/
  public class MyException extends Exception{
    public MyException(){
          
    }
      
    public MyException(String message){
          super(message);
    }
  }
 
  public class Test {
      public void display(int i) throws MyException{
          if(i == 0){
              throw new MyException("该值不能为0.......");
          }
          else{
              System.out.println( i / 2);
          }
      }
      
      public static void main(String[] args) {
          Test test = new Test();
          try {
              test.display(0);
              System.out.println("---------------------");
          } catch (MyException e) {
              e.printStackTrace();
          }
      }
  }
  ```
  
  使用结论：
  
  - 尽可能缩小trycatch块
  - 保证所有的资源都释放 充分使用finally
  - catch应分清类型
  
    



## 判断语句
 if ...else

 ## switch case
 switch 语句中的变量类型可以是： byte、short、int 或者 char。从 Java SE 7 开始，switch 支持字符串 String 类型了，同时 case 标签必须为字符串常量或字面量。


 ## java Number&Math
 ceil 向上取整
 floor （地板） 向下取整
 round 算法为Math.floor(x+0.5) 向下取整
 ## String StringBuffer StringBuilder
 String 类是不可改变的，所以你一旦创建了 String 对象，那它的值就无法改变了
 为什么门说String对象是不可变的呢？

原因在于实例中的 s 只是一个 String 对象的引用，并不是对象本身，当执行 s = "Runoob"; 创建了一个新的对象 "Runoob"，而原来的 "Google" 还存在于内存中



# 集合

## 概要

- java8位Iteraable接口新增了了一个foreach（Consumer action） 函数式接口

  ```java
   Collection<String> strings = new ArrayList<>();
          strings.add("dgad");
          strings.add("dfsgad");
          strings.add("safh");
          strings.forEach(System.out::println);
  ```

  

- 使用java8 增强的Iterator进行遍历

- 使用java8增强的Iterator进行lambda进行遍历 itrrator.foreachremaining(s->sout("s"))

- 使用foreach遍历

- 使用java8增强的Precidate操作集合

  ```java
  strings.removeIf(s -> s.length() < 10);//predicate操作判断是否符合条件实现过滤操作
  ```

- 使用Stream操作集合

  ```java
    Stream stream = Stream.builder()
                  .add("ssg")
                  .add("fdsa")
                  .build();
          stream.forEach(System.out::println);
  ```

## Set集合

  set集合就相当于把元素丢进一个罐子里，所以记不得顺序，也不能重复

- HashSet 插入删除操作好一些  

- LinkedHashSet  查询好一些  链表维护

- TreeSet  红黑树算法维护

- EnumSet   枚举元素

  均不是线程安全的。

## List  

### ArrayList

线性表实现

ArrayList是实现List接口的动态数组，所谓动态就是它的大小是可变的。实现了所有可选列表操作，并允许包括 null 在内的所有元素。除了实现 List 接口外，此类还提供一些方法来操作内部用来存储列表的数组的大小。

每个ArrayList实例都有一个容量，该容量是指用来存储列表元素的数组的大小。默认初始容量为10。随着ArrayList中元素的增加，它的容量也会不断的自动增长。在每次添加新的元素时，ArrayList都会检查是否需要进行扩容操作，扩容操作带来数据向新数组的重新拷贝，所以如果我们知道具体业务数据量，在构造ArrayList时可以给ArrayList指定一个初始容量，这样就会减少扩容时数据的拷贝问题。当然在添加大量元素前，应用程序也可以使用ensureCapacity操作来增加ArrayList实例的容量，这可以减少递增式再分配的数量。

**注意，ArrayList实现不是同步的**。如果多个线程同时访问一个ArrayList实例，而其中至少一个线程从结构上修改了列表，那么它必须保持外部同步。所以为了保证同步，最好的办法是在创建时完成，以防止意外对列表进行不同步的访问：

```java
List list = Collections.synchronizedList(new ArrayList(...));
```

- ArrayList源码分析  

​        ArrayList我们使用的实在是太多了，非常熟悉，所以在这里将不介绍它的使用方法。ArrayList是实现List接口的，底层采用数组实现，所以它的操作基本上都是基于对数组的操作。

**2.1、底层使用数组**

```
 private transient Object[] elementData;
```

transient？？为java关键字，为变量修饰符，如果用transient声明一个实例变量，当对象存储时，它的值不需要维持。Java的serialization提供了一种持久化对象实例的机制。当持久化对象时，可能有一个特殊的对象数据成员，我们不想用serialization机制来保存它。为了在一个特定对象的一个域上关闭serialization，可以在这个域前加上关键字transient。当一个对象被序列化的时候，transient型变量的值不包括在序列化的表示中，然而非transient型的变量是被包括进去的。

这里Object[] elementData，就是我们的ArrayList容器，下面介绍的基本操作都是基于该elementData变量来进行操作的。

**2.2、构造函数**

ArrayList提供了三个构造函数：

- `ArrayList()`：默认构造函数，提供初始容量为10的空列表。
- `ArrayList(int initialCapacity)`：构造一个具有指定初始容量的空列表。
- `ArrayList(Collection<?> extends [E] c)`：构造一个包含指定 collection 的元素的列表，这些元素是按照该 collection 的迭代器返回它们的顺序排列的。

```java
    /**
     * 构造一个初始容量为 10 的空列表
     */
    public ArrayList() {
        this(10);
    }

    /**
     * 构造一个具有指定初始容量的空列表。
     */
    public ArrayList(int initialCapacity) {
        super();
        if (initialCapacity < 0)
            throw new IllegalArgumentException("Illegal Capacity: "
                    + initialCapacity);
        this.elementData = new Object[initialCapacity];
    }

    /**
     *  构造一个包含指定 collection 的元素的列表，这些元素是按照该 collection 的迭代器返回它们的顺序排列的。
     */
    public ArrayList(Collection<? extends E> c) {
        elementData = c.toArray();
        size = elementData.length;
        // c.toArray might (incorrectly) not return Object[] (see 6260652)
        if (elementData.getClass() != Object[].class)
            elementData = Arrays.copyOf(elementData, size, Object[].class);
    }
```

**2.3、新增**

ArrayList提供了`add(E e)`、`add(int index, E element)`、`addAll(Collection<? extends E> c)`、`addAll(int index, Collection<? extends E> c)`、`set(int index, E element)` 这个五个方法来实现ArrayList增加。

add(E e)：将指定的元素添加到此列表的尾部。

```java
 public boolean add(E e) {
    ensureCapacity(size + 1);  // Increments modCount!!
    elementData[size++] = e;
    return true;
    }
```

这里ensureCapacity()方法是对ArrayList集合进行扩容操作，elementData(size++) = e，将列表末尾元素指向e。

add(int index, E element)：将指定的元素插入此列表中的指定位置。

```java
public void add(int index, E element) {
        //判断索引位置是否正确
        if (index > size || index < 0)
            throw new IndexOutOfBoundsException(
            "Index: "+index+", Size: "+size);
        //扩容检测
        ensureCapacity(size+1);  
        /*
         * 对源数组进行复制处理（位移），从index + 1到size-index。
         * 主要目的就是空出index位置供数据插入，
         * 即向右移动当前位于该位置的元素以及所有后续元素。
         */
        System.arraycopy(elementData, index, elementData, index + 1,
                 size - index);
        //在指定位置赋值
        elementData[index] = element;
        size++;
        }
```

在这个方法中最根本的方法就是System.arraycopy()方法，该方法的根本目的就是将index位置空出来以供新数据插入，这里需要进行数组数据的右移，这是非常麻烦和耗时的，所以如果指定的数据集合需要进行大量插入（中间插入）操作，推荐使用LinkedList。

`addAll(Collection<? extends E> c)`：按照指定 collection 的迭代器所返回的元素顺序，将该 collection 中的所有元素添加到此列表的尾部。

```java
public boolean addAll(Collection<? extends E> c) {
        // 将集合C转换成数组
        Object[] a = c.toArray();
        int numNew = a.length;
        // 扩容处理，大小为size + numNew
        ensureCapacity(size + numNew); // Increments modCount
        System.arraycopy(a, 0, elementData, size, numNew);
        size += numNew;
        return numNew != 0;
    }
```

这个方法无非就是使用System.arraycopy()方法将C集合(先准换为数组)里面的数据复制到elementData数组中。这里就稍微介绍下System.arraycopy()，因为下面还将大量用到该方法。该方法的原型为：public static void**arraycopy**(Object src, int srcPos, Object dest, int destPos, int length)。它的根本目的就是进行数组元素的复制。即从指定源数组中复制一个数组，复制从指定的位置开始，到目标数组的指定位置结束。将源数组src从srcPos位置开始复制到dest数组中，复制长度为length，数据从dest的destPos位置开始粘贴。

`addAll(int index, Collection<?> extends E> c)`：从指定的位置开始，将指定 collection 中的所有元素插入到此列表中。

```java
public boolean addAll(int index, Collection<? extends E> c) {
        //判断位置是否正确
        if (index > size || index < 0)
            throw new IndexOutOfBoundsException("Index: " + index + ", Size: "
                    + size);
        //转换成数组
        Object[] a = c.toArray();
        int numNew = a.length;
        //ArrayList容器扩容处理
        ensureCapacity(size + numNew); // Increments modCount
        //ArrayList容器数组向右移动的位置
        int numMoved = size - index;
        //如果移动位置大于0，则将ArrayList容器的数据向右移动numMoved个位置，确保增加的数据能够增加
        if (numMoved > 0)
            System.arraycopy(elementData, index, elementData, index + numNew,
                    numMoved);
        //添加数组
        System.arraycopy(a, 0, elementData, index, numNew);
        //容器容量变大
        size += numNew;   
        return numNew != 0;
    }
```

set(int index, E element)：用指定的元素替代此列表中指定位置上的元素。

```java
public E set(int index, E element) {
        //检测插入的位置是否越界
        RangeCheck(index);

        E oldValue = (E) elementData[index];
        //替代
        elementData[index] = element;
        return oldValue;
    }
```

**2.4、删除**

ArrayList提供了remove(int index)、remove(Object o)、removeRange(int fromIndex, int toIndex)、removeAll()四个方法进行元素的删除。

remove(int index)：移除此列表中指定位置上的元素。

```java
public E remove(int index) {
        //位置验证
        RangeCheck(index);

        modCount++;
        //需要删除的元素
        E oldValue = (E) elementData[index];   
        //向左移的位数
        int numMoved = size - index - 1;
        //若需要移动，则想左移动numMoved位
        if (numMoved > 0)
            System.arraycopy(elementData, index + 1, elementData, index,
                    numMoved);
        //置空最后一个元素
        elementData[--size] = null; // Let gc do its work

        return oldValue;
    }
```

remove(Object o)：移除此列表中首次出现的指定元素（如果存在）。

```java
public boolean remove(Object o) {
        //因为ArrayList中允许存在null，所以需要进行null判断
        if (o == null) {
            for (int index = 0; index < size; index++)
                if (elementData[index] == null) {
                    //移除这个位置的元素
                    fastRemove(index);
                    return true;
                }
        } else {
            for (int index = 0; index < size; index++)
                if (o.equals(elementData[index])) {
                    fastRemove(index);
                    return true;
                }
        }
        return false;
    }
```

其中fastRemove()方法用于移除指定位置的元素。如下

```java
private void fastRemove(int index) {
        modCount++;
        int numMoved = size - index - 1;
        if (numMoved > 0)
            System.arraycopy(elementData, index+1, elementData, index,
                             numMoved);
        elementData[--size] = null; // Let gc do its work
    }
```

removeRange(int fromIndex, int toIndex)：移除列表中索引在 `fromIndex`（包括）和 `toIndex`（不包括）之间的所有元素。

```java
protected void removeRange(int fromIndex, int toIndex) {
        modCount++;
        int numMoved = size - toIndex;
        System
                .arraycopy(elementData, toIndex, elementData, fromIndex,
                        numMoved);

        // Let gc do its work
        int newSize = size - (toIndex - fromIndex);
        while (size != newSize)
            elementData[--size] = null;
    }
```

removeAll()：是继承自AbstractCollection的方法，ArrayList本身并没有提供实现。

```java
public boolean removeAll(Collection<?> c) {
        boolean modified = false;
        Iterator<?> e = iterator();
        while (e.hasNext()) {
            if (c.contains(e.next())) {
                e.remove();
                modified = true;
            }
        }
        return modified;
    }
```

**2.5、查找**

ArrayList提供了get(int index)用读取ArrayList中的元素。由于ArrayList是动态数组，所以我们完全可以根据下标来获取ArrayList中的元素，而且速度还比较快，故ArrayList长于随机访问。

```java
 public E get(int index) {
        RangeCheck(index);

        return (E) elementData[index];
    }
```

**2.6、扩容**

在上面的新增方法的源码中我们发现每个方法中都存在这个方法：ensureCapacity()，该方法就是ArrayList的扩容方法。在前面就提过ArrayList每次新增元素时都会需要进行容量检测判断，若新增元素后元素的个数会超过ArrayList的容量，就会进行扩容操作来满足新增元素的需求。所以当我们清楚知道业务数据量或者需要插入大量元素前，我可以使用ensureCapacity来手动增加ArrayList实例的容量，以减少递增式再分配的数量。

```java
public void ensureCapacity(int minCapacity) {
        //修改计时器
        modCount++;
        //ArrayList容量大小
        int oldCapacity = elementData.length;
        /*
         * 若当前需要的长度大于当前数组的长度时，进行扩容操作
         */
        if (minCapacity > oldCapacity) {
            Object oldData[] = elementData;
            //计算新的容量大小，为当前容量的1.5倍
            int newCapacity = (oldCapacity * 3) / 2 + 1;
            if (newCapacity < minCapacity)
                newCapacity = minCapacity;
            //数组拷贝，生成新的数组
            elementData = Arrays.copyOf(elementData, newCapacity);
        }
    }
```

在这里有一个疑问，为什么每次扩容处理会是1.5倍，而不是2.5、3、4倍呢？通过google查找，发现1.5倍的扩容是最好的倍数。因为一次性扩容太大(例如2.5倍)可能会浪费更多的内存(1.5倍最多浪费33%，而2.5被最多会浪费60%，3.5倍则会浪费71%……)。但是一次性扩容太小，需要多次对数组重新分配内存，对性能消耗比较严重。所以1.5倍刚刚好，既能满足性能需求，也不会造成很大的内存消耗。

处理这个ensureCapacity()这个扩容数组外，ArrayList还给我们提供了将底层数组的容量调整为当前列表保存的实际元素的大小的功能。它可以通过trimToSize()方法来实现。该方法可以最小化ArrayList实例的存储量。

```java
public void trimToSize() {
        modCount++;
        int oldCapacity = elementData.length;
        if (size < oldCapacity) {
            elementData = Arrays.copyOf(elementData, size);
        }
    }
```

#### String的hashcode重复问题

在A-z范围内有特殊字符，从结果看，仅仅3位长度的字符串：
不处理：　138510次重复
去掉字母意外字符：　122500次重复
所有字符转小写：6612次重复(少了很多）
去掉字母意外字符，并且转小写：没有重复！4位字符串也没见重复

不难看出：
1. 缺省实现为英文字母优化
2. 字母大小写可能导致重复

可能：
长字符串可能hashcode重复
中文字符串和特殊字符可能hashcode重复 

```java
System.out.println("重地".hashCode());
System.out.println("通话".hashCode());
```

### Vector 

线程安全的 list的实现类，性能比arraylist差

vector还有一个stack子类 ，栈，先进后出，同样性能较差

### Queue 集合

用来模拟队列这种集合

有一个PriorityQueue实现类，此外还有一个Deque接口，代表一个双端队列，可以同时从两端添加删除元素，因此Deque实现类既可以当成队列又可以当成栈来使用，java位Deque提供了ArrayDeque喝LinkedDeque是实现类

#### PriorityQueue

违反了队列先进先出原则，按照从小到大的原则。

#### Deque  ArrayDeque

### LinkedList

实现了Deque接口 因此既可以当成栈队列使用，底层使用链表，查询性能较低，但插入删除性能出色。

因为链表存储是不连续的，不能根据索引找到元素。

## Map

#### HashMap 

线程不安全，使用null为key或value，key只能一个，value可以多个

 #### Hashtable 

线程安全但是太老不推荐使用，不允许keyvalue为null

#### LinkedHashMap

使用双向链表维护顺序

#### SortMap

子类treemap 使用红黑树 有序

#### WeakedHashMap

保持了对key的弱引用

#### IdentifyHashMap

#### EnumHashMap

## Collections

工具类。同步集合。

## Enumeration

古老的接口

# 泛型

java泛型有个缺点把一个对象丢进去之后集合就会忘记对象类型，再次取出对象时 发现时object类型

- 集合对对象没有限制，会发生不同对象放进去出现问题
- 丢失对象信息后拿出来 出来之后强制类型转换增加编程复杂度，可能会引起classcastexception
- 参数化类型，成为泛型 parammeterized type
- list<E> element  Set<K>  key 
- List<String>并不是List<Object> 的子类 。java中 数组与泛型不同，a与b为父子，a[] b[] 也是父子，但是List<a> list<b> 并不是父子
- List<?> ? 通配符
- null 是所有引用类型的实例即使是list<?> 也可以添加null
- List<? extend Shape> 上限 必须是父类的子类或者本身   可以继承一个上限或者实现多个接口上限

 ```
  public class Apple<T extends Object & Serializable>  
 ```

- 泛型方法  

  ```java
   public static <Base> void fg(Base[] a,Base[] b) {
  
      }
  public static void main(String[] args){
      fg(String[]a,String[] b);//注意 前后类型必须相等
  }
  ```
  
- 泛型方法 和类型通配符

  ```java 
  public interface Collection<E>{
      boolean contaionsAll(Collection<?> c);
      boolean addAll(Collection<? extend E> c);
  }
  public interface Collection<E>{
      <T> boolean containAll(Collection<T> c);
      <T extend E> boolean addALl(Conllection<T> c )
  }
  ```

- 下限 super 表示 本身或者父类

- java8 改进的类型判断。就是调用传参 有类型。

  - 可通过调用方法的上下文判断类型

  - 可在方法调用链中将推断得到的类型参数传到下一个方法

- 擦除和转换

    当一个具有泛型信息的对象赋给另一个没有泛型信息的变量时，所有尖括号的信息都被扔掉。

   此部分大概是说要指定具体类型不然会出错，classcastex，或者未检查的转换异常

- 数组与泛型  不能出现类似List<String> [] s = new List<>[10];

  # 异常

  try catch finally（回收物理资源），try出现，catch和finally只要要出现一个。

  try（这里面可以放回收的资源的定义，会自动回收）{}

  throws 放在方法签名，意思是将异常抛给上一层。
  
  throw 手动抛出异常，进入catch中

#  注解

- FunctionalInterface 函数式接口 只包含一个抽象方法 多个默认方法或者静态方法

  

# IO

- file

- InputStream/Reader

- OutPutStream/Writer

- InputStreamReader/OutPutStreamWriter  转换流

- RandomAccessFile  可以跳转到文件的任意位置读写数据

- 递归序列化  引用的变量也会被序列化

- Buffer    NIO

  ```java
  CharBuffer charBuffer = CharBuffer.allocate(9);
          charBuffer.put("a");
          charBuffer.put("b");
          charBuffer.put("C");
          charBuffer.flip();
          System.out.println(charBuffer.get(6));
  
  ```
  
- Channel 映射成Buffer   NIO  

- 文件锁 FileLock 防止并发访问

- FileVisitor 遍历文件和目录

- WatchService 监控文件变化

# 多线程

- 进程

  - 独立性。进程是系统独立存在的实体，拥有自己独立的资源，每一个进程都拥有自己独立的地址空间。在没有进程本身的允许下，一个用户进程不能访问其他的地址空间

  - 动态性。进程与程序最大的区别在于。程序只是一个静态的指令集和，而进程是一个正在系统中活动的指令集和，在进程中加入了时间的概念。进程具有自己的生命周期和各种不同的状态，这些概念是程序不具备的。

  - 并发性。多个进程可以在单个处理器并发执行，多个进程间不会影响。
  
- 并发和并行 
  - 并行是指在同一时刻，有多条指令在多个处理器上同时执行
  - 并发在指在同一时刻只有一条指令执行，但多个进程指令被快速轮换执行，使得宏观上具有多个进程同时执行的效果
  
- 多线程  与其他线程共享父进程的共享变量及部分环境。拥有自己的堆栈自己的程序计数器和自己的局部变量，但不拥有系统资源它与父进程的其他线程共享该进程的全部资源。线程的执行是抢占式的，也就是说当前的线程可以随时挂起，以便另一个线程可以运行。

- 线程的创建
  - 继承Thread
  
  - 实现Runnable接口
  
  - 使用Callable和Future创建线程  Call方法可以作为线程执行体，但call方法比run方法更强大，可以有返回值，可以抛出异常
  
    ```java
     FutureTask<Integer> task = new FutureTask<>(new Callable<Integer>() {
                @Override
                public Integer call() throws Exception {
                    return null;
                }
            });
            new Thread(task, "ds").start();
    ```
  
    
  
- 线程的生命周期 新建 就绪 运行 阻塞 死亡。
  
  - 新建和就绪状态  new 创建之后就处于新建状态，调用了start之后就处于就绪状态，至于何时开始运行，取决于JVM里线程调度器和调度。
  
- 运行和阻塞状态  开始执行run方法体就进入了运行状态，

  抢占式策略，系统考虑线程优先级，当发生以下情况时就进入阻塞状态

  - 线程调用sleep（）方法主动放弃所占用的处理器资源

  - 线程调用了一个阻塞式IO方法，在该方法返回之前，该线程被阻塞。

  - 线程获得一个同步监视器，但该同步监视器正被其他线程持有，

  - 线程在等待某个通知 notify

  - 程序调用了线程的suspend（）方法将该线程挂起，但这个方法容易导致死锁，应该避免使用。

    针对上面几种情况，发生如下几种情况可以解除上面的阻塞，让线程进入就绪状态

    - 调用sleep 方法的线程过了指定的时间

    - 线程调用的阻塞式IO已经返回

    - 线程成功获得了同步监视器

    - 其他线程发出了一个通知

    - 处于挂起状态的线程调用了resume恢复方法

- 线程死亡

  run或call方法执行完成，线程正常结束

  线程抛出一个未捕获的exception或error

  直接调用该线程的stop方法来结束该线程-该方法容易导致死锁

- 控制线程

  - join 线程  一个线程等待另一个线程完成的方法--join方法

  - sleep
  - 后台线程  Dameon线程
  - 线程让步 yield
  - 改变线程优先级

# 网络编程



# 反射




