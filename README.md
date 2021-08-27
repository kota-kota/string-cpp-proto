# string-cpp-proto

`std::string` に文字コード変換機能を拡張させた `my::String`, `my::WString` クラス。

以下の2種類の文字コードの相互変換をサポートしています。

- SJIS
- UTF-8

## ビルド

### Windows

`cmake-gui` を起動して、以下の設定をします。

- Where is the source code：${クローンしたフォルダ}
- Where to build the binaries：${クローンしたフォルダ}/build_windows

`Configure` をクリックします。
ビルドしたいプラットフォームを選択します。

`BUILD_LIBRARY` にチェックを入れて、`Generate` をクリックします。

`Open Project` をクリックしてVisual Studioを起動します。

Visual Studio上でビルドを実行します。

### Linux

```bash
$ mkdir build_linux
$ cd build_linux

# x86_64 Debug
$ cmake .. -DCMAKE_BUILD_TYPE=Debug -DCMAKE_TOOLCHAIN_FILE=../cmake/x86_64.clang.toolchain.cmake
# x86_64 Release
$ cmake .. -DCMAKE_BUILD_TYPE=Release -DCMAKE_TOOLCHAIN_FILE=../cmake/x86_64.clang.toolchain.cmake
# arm64 Debug
$ cmake .. -DCMAKE_BUILD_TYPE=Debug -DCMAKE_TOOLCHAIN_FILE=../cmake/aarch64.clang.toolchain.cmake
# arm64 Release
$ cmake .. -DCMAKE_BUILD_TYPE=Release -DCMAKE_TOOLCHAIN_FILE=../cmake/aarch64.clang.toolchain.cmake
```

### Android

```bash
$ mkdir build_android
$ cd build_android

# x86_64 Debug
$ cmake .. -DCMAKE_BUILD_TYPE=Debug -DCMAKE_TOOLCHAIN_FILE=/opt/android-sdk-linux/android-ndk-r21e/build/cmake/android.toolchain.cmake -DANDROID_ABI=x86_64 -DANDROID_PLATFORM=16
# x86_64 Release
$ cmake .. -DCMAKE_BUILD_TYPE=Release -DCMAKE_TOOLCHAIN_FILE=/opt/android-sdk-linux/android-ndk-r21e/build/cmake/android.toolchain.cmake -DANDROID_ABI=x86_64 -DANDROID_PLATFORM=16
# arm64-v8a Debug
$ cmake .. -DCMAKE_BUILD_TYPE=Debug -DCMAKE_TOOLCHAIN_FILE=/opt/android-sdk-linux/android-ndk-r21e/build/cmake/android.toolchain.cmake -DANDROID_ABI=arm64-v8a -DANDROID_PLATFORM=16
# arm64-v8a Release
$ cmake .. -DCMAKE_BUILD_TYPE=Release -DCMAKE_TOOLCHAIN_FILE=/opt/android-sdk-linux/android-ndk-r21e/build/cmake/android.toolchain.cmake -DANDROID_ABI=arm64-v8a -DANDROID_PLATFORM=16
```
