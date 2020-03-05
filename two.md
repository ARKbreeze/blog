# 今日计划

- [ ] test1 

## 控制流

### while
---
- while
```
while(判断){
判断为真时执行操作
}

```
- do while
```
do{
执行操作
不论while判断真假都会执行一次
判断为真时会继续执行
}while（判断）；
```
---
### for
---
- for
```
for(初始条件，判断条件，循环体执行后执行此操作){
判断为真执行
}
```

- for each
```
for(String s : Iterable<String>){
迭代器遍历，需要指定集合实现了 迭代器接口；
}
```
---

### 改变循环
---
- break
1. break 会直接跳出所有循环

- continue
1. 只会跳出当前执行循环体，循环计数加一进行下一次循环

- break label

1. 类似于goto语句
2. label ——> （任意+：）来声明一个label
3. 实现控制流程的转移
```
	最外层循环：
	for（）{
    一层循环
    	for（）{
        	// break 只会跳出内层循环
        	break 最外层循环；
            // break label 会跳出到label所在处。
        }
    }
```

---


### switch 控制流
---

- switch
1. long\short\int\byte 
2. enum 枚举
3. String （jdk7+）
```
switch(i){
case 1 :
执行语句；

case 2 ：
执行语句

case 3 ：
执行语句

defaul ：
以上情况都不是执行

}


```

- 作用域 通常以一个花括号为最小限制

* 所有的控制语句都可以相互嵌套

---

 ** Math.pow(x,3) 求立方，改后面数字


