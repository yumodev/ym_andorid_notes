### 考虑使用静态工厂方法代替构造器

好处：
1、静态工厂方法有名称。
2、静态工厂方法不用再调用他们的时候都创建一个新的实例。
3、可以返回类型的任何子类型。
4、使得代码简洁。

缺点：
1、如果类不含有公共的或者受保护的构造方法，就不能通过静态工厂方法实例化
2、静态工厂方法和其他的静态方法没有什么区别。

### 遇到多个构造器参数时要考虑使用构建器。

建造者模式的典型应用场景。

### 通过定义私有构造方法强化不可实例化的能力。

不要通过抽象类实现不可实例化。主要是工具类和单例类的使用。

