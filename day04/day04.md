## 笔记
### 背景background
| 属性|说明|值|备注|
|:-----:|:-----:|:-----:|:-----:|
|background-color   | 背景色  |   |   |
|background-image   | 背景图像  | url(..);/渐变 linear-gradient |线性渐变属性至少需要用逗号分隔的三个参数——背景中渐变的方向，开始的颜色和结尾的颜色。  |
|background-position  | 背景位置  | 绝对值px/相对值rems/百分比xx%/关键字(left center right top bottom) | 可分别取值 |
|background-repeat   | 背景重复  | no-repeat/repeat-x/repeat-y  |   |
|background-attachment | 背景活动  | scroll（默认）/fixed/local（ie9+）  |[效果参考](https://mdn.github.io/learning-area/css/styling-boxes/backgrounds/background-attachment.html) |
|background   | 简写  |   | 一行指定以上五个属性的缩写；多重背景  |
|background-size   | 背景大小  |   | 不支持ie9以下版本  |

### 边框 border  
| 属性|说明|值|备注|
|:-----:|:-----:|:-----:|:-----:|
|border| 简写  |   |   |
|border-color   | 边框颜色  |   |  注意顺序 |
|border-style   | 边框样式  |none、hidden、dotted、dashed、solid、double、(groove、ridge、inset、outset、)inherit  |  [样式预览](https://developer.mozilla.org/zh-CN/docs/Web/CSS/border-style) |
|border-width   | 边框宽度  |   |   |
|border 四边   |   |   |   |     
注意：希望边框出现，就必须声明一个边框样式。

### 列表 list
| 属性|说明|值|备注|
|:-----:|:-----:|:-----:|:-----:|
|list-style   | 简写  |   | 属性值可以任意顺序排列，你可以设置一个，两个或者三个值（该属性的默认值为 disc, none, outside）  |
|list-style-type   | 符号样式  | disc/circle/square  |   |
|list-style-position  | 符号位置  | outside/inside  |   |
|list-styel-image   | 符号图片  | url(..)/none  |  可用background代替 |

### 链接 link
| 属性|说明|
|:-----:|:-----:|
| a: link   | 未访问过的  |
| a: visited  | 已访问过  |
| a: hover   | 鼠标停留  |
| a: active   | 链接激活  |
可参考导航栏的[制作方式](http://www.runoob.com/css/css-navbar.html)


### 选择器（2）
1. [分组与继承：](http://www.w3school.com.cn/css/css_syntax_pro.asp)
分组：可以对选择器进行分组，这样，被分组的选择器就可以分享相同的声明。用逗号将需要分组的选择器分开。
继承及其问题：根据 CSS，子元素从父元素继承属性。少部分浏览器并不总是按此方式工作。
2. [派生选择器：](http://www.w3school.com.cn/css/css_syntax_descendant_selector.asp)
通过依据元素在其位置的上下文关系来定义样式
3. [伪类选择器](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Introduction_to_CSS/Pseudo-classes_and_pseudo-elements)
伪类 :
伪元素 ::
4. [组合](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Introduction_to_CSS/Combinators_and_multiple_selectors)
比较难。。。
5. [选择器的优先级](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Introduction_to_CSS/Cascade_and_inheritance)


## 验证
1. CSS 各种选择器的概念，使用方法及使用场景
1.1. 简易选择器
1.2. 属性选择器
1.3. 派生选择器
1.4. 伪类选择器
2. CSS 选择器的优先级
2.1. 重要性（Importance）：!important
2.2. 专用性（Specificity）
2.3. 源代码次序（Source order）

## 参考来源
百度前端学院-基础学院-[day04](http://ife.baidu.com/course/detail/id/38)
[俞綮源的笔记](http://ife.baidu.com/note/detail/id/823)
MDN
w3school
