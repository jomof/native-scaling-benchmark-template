
#language: android
#jdk: oraclejdk8

env:
  global:
#     - ANDROID_API_LEVEL=23
#     - ANDROID_BUILD_TOOLS_VERSION

before_install:
    - chmod +x gradlew

install:

#  - wget --no-check-certificate "https://cmake.org/files/v3.10/cmake-3.10.2-Linux-x86_64.tar.gz"
#  - tar -xzf cmake-3.10.2-Linux-x86_64.tar.gz
  
#  - wget --no-check-certificate https://github.com/ninja-build/ninja/releases/download/v1.8.2/ninja-linux.zip
#  - unzip ninja-linux.zip
#  - mv ninja cmake-3.10.2-Linux-x86_64/bin
  
#  - wget --no-check-certificate https://dl.google.com/android/repository/sdk-tools-linux-3859397.zip
#  - unzip sdk-tools-linux-3859397.zip
#  - yes | tools/bin/sdkmanager --licenses
  
#  - ccache --version
  
  
#   - wget --no-check-certificate https://dl.google.com/android/repository/android-ndk-r13b-linux-x86_64.zip -O android-ndk-r13b-linux-x86_64.zip
#   - unzip android-ndk-r13b-linux-x86_64.zip > android-ndk-r13b-linux-x86_64.uncompress-log 2>&1
#   - export ANDROID_NDK_HOME=$PWD/android-ndk-r13b
#   - wget https://github.com/Commit451/android-cmake-installer/releases/download/1.1.0/install-cmake.sh
#   - chmod +x install-cmake.sh
#   - "./install-cmake.sh"
#   - find ${ANDROID_HOME}/cmake/*/bin/cmake

script:
 # - echo sdk.dir=$PWD > local.properties 
 # - echo cmake.dir=$PWD/cmake-3.10.2-Linux-x86_64 >> local.properties 
 # - cat local.properties
  - ./gradlew assemble

#   - android list targets
  
#   - echo no | android create avd --force -n test -t android-22 --abi armeabi-v7a
#   - emulator -avd test -no-audio -no-window &
#   - android-wait-for-emulator
#   - adb shell input keyevent 82 &
  
#   - ./gradlew connectedAndroidTest
