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
特殊值通过位运算取整结果
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
parseInt([1]) //1
parseInt([[1],"a"]) //1
parseInt([a,[1]]) //NaN
parseInt(Object) //NaN
parseInt(Symbol) //Uncaught TypeError: Cannot convert a Symbol value to a string
parseInt("0x1a") //26
```
