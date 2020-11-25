<!--
 * @Date: 2020-11-14 20:12:16
 * @LastEditors: uppjs@qq.com
 * @LastEditTime: 2020-11-22 01:44:06
-->
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
7. Color Scheme - Atom OneDark Theme
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

- {MONTH} - 当月；
- {YEAR} - 当年；
- {DAY} - 当天；
- {HOUR} - 当前的小时；
- {MINUTE} - 当前分钟；
- {TIME} - 当前系统时间；
- {DATE} - 当前的系统日期；
- {USER} - 当前用户的登录名；
- {PROJECT_NAME} - 当前项目的名称；
- {MONTH_NAME_FULL} - 一个月的全名；
- {MONTH_NAME_SHORT} - 月份名称的前3个字母；
- {PRODUCT_NAME} - 当前集成开发环境；
- {NAME} - 在文件创建过程中在“新建文件”对话框中指定的新文件的名称；

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
