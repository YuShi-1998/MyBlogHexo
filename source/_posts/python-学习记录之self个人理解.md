---
title: python-学习记录之self个人理解
date: 2021-03-29 18:03:31
tags:
cover: https://img.imgdb.cn/item/6061a6468322e6675cdfa36c.png
---
> 先简单的聊一下self，我们每次在写类的构造方法或者是类的实例方法，都会把self作为方法的第一个参数。假如这个时候把self参数给删了，如果你用的pycharm，就会显示红色下划线，鼠标光标移至红色下划线处，就会告诉你报错信息是：方法必须有第一个参数，通常称为self（看下图）。注意这里说的是通常称为self，其实我们也可填其他的名字，python并没有限制，但是不建议这么做。为什么呢！只是程序员之间约定俗成的一种习惯，遵守这个约定，可以使我们编写的代码具有更好的可读性（大家一看到 self，就知道它的作用）。

![](https://img.imgdb.cn/item/6066c72f8322e6675cc9efd7.png)



## self是什么

上面已经说了self的由来，那么self到底是什么呢。

例如，定义个学生类Student

```python
class Student:
    """学生类"""

    # 定义一个name()方法
    def name(self):
        student_name = "二狗"
        print(f"学生名字：{student_name}")
        return student_name

    # 定义一个age()方法
    def age(self):
        student_age = "18"
        print(f"学生年龄：{student_age}")
        return student_age

    # 定义一个info()方法
    def info(self):
        print(f"学生名字：{self.name()}，学生年龄：{self.age()}")

test = Student()
test.info()
test.name()
test.age()
```

上面代码，实例化Student类，然后调用实例方法info，然后info方法中调用了name方法跟age方法，得到结果如下

> 学生名字：二狗，学生年龄：18
>
> 学生名字：二狗
>
> 学生年龄：18

那么这里就可以看出了info()方法中的self.name()和self.age()就等同于test.name()和test.age()，而test = Student()，所以self就代表类本身



最后我们可以得到的结论就是：类里面创建的方法的第一个参数就是类本身















