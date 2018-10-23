# APP

## 新建

1. Start a new Android Studio project - 新建项目。
2. 应用名称，公司域名，项目本地地址，包名默认。
3. Target Android Devices - 默认就好。
4. Add an Activity to Mobile - 一般选择 Empty。
5. 活动名字和布局命名。

## 建议

1. 删除无用的 Activity - Safe Delete。

## 错误

- App is not indexable by Google Search; consider adding at least one Activity with an ACTION-VIEW intent filter. See issue explanation for more details.
  - 解决：build.gradle(app) =》android 中添加：
  - ```txt
    lintOptions {
            disable 'GoogleAppIndexingWarning'
            baseline file("lint-baseline.xml")
    }
    ```

- On SDK version 23 and up, your app data will be automatically backed up and restored on app install. Consider adding the attribute android:fullBackupContent to specify an @xml resource which configures which files to backup.
  - 解决：在 AndroidMainifests.xml =》 application 中添加：
  - ```txt
    android:allowBackup="true"
    android:fullBackupContent="true"
    ```

- Type parameter T has incompatible upper bounds: View and TextView.
  - File -> Invalidate Caches / Restart，这是清理缓存并重启吧
