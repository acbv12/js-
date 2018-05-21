# js运算

## 一、取整
### 1.位运算（位运算操作要求是整数）
按位取反两次：
```JavaScript
~~n
```
左移运算符、右移运算符
```JavaScript
n<<0
n>>0
```
按位或
```JavaScript
n|0
```
通过位运算取整结果
```JavaScript
//以两次按位取反为例，其它位运算取整结果一致
~~undefined //0
~~null //0
~~false //0
~~true //1
~~"1.01" //1
~~".1.01" //0
~~[1.01] //1
~~[[1.01]] //1
~~[1.01,1] //0
~~{} //0
~~Symbol //Uncaught TypeError: Cannot convert a Symbol value to a number
```
### 2.Javascript函数
parseInt
解析一个字符串,并返回一个整数。
```Javascript
parseInt(1.02) //1
parseInt("1.02") //1
parseInt("x") //NaN
parseInt(Boolean) //NaN
parseInt([1]) //1
parseInt([[1],"a"]) //1
parseInt([a,[1]]) //NaN
parseInt(Object) //NaN
parseInt(Symbol) //Uncaught TypeError: Cannot convert a Symbol value to a string
parseInt("0x1a") //26
```

Math对象
```Javascript
//向上取整
Math.ceil(3.1) //4
//四舍五入
Math.round(3.1) //3
//向下取整
Math.floor(3.6) //3
---------------------------
Math.ceil(true) //1
Math.ceil(false) //0
Math.ceil(true) //1
Math.ceil(null) //0
Math.ceil("x") //NaN
Math.ceil([1]) //1
Math.ceil([,1]) //NaN
Math.ceil(Object) //NaN
Math.ceil(Symbol) //Uncaught TypeError: Cannot convert a Symbol value to a number
```
