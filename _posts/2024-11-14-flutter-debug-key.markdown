---
layout: post
title: flutter android debug key, release key 생성 
tags: [flutter]
---


## 준비
### java11 이상 설치
```
# brew 통해서 설치 가능
brew update
brew install openjdk@11 

# 11 버전 확인 
java --version 
# openjdk version "11.0.19" 2023-04-18
# OpenJDK Runtime Environment Homebrew (build 11.0.19+0)
# OpenJDK 64-Bit Server VM Homebrew (build 11.0.19+0, mixed mode)
```
## 1. debug key 생성
```
cd ~/.android
keytool -genkey -v -keystore debug.keystore -alias androiddebugkey -storepass android -keypass android -keyalg RSA -keysize 2048 -validity 999999 -dname "CN=Android Debug,O=Android,C=US"
```


## 2. release key 생성 
```
cd ~/.android
keytool -genkey -v -keystore release.keystore -alias androidreleasekey -storepass android -keypass android -keyalg RSA -keysize 2048 -validity 999999 -dname "CN=Android Debug,O=Android,C=US"
```

## 

