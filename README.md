# weexNotes
my notes about weex

# weex自学随记
## weex使用指南参考 weex官网或博客
https://blog.csdn.net/Yongle_F/article/details/80712124
## 简介
weex是一个可以使用现代化web技术开发高性能原生应用的框架。让移动开发者通过简捷的前端语法写出Native级别的性能体验，并支持iOS、安卓及Web等多端部署。
## 在 Weex 中使用 Vue.js
安装及使用可参考文档：https://segmentfault.com/a/1190000011027225
## vue在weex中的不同
### 语法差异
1. html标签
weex支持了基本的容器 (div)、文本 (text)、图片 (image)、视频 (video) 等组件，注意是组件，而不是标签，虽然使用起来跟 html 标签很像，至于其他标签基本可以使用以上组件组合而成。
2. Weex 环境中没有 DOM、BOM
没有element、event、file等DOM对象，也没有doument.getElementById，document.querySeletor等，当然也不支持基于 DOM API 的程序库（如 jQuery）。
没有BOM但可以调用weex原生API，使用方法是通过注册、调用模块来实现。其中有一些模块是 Weex 内置的，如 clipboard 、 navigator 、storage 等。
3. 支持有限的事件
并不支持 Web 中所有的事件类型，详情请参考
### 样式差异
Weex 中的样式是由原生渲染器解析的，出于性能和功能复杂度的考虑，Weex 对 CSS 的特性做了一些取舍
1. Weex 中只支持单个类名选择器，不支持关系选择器，也不支持属性选择器。单位只能是像素（px）,子元素不会继承父元素的样式。
2. 组件级别的作用域，为了保持 web 和 Native 的一致性，需要<style scoped>写法
3. 支持了基本的盒模型和 flexbox 布局，详情可参考Weex 通用样式文档。但是需要注意的是，
不支持display: none;可用opacity: 0;代替，（opacity<=0.01时，元素可点透）
样式属性暂不支持简写（提高解析效率）
flex 布局需要注意 web 的兼容性
css 不支持 3D 变换

