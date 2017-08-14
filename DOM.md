# DOM
***
###### 1.DOM简介  

D——document，没有文档，也就是没有网页，DOM就无从谈起。  

当创建了一个网页并把它加载到web浏览器中时，DOM就悄然而生。浏览器根据网页文档创建一个文档对象。

###### O——object，对象。

对象有三种，

1、用户自定义对象

2、内建对象，javascript中的对象，如Array，Math，Date等。

3、宿主对象，由浏览器提供的对象，如window对象。

###### M——model，模型。

正如一个火车模型代表一列真正的火车，DOM代表被加载到浏览器窗口里的当前网页。浏览器为我们提供了当前网页的模型，可通过javascript去读写它。

所以DOM(Document Object Model),文档对象模型，可以简单理解为代表网页文档的一颗树.


2.DOM的缺点主要表现在：效率低，解析速度慢，内存占用量过高，对于大文件来说几乎不可能使用。另外效率低还表现在大量的消耗时间.

 
3.DOM节点是DOM中最基本的组成单元 



层级方式划分 ： `父节点 、 子节点 、 兄弟节点`  


类型方式划分 ：`1 元素节点、2 属性节点、3 文本节点、8 注释节点、9 document节点`  


```  
7、节点的公共属和方法  

nodeName ——元素的标签名(如P,SPAN,#text(文本节点),DIV)，以大写形式表示  

nodeVlue ——Text节点或Comment节点的文本内容  

childNodes—–获取子节点  


`parentNode——获取父节点  `

`firstNode——获取第一个子节点  `

`lastNode——获取最后一个子节点`  

`nextSibling——获取下一个兄弟节点  `

`previousSibling——获取上一个兄弟节点   `

`hasChildNodes()——判断是否有子节点  `

`appendChild()`——添加子节点,接收一个参数表示要添加的节点,返回添加的节点.  


`insertBefore()`——在参考节点前添加子节点,接收两个参数,第一个参数表示要添加的节点,第二个参数表示参考节点,返回添加的节点.  
//插入后成为第一个子节点 

`replaceChild()`——替换子节点,接收两个参数,第一个参数表示要添加的节点,第二个参数表示被替换的节点,返回被替换的节点.  
//替换第一个子节点 

`removeChild()`—–移除子节点,这个方法接受一个参数，即要移除的节点。被移除的节点将成为方法的返回值  
//移除第一个子节点  

`cloneNode()`——克隆节点,接收一个boolean类型的参数,当参数为true时执行深复制,意即复制内容包含其子节点.  

```    

```
查看节点名称 ： nodeName 属性
元素节点的 nodeName : 元素的本身
属性节点的 nodeName : 属性名本身
文本节点的 nodeName : #text
注释节点的 nodeName : #comment
document的 nodeName : #document
```

```
查看节点的值： nodeValue 属性
元素节点的 nodeValue : null
属性节点的 nodeValue : 属性值
文本节点的 nodeValue : 文本内容
注释节点的 nodeValue : 注释的内容
document的 nodeValue : null
```



