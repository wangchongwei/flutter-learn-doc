### flutter数据持久化



##### shared_preferences

本地存储临时数据
此插件在 iOS 上使用 NSUserDefaults，在 Android 上使用 SharedPreferences，为简单数据提供持久存储。

添加插件依赖：

```
// 在pubspec.yaml文件中添加依赖

dependencies:
  flutter:
    sdk: flutter
  shared_preferences: "<newest version>"


```

调用：

shared_preference 存储方式是根据key-value形式
使用便捷，但有限制：
    a: 只能使用原始类型: int，double，bool，string 和 string list。
    b: 它不是用来存储大量数据，因此不适合作为应用程序缓存。

```

import 'package:shared_preferences/shared_preferences.dart';

getAsyncData() async {
    // 获取实例
    var prefs = await SharedPreferences.getInstance();
    // 获取存储数据
    var count = prefs.getInt('count') ?? 0 + 1;
    // 设置存储数据
    await prefs.setInt('count', count);
}


```

