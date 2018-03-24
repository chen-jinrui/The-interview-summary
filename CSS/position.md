# CSS POSITION
## HTML中的三种布局方式
+ 标准流(顺序布局)
+ float
+ position(通过top left right bottom 设置位置)
### position中的可选参数
+ static
+ relative参考点:左上为原点)
+ absolute
+ fixed
+ inherit
#### relative
> 正常文档流中，设置了relative定位后，元素有了层级关系，后写的relative定位的元素层级高于先写的relative元素层级。
  通过top,left,right,bottom移动元素位置时，相应坐标轴方向发生变化，以最左最顶为原点，left和top以右下为x轴、y轴正方向，
  right,bottom以左上为x轴、y轴正方向。
#### absolute
> 脱离正常文档流，通过设置位置属性，可以在整个文档里定位，有了层级关系，后写的absolute定位的元素层级高于先写的absolute元素层级。
  如若父元素没有定位属性，absolute定位元素将以窗口的四个角为参照。

`div.class{width:100px; height:100px; postion:absolute;}`

`div.class{width:100px; height:100px; postion:absolute; left:10px; top:10px;}`

上面的代码，下面的才会真正的触发定位特性。

#### fixed

> 脱离正常的文档流，在整个窗口进行移动定位并拥有层级概念。常用场景:对联广告，登录弹窗。固定定位元素以窗口四个顶点为参照，不受任何定位元素的影响。

#### inherit
> 继承父元素的定位属性；

### z-index
+ 可以设置元素的叠加顺序，但**依赖定位属性**
+ z-index大的元素会覆盖z-index小的元素
+ z-index为auto的元素不参与层级比较
+ __z-index为负值，元素被普通流中的元素覆盖__
#### 层级关系以及通过z-index改变层级关系
