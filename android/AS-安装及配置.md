# Android Studio 安装及配置

## AS 安装

1. 网址：<http://www.android-studio.org/>
2. 安装 AS 时，将 SDK 和 AVD 直接安装好（SDK 要选择好安装目录）。
3. 无线连接插件：ADB idea、ADB WiFi 和 Android WiFi ADB。

## AS 设置

1. setting -> Android SDK -> SDK Platforms 选择相应的 SDK 安装，SDK Tools 中 Android SDK Platform-Tools 安装。
2. File -> Project Structure：将各种 SDK 都设置成想要的。
3. 内存配置：

```txt
-Xms1024m  // JVM启动的起始堆内存
-Xmx4096m  // AndroidStudio 能使用的最大 heap 内存
-XX:MaxPermSize=1024m  // 最大的 Permanent generation 大小。存放的事类本身（不是对象），以及方法，一些固定的字符串等等。
-XX:ReservedCodeCacheSize=512m  // 设置 JIT java compiler 在 compile 的时候的最大代码缓存
-XX:+UseConcMarkSweepGC
-XX:SoftRefLRUPolicyMSPerMB=300
```

## Flutter

安装，在 cmd 中选个文件夹执行命令：`git clone -b beta https://github.com/flutter/flutter.git`。

添加环境变量：

- ANDROID_HOME：Android\platform-tools 和 Android\sdk\tools
- Path：上面的也加入一遍 和 Android 文件夹

命令行：

- adb：是否安装成功。
- flutter doctor --android-licenses： 注册，可以解决一些问题。
- flutter doctor：发现若干问题，搜索解决就好了。
