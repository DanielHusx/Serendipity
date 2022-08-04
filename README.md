# Serendipity
**Serendipity** 是集自动打包上传、描述文件管理、崩溃日志解析、符号表解析功能为一体的mac应用

代码主要用SwiftUI编写、纯本地工具管理类应用（说真的，SwiftUI资料是真的少）



#### 环境支持

- macOS 11.0+



### 核心功能简要：

- 自动打包支持`.git`, `Podfile`, `.xcworkspace`, `.xcodeproj`, `.ipa`, `.xcarchive`识别
- 上传应用支持`蒲公英`、`Fir.im`。另：理论上支持上传至AppStore~ 嗯，理论上~
- 描述文件管理器可管理全盘的`.mobileprovision`文件，自动解析识别已过期文件，支持搜索文件内容
- 崩溃日志支持创建、打开与导入识别`.log`, `.crash`, `.ips`文件
- 崩溃日志解析支持友盟、Apple Crash格式
- 符号表管理器会自动搜索全盘`.dSYM`、`.xcarchive`文件内的可执行文件，解析其架构、UUID等内容以供崩溃日志符号化



### 主页面

- 提供添加任务、描述文件管理器、符号表管理器、崩溃日志管理器的入口。相关快捷键，具体在菜单栏 “视图”中显示
- 可编辑、运行、暂停任务以及快捷修改更新日志
- 少量的日志展示

![main](Capture/main.jpg)



### 描述文件管理器

- 右上角可搜索具体描述文件内所有内容
- 中下方可搜索文件名以及UUID等

![profile](Capture/profile.jpg)



### 符号表管理器

- 由于符号表量大所以展示比较粗糙~ 嘿嘿

![symbol](Capture/symbol.jpg)



### 崩溃日志

- 支持官方崩溃日志以及友盟日志格式解析
- 日志解析查阅官方文档上的少量异常解析的说明展示
- 支持自定义地址符号化
- 虽然内置了`symbolicatecrash`脚本，但实际上自己参照它的逻辑用swift实现它的功能~ 感觉大概可能或许理论上不会慢~ 嗯，应该不会慢...太多吧

![友盟解析](Capture/crashmanager.jpg)

![Apple Crash解析](Capture/crash_apple.jpg)

![创建日志](Capture/crash_new.jpg)

### 自动打包上传

- 添加任务支持文件夹, `.git`, `Podfile`, `.xcworkspace`, `.xcodeproj`, `.ipa`, `.xcarchive`识别。**输入后Enter会开始识别相关内容，如果是文档路径自会识别该路径下所有可识别的文件**
- Xcode项目目前支持编辑版本号（自增）、build号（自增）、签名以及导出配置等。（**如果存在导出配置时，那么结束运行任务后会重置编辑项，相当于编辑项只对运行任务时生效**）
- 添加其他的`.xcarchive`, `.ipa`解析，可在上传时一并导包上传
- 发布配置可支持`蒲公英`、`Fir.im`
- 发布配置理论上支持上传至AppStore，内置写了xcrun altool相关命令。可以试试~

![add_task](Capture/add_task.jpg)

![config_engineer](Capture/config_engineer.jpg)

![config_distribution](Capture/config_distribution.jpg)

### NOTE:

2022-08-04

- 七夕发布第一个版本~ 希望会有人喜欢吧


---
如果你觉得还不错，就赞一个啦~ 谢谢！

[MIT LICENSE](LICENSE)
