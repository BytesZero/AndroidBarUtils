# AndroidBarUtils
Android  StatusBar And NavigationBar Tools

Android 透明(沉浸式)状态栏细研

## 实现的功能

- 透明状态栏（非半透明状态栏，个别机型无法适配全透明）
- 动态改变ToolBar或者自定义的TitleBar颜色，修改背景色即可，不需要动态改变状态栏颜色
- 状态栏主题模式（黑白色）切换
- 修复 DrawerLayout 在 4.4 上白边的问题
- 适配“刘海屏”状态栏
- 导航栏实现个人认为美观并通配的配色

系统 | 导航栏配色方案
--- | ---
4.4 | 黑色 
5.0~7.0 | 1/4透明黑底色+白色导航
8.0及以上| 白底+灰色导航主题

## 未来可能会去实现的功能

- 动态改变导航栏颜色（5.0及以上可以自己修改实现，目前是写死的配色方案）
- 状态栏和导航栏主题模式设置分离

## 预览效果（均为模拟器测试）

- Android 9.0 gif

![Android 9.0 gif](https://github.com/yy1300326388/AndroidBarUtils/blob/master/images/Android%209.0%20%E5%8A%A8%E6%80%81.gif)

- 4.4.2 

![4.4](https://github.com/yy1300326388/AndroidBarUtils/blob/master/images/Android%204.4.2.png)

- 5.0.2 

![5.0.2]https://github.com/yy1300326388/AndroidBarUtils/blob/master/images/Android%205.0.2.png)

- 6.0

![6.0](https://github.com/yy1300326388/AndroidBarUtils/blob/master/images/Android%206.0.png)

- 9.0

![9.0](https://github.com/yy1300326388/AndroidBarUtils/blob/master/images/Android%209.0.png)

> 以上效果均为模拟器测试，如果你的真机测试有问题，请发给我并附上效果图和机型。

## 使用方式

暂不提供远程库的方式使用，就一个类 [AndroidBarUtils.java](/app/src/main/java/cn/zsl/androidbarutils/utils/AndroidBarUtils.java) ,直接拷贝到项目中使用，也方便在此基础上扩展。

- 设置透明状态栏

```java
AndroidBarUtils.setTranslucent(this);
```

- 修复重叠问题以及适配“刘海屏”(ToolBar、自定义的TitleBar、NavigationView 都可用)

```java
//ToolBar、自定义的TitleBar 重叠问题以及适配刘海屏
AndroidBarUtils.setBarPaddingTop(this, toolbar);
```

- 设置状态栏主题(6.0以上才有效果)

```java
//false:白色 true:黑色
AndroidBarUtils.setBarDarkMode(this, false);
```

- 修复DrawerLayout 在4.4 下出现白条的问题

```java
AndroidBarUtils.setTranslucentDrawerLayout(drawerLayout);
```

- 适配 NavigationView 刘海屏

```java
//适配 NavigationView 刘海屏
AndroidBarUtils.setBarPaddingTop(this,navigationView.getHeaderView(0));
```

## 下载 APK 测试
[AndroidBarUtils APK](apk/app-release.apk)





