### 布尔值

示例

```
let bool: boolean = false;
console.log(bool)
```
注意事项

- 使用构造函数 `new Boolean(1)`创建的不是布尔值而是布尔对象
- 直接调用Boolean返回的是布尔**值**
- 基本类型中除了null和undefined也有上述两种特征

### 数值

各种数值

```
// 整数
let decLiteral: number = 10
// 小数
let decimal: number = 1.00
// 16进制
let hexLiteral: number = 0xffff
// NaN
let nanLiteral: number = NaN
// 无限大
let infinity: number = Infinity
// es6二进制表示
let es6binaryLiteral: number = 0b1010
// es6八进制表示
let es6octalLiteral: number = 0o7777
```

### 字符串

注意普通字符串与模板字符串使用

```
let str: username = "string"
// 模板字符串
let str2 = `我的名字是${username},
今年不小了`
```

### 空值

- ts中用`void`来表示没有任何返回值的函数

    ```
    function showName():void {
        console.log("name")
    }
    ```

- 声明一个`void`变量，它就只能赋值`null`和`undefined`
- `null`和`undefined`是所有类型的子类型

### 任意值any

- any类型的变量可以被任意类型赋值
- **在任意值上可以访问任意属性、调用任意方法，返回的内容也都是任意值**
- 一个变量如果声明时如果**没有赋值且没有指定类型**，则为任意型

    ```
    let a;
    a = 123
    a = "123"
    ```

### 类型推断

如果声明一个变量时进行赋值但没有指定类型，会根据推断给一个类型

```
let a = 123;
a = "123"; // 报错
```

### 联合类型

- 表示值可以为多种类型中一种

    ```
    let a: string | number = 123
    a = "123"
    ```
- 当联合类型变量被赋值时，会推断出一个类型

    ```
    let test: string | number = 12
    console.log(test)
    test = "abc"
    console.log(test.length)
    ```
- **当访问联合类型的属性或者方法时，只能访问它们共有的属性或者方法**

