# 实践音频触感设计

### Audio and haptic design principles音频和触觉设计原则

- Causality有因果关系

```
例如屏幕上的小球撞击屏幕边框
例如小球在纹理路面上滚动
```

- Harmony和谐

```
外观和声音应当保持一致，例如小球的震动强度是0.3，大球的震动强度是0.9
```

- Utility实用

```
只在需要的时候给予反馈而不是乱加，例如小球变大的时候可以加
```

### Introduction to Core Haptics 框架简介

仅在iPhone上支持

CHHapticEngine连接手机的实体执行器

CHHapticPlayer用于控制播放开始停止和暂停

CHHapticPattern和Event  一个Pattern由多个Event构成

一个pattern文件是以.ahap结尾，是个json文件，里面记录了声音和触觉的波形

### HapticRicochet Xcode project 软件示例

CHHapticAdvancedPatternPlayer是CHHapticPattern的进阶版，相比基础版本，除了基础功能外还增加了暂停继续功能，循环播放功能和执行回调