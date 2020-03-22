# Java 异常体系

## 异常

- throw 抛出异常
  1. 当执行到throw语句时会进行方法的结束，然后将这个异常上抛，依次进行，如果都没有try catch 会击穿方法栈然后结束运行。有try catch 时会尝试进行。

- try catch

  ```java
  try {
      a(); //想要执行的东西
  } catch (Exception e) {
      e.printStackTrace();//打印异常信息，在这里处理捕捉到的异常
  } finally {
      //在前面两个操作无论是正常执行，还是出现异常，都会执行finally中的操作，finally只执行资源的清理工作，不要在这里写return语句。
  } 
  ```

- File Leak Detector

  用于检测没有被正常关闭的文件的操作。

- try with resource 语法糖

  1. java 7 之后 ，会自动为你加入finally，正常写，需要改变的地方会变黄提示你更改。 

- throw throws
  1. throw 丢出一个异常
  2. throws 声明一个异常 ，声明不一定抛出，但是抛出一定声明，也可以不声明自己处理try catch。
  3. 你声明之后所有调用你的这个方法的方法都要声明这个异常。

## 异常体系

- Object

- Throwable

  可以抛出的东西（有毒）

- Exception - checked exception 受检异常，有毒

  预料之内的异常

- RuntimeException

  运行时异常，无毒

- NullPonitException

  预料之外的异常

- error 

  严重的错误，无法处理

- catch 的级联和合并

  多个错误，声明最高的错误，

  可以根据不同的异常来进行异常的操作

  先处理最低的异常，从小到大去catch，从大的处理会使后面的无法被处理

  - java 7 语法糖，idea会提醒你

## 异常的栈轨迹

- 异常抛出后会提供每一级的调用过程 StackTrace

- 异常链 

  异常抛出后可能被捕获后再次抛出，每被捕获抛出一次都会产生一个cause by

## 异常的抛出原则

- 能用if else 判断，就不要用异常，异常是很昂贵的操作，异常十分占用资源相比于if else 来说
- 异常要抛出，能处理处理，不能尽早抛出
- 异常尽量要准确，尽量把发生异常时的环境参数添加进去，带有详细信息
- 抛出异常比你悄悄执行好得多（不要吞掉你无法解决的异常）
- 不处理不归自己管的异常，不能处理的异常就抛出，如无必要，不要忽略异常



## JDK内置的异常

- NullPointerException  空指针异常
-  ClassNotFoundException/NoClassDefFoundError 类不存在/类未定义
-  IllegalStateException  不正常的状态
-  IllegalArgumentException  不正常的参数
-  IllegalAccessException  非法访问
-  ClassCastException  类型转换



