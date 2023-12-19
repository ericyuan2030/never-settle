# adb操作1

### 1.将文本粘贴到adb：

```
adb shell am start-foreground-service -n com.ylw.mediascan/com.ylw.mediascan.clip.MyClipService -a set --es type text --es text \\"测试123\\"

```

### 2.从adb获取粘贴的文本：

```
adb shell am broadcast -a "com.ylw.clip.get"

```

### 3.刷新文档中的图片/视频：

```
adb shell am start-foreground-service -n com.ylw.mediascan/com.ylw.mediascan.clip.MyClipService -a set --es type scan

adb shell am start-foreground-service -n com.ylw.mediascan/com.ylw.mediascan.clip.MyClipService -a activity

```

### 4.将应用程序变为系统应用的方法：

[https://juejin.cn/post/7052229760503513095](https://juejin.cn/post/7052229760503513095)

```
adb shell pm grant com.ylw.mediascan android.permission.READ_LOGS；

adb shell pm grant com.dp.logcatapp android.permission.READ_LOGS

adb shell am start-foreground-service -n com.ylw.mediascan/com.ylw.mediascan.clip.MyClipService -a activity

```

```
java -jar signapk.jar platform.x509.pem platform.pk8 /Users/ylw/AndroidProjects/BlankProjec19/app/release/app-release.apk app_release_sign.apk

/Users/ylw/Library/Android/sdk/build-tools/30.0.2/zipalign -p -f -v 4 /Users/ylw/Documents/system/app_release_sign.apk /Users/ylw/Documents/system/app_release_sign_zip.apk

ai /Users/ylw/Documents/system/app_release_sign_zip.apk

```

## 总结
本文主要介绍了adb shell命令在Android开发中的应用。其中，第1和第2部分介绍了如何在adb中粘贴和获取文本，第3部分介绍了如何刷新文档中的图片/视频。另外，本文还介绍了将应用程序变为系统应用的方法。

1. adb shell命令用于在Android设备上执行命令。使用`am start-foreground-service`命令并提供要粘贴的文本，可以将文本粘贴到设备中。使用`am broadcast`命令并提供指定的广播动作，可以获取设备上的粘贴文本。
2. 在Android设备上，使用`am start-foreground-service`命令并提供指定的广播动作，可以刷新文档中的图片/视频。
3. 将应用程序变为系统应用需要授予应用程序读取日志的权限，并使用`pm grant`命令进行授权。然后，使用`am start-foreground-service`命令并提供指定的广播动作，即可将应用程序变为系统应用。