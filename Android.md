# Android

## Development setup

* Docker for Windows と Android Emulatorを共存させる方法
  * 背景に、Docker for WindowsはHyper-Vを利用（Windowsの仮想化機能）、Android EmulatorはIntelの仮想化機能であるvt-xを利用する
  * 両者は両立できないとかで困っていたが、2017,2018くらいに回避できる設定が入った模様
     * https://www.yuuniworks.com/blog/2018-08-22-docker%E3%81%A8android-emulator%E3%82%92%E5%90%8C%E6%99%82%E3%81%AB%E4%BD%BF%E3%81%86/


## Build APK

```sh
cd <repository>
gradlew assembleDebug

# You can find apk file like below.
<repository>/app/build/outputs/apk/debug/app-debug.apk`
```
