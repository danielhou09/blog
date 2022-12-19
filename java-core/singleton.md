# java 单例模式
## 什么是单例模式

单例模式（Singleton Pattern）是一种软件设计模式，其目的是确保某一个类只有一个实例，并提供一个全局访问点来访问这个实例。

## 优缺点
- 优点
  1. 在内存中只有一个对象，节省了内存空间。
  2. 全局访问点，方便调用。
   
- 缺点：
1. 某些情况下，单例模式的单例对象可能需要持久化，这时候就需要实现序列化接口。
1. 单例模式可能会导致测试困难，因为单例对象无法被替换。

## 哪里用到了单例模式？
- 缓存
- spring bean
- 读取配置
- 数据库
- 线程池
- 日志对象

## java 实现 singleton
- 懒汉模式
- 饿汉模式
- 枚举单例：Java 枚举类型本身就是单例的，因此可以直接使用枚举实现单例模式


> 饿汉模式（静态常量）
> 初始化的时候就创建好了。
```
public class Singleton1 {
    //构造器私有化 防止外部实例
    private Singleton1() {
    }

    private static final Singleton1 SINGLETON_1 = new Singleton1();

    public static Singleton1 getInstance(){
        return SINGLETON_1;
    }
}

```

>枚举单例

    public enum Singleton {
        INSTANCE;

        public void doSomething() {
            // do something
        }
    }
