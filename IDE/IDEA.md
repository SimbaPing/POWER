# IDEA 安装与调试

## IDEA 安装

1. 网址：<https://www.jetbrains.com/idea/download/#section=windows/>
2. 下载后选择安装目录进行安装。
3. 登录账号同步设置。
4. 通过安装插件可以代替（非绝对）PhpStorm、PyCharm、WebStorm。IDEA 主要还是用来写 Java 的。

## settings

1. Appearance - show memory indicator = 右下角显示内存大小
2. Font - Consolas 12 1.1 microsoft YaHei UI
3. code completion - 去掉 ✔ Match case all letter = 提示不分大小写
4. File Encodings - 都改为 UTF-8 ✔ Transparent native-to-ascii conversion
5. Editor Tabs - ✔ Mark modified = 用 * 标识编辑过的文件
6. System Settings - 去掉 reopen ✔ open project in the same window
7. Color Scheme - Atom One Dark
8. GitHub - Token

## plugs

1. Atom File icons IDEA = 图标样式
2. Rainbow Bracket = 彩虹括号
3. codeGlace = 右侧小地图
4. Statistic = 代码统计
5. .ignore = 忽略杂文件
6. liveEdit = 在 Chrome 实时调试
7. ESLint = 代码检查工具
8. NodeJS

## 头文件

` Created with IntelliJ IDEA by Django on ${DATE} ${TIME} `

## 快捷键

1. Ctrl + W = 扩选
2. 新建
  - java: alt + 引号
  - python: alt + 冒号
  - html: atl + H
  - css: alt + <
  - javascript: alt + >

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
