# font-pack-demo
字体压缩Demo

## 背景
- 线上部署包体积大，字体库达到 10M 
- 需要针对字体库进行压缩，减小打包后体积

## 实践

参考网上压缩字体的方法

[font-spider（字蛛）---前端压缩字体](https://segmentfault.com/a/1190000022802934)

然而并没有达到期望目标，附上效果图：

![20210615145637](https://cdn.jsdelivr.net/gh/whf605319646/image_store/assets/blog/20210615145637.png)

## 分析

font-spider 适合做压缩文本固定不变的html页面，只能压缩页面上出现的文字，而当页面上有出现了新的文字，但之前并未经过压缩，那么这个文字就会呈现默认字体样式，并不会带上压缩后的字体样式。总之，font-spider 不能做到 动态渲染页面 文字。

## 网上新的解决方案

[font-spider-plus](https://www.npmjs.com/package/font-spider-plus)

font-spider-plus 支持动态渲染页面文字，但该方案适配兼容性个人感觉不是很好，所以未尝试。