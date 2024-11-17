[fork from](https://github.com/KingWu/flutter_starter_kit)

```
git clone https://github.com/KingWu/flutter_starter_kit.git
```


# Flutter Starter Kit - 应用商店示例

一个为初学者设计的入门工具包，使用 Bloc 模式、RxDart、sqflite、Fluro 和 Dio 构建 Flutter 项目。此示例项目构建了一个应用商店 (App Store) 应用作为案例。

![App Store Flutter 演示](https://i.ibb.co/FsyWhpY/ezgif-3-5dbb34baf658.gif)

## 功能特色

- **Bloc 模式**
- 使用 [Fluro](https://github.com/theyakka/fluro) 进行页面导航
- 使用 [sqflite](https://github.com/tekartik/sqflite) 实现本地缓存
- 使用 [Dio](https://github.com/flutterchina/dio) 进行 RESTful API 调用
- 使用 [flutter_stetho](https://github.com/brianegan/flutter_stetho) 进行数据库调试（仅支持 Android）
- 网络图片加载
- 使用 [gen_lang](https://github.com/KingWu/gen_lang) 和 [lang_table](https://github.com/KingWu/lang_table) 实现本地化
- 根据不同项目环境（开发、预发布、生产）设置环境变量和项目配置（如应用名称、Bundle ID）
- 使用 `json_serializable` 生成 POJO 类
- 当列表项数据变化时，仅更新对应项，而非重新渲染整个列表视图
- Hero 动画
- 在列表为空时显示空视图

## 安装指南

1. 按照 Flutter 的[官方安装指南](https://flutter.io/docs/get-started/install)设置 Flutter 开发环境。
2. 下载 [Flutter 版本 1.17.3](https://flutter.dev/docs/development/tools/sdk/releases)。

**备注**：此工具包支持 Flutter 1.17.3 版本，因为较新版本可能包含破坏性更改。

## 运行配置

1. 点击“Edit Configuration”（编辑配置）。
2. 为不同环境创建运行配置。

![编辑配置](https://i.ibb.co/sbkgnmN/Screen-Shot-2019-01-13-at-7-28-44-PM.png)

![配置](https://i.ibb.co/tqPgMVz/Screen-Shot-2019-01-13-at-7-52-38-PM.png)

![环境](https://i.ibb.co/hCP2QJ1/Screen-Shot-2019-01-13-at-7-40-16-PM.png)

## 常用命令

### 运行 `flutter_starter_kit`

开发环境：

```bash
flutter run --flavor development -t lib/config/main_development.dart
```

预发布环境：

```bash
flutter run --flavor staging -t lib/config/main_staging.dart
```

生产环境：

```bash
flutter run --flavor production -t lib/config/main_production.dart
```

### 生成 JSON 序列化和反序列化函数

```bash
flutter packages pub run build_runner build --delete-conflicting-outputs
```

### 使用 `lang_table`

```bash
flutter packages pub run lang_table:generate --platform=airTable --input=https://api.airtable.com/v0/appZmh0WMg3y6APAg/example --api-key={YOUR API KEY} --target=Flutter
```

### 使用 `gen_lang`

```bash
flutter packages pub run gen_lang:generate
```

## 已知问题

- [在 iOS 模拟器上运行不同环境的应用时无法启动](https://github.com/flutter/flutter/issues/21335)

## 迁移指南

如果你想将此项目作为你项目的基础，请阅读 [迁移指南](https://github.com/KingWu/flutter_starter_kit/wiki/Migration-Guide)。

## 参考资源

- [我的 Flutter 学习路径](https://medium.com/@kingwu/flutter-learning-path-d6b3b0235799)

#### 来自其他平台？

- [面向 Android 开发者的 Flutter 指南](https://flutter.io/docs/get-started/flutter-for/android-devs)
- [面向 iOS 开发者的 Flutter 指南](https://flutter.io/docs/get-started/flutter-for/ios-devs)
- [面向 React Native 开发者的 Flutter 指南](https://flutter.io/docs/get-started/flutter-for/react-native-devs)
- [面向 Web 开发者的 Flutter 指南](https://flutter.io/docs/get-started/flutter-for/web-devs)
- [面向 Xamarin.Forms 开发者的 Flutter 指南](https://flutter.io/docs/get-started/flutter-for/xamarin-forms-devs)

#### 学习 Widget 和布局

- [构建布局](https://flutter.io/docs/development/ui/layout)
- [Widget 目录](https://flutter.io/docs/development/ui/widgets)
- [每周一个 Flutter Widget 视频系列](https://www.youtube.com/playlist?list=PLOU2XLYxmsIL0pH0zWe_ZOHgGhZ7UasUE)
- [Flutter Widget 101 视频系列](https://www.youtube.com/playlist?list=PLOU2XLYxmsIJyiwUPCou_OVTpRIn_8UMd)

#### Bloc 模式

- [使用 Bloc 模式架构你的 Flutter 项目](https://medium.com/flutterpub/architecting-your-flutter-project-bd04e144a8f1)

#### JSON 序列化

- [JSON 与序列化](https://flutter.io/docs/development/data-and-backend/json)

#### 本地化

- [Flutter 本地化新方法](https://medium.com/@kingwu/a-new-approach-of-localization-in-flutter-e18bfb2b14ab)
- [Flutter 国际化教程：第三部分— Android Studio 插件](https://medium.com/@datvt9312/flutter-internationalization-tutorials-part-3-android-studio-plugin-8604e2dc90f0)
- [让 Flutter 应用支持多语言开发流程](https://medium.com/@zonble/%E8%AE%93-flutter-app-%E6%94%AF%E6%8F%B4%E5%A4%9A%E5%9C%8B%E8%AA%9E%E7%B3%BB%E7%9A%84%E9%96%8B%E7%99%BC%E6%B5%81%E7%A8%8B-ceb31532e2e1)

#### 项目多环境支持

- [Flutter 环境区分（Flavour）指南](https://medium.com/@salvatoregiordanoo/flavoring-flutter-392aaa875f36)
- [创建 Flutter 应用的环境区分（Flutter & Android 设置）](http://cogitas.net/creating-flavors-of-a-flutter-app/)

#### 高级主题

- [Flutter 的分层设计](https://www.youtube.com/watch?time_continue=1&v=dkyY9WCGMi0)
- [Flutter 的渲染管道](https://www.youtube.com/watch?v=UUfXWzp0-DU)

### 支持者

- [Plaker Lab 创玩坊](https://www.plakerlab.com/)
- [Wenjetso 搵着数](https://www.wenjetso.com/zh_HK/)
