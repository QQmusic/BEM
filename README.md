# BEM

BEM的意思是指“**块（Block）**,**元素（Element）**,**修饰符（Modifier）**”，是一种新的前端命名方式。这种命名方法让你的CSS类对其他开发者来说更加透明而且更有意义。

```
.block_name{}
.block_name__element_name{}
.block_name--modifier_name{}
```
由以下三种符合来表示三者之间的关系：
- __ 双下划线：双下划线用来连接块和块的子元素。
- -- 双中划线：双中划线用来描述一个块或者块的子元素的一种状态。
- _  下划线 ：仅作为连字符使用，表示某个块或者某个子元素的多单词之间的连接记号。

注：每个团队可以不同的命名约定，可以使用不同的连接符号，只要符合BEM的原则即可。

## 了解BEM

**Block**


**Element**  
一个块的的子元素。

**Modifier**  
修饰符用于描述一个块的特定状态，如：.current .active。

## 完整范例
```
.mod_xxx{}
.xxx__item{}
.xxx__product_name{}
.xxx__link{}
.xxx__ming_zi_ke_yi_hen_chang{}
.xxx__item--hightlight{}
.xxx__item--current .xxx__link{}
```
**对应的HTML结构如下：**
```
<ul class="mod_xxx">
    <li class="xxx__item">第一项
        <div class="xxx__product_name">我是名称</div>
        <span class="xxx__ming_zi_ke_yi_hen_chang">看类名</span>
        <a href="#" class="xxx__link">我是link</a>
    <li>
    <li class="xxx__item xxx__item--current">第二项 且 当前选择项
        <div class="xxx__product_name">我是名称</div>
        <a href="#" class="xxx__link">我是link</a>
    <li>
    <li class="xxx__item xxx__item--hightlight">第三项 且 特殊高亮
        <div class="xxx__product_name">我是名称</div>
        <a href="#" class="xxx__link">我是link</a>
    <li>
</ul>
```