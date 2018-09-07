
flutter问题汇总，便于大家查找

# 环境安装


# 开发

## 技巧类

### InkWell怎么不拦截指定的事件


## 编译类

### 已有的项目增加flutter
https://github.com/flutter/flutter/wiki/Add-Flutter-to-existing-apps

### 为什么插上苹果真机却没办法识别
确保在mac下工作。


## The “Swift Language Version” (SWIFT_VERSION) build setting must be set to a supported value for targets which use Swift. This setting can be set in the build settings editor.


如果是静态库，那么这里可以解决
https://blog.csdn.net/nathan1987_/article/details/79757368

如果是pod，那么参考这里:
https://github.com/CocoaPods/CocoaPods/issues/7098

```
Anything works for me :(

Installing pre-release version
Uninstalling cocoapods and installing it again
s.pod_target_xcconfig = { "SWIFT_VERSION" => "4.0" }
echo "4.0" > .swift-version
I do pod spec lint --verbose --no-clean and I get Pods workspace available at ... for inspection.. When I am opening the project it says that:

This workspace has projects that contain source code developed with Swift 2.x. Xcode 9 does not support building or migrating Swift 2.x targets.
Use Xcode 8.x to migrate the code to Swift 3.


```


# ios -Swift.h not found

https://stackoverflow.com/questions/26328034/importing-project-swift-h-into-a-objective-c-class-file-not-found

基本上是路径不对,试下导入的<>改成"",或者去掉前面的包名，如"AAA/BBB-Swift.h" 改成 "BBB-Swift.h"


# 编译release版本

## 真机运行报错couldn't find "libflutter.so"

https://github.com/flutter/flutter/issues/18939


## Android Studio升级至3.1出现AAPT2 error

https://www.jianshu.com/p/2a63c5710ee9
