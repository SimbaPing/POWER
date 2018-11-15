# Java 安装及开发环境配置

## 安装

1. 下载 Java 开发工具包，别问为什么，下载奇数版就对了。[点我下载 JDK](http://www.oracle.com/technetwork/java/javase/downloads/index.html)。
2. 选择合适目录进行安装。`C:\Program Files\Java\jdk`。

## 环境变量

右击“我的电脑”→“属性”→“高级系统设置”→“高级”→“环境变量”。

系统变量三个属性名和值：

```txt
JAVA_HOME：C:\Program Files (x86)\Java\jdk1.8.0_91  // JDK 的目录
Path：%JAVA_HOME%\bin
（JDK1.5 以上不需要配置这个 CLASSPATH）。
```

测试是否成功：

- 测试是否安装成功：“开始”→“运行”，键入“cmd”。
- 键入命令：java -version，java，javac。出现正确信息说明配置成功。
