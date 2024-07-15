# SF Symbols2

### The basics基础知识

Small尺寸为-20% 相对于Medium

Large尺寸为+30% 相对于Medium

在设计时，可以直接复制粘贴SF Symbol符号到Sketch中粘贴

在开发时，可以Shift+Command+C 复制名字粘贴到引号里

```swift
Image(systemName: "shuffle")
	.font(.headline)
	.imageScale(.small)// 适应设计师的缩放
或者直接使用Label
Label("globe", systemImage: "globe")
```

### Additions and refinements补充和完善

可以导出已经有的符号为模板制作属于自己的符号

### Localization本地化

符号会自动本地化，你自定义的也会

### Deployment targets部署目标

选择符号的时候他会告诉你支持的os版本

### Colors颜色

可以使用App查看颜色版本，有四种渲染方式

单色、分层、调色盘、多色渲染

### Layout with SF Symbols使用SF Symbols布局

使用Label他们会有默认的对齐方式，目前千千不确定用HStack拼接和SF Symbol和Text是否一致

