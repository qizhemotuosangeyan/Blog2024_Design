# 设计适用于 Mac 的 iPad App

将iPad上的App带到Mac上

### 前置条件

支持多任务，移动窗口位置以及自动布局

### 已经在系统层级自动实现的功能

分割视图、文件浏览器、活动视图、上下文菜单、复制粘贴、文本编辑、按键聚焦

iOS和macOS的最大差别在于输入是触摸还是指针和键盘

对于iOS中的手势，移植到macOS时需要考虑替代方案

### Architecture

iPad上：tab样式、列表样式、文件夹样式

mac上使用这些代替：use segmentControl in tool bar, list, file browser

### Toolbars

对于iPad上可能放置在底部的按钮，mac上需要放置在顶部工具栏，因为mac的窗口是可以拖动的，所以可能会被挡住

并且，不应该用禁用和不禁用来罗列很多功能在不同页面的工具栏，而是对不同的页面提供对应功能的工具（例如Finder中仅当查看图片时才显示一些特有操作）

### Layout

iPad和mac不应该是iPhone的放大版，而应该具备更适合硬件的布局

尝试用分屏来代替iOS复杂的导航结构

### Type打字

macOS会自动将iOS的应用字体缩放77%，MacOS不支持动态字体类型

### Colors

iOS多数时候是开发者选择颜色，而macOS多数时候是根据用户的颜色偏好去选择颜色，mac OS中有用户自定义外观和强调色

### Gestures

多数手势都做了不错的映射，下拉刷新可能不行

mac可以接受鼠标停留，这在一定程度上会比iOS的点按更好

### Touch Bars

千千：emmm，好像新版本mac已经没有了，应该不用着重注意这部分的设计

### App icons

mac有自己独自的轮廓而不总是圆角矩形

### Contextual menus上下文菜单

mac有右键后展开的「上下文菜单」，里面包括了常见的操作，如果你为你的iOS做了这个上下文菜单的话，它们之间会自动转换。

### Menu bar menus

对于macOS App，人们应当可以从顶部的Menu bar执行App的所有功能，以帮助他们设定快捷键

记得为最常用的操作分配默认快捷键