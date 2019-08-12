---
description: 用于描述如何将类或对象按某种布局组成更大的结构，GoF 中提供了代理、适配器、桥接、装饰、外观、享元、组合等 7 种结构型模式。
---

# 结构型模式

### 代理模式（Proxy）

{% hint style="info" %}
为某对象提供一种代理以控制对该对象的访问。即客户端通过代理间接地访问该对象，从而限制、增强或修改该对象的一些特性。
{% endhint %}

![Proxy Pattern Class Diagram](../../.gitbook/assets/image%20%285%29.png)

对于代理模式，有个缺点，就是真实类必须预先存在。否则，无法实现代理类，对此，延伸出了改进的动态代理模式，即不需要关注真实类，都能实现代理类。Spring AOP采用两种实现方式，第一种就是通过JDK的动态代理类Proxy来实现，第二种是通过Cglib改变字节码来实现，第一种的类图如下：

![Dynamic Proxy Pattern Class Diagram](../../.gitbook/assets/image%20%284%29.png)

### 

### 适配器模式（Adapter）

{% hint style="info" %}
将一个类的接口转换成客户希望的另外一个接口，使得原本由于接口不兼容而不能一起工作的那些类能一起工作。
{% endhint %}

![Class Adapter Pattern Class Diagram](../../.gitbook/assets/image.png)

类适配器相当于在原业务类的上层套一个壳以满足新业务的接口，在Java中1.8之前，由于没有多继承，所以需要用一个接口和一个适配器类来实现模式，但是1.8之后由于可以对接口写抽象方法的默认实现，也就只需要用一个接口就可以实现适配器模式，对于C++，由于天生支持多继承，直接可以实现适配器。

![Method Adapter Pattern Class Diagram](../../.gitbook/assets/image%20%282%29.png)

方法适配器通过引用对象的方式实现。

### 

### 桥接模式（Bridge）

{% hint style="info" %}
将抽象与实现分离，使它们可以独立变化。它是用组合关系代替继承关系来实现的，从而降低了抽象和实现这两个可变维度的耦合度。
{% endhint %}

![Bridge Pattern Class Diagram](../../.gitbook/assets/image%20%288%29.png)

桥接主要是利用引用的方式代替继承的高耦合，将属性抽象化，然后引用抽象化的属性



### 装饰模式（Decorator）

{% hint style="info" %}
动态地给对象增加一些职责，即增加其额外的功能。
{% endhint %}

![Decorator Pattern Class Diagram](../../.gitbook/assets/image%20%2810%29.png)

在具体类上进行装饰，而不改变原来的类的方法，符合开闭原则



### 外观模式（Facade）

![Facade Pattern Class Diagram](../../.gitbook/assets/image%20%286%29.png)

当需要增加或删除子系统时，虽然不用修改客户类，但是需要改变Facade类，这就有悖于开闭原则，所以改进如下：

![Abstract Facade Pattern Class Diagram](../../.gitbook/assets/image%20%2812%29.png)



### 享元模式（Flyweight）

{% hint style="info" %}
运用共享技术来有效地支持大量细粒度对象的复用。
{% endhint %}

![Flyweight Pattern Class Diagram](../../.gitbook/assets/image%20%283%29.png)

对大量相同特性的对象引用同一个对象



### 组合模式（Composite）

{% hint style="info" %}
将对象组合成树状层次结构，使用户对单个对象和组合对象具有一致的访问性。
{% endhint %}

![Composite Pattern Class Diagram](../../.gitbook/assets/image%20%289%29.png)

透明方式的组合模式对客户来说是透明的，不区分树枝节点和树叶节点，但是由于树叶节点比树枝节点实际上是缺少了部分方法的实现，所以有一些安全的问题。

![Composite Pattern Class Diagram](../../.gitbook/assets/image%20%287%29.png)

安全模式区分了树枝节点和树叶节点，所以没有安全问题，但是对客户来说区分了这两个节点，所以不再是透明的。



