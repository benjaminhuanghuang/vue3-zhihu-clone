

## 2-1 什么是 Typescript (05:54)

## 2-2 为什么要学习 typescript (06:04)
 - 代码更容易理解
 - 更少的错误
 - 提示，效率更高


## 2-3 安装 typescript (05:59)
```
  npm i -g typescript

  tsc -v

  tsc test.ts
```


## 2-4 原始数据类型和 Any 类型 (06:04)




## 2-5 数组和元组 (06:52)
Array
```
  let arrNum: number[] = [1,2,3];   
```

Array like :
```
  arguments IArguments

  HTMLCollection

```

tuple
```
  let user: [string, number] = ["ben", 123]
```

## 2-6 Interface- 接口 初探 (05:40)

Duck typing

Deifne obj Shape

```
interface Person {
  readonly id: number
  name: string;
  age?: number;
}

let a : Persion = {
  id : 1,
  name: 'ben',
  age: 99
}
```

## 2-7 函数 (06:52)
```
  function add(a: number, b: nubmer, z?:number): number {
    if(typeof z === 'number')
      return x + y + z;
    return x + y;
  }

  // function type
  const func: ( x: number, y: number, z?:number) => number = add;

  // Interface function type
  interface ISum {
    ( x: number, y: number, z?:number): number 
  }
  let add2: ISum = add;
```
## 2-8 类型推论 联合类型和 类型断言 (07:43)
```
  const str = input as string;
```

type guard
```
  if(typeof input === 'string')
      return input.length;      // call use method on string
    return input.toString().length;
```
## 2-9 class - 类 初次见面 (09:55)

extends

super

static

public(default), private, protected

readonly

## 2-10 类和接口 - 完美搭档 (05:44)
implements


## 2-11 枚举（Enum） (07:11)
```
  enum Direction {
    up
  }

  // for const value
  const enum Direction {
    up = 'UP'
  }
```

## 2-12 泛型（Generics） 第一部分 (07:28)

## 2-13 泛型（Generics） 第二部分 - 约束泛型 (06:07)
```
  function func<T extends IWithLength>(arg: T) :T

```
## 2-14 泛型第三部分 - 泛型在类和接口中的使用 (08:47)
```
  interface KeyPair<T, U> {
    key: T
    value: U
  }

  let kp1: KeyPair<number, string> = {key: 1, value: "one"} 
```

## 2-15 类型别名，字面量 和 交叉类型 (07:12)
```
  type PlusType = (x: number, y: number) =>number
  
  let sum: PlusType

  type StrNum = string | number
  
  type Directions = 'Up' | 'Down'
  
```
## 2-16 声明文件 (07:32)

## 2-17 内置类型 (08:33)

## 2-18 作业节