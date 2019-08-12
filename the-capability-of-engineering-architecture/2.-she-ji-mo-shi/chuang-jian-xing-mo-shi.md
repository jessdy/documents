---
description: 用于描述“怎样创建对象”，它的主要特点是“将对象的创建与使用分离”。GoF 中提供了单例、原型、工厂方法、抽象工厂、建造者等 5 种创建型模式。
---

# 创建型模式

### 单例模式（Singleton）

{% hint style="info" %}
某个类只能生成一个实例，该类提供了一个全局访问点供外部获取该实例，其拓展是有限多例模式。
{% endhint %}

![Singleton Class Diagram](../../.gitbook/assets/singleton.gif)

### 原型模式（Prototype）

{% hint style="info" %}
将一个对象作为原型，通过对其进行复制而克隆出多个和原型类似的新实例。
{% endhint %}

![Prototype Class Diagram](../../.gitbook/assets/prototype.gif)

### 工厂方法（FactoryMethod）

{% hint style="info" %}
定义一个用于创建产品的接口，由子类决定生产什么产品。
{% endhint %}

![FactoryMethod Class Diagram](../../.gitbook/assets/factorymethod.gif)

### 抽象工厂（AbstractFactory）

{% hint style="info" %}
提供一个创建产品族的接口，其每个子类可以生产一系列相关的产品。
{% endhint %}

![Abstract Factory Class Diagram](../../.gitbook/assets/image%20%281%29.png)

### 建造者模式（Builder）

{% hint style="info" %}
将一个复杂对象分解成多个相对简单的部分，然后根据不同需要分别创建它们，最后构建成该复杂对象。
{% endhint %}

![Builder Class Diagram](../../.gitbook/assets/image%20%2811%29.png)

