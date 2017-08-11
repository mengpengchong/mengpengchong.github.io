
#JS字符串方法
***
###1.indexOf ( )  查找该字符串的位置
`(1).不存在的话返回-1; ` 

`(2).第二个参数表示下标  `


```
var str = "hello world";

console.log(str.indexOf('l')); //返回2	

console.log(str.indexOf('l',5)); //返回9	
```

		
				
###2.lastIndexOf ( ) 

`(1).不存在同样返回-1;`  

`(2).同样有第二个参数，表示从该下标的位置开始往前找`。  

  
```

var str = "hello world";  

console.log(str.lastIndexOf('l')); //返回9  

console.log(str.lastIndexOf('l',6)); //返回3
```


###3.slice ( ) 提取字符串的某个部分,有第二个参数，前闭后开

`(1).两个参数,第一个指定开始提取的位置,第二个指定提取结束的位置;  `  

```
1，提取的范围包括开始位置，但是不包括结束位置。  

2，如果省略第二个参数，表示从开始位置提取到字符串结束。 
 
3，不会比较两个参数的大小关系。  

4，如果没有参数，默认提取整个字符串。

5，参数只能为整数（正、负、零），非法参数会解析成0.  

var str = "hello world";  

console.log(str.slice(6)); //返回world  

console.log(str.slice(3,7); //返回low  
```



###4.split ( ) 用于把一个字符串分割成字符串数组

`(1).有两个参数,第2个参数可选。该参数可指定返回的数组的最大长度。如果设置了该参数，返回的子串不会多于这个参数指定的数组。如果没有设置该参数，整个字符串都会被分割，不考虑它的长度。`

```
var str = "Hello World";  

console.log(str.split('1'));//["Hello World"];

console.log(str.split('l'));//["he", "", "o wor", "d"];

var str = "a-b-c-d-e-f-g";

console.log(str.split('-',3));//["a", "b", "c"];
```

  
  
###5.substring ( ) 提取相应区间的字符

`(1).有两个参数,第一个 指定开始提取的位置,第二个 指定提取结束的位置。`  

```
1，提取的范围包括开始位置，但是不包括结束位置。

2，如果省略第二个参数，表示从开始位置提取到字符串结束。  

3，在提取之前会先比较两个参数的大小，然后按从小到大的顺序调整两个参数的位置，再提取。  

4，如果没有参数，默认提取整个字符串。 
 
5，参数只能为正整数，非法参数会解析成0. 

var str = "a-b-c-d-e-f-g"; 

console.log(str.substring(3,6));//-c-(截取的字符串长 度为6-3，从3开始，不包含6;
```
 

###6.charCodeAt()返回指定下标位置的字符Unicode编码
```
var str = 'abc'.charCodeAt(0);//括号内表示下标  

console.log(str);//a的Unicode编码是97,b98,c99;
```



###7.charAt()返回指定位置的字符

`(1).参数：一个 指定要获取的字符位置.如果不设置参数，默认获取第一个位置上的字符 `

```

var str = 'abc'.charAt(0);  

console.log(str); //返回a
```


###8.toUpperCase() / toLowerCase() 把字符串转化为大/小写

```
var str1 = "hello world";  

console.log(str1.toUpperCase()); //返回HELLO WORLD ; 

var str2 = "HELLO WORLD";  

console.log(str2.toUpperCase()); //返回hello world;  
```


###9.replace() 方法在字符串中用某些字符替换另一些字符


```
var str = " Please visit Microsoft!";  

var str2 = str.replace("Microsoft","w3cschool");
```


###10.trim()去掉字符串前后的空格

`(1).不兼容低版本IE浏览器  `

```

str = " abc def ghi ";
  
str2 = str.trim();  

console.log(str2); //返回abc def ghi 
 
那要想保留字符串前面的空格，只去掉后面的空格呢？看下面：
  
str = " abc def ghi ";  

console.log(str.length) //返回13  

str2 = ("a"+str).trim().substring(1);  

console.log(str2);// abc def ghi  

console.log(str2.length); //返回12
```

###11.search 是模糊查找 每次查找都从第一个字符开始 不能指定开始查找的下标的位置


```

var str1 = "hello world";  

console.log(str1.toUpperCase()); //返回HELLO WORLD  

var str2 = "HELLO WORLD";  

console.log(str2.toUpperCase()); //返回hello world
```


***
#JS数组方法
***
###1.join()把数组转化为字符串

`如果不写参数的话默认是以逗号隔开，有参数的话会通过指定的参数隔开。`

```
var arr = [1,2,3];

arr.join(); //返回 "1,2,3"

arr.join("|"); //返回 "1|2|3"

```
###2.reverse ( ) 将数组逆序

` 原数组会被修改`  

```
var arr = [1,2,3];  

arr.reverse ( ); //返回[3,2,1]
```

###3.sort ( ) 排序

`默认按照字母的顺序排序,原数组会被修改`

```
var arr = ["e","d","c","b","a"];
arr.sort ( ) ; //返回["a","b","c","d","e"];

代表升序
function asce(a,b){
   return a-b; //升序
}
代表降序
function desc(a,b){
   return b-a; //降序
}
```

###4.concat ( ) 数组合并

`原数组不会被修改`

```
var arr = [1,2,3]
arr.concat(4,5); //返回[1,2,3,4,5]
arr; //返回[1,2,3]
参数可以为数组
arr.concat([10,11],13]); //返回[1,2,3,10,11,13]
arr.concat([1,[2,3]]); //返回[1,2,3,1[2,3]]参数中的子数组 元素不会被拉平
```

###5.slice ( ) 返回部分数组

`原数组不会被修改，参数可以为负数，表示从后往前的相对的位置，-1表示最后一个元素，-2表示倒数第二个，以此类推`

```
var arr = [1,2,3,4,5];
arr.slice(1,3); //返回[2,3]（从下标为1开始，数组长度为3-1）
arr.slice(1); //返回[2,3,4,5](没有第二个参数的话表示从该下标 位置开始到最后所有的元素）
arr.slice(1,-1); //返回[2,3,4]
```

###6.splice ( ) 数组拼接

`原数组会被修改`

`第一个参数表示从该位置开始，第二个参数表示删除多少项，为0的话表示不删除，第三个参数表示插入`

```
var arr = [0,1,2,3,4,5,6,7,8];
console.log(arr.splice(3,3,'abcdefg'),arr);
//[3, 4, 5]
//[0, 1, 2, "abcdefg", 6, 7, 8]
```

###7.pop ( ) 移除数组中的最后一个元素并返回该元素


```
var arr = [1,2,3,4,5];
console.log(arr.pop()); //返回5
console.log(arr.pop(),arr); //返回4[1,2,3]
```

###8.shift ( ) 移除数组中的第一个元素并返回该元素


```
var arr = [1,2,3,4,5];
console.log(arr.shift()); //返回1
console.log(arr.shift(),arr); //返回2,[3,4,5]

```

###9.push ( ) 向数组的末尾添加一个或者更多元素，返回新的长度


`把它的参数顺序添加到Array的尾部，原数组会被修改`

```
var arr = [1,2,3,4,5]
console.log(arr.push(6,7,8,'a','b','c'),arr) 
//返回11, [1, 2, 3, 4, 5, 6, 7, 8, "a", "b", "c"]
```

###10.forEach ( ) 遍历数组(有兼容性问题）


`第1个参数代表下表对应的元素，第2个参数代表的是下标，第3个参数代表数组本身`

```
var arr =['a','b',2,true,{},5,6,7,8];
arr.forEach(function(aa,bb,cc){
console.log(aa,bb,cc)
})
//a 0 Array[9]
//b 1 Array[9]
//2 2 Array[9]
//true 3 Array[9]
//Object 4 Array[9]
//a 5 Array[9]
//a 6 Array[9]
//a 7 Array[9]
//a 8 Array[9]
```

###1.map ( ) ：指“映射”，对数组中的每一项运行给定函数，返回每次函数调用的结果组成的数组。

`下面代码利用map方法实现数组中每个数求平方。`

```
var arr = [1, 2, 3, 4, 5];
var arr2 = arr.map(function(item){
return item*item;
});
console.log(arr2);  //返回[1, 4, 9, 16, 25]
```

###2.filter ( ) ：“过滤”功能，数组中的每一项运行给定函数，返回满足过滤条件组成的数组。filter() 不会对空数组进行检测,可以传3个参数

```
var arr = [11,2,33,5,7,24];
function fn(x){
return x > 10;
}
console.log(arr.filter(fn));  //返回[11,33 24]

```

###3.every ( ) ：判断数组中每一项都是否满足条件，只有所有项都满足条件，才会返回true,否则返回false

```
var arr = [1, 2, 3, 4, 5];
var arr2 = arr.every(function(x) {
return x < 10;
});
console.log(arr2); //返回true
var arr3 = arr.every(function(x) {
return x < 3;
});
console.log(arr3); //返回false
```

###4.some ( ) ：判断数组中是否存在满足条件的项，只要有一项满足条件，就会返回true。

```
var arr = [1, 2, 3, 4, 5];
var arr2 = arr.some(function(x) {
return x < 3;
});
console.log(arr2); //返回true
var arr3 = arr.some(function(x) {
return x < 1;
});
console.log(arr3); //返回false
```










