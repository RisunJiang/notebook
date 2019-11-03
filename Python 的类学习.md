
#### Python 的类学习
1. 中文参考: [Python中self用法详解](https://blog.csdn.net/clhugh/article/details/75000104)
2. Python 定义一个Class:
```python
class Student(Obejct):
    pass
```
  - 其中, (Object) 表示该类从哪个类继承下来的, Object是所有类都会继承的类;
3. 实例:
```python
student = Student()
```
4. 构造函数或叫初始化方法, 以及self 用法:
```python
class Student(object):
    def __init__(self, name, score):
        self.name = name
        self.score = score
```
- __init__方法的第一个参数永远是self, 表示创建的类实例本身.
- self参数不需要传入, Python解释器自己把实例变量传进去.
```python
>>>student = Student("Hugh", 99)
>>>student.name
"Hugh"
>>>student.score
99


> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTg0MTEwNTYyMV19
-->