# BFC---块格式上下文（Block Formatting Context）

### BFC如何生成

+ 根元素(`<html>`)
+ 浮动元素（元素的 float 不是 none）
+ 绝对定位元素（元素的 position 为 absolute 或 fixed）
+ 行内块元素（元素的 display 为 inline-block）
+ 表格单元格（元素的 display为 table-cell，HTML表格单元格默认为该值）
+ 表格标题（元素的 display 为 table-caption，HTML表格标题默认为该值）
+ 匿名表格单元格元素（元素的 display为 table、table-row、 table-row-group、table-header-group、table-footer-group（分别是HTML table、row、tbody、thead、tfoot的默认属性）或 inline-table）
+ overflow 值不为 visible 的块元素
+ display 值为 flow-root 的元素
+ contain 值为 layout、content或 paint 的元素
+ 弹性元素（display为 flex 或 inline-flex元素的直接子元素）
+ 网格元素（display为 grid 或 inline-grid 元素的直接子元素）
+ 多列容器（元素的 column-count 或 column-width 不为 auto，包括 column-count 为 1）
+ column-span 为 all 的元素始终会创建一个新的BFC，即使该元素没有包裹在一个多列容器中（标准变更，Chrome bug）。
</br>
还可以添加border或者padding
</br>
《CSS权威指南》中提到块级正常流元素的高度设置为auto，而且只有块级子元素，其默认高度将是从最高块级子元素的外边框边界到最低块级子元素外边框边界之间的距离。如果块级元素右上内边距或下内边距，或者有上边框或下边框，其高度是从其最高子元素的上外边距边界到其最低子元素的下外边距边界之间的距离。