# flutter-learn-doc
flutter 学习时归纳知识点

## 该路径都是.md文件，解释性说明

### 依赖下载

当需要下载一个插件，但不知道该插件最新版本时,
可以用any取代，如：

```
dependencies:
  flutter:
    sdk: flutter

  shared_preferences: any

```
我需要下载shared_preferences插件，但不知道最新版本，此时用any取代，修改后保存文件即会自动下载最新版本的该插件

再在pubspec.lock文件中可以查看到该插件的版本号，最好再用该版本号替换掉此处的any
