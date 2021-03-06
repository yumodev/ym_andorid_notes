# Kotlin基础部分

## HelloWorld


```

fun main(args:Array<String>){
    println("hello world!")
}
```

## 函数

### 一个完整函数实现

```Kotlin
/**
 * 返回a，b中的最大值
 */
fun max(a : Int, b : Int) : Int{
    return if(a > b) a else b
}
```

* `fun` 定义函数。
* `fun` 后面是函数的名字
* 之后是参数列表，参数名写在参数类型前面，中间用冒号分割。
* 最后是方法的放回类型，中间有冒号风格。返回类型可以省略。
* 函数的语句和表达式后面的分号，可以省略。

### 表达式体函数


```Kotlin
fun max(a : Int, b : Int) : Int = if( a > b) a else b
```

省略返回类型的表达式体

```Kotlin
fun max2(a : Int, b : Int) = if( a > b) a else b
```

### 语句和表达式

语句和表达式的区别是语句没有值，表达式有值。
在Kotlin中除了循环(for,do,do/while)外的大多数控制结构都是表达式。
在Java中所有的控制结构都是语句。

## Kotlin数据类型

类型 | 位长度
------|------
Long | 64
Double | 64
Float | 32
Int | 32
Short | 16
Byte | 8

Kotlin中字符不是数字。

## 变量和常量

在Kotlin中使用关键字`var`声明一个变量，使用`val`声明一个变量声明格式为`var 变量名 : 变量类型 = 值 `
下面声明一个字符串变量`a`和一个字符串常量`b`，并设置初始值

```
var a : String = "a";//声明一个变量a，并设置初始值。
val b : String = "b";//声明一个常量b，并设置初始值。
```

在Kotlin中变量和常量的类型是可以省略的，编译期对自动推断出来变量和常量类型，在上面的列子中，可以声明如下：

```
var a = "a";
val b = "b";
```

## 字符串模块

在一个字符串字面量中在一个变量前面加上 `$`就可以引用这个变量的值，这种特性称作字符串模板。定义一个变量a，然后在一个字面量中通过`$a`引用它。如果`$a`后面也紧跟字符串的话，我们需要中大括号将变量包裹起来,例如`${a}`


```Kotlin
 val a = "字符串模板"
 println("这是$a 的演示") //输出为：这是字符串模板 的演示
 println("这是$a的演示") //编译不通过
 println("这是${a}的演示") //输出为：这是字符串模板的演示
```

字符串模板中不仅可以引用变量，还可以引用表达式，表达式必须使用大括号包裹起来。参见下面的实例


```
println("1 + 1 = ${1+1}")//输出为：1 + 1 = 2
```

## 类

## if

## for

## while


