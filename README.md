# BEM

BEM的意思是指“**块（Block）**,**元素（Element）**,**修饰符（Modifier）**”，是一种新的前端命名方式。这种命名方法让你的CSS类对其他开发者来说更加透明而且更有意义。

`
		.block_name{}
		.block_name__element_name{}
		.block_name--modifier_name{}
`
- _  下划线 ：仅作为连字符使用，表示某个块或者某个子元素的多单词之间的连接记号。
- __ 双下划线：双下划线用来连接块和块的子元素。
- -- 双中划线：双中划线用来描述一个块或者块的子元素的一种状态。

## 了解BEM

**Block**


**Element**  
一个块的的子元素。

**Modifier**  
修饰符用于描述一个块的特定状态，如：.current .active。

## 命名约定

