## [Android Studio]()

<font size="2">

Android Studio 安装好以后默认会在系统盘用户目录下(C:\Users\用户名\)生成文件夹
* .android：这个文件夹是Android SDK生成的AVD（Android Virtual Device Manager）即模拟器存放路径
* .AndroidStudio：这个文件夹是Android Studio的配置文件夹，主要存放一些AndroidStudio设置和插件和项目的缓存信息
* .gradle 这个文件夹是构建工具 Gradle的配置文件夹，也会存储一些项目的构建缓存信息

</font>

#### .AndroidStudio文件夹路径的修改

<font size="2">进入Android Studio的安装目录，进入bin文件夹，用文本编辑软件打开idea.properties，去掉以下两项的注释符号#，修改对应的路径为新路径即可。</font>

```
idea.config.path=G:/AndroidStudioSetup/.AndroidStudio3.x/config
idea.system.path=G:/AndroidStudioSetup/.AndroidStudio3.x/system
```

#### .gradle文件夹路径的修改

<font size="2">

Android Studio > File > Settings... > Build, Execution, Deployment > Gradle > General settings > Gradle user home

</font>

#### .android文件夹路径的修改

<font size="2">

添加环境变量 ANDROID_AVD_HOME 或 ANDROID_SDK_HOME = `D:\Program Files\Android`, 这样以后下载的模拟器都下到这个目录下了

</font>