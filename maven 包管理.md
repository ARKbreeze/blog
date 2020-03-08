# maven 包管理

## Java 包管理

- Java当遇到不认识的类时，会去找这个类，找的路径即为 classpath，从头开始一个一个找，直到唯一确定了这个类。
- 在`maven`没出现以前，还需要自己自己对类的路径进行编写，
  1. 依赖地狱，当配置依赖的classpath中出现两个相同jar包的不同版本时，如果路径是低版本在前可能会出现不可预测的危险，
  2. 庞大的类依赖可能需要配置的工作量十分巨大
  3. 同时后期出现的 `Apache Ant`虽然一定量的解决了这种问题，但是也带来了一些其他的问题，没有相应的标准，每个人都可能造自己的轮子，并没有有效解决这个问题

## Maven 时代

- 约定优于配置

  1. maven的包

  ``` java
  <dependencies>
  <groupId> <groupId>
  <artifactId> <artifactId>
  <version> <version>
  </dependencies>
  ```

- maven 主仓库
  1. 按照一定约定来存储所有的包
  2. 程序会根据maven约定来这个仓库找到包进行下载
  3. 可以根据需求选择从不同的仓库获得包
  
- maven本地库
  1. 默认位于~/.m2文件夹下
  2. 下载的包会缓存在这里 

- 传递依赖的自动管理
  
  1. 优先选择距离近的同名包，不分析语义化版本
  
- 包冲突
  1. AbstractMethodError
  2. NoClassDefFoundError
  3. ClassNotFoundException 
  4. LinkageError

- 冲突处理

  1. 直接在最外层添加需要的版本包

  2. 添加

     ```Java
     <exclusion>
       <groupId>       </groupId>    
       <artifactId>     <artifactId>
     </exclusion>
     ```

  3. 查看依赖，通过maven图形化界面；命令行`mvn dependeny:tree`

  4.  插件 `maven helper`

- scope
  1.  <scope>  </scope> 指定作用域，只在指定的作用域中生效
  2.  compile 编译运行测试  provided (编译时提供，运行时由其他来提供) test 仅测试

- maven实战- 5,6,7,8;

- 基本概念:坐标和依赖/生命周期/仓库/聚合与继承

**“.”和“|”**  转义要加 ` \\`