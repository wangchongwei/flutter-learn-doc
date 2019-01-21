### Container widget使用说明


##### 1、 construct 构造函数

```

Container({
    Key key,
    this.alignment, // child 在朝向垂直方向的排列方式
    this.padding,
    Color color,
    Decoration decoration, // 朝向
    this.foregroundDecoration, // 绘制在child前面的装饰
    double width,
    double height,
    BoxConstraints constraints, // 添加到child上的额外约束条件
    this.margin,
    this.transform, // 设置container的变换矩阵，类型为Matrix4。
    this.child,
  })


```
