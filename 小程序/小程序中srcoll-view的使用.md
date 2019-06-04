# 小程序中srcoll-view的使用

#### 简介：因为官方文档描述不是特别清楚，所以记录一下小程序中srcoll-view横向滚动的使用

#### 原理

- 首先设置滚动方向为 `scroll-x` ；
- 然后要给里面item设置` white-space` 为 `nowrap` 不换行；
- 最后需要将容器中包裹的标签的 `display` 属性设置为 `inline-block` 。

#### 代码

```xhtml
 <scroll-view scroll-x style="width: 100%;white-space: nowrap; height:200px;">
   <view style='display:inline-block;width:200px;height:200px;background:red;' > </view>
   <view style='display:inline-block;width:200px;height:200px;background:blue;' > </view>
   <view style='display:inline-block;width:200px;height:200px;background:green;'> </view>
   <view style='display:inline-block;width:200px;height:200px;background:black;'> </view>
 </scroll-view>
```

