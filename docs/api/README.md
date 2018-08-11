# 通用规则

在接下来的API的类型中，您会看到类型为`Icon`、`Size`、`Point`、`ContextMenu`的类型，在此为您统一解释。

## Point
``` ts
{
  [lng: number], // 经度
  [lat: number], // 维度
}
```

## Size
``` ts
{
  [height: number], // 高度
  [width: number], // 宽度
}
```

## Icon
``` ts
{
  [url: string],  // icon url地址
  [size: Size], // 图标可视区域的大小
  [opts: IconOptions]: {
    [anchor: ControlAnchor], // 图标的定位点相对于图标左上角的偏移值
    [imageSize: Size], // 图片的大小，同CSS中background-size。
    [imageOffset: Size], // 图片相对于可视区域的偏移值，同CSS中background-position
    [infoWindowAnchor: Size], // 信息窗口开启位置相对于图标左上角的偏移值
    [printImageUrl: string], // 设置icon打印图片的url，该打印图片只针对IE6有效
  }
}
```

## ContextMenu

`items`为数组

``` ts
{
  [items: ContextMenuItem[]]: [
    {
      [text: string], // 设置菜单项显示的文本
      [callback: Function], // 菜单项被点击回调函数
      [separator: boolean], // 是否显示分隔线
      [width: number], // 指定此菜单项的宽度
      [iconUrl: string], // 指定此菜单项的icon URL（大小为17px*17px)
      [disabled: boolean] // 是否禁用
    }
  ]
}
```

## Enum
每个`Enum`类型均为对应常量，您可以通过点击其链接来查看常量中具体包含值