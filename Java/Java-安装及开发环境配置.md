# Java 安装及开发环境配置

## 安装

1. 下载 Java 开发工具包 JDK，<http://www.oracle.com/technetwork/java/javase/downloads/index.html>。
2. 选择目录进行安装。

## 环境变量

右击“我的电脑”→“属性”→“高级系统设置”→“高级”→“环境变量”。

系统变量三个属性名和值：

- JAVA_HOME：C:\Program Files (x86)\Java\jdk1.8.0_91 // 要根据自己的实际路径配置
- CLASSPATH：.;%JAVA_HOME%\lib\dt.jar;%JAVA_HOME%\lib\tools.jar //记得前面有个"."
- Path：%JAVA_HOME%\bin;%JAVA_HOME%\jre\bin

测试是否成功：

- 测试是否安装成功：“开始”→“运行”，键入“cmd”。
- 键入命令：java -version，java，javac。出现正确信息说明配置成功。

## 解释三个环境变量

CLASSPATH 是什么？它的作用是什么？

它是 javac 编译器的一个环境变量。它的作用与 import、package 关键字有关。当你写下 `improt java.util.*` 时，编译器面对 import 关键字时，就知道你要引入 java.util 这个 package 中的类；但是编译器如何知道你把这个 package 放在哪里了呢？所以你首先得告诉编译器这个 package 的所在位置；如何告诉它呢？就是设置 CLASSPATH 啦 :) 如果 java.util 这个 package 在 c:/jdk/ 目录下，你得把 c:/jdk/这个路径设置到 CLASSPATH 中去！当编译器面对 import java.util.*这个语句时，它先会查找 CLASSPATH 所指定的目录，并检视子目录 java/util 是否存在，然后找出名称吻合的已编译文件（.class 文件）。如果没有找到就会报错！CLASSPATH 有点像 c/c++编译器中的 INCLUDE 路径的设置哦，是不是？当 c/c++编译器遇到 include 这样的语句，它是如何运作的？哦，其实道理都差不多！搜索 INCLUDE 路径，检视文件！当你自己开发一个 package 时，然后想要用这个 package 中的类；自然，你也得把这个 package 所在的目录设置到 CLASSPATH 中去！CLASSPATH 的设定，对 JAVA 的初学者而言是一件棘手的事。所以 Sun 让 JAVA2 的 JDK 更聪明一些。你会发现，在你安装之后，即使完全没有设定 CLASSPATH，你仍然能够编译基本的 JAVA 程序，并且加以执行。

---

1. PATH 环境变量。作用是指定命令搜索路径，在命令行下面执行命令如 javac 编译 java 程序时，它会到 PATH 变量所指定的路径中查找看是否能找到相应的命令程序。我们需要把 jdk 安装目录下的 bin 目录增加到现有的 PATH 变量中，bin 目录中包含经常要用到的可执行文件如 javac/java/javadoc 等待，设置好 PATH 变量后，就可以在任何目录下执行 javac/java 等工具了。我们这里设定的 PATH 值为：%SystemRoot%/system32;%SystemRoot%;%SystemRoot%/System32/Wbem;%SYSTEMROOT%/System32/WindowsPowerShell/v1.0/;C:/Program Files/Common Files/Thunder Network/KanKan/Codecs;C:/Program Files/Microsoft SQL Server/90/Tools/binn/;C:/Program Files/Common Files/TTKN/Bin;C:/Program Files/Common Files/Teleca Shared;C:/Program Files/Java/jdk1.6.0_21/bin 上述只有红色部分;C:/Program Files/Java/jdk1.6.0_21/bin 是 java 的 PATH 变量，注意变量之间需要用";”隔开。
2. CLASSPATH 环境变量。作用是指定类搜索路径，要使用已经编写好的类，前提当然是能够找到它们了，JVM 就是通过 CLASSPATH 来寻找类的。我们需要把 jdk 安装目录下的 lib 子目录中的 dt.jar 和 tools.jar 设置到 CLASSPATH 中，当然，当前目录“.”也必须加入到该变量中。这里 CLASSPATH 为：.;C:/Program Files/Java/jdk1.6.0_21/lib/dt.jar;C:/Program Files/Java/jdk1.6.0_21/lib/tools.jar
3. JAVA_HOME 环境变量。它指向 jdk 的安装目录，Eclipse/NetBeans/Tomcat 等软件就是通过搜索 JAVA_HOME 变量来找到并使用安装好的 jdk。这里 JAVA_HOME 为：C:/Program Files/Java/jdk1.6.0_21
