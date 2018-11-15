# 1. Java

## 1.1. Java 是什么？

### 1.1.1. Java分为三个体系
* JavaSE(J2SE)(Java2 Platform Standard Edition，java平台标准版)
* JavaEE(J2EE)(Java 2 Platform,Enterprise Edition，java平台企业版)
* JavaME(J2ME)(Java 2 Platform Micro Edition，java平台微型版)

面向对象编程语言。

摒弃了 C++ 里的多继承. 指针等概念。

功能强大，简单易用。

需要更多的内存。

缓慢的启动时间。

下载JDK开发工具包，并配置环境。

## 1.2. Java 能做什么？

视频游戏开发。
Android 应用开发。
桌面 GUI。
软件开发。

## 1.3. 名词解释

### 1.3.1. MVC

Model View Controller，模型-视图-控制器。

* Model（模型）表示应用程序核心（比如数据库记录列表）。
* View（视图）显示数据（数据库记录）。
* Controller（控制器）处理输入（写入数据库记录）。

MVC 模式同时提供了对HTML、CSS、JavaScript 的完全控制。

### 1.3.2. SSH

Secure Shell（安全外壳协议）。

建立在应用层基础上的安全协议。

主要由三部分组成：

* 传输层协议[SSH-TRANS]
* 用户认证协议[SSH-USERAUTH]
* 连接协议[SSH-CONNECT]

由客户端和服务端的软件组成。

## 1.4. 基本语法

大小写敏感。

类名：大驼峰；方法名：小驼峰。

源文件名与类名相同。

主方法入口：public static void main(String args[]) 。

**修饰符**：

* 修饰类中的属性和方法。
* 可访问修饰符：default. public. protected. private 。
* 不可访问修饰符：final. abstract. strictfp 。

局部变量。

类变量（静态变量）。

成员变量（非静态变量）。

**数组**是储存在堆上的对象，可以保存多个同类型的变量。

**枚举**限制变量只能在预先设定好的值。使用枚举可以减少代码中的 bug 。

## 1.5. 学习

### 1.5.1. 数据类型

byte, short, int, long, float, double, boolean, char.

**引用数据类型**：

* 变量一旦声明后，类型就不能改变了。
* 对象和数组都是引用数据类型。
* 所有引用类型的默认值都是 null 。
* 例子：Site site = new Site("name")

**常量**：

* 例如：PI
* 使用 final 关键字来修饰常量。
* 通常使用大写字母表示常量。
* 转义字符列表，例如 \n 。

**自动类型转换**：

* 不同类型的数据要先转化为同一类型，才能进行混合运算。
* 从低级到高级：byte, short, char->int->long->float->double
* 强制类型转换：
* 隐含强制类型转换：

### 1.5.2. 变量类型

类型量：独立于方法之外的变量，用 static 修饰。

实例变量：独立于方法之外的编码，没有 static 修饰。

局部变量：类的方法中的变量。

```java
public class Variable {
    static int allClicks = 0; // 类变量

    String str = "hello world";// 实例变量

    public void method() {

        int i =0;  // 局部变量

    }
}
```

**局部变量**：
局部变量声明在方法. 构造方法或者语句块中；
访问修饰符不能用于局部变量；
局部变量是在栈上分配的；
没有默认值，所以局部变量被声明后，必须经过初始化，才可以使用。

实例变量：

类变量：

修饰符：

### 1.5.3. 运算符

算数运算符：

布尔运算符：

关系运算符：

三元运算符：

按位运算符：

### 1.5.4. 循环结构

while循环：

do...while 循环：

for 循环：

增强 for 循环：

**break**关键字:

* 主要用在循环语句或者 switch 语句中，用来跳出整个语句块。
* 跳出最里层的循环，并且继续执行该循环下面的语句。

**continue**关键字：

* 适用于任何循环控制结构中；
* 作用是让程序立刻跳转到下一次循环的迭代。

### 1.5.5. 分支结构

if 语句：

if...else 语句：

if...else if...else语句：

嵌套的 if...else 语句：

switch 语句：

### 1.5.6. 数组

数组对于每一门编程语言来说都是重要的数据结构之一。

数组是用来存储固定大小的同类型元素。

数组的声明，创建，初始化。

**声明**数组变量：

* dataType[] arrayRefVar; 或 dataType arrayRefVar[];

**创建**数组：

* arrayRefVar = new dataType[arraySize];
* 使用 dataType[arraySize] 创建了一个数组。
* 把新创建的数组的引用赋值给变量 arrayRefVar 。

**处理**数组：

* 数组的元素类型和数组的大小都是确定的，所以当处理数组元素时候，我们通常* 使用基本循环或者 foreach 循环。

foreach 循环：
在不使用下标的情况下遍历数组。

数组作为函数的参数：
数组作为函数的返回值：
多维数组：
数组的数组。

Arrays 类：
java.util.Arrays 类更方便地操作数组，它提供的方法都是静态的。

### 1.5.7. 异常

**关键字**：try, catch, throw, throws, finally 。

* try 块包含要监视的程序语句异常。
* catch 语句可以捕获异常并以合理的方式处理它。
* 手动抛出异常，throw 。
* 任何抛出的异常一个方法必须由一个 throws 子句指定。
* 任何代码绝对必须是在 try 块完成之后执行的命令被放在 finally 块中。

try catch 语句。

多 catch 子句。

嵌套 try 语句。

throw， throws， finally.

异常都派生于 Throwable 类。

Error 系统错误。

Exception ： RuntimeException（程序错误），IOException（I/O错误）。

自定义异常类。

链接异常。

## 1.6. 面向对象

### 1.6.1. 对象和类

面向对象

* 面向对象程序设计（OOP）；
* 面向对象的程序由对象组成，每个对象包含读用户公开的特定功能部分和隐藏的实现部分；
* 算法 + 数据结构 = 程序，Algorithms + DataStructures = Programs ；
* 算法（Algorithm）是指解题方案的准确而完整的描述，是一系列解决问题的清晰指令，算法代表着用系统的方法描述解决问题的策略机制；
* 面向对象将数据放在第一位，面向过程将算法放在第一位；
* 面向对象更加适用于解决规模较大的问题。

对象

* 三个主要特征：行为（behavior），状态（state），标识（identity）；
* 对象的行为是用可调用的方法定义的；
* 对象的状态是每个对象都保存着描述当前特征的信息；
* 每个对象都有唯一的身份。

类

* 类是构造对象的模板或蓝图；
* 类构造对象的过程称为创建类的实例（instance）；

封装（encapsulation），有时称为数据隐藏；

* 封装将数据和行为组合在一个包中，并对对象的使用者隐藏了数据的实现方式；
* 对象中的数据称为实例域（instance field），操纵数据的过程称为方法（method）；
* 超类 Object 。

类之间的关系

* 依赖（dependence），如果一个类的方法操纵另一个类的对象；
* 聚合（aggregation），类 A 的对象包含类 B 的对象；
* 继承（inheritance）。
* UML（Unified Modeling Language），统一建模语言。

预定义类
Math, Data

对象和对象变量

* 要想使用对象，就必须首先构造对象，并指定其初始状态。然后，对对象应用方法。
* 构造器（constructor）构造新实例。一种特殊的方法，构造并初始化对象。
* 一个对象变量没有实际包含一个对象，而仅仅引用一个对象。

隐式(implicit)参数和显示(explicit)参数

* 显示参数是明显地列在方法声明中的，饮食参数没有出现杂在方法声明中。
* 关键字 this 表示隐式参数。可以将实例域与局部变量明显的区分开。

**域**（field）即属性。

**实例域**（instance field），对象中的数据。

**静态域**，又叫类域，定义为 static 。

对象本身已知的的事物称为**实例变量**（instance variable）。

他们代表对象的状态（数据），且该类型的每一个对象都会独立的拥有一份该类型的值。

可以把对象当作为实例。

对象可以执行的动作称为**方法**（methods）。

```java
class bike{ 
static int bikes;  // 类变量（静态域）（类域）
int gear;  // 对象变量（实例变量）（非静态域）
int cadence;  // 对象变量（实例变量）（非静态域） 

  void create( int newGear, int newCadence ){  // 方法中的两个参数
    bikes = bikes + 1;
    gear = newGear;
    cadence = newCadence;}
  int getSpeed(){
    int speed = gear*cadence*5*3.141;  // 局部变量（方法中的变量）
    return speed;
  }
}
```

创建一个对象需要两个类：

一、被操作对象的类。

二、测试该类的类。测试用的类带有 main() 并且你会在其中建立与存取被测的对象。

（受测类名 +TestDrive，*Head First Java*）

真正的 Java 程序只会让对象与对象交互，此处的交互是指相互调用的方法。

main() 是应用程序的入口点。

一个方法可以访问所属类的所有对象的私有数据。

封装（encapsulation），将你的实例变量标记为私有的，并提供公有的 getter 与 setter 来控制存取动作。

### 1.6.2. 继承

``` java
  public class ParentClass extends ChildClass {
    private double bonus;
    ...
    public void setBonus(double bonus) {
      this.bonus = bonus;
    }
  }
```

extends 表明正在构造的新类派生于一个已存在的类。

* 已存在的类：超类（superclass），基类（base class）、**父类**（parent class）；
* 新类：子类（subclass）、派生类（derived class）、**子类**（child class）。
* implement 使用在类继承接口的情况下，这种情况不能使用 extends。

重写（Override）。 （Core Java 中管这个叫“覆盖”）。

* 子类可以根据需要，定义特定于自己的行为。
* 在重写一个方法的时候，子类不能低于超类方法的可见性。
* 如果父类的方法时 public ，那么子类的方法一定也要是 public 。
* 重载(overloading) 
* 在一个类里面，方法名字相同，而参数不同。
* this 的两个用途：一、引用隐式参数，二、调用该类其他的构造器。
* super 的两个用途：一、调用超类的方法，二、调用超类的构造器。

多态

* 置换法则。
* 不能将一个父类的引用赋给子类变量。

类型转换

抽象类

* public abstract class Person();
* 包含一个或多个抽象方法的类本身必须被声明为抽象的。
* 抽象方法充当占位的角色，它们的具体实现在子类中。
* 类即使不含抽象方法，也可以将类声明为抽象类。

阻止继承

* 将方法和类声明为 final 的主要目的是：确保它们不会在子类中改变语义。

最好将类中的域标记为 private，而方法标记为 public。

Object 是所有类的始祖，所有类的超类。

equals 方法，用于检测一个对象是否等于另一个对象。

hash code: 散列码，哈希码。

由对象导出的一个整型值，没有规律。

toString 方法。

用来打印输出对象的类名和散列码。

非常有用的调试工机。

泛型数组列表

枚举类

反射

* 反射库（reflection library）提供了一个非常丰富且精心设计的工具集，以便编写能够动态 Java 代码的程序。
* 反射是指在程序运行期间发现更多的类及其属性的能力。

## 1.7. 高级技术

### 1.7.1. 接口

接口（interface）

一个类可以实现（implement）一个或多个接口，并在需要接口的地方，随时使用实现了相应接口的对象。

接口并不是类。而是对类的一组需求描述。

所有方法自动属于 public，声明方法时不必提供。

接口是没有实例域的抽象类。

泛型 Comparable 接口中的 compareTo 方法将返回一个整型数值。

不能使用 new 运算符实例化一个接口，但可声明接口的变量。

### 1.7.2. 试验一下
