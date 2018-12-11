### 一. 国内镜像地址
当前用户目录下：vi ~/.bash_profile
~~~
 # fultter
  export PUB_HOSTED_URL=https://pub.flutter-io.cn
  export FLUTTER_STORAGE_BASE_URL=https://storage.flutter-io.cn
 
~~~
~~~
source ~/.bash_profile
~~~
### 二.安装sdk
* 1. 建立 flutterProjects目录下载sdk,
~~~
git clone -b dev https://github.com/flutter/flutter.git
cd ./flutter
flutter doctor
~~~
* 2.运行结果：
~~~
[✓] Flutter (Channel dev, v1.0.0, on Mac OS X 10.13.5 17F77, locale zh-Hans-CN)
[✗] Android toolchain - develop for Android devices
    ✗ Unable to locate Android SDK.
      Install Android Studio from: https://developer.android.com/studio/index.html
      On first launch it will assist you in installing the Android SDK components.
      (or visit https://flutter.io/setup/#android-setup for detailed instructions).
      If Android SDK has been installed to a custom location, set $ANDROID_HOME to that location.
      You may also want to add it to your PATH environment variable.

[!] iOS toolchain - develop for iOS devices (Xcode 9.4.1)
    ✗ libimobiledevice and ideviceinstaller are not installed. To install with Brew, run:
        brew update
        brew install --HEAD usbmuxd
        brew link usbmuxd
        brew install --HEAD libimobiledevice
        brew install ideviceinstaller
    ✗ ios-deploy not installed. To install with Brew:
        brew install ios-deploy
    ✗ CocoaPods not installed.
        CocoaPods is used to retrieve the iOS platform side's plugin code that responds to your plugin usage on the Dart
        side.
        Without resolving iOS dependencies with CocoaPods, plugins will not work on iOS.
        For more info, see https://flutter.io/platform-plugins
      To install:
        brew install cocoapods
        pod setup
[!] Android Studio (not installed)
[!] VS Code (version 1.29.1)
[!] Connected device
    ! No devices available

! Doctor found issues in 5 categories.

~~~

* 3.根据提示
第一个对勾：说明Flutter安装成功，
vi ~/.bash_profile
~~~
# FLUTTER_HOME 为你自己的gitclone下来到目录，待会儿再来下载
export FLUTTER_HOME=/Users/tom/flutterProjects/flutter/bin/flutter
export PATH=${FLUTTER_HOME}/bin:$PATH
# 或者
export PATH="/Users/tom/goprojects/bin:{"$PATH"}"
~~~
~~~
source ~/.bash_profile
~~~
没有对勾的组件参考提示，继续安装，例如：

iOS toolchain - develop for iOS devices (Xcode 9.4.1)

~~~

# tom @ tom-pc in ~/flutterProjects/flutter on git:dev o [20:13:41] C:1
$ brew update
        brew install --HEAD usbmuxd
        brew link usbmuxd
        brew install --HEAD libimobiledevice
        brew install ideviceinstaller
~~~

* 4.执行成功后，再次执行 
~~~
flutter doctor
~~~
* 5.查看组件安装是否成功(是否有对勾),继续根据提示安装

~~~
# tom @ tom-pc in ~/flutterProjects/flutter on git:dev o [20:17:57]
$ flutter doctor
Doctor summary (to see all details, run flutter doctor -v):
[✓] Flutter (Channel dev, v1.0.0, on Mac OS X 10.13.5 17F77, locale zh-Hans-CN)
[✗] Android toolchain - develop for Android devices
    ✗ Unable to locate Android SDK.
      Install Android Studio from: https://developer.android.com/studio/index.html
      On first launch it will assist you in installing the Android SDK components.
      (or visit https://flutter.io/setup/#android-setup for detailed instructions).
      If Android SDK has been installed to a custom location, set $ANDROID_HOME to that location.
      You may also want to add it to your PATH environment variable.

[!] iOS toolchain - develop for iOS devices (Xcode 9.4.1)
    ✗ ios-deploy not installed. To install with Brew:
        brew install ios-deploy
    ✗ CocoaPods not installed.
        CocoaPods is used to retrieve the iOS platform side's plugin code that responds to your plugin usage on the Dart
        side.
        Without resolving iOS dependencies with CocoaPods, plugins will not work on iOS.
        For more info, see https://flutter.io/platform-plugins
      To install:
        brew install cocoapods
        pod setup
[!] Android Studio (not installed)
[!] VS Code (version 1.29.1)
[✓] Connected device (1 available)

! Doctor found issues in 4 categories.

# tom @ tom-pc in ~/flutterProjects/flutter on git:dev o [20:27:47]
$ brew install ios-deploy
~~~

### 三、vscode写第一个项目
* 1.安装Flutter插件
~~~
启动 VS Code
调用 View>Command Palette…
输入 ‘install’, 然后选择 Extensions: Install Extension action
在搜索框输入 flutter , 在搜索结果列表中选择 ‘Flutter’, 然后点击 Install
选择 ‘OK’ 重新启动 VS Code
通过Flutter Doctor验证您的设置
调用 View>Command Palette…
输入 ‘doctor’, 然后选择 ‘Flutter: Run Flutter Doctor’ action
查看“OUTPUT”窗口中的输出是否有问题
~~~
* 2.创建项目
在vscode 下，创建目录应该是在。
调用 View>Command Palette…（ctrl + shift + p）
输入 ‘flutter’, 然后选择 ‘Flutter: New Project’ action
输入 Project 名称 (如myapp), 回车键 等待创建成功。

* 3.f5运行
[详见](https://flutterchina.club/get-started/codelab/)

> reference
* [flutterchina](https://flutterchina.club/setup-macos/)
