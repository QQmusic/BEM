# BEM

BEM的意思是指“**块（Block）**,**元素（Element）**,**修饰符（Modifier）**”，是一种新的前端命名方式。这种命名方法让你的CSS类对其他开发者来说更加透明而且更有意义。

``` css
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
在大多数情况下，任何独立的页面元素（或复杂或简单）都可以被视作一个块，一个header是block，header里嵌套的搜索框是block，甚至一个logo也可以是block。

误区：这个block并非display:block;里的block。

例如：一个自定义列表list是一个块，那么列表的block写法应该为:

``` css
.list{}
```
如果这个列表list是属于模块类别，在这种情况下，一个list列表模块的block写法应该为:
``` css
.mod_list{}
```
**Element**  
一个块的的子元素，并且子元素的子元素在BEM里也被认为是块的直接子元素。

如下面的例子，.item是列表的一个子元素，.link是.item的一个子元素。
``` css
<!--before-->
.mod_list{}
.mod_list .item{}
.mod_list .item .link{}

<!--now-->
.mod_list{}
.list__item{}
.list__link{}
```
注：mod_前缀只用于block命名上。

**Modifier**  
修饰符用于描述一个块或一个子元素的特定状态。

例如：一个表示按钮的块默认有三个大小：小，中，大。为了避免创建三个不同的块，最好是在块上加修饰符。这个修饰符应该有个名字（比如：size ）和值（ small，normal 或者 big ）。
``` css
.btn{}
.btn--size_small{}
.btn--size_normal{}
.btn--size_big{}
```

另一个例子，表示一个选中的列表，和一个激活的列表项。
``` css
<!--before-->
.mod_list{}
.mod_list.select{}
.mod_list .item{}
.mod_list .item.active{}
 
<!--now--> 
.mod_list{}
.list--select{}
.list__item{}
.list__item--active{}
```
注：mod_前缀只用于block命名上。

## 完整范例
``` css
.mod_xxx{}
.xxx__item{}
.xxx__product_name{}
.xxx__ming_zi_ke_yi_hen_chang{}
.xxx__link{}
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