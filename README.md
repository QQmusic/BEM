# BEM

BEM的意思是指“**块（Block）**,**元素（Element）**,**修饰符（Modifier）**”，是一种新的前端命名方式。这种命名方法让你的CSS类对其他开发者来说更加透明而且更有意义。

```
.block{}
.block__element{}
.block--modifier{}
```
- __ 双下划线：双下划线用来连接块和块的子元素。
- -- 双中划线：双中划线用来描述一个块或者块的子元素的一种状态。
- _  下划线 ：仅作为连字符使用，表示某个块或者某个子元素的多单词之间的连接记号。
如：play_list__item

## 了解BEM

**Block**


**Element**  
一个块的的子元素。

**Modifier**  
修饰符用于描述一个块的特定状态，如：.current .active。

## 完整范例
```
.mod_xxx{}
.mod_xxx__item{}
.mod_xxx__item--hightlight{}
.mod_xxx__product_name{}
.mod_xxx__link{}
.mod_xxx__ming_zi_ke_yi_hen_chang{}
.mod_xxx__item--current .mod_xxx__link{}
```
**对应的HTML结构如下：**
```
<ul class="mod_xxx">
    <li class="mod_xxx__item">第一项
        <div class="mod_xxx__product_name">我是名称</div>
        <span class="mod_xxx__ming_zi_ke_yi_hen_chang">看类名</span>
        <a href="#" class="mod_xxx__link">我是link</a>
    <li>
    <li class="mod_xxx__item mod_xxx__item--current">第二项 且 当前选择项
        <div class="mod_xxx__product_name">我是名称</div>
        <a href="#" class="mod_xxx__link">我是link</a>
    <li>
    <li class="mod_xxx__item mod_xxx__item--hightlight">第三项 且 特殊高亮
        <div class="mod_xxx__product_name">我是名称</div>
        <a href="#" class="mod_xxx__link">我是link</a>
    <li>
</ul>
```