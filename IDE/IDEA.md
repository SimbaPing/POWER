<!--
 * @Date: 2020-11-14 20:12:16
 * @LastEditors: uppjs@qq.com
 * @LastEditTime: 2021-01-07 10:32:34
-->
# IDEA 安装与调试

## IDEA 安装

- 网址：<https://www.jetbrains.com/idea/download/#section=windows/>
- 下载后选择安装目录进行安装。
- 登录账号同步设置（File→Manage IDE Setting）。
- 通过安装插件可以代替（非绝对）PhpStorm、PyCharm、WebStorm。IDEA 主要还是用来写 Java 的。

## 编辑器优化

### 设置

- 先设置成中文，将看得懂的优化一下
- 修改内存：Help→Edit Custom VM，前三个值1024 2048 1024
- Appearance - show memory indicator = 右下角显示内存大小
- Font - Consolas 12 1.1 microsoft YaHei UI
- code completion - 去掉 √ Match case all letter = 提示不分大小写
- File Encodings - 都改为 UTF-8 √ Transparent native-to-ascii conversion
- Editor Tabs - √ Mark modified = 用 * 标识编辑过的文件
- System Settings - 去掉 reopen √ open project in the same window

### 主题优化

- Material Theme UI
  - Atom One Dark
  - √ Contrast Mode
  - 全√ Compact
  - √ Custom Sidebar Height 18
  - √ Custom Tree Indent 2
  - √ Transparent Scrollbars
  - √ Tabs Shadow
  - √ Material File Status Colors
  - 全√ other Tweaks
- Atom Material Icons
  - 除了隐形和黑白全√
  - Arrows style Material


### 快捷键

- 扩选 = Ctrl + W
- 直接运行当前代码 = ALT + A
- 新建
  - java: alt + 引号
  - python: alt + 冒号
  - html: atl + H
  - css: alt + <
  - javascript: alt + >

### plugs

- 综合性插件
  - Atom File icons IDEA = 图标样式
  - Rainbow Bracket = 彩虹括号
  - codeGlace = 右侧小地图
  - .ignore = 忽略杂文件
  - liveEdit = 在 Chrome 实时调试
  - ESLint = 代码检查工具
  - NodeJS
  - IDE Eval Reset = 循环试用
- 统计类插件
  - wakatime
  - CodeTime
  - Statistic

### 头文件

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

