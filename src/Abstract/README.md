## 9. 抽象类和抽象方法

随着继承层次中一个个新子类的定义，类变得越来越具体，而父类则一般，更通用。类的设计应该包装父类和子类能够共享特征。有时**将一个父类设计得更加抽象，以至于它没有具体的实例，这样的类叫做抽象类**。

### 9.1 abstract 关键字的使用

1. abstract ： 抽象的

2. abstract 可以用来修饰的结构：类、方法

3. abstract 修饰类：抽象类 

   - 此类不能实例化 `abstract class Person {}`

   - 抽象类中一定有构造器，便于子类实例化时调用（涉及：子类对象实例化的全过程）
   - 开发中，都会提供抽象类的子类，让子类对象实例化，完成相关工作。

4. abstract 修饰方法：抽象方法 

   - 抽象方法只有方法声明，没有方法体。如，`public abstract void eat();`
   - 包含抽象方法的类一定是一个抽象类。反之，抽象类中可以没有抽象方法。
   - **继承抽象类的子类必须重写父类中的抽象方法** / **将子类也标记为抽象类**
   - 若子类重写了父类中的所有的抽象方法，此子类方可实例化对象
   - 若子类没有重写父类中所有的抽象方法，则子类也必须标记为抽象类，需要使用 abstract
