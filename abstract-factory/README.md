# 抽象工厂（Abstract Factory）
抽象工厂（Abstract Factory）模式，又称工具箱（Kit 或Toolkit）模式。

工厂方法模式通过引入工厂等级结构，解决了简单工厂模式中工厂类职责太重的问题，但由于工厂方法模式中的每个工厂只生产一类产品，可能会导致系统中存在大量的工厂类，势必会增加系统的开销。此时，我们可以考虑将一些相关的产品组成一个**产品族**，由同一个工厂来统一生产。

## 适用场景
* 和工厂方法一样客户端不需要知道它所创建的对象的类。
* 需要一组对象共同完成某种功能时，并且可能存在多组对象完成不同功能的情况（同属于同一个产品族的产品）。
* 系统结构稳定，不会频繁的增加对象。（因为一旦增加就需要修改原有代码，不符合开闭原则）

#### 抽象工厂方法模式角色分配
* 抽象工厂（AbstractFactory）角色 ：是工厂方法模式的核心，与应用程序无关。任何在模式中创建的对象的工厂类必须实现这个接口。
* 具体工厂（ConcreteFactory）角色 ：这是实现抽象工厂接口的具体工厂类，包含与应用程序密切相关的逻辑，并且受到应用程序调用以创建某一种产品对象。
* 抽象产品（Abstract Product）角色 ：工厂方法模式所创建的对象的超类型，也就是产品对象的共同父类或共同拥有的接口。
* 具体产品（Concrete Product）角色 ：抽象工厂模式所创建的任何产品对象都是某一个具体产品类的实例。在抽象工厂中创建的产品属于同一产品族，这不同于工厂模式中的工厂只创建单一产品。

#### 抽象工厂的工厂和工厂方法中的工厂有什么区别？
抽象工厂是生产一整套有产品的（至少要生产两个产品)，这些产品必须相互是有关系或有依赖的，而工厂方法中的工厂是生产单一产品的工厂。
#### 抽象工厂图示
![abstract-factory](https://github.com/caozongpeng/javaDesignPatterns/blob/master/images/abstract-factory.jpg)
## 具体实现
现在手机基本上人人都有，我们假设现在存在苹果、三星两种手机，每一种手机对应一种手机壳。我们现在这样考虑生产苹果手机的工厂可以顺便生产苹果手机的手机壳，生产三星手机的工厂可以顺便生产三星手机的手机壳（苹果工厂生产苹果系统产品包括手机壳，三星工厂同理）。
![abstract-factory2](https://github.com/caozongpeng/javaDesignPatterns/blob/master/images/abstract-factory2.jpg)












