### 布尔值

1. 示例

    ```
    let bool: boolean = false;
    console.log(bool)
    ```

2. 注意事项
    - 使用构造函数 `new Boolean(1)`创建的不是布尔值而是布尔对象
    - 直接调用Boolean返回的是布尔**值**
    - 基本类型中除了null和undefined也有上述两种特征

### 数值

1. 各种数值

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

1. 普通字符串与模板字符串使用

    ```
    let str: username = "string"
    // 模板字符串
    let str2 = `我的名字是${username},
    今年不小了`
    ```

### 空值

1. ts中用`void`来表示没有任何返回值的函数
    ```
    function showName():void {
        console.log("name")
    }
    ```

2. 声明一个`void`变量，它就只能赋值`null`和`undefined`
3. `null`和`undefined`是所有类型的子类型

### 任意值any

1. any类型的变量可以被任意类型赋值
2. **在任意值上可以访问任意属性、调用任意方法，返回的内容也都是任意值**
3. 一个变量如果声明时如果**没有赋值且没有指定类型**，则为任意型

    ```
    let a;
    a = 123
    a = "123"
    ```

### 类型推断

1. 如果声明一个变量时进行赋值但没有指定类型，会根据推断给一个类型

    ```
    let a = 123;
    a = "123"; // 报错
    ```

### 联合类型

1. 表示值可以为多种类型中一种

    ```
    let a: string | number = 123
    a = "123"
    ```
2. 当联合类型变量被赋值时，会推断出一个类型

    ```
    let test: string | number = 12
    console.log(test)
    test = "abc"
    console.log(test.length)
    ```
3. **当访问联合类型的属性或者方法时，只能访问它们共有的属性或者方法**

### 对象的类型——接口

1. TypeScript中的接口非常灵活，除了可用于对类的行为进行部分抽象外，还可以对[对象的形状]进行描述
2. 固定属性的例子，在这个例子中，**he多一些属性会报错，少一些属性也不行**

    ```
    interface Person {
        name: string
        age: number
    }

    let he: Person = {
        name: "张三",
        age: 23,
    }
    ```
3. 可选属性：不完全匹配一个形状
    ```
    interface Person {
        name: string
        age?: number
    }
    let person1: Person = {
        name: "张三"
    }
    let person2: Person = {
        name: "李四",
        age: 11
    }
    ```
4. 任意属性
    
    
    
