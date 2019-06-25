# -css-js-hack
## IE浏览器兼容问题总结

### 一、 标准盒模型和怪异盒模型

* 标准的W3C盒子模型

    **实际的宽/高 = width/height + 2padding + 2border;** 

* 怪异盒模型     

    **width/height就是该盒子的大小，是包含内边距padding和边框border宽度在内的**

* chrome, firefox, IE9, IE10, IE11的盒模型为标准盒模型；

* IE6-8：

    （1）在HTML文档中没有文档声明的情况下，盒模型为怪异盒模型；

    （2）可以使用doctype声明<!doctype html>，让浏览器使用标准模式；

* box-sizing属性（css3）

    （1）box-sizing:content-box，采用标准模式解析计算，默认模式；

    （2）box-sizing:border-box，采用怪异模式解析计算；