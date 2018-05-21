# 验证  
今天代码部分其实比较简单，主要是多尝试，学习之后，回顾以下自己是否已经掌握以下概念：  

- 什么是CSS，CSS是如何工作的
  1.  浏览器将 HTML 和 CSS 转化成 DOM （文档对象模型）。DOM在计算机内存中表示文档。它把文档内容和其样式结合在一起。
  2. 浏览器显示 DOM 的内容。
- CSS的基本语法是怎样的
  - 语法：CSS是由两块内容组合而成的
    - 属性（Property）：一些人类可理解的标识符，这些标识符指出你想修改哪一些样式，例如：字体，宽度，背景颜色等。
    - 属性值（Value）：每个指定的属性都需要给定一个值，这个值表示你想把那些样式特征修改成什么样，例如，你想把字体，宽度或背景颜色改成什么。
- CSS选择器是什么概念，简单选择器和属性选择器是什么
  - 简单选择器：
    - 元素选择器 p/a/h1{}
    - 类选择器 .xx{}
    - ID选择器 #xx{}
  - 属性选择器：
    - 存在和值（Presence and value）属性选择器
    - 子串值（Substring value）属性选择器
4. 文本样式都有哪些相关属性，对应哪些值
```
color:
font-family: Helvetica, Arial,sans-serif；
font-size: 10px
font-style: none/normal/italic/oblique
font-weight: normal/bold/(lighter/bolder: 100–900: 数值粗体值)
text-transform: none/uppercase/lowcase/capitalize/full-width
text-decoration: none/overline/underline/line-through
```

# 总结

## 关于属性选择器的匹配属性值的问题。
 问题：`[attr|="val"]`， `[attr^="val"]` 的区别；以及`[attr~=”val”]` ， `[attr*=”val”]`的区别
MDN文档里的 [属性选择器](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Introduction_to_CSS/Attribute_selectors) 这一章不太好懂。比如 `[attr~=”val”]` ， `[attr*=”val”]`的区别；以及 `[attr|="val"]`， `[attr^="val"]` 的区别。  
>`[attr|=val] `: 选择attr属性的值是 val 或值以 val- 开头的元素（-用来处理语言编码）。
> `[attr^=val]` : 选择attr属性的值以val开头（包括 val）的元素。  

可以参考大神张鑫旭博客关于 [简单聊聊CSS选择器中的正则表达式](http://www.zhangxinxu.com/wordpress/2016/08/regular-expression-in-css-selector/) 此文的解释：
> `[attr|=”bar”]`'attr'属性值开头必须是bar的单词，或者开头是bar-。同样的，是“单词”，不是“字符”。
> `[attr=^”val”]`attr'属性值开头三个字符需要是val  

注意 “单词” 与 ”字符” 的区别。  
ps. 所以能看英文的还是得看英文，中文有时候翻译不太准确。


## 关于属性选择器的覆盖问题：
根据属性选择器的顺序，同一个属性，第二个选择器会覆盖上一个的效果，而不是叠加：
例子如下
html:
```
<h2 class="edu title"id="education" edu="abc def">教育背景
</h2>
<ol>
 <h3 edu="abc def">本科：</h3>
    <p><time>2016.9</time>至<time>2020.6</time>
    </p>
    <ul>
    <li>汴梁大学-XX专业</li>
    <li>卡基大学-XX专业</li>
    </ul>
  <h3 edu="abc defg">硕士：</h3>
    <p><time>2020.9</time>至<time>2023.6</time></p>
    <ul>
    <li>社会大学-XX专业</li>
    </ul>
</ol>
```
css：
```
/**硕士**/
[edu$="defg"]{
    text-decoration: underline;
  }
/**教育背景、本科、硕士**/
  [edu*="b"]{
    text-decoration: overline;
    color: gray;
  }
```
显示图片效果如下，可以看到我第一个选择器给“硕士”赋予的下划线的值被第二个选择器的上划线给覆盖掉了。不是我想象中在“硕士”上出现上下划线的结合。
![day03-1](images/2018/05/day03-1.png)  
日后待学CSS层叠机制再来进一步了解。
