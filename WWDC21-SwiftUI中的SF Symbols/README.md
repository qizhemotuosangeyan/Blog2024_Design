# SwiftUI中的SF Symbols

```swift
Image(systemName: "heart")

Label("Heart", systemImage: "heart")


```

Label、Iamge等都提供了无障碍的文本描述

也可以自定义描述而不是用图片的文本描述

```swift
Iamge(systemName: "person.circle")
	.accessibilityLabel("Profile")
```

更好的处理方案是在Localizable.strings中对sy symbol进行各个国家的本地化

 希望文字与符号自动重排的时候可以这样写

```swift
Text("""
    Thalia, Paul, and
     3 other \(Image(systemName: "chevron"))
""")

```

```swift
.font(.body)//可以使用font修饰符号大小
.imageScale(.medium)//使用imageScale缩放，不改变文本大小而仅仅是修改SF Symbol的大小
可以批量使用.symbolVariant(.fill)将一个List中的所有Symbol设置为fill样式
可以使用.symbolRenderingMode(.hierarchical)来强调渲染元素
.symbolVariant(.circle.fill)
.foregroundStyle可以设置多层着色(.white, .yellow, .red)
大多为两个图层，有的是3个图层
```



