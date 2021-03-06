# Android Studio 安装及配置

## AS 安装

1. 网址：<http://www.android-studio.org/>
2. 安装 AS 时，将 SDK 和 AVD 直接安装好（SDK 要选择好安装目录）。
3. 安装 Dart，然后 flutter。
4. 无线连接插件：WIFI ADB ULTIMATE。

## AS 设置

- setting -> Android SDK -> SDK Platforms 选择相应的 SDK 安装，SDK Tools 中 Android SDK Platform-Tools 以及 Android SDK Build-Tools 安装及更新。

- File -> Project Structure：将各种 SDK 都设置成想要的。
- 内存配置：

```txt
-Xms1024m  // JVM启动的起始堆内存
-Xmx4096m  // AndroidStudio 能使用的最大 heap 内存
-XX:MaxPermSize=1024m  // 最大的 Permanent generation 大小。存放的事类本身（不是对象），以及方法，一些固定的字符串等等。
-XX:ReservedCodeCacheSize=512m  // 设置 JIT java compiler 在 compile 的时候的最大代码缓存
-XX:+UseConcMarkSweepGC
-XX:SoftRefLRUPolicyMSPerMB=300
```

- 更改 APK 支持的最低安卓版本：文件 `build.gradle(app)` 中 minSdkVersion-最低支持版本，targetSdkVersion-理想支持版本，compileSdkVersion-编译版本，所以修改 minSdkVersion 就行，minSdkVersion 与 targetSdkVersion 可以理解为一个区间。

- AVD 无法正常打开时，在 settings 里 SDK Tools 安装 Android Emulator，当然相应的 SDK Platform 也要下载。

- setting：
  - 自动导入类。auto import 中勾选 Add unambiguous imports on the fly。
  - 鼠标悬停显示方法说明。Editor --> General --> other 中 show quick...

- 删除无用资源文件。Refactor --> Remove Unused Resources，不要勾选。

## Gradle

- 查看版本：Project Structure 中的 project。
- 更新：将 AS 中 gradle-wrapper.properties 里的版本号改为 [Gradle 版本](http://services.gradle.org/distributions/) 的结尾为 all 就可以了。然后在 AS 的终端输入 gradlew build。在 build.gradle classpath 里修改一下 gradle 的插件号。
- 优化：
  - settings-gradle 中 JVM 改为 java 版本。

## 问题

-  `Cannot resolve symbol 'Theme'`，能用但是红色，在 build.gradle 中注释掉 v7，sync 之后再 添加上就好了，也可以清理一下缓存试试。

- coordinatorLayoutStyle 问题，在 style 中添加 `Base.Theme` 和`<item name="coordinatorLayoutStyle">@style/Widget.Support.CoordinatorLayout</item>`

- 解决 Unknown host 'd29vzk4ow07wi7.cloudfront.net'. You may need to adjust the proxy settings in Gradle. 把 build.gradle(app) 中的两个 jcenter() 用 maven{ url ‘http://maven.aliyun.com/nexus/content/groups/public/’} 代替。

```xml
# 在 gradle.proerties 文件中加入这个，不是很懂
org.gradle.daemon=true
org.gradle.jvmargs=-Xmx2048m -XX:MaxPermSize=512m -XX:+HeapDumpOnOutOfMemoryError -Dfile.encoding=UTF-8
org.gradle.parallel=true
org.gradle.configureondemand=true
```

## Flutter

安装，在 cmd 中选个文件夹执行命令：`git clone -b beta https://github.com/flutter/flutter.git`。

添加环境变量：

```txt
- ANDROID_HOME：Android\sdk\platform-tools 和 Android\sdk\tools
- Path：上面的也加入一遍 和 Android 文件夹
- PUB_HOSTED_URL: https://pub.flutter-io.cn
- FLUTTER_STORAGE_BASE_URL: https://storage.flutter-io.cn
```

在 flutter 目录下找到 flutter_console.bat 进行操作：

- adb：是否安装成功。
- flutter doctor --android-licenses： 注册，可以解决一些问题。
- flutter doctor：发现若干问题，搜索解决就好了。

AS→setting：

- flutter 添加位置 `C:\Users\uppjs\Flutter\flutter`
- Dart 添加位置 `C:\Users\uppjs\Flutter\flutter\bin\cache\dart-sdk`