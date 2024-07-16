# WatchOS 中的新设计

Watch apps are lightweight 手表App应当轻巧

在功能方面，要限制长时间交互，并应苛刻挑剔允许在手表上操作的功能

Make acitions discoverable让你的某个操作可以被发现，也就是要清晰且用户可理解，操作最好是始终可见

如果列表比较长，最好在上方提供排序/筛选菜单 以帮助用户发现

代码实现非常容易：给List里嵌套一个选择器即可

```swift
var body: some View {
  List {
    Picker(selection: $viewing title: Text("Viewing")) {
      // 排序选项
    }
    // 正常的List Item
  }
}
```

左滑删除使用.onDelete修饰符

可以在左下角提供一个三个点的操作将复杂的操作放在模态视图中（例如遥控iPhone相机时选择人像或者实况）

.toolBar API用来将一个按钮隐藏在上方，用户需要向上滚动才能看到这个按钮

