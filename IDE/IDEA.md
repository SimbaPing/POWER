# IDEA 安装与调试

## IDEA 安装

1. 网址：<https://www.jetbrains.com/idea/download/#section=windows/>
2. 下载后选择安装目录进行安装。
3. 选择是否导入之前配置。
4. 通过安装插件可以代替（非绝对）PhpStorm、PyCharm、WebStorm。IDEA 主要还是用来写 Java 的。

## 使用

主题：Atom One Dark

文字字体、大小，行高：Consolas，Microsoft Yahei UI，14，1.1

## 修改内存

- idea64.exe.vmoptions

```txt
-server
-Xms1024m
-Xmx4096m
-XX:MaxPermSize=1024m
-XX:ReservedCodeCacheSize=512m
-XX:+UseConcMarkSweepGC
-XX:SoftRefLRUPolicyMSPerMB=300
-ea
-Dsun.io.useCanonCaches=false
-Djava.net.preferIPv4Stack=true
-Djdk.http.auth.tunneling.disabledSchemes=""
-XX:+HeapDumpOnOutOfMemoryError
-XX:-OmitStackTraceInFastThrow
```

- idea.exe.vmoptions

```txt
-Xms1024m
-Xmx4096m
-XX:MaxPermSize=1024m
-XX:ReservedCodeCacheSize=512m
-XX:+UseConcMarkSweepGC
-XX:SoftRefLRUPolicyMSPerMB=300
-ea
-Dsun.io.useCanonCaches=false
-Djava.net.preferIPv4Stack=true
-Djdk.http.auth.tunneling.disabledSchemes=""
-XX:+HeapDumpOnOutOfMemoryError
-XX:-OmitStackTraceInFastThrow
```

## 快捷键

## 插件
