# 小程序input样式改进

#### 简介：小程序原生UI input样子很难看，功能还不够完善。封装一个可清除的input自定义组件。

#### 效果：输入框内没有内容时，删除按钮隐藏；当输入框内有内容时，删除按钮显示，点击删除按钮则清空输入框内所有内容。并且还可以设置输入框整体样式以及输入框左侧图标

##### wxml

```
<view class='input-class'>
     <image src='{{inputIcon}}' mode="scaleToFill" class='icon-class'></image>
     <input placeholder='{{inputHint}}' bindconfirm='{{confirmTap}}' style='flex:1;width:100%;padding-left:12rpx;' bindinput='inputListener' bindconfirm='inputConfirm' value='{{inputValue}}' type='{{inputType}}' password='{{isPassword}}' confirm-type='{{confirmType}}'></input>
     <image class="{{isClearShow?'clearImgShow':'clearImgHide'}}" src='clear.png' bindtap='clearTap' mode='widthFix'></image>
</view>
```

