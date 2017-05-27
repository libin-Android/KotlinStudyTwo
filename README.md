# KotlinStudy
使用Kotlin写Hello Word
========================
最近谷歌IO大会, 把kotlin纳入了Android开发首选语言, 估计这与谷歌和Oracle一直在打官司的缘故分不开吧, 而且kotlin本身就很好用,

而且kotlin-native是基于自己的runtime, 之前讲了 [android studio3.0预览版使用kotlin], 但是很多涌进来的新人在android studio2.0中使用kotlin有问题

我现在就来演示一次, 希望有所帮助!(假定已经拥有了开发Android的基础, 约定Android Studio简称as)

首先需要了解 kotlin
-------------------
kotlin官方文档：https://kotlinlang.org/docs/reference/basic-syntax.html

Kotlin是JetBrains开发的基于JVM的语言，JetBrains想必大家应该很熟悉了，他们创造了很多强大的IDE，android studio谷歌官方的android IDE就是基于Intellij，kotlin可以作为一个插件被用来开发android跟java比kotlin有什么好处？

1.它更容易表现，使用kotlin你可以少写很多代码，比如创建数据类等。

2.它更安全，在用Java开发时，大多数代码都是预防性的。为了不遇到非预期的NullPointerException，在使用之前，要不断的检测对象是否为空。与许多其它语言一样，因为需要使用安全调用运算符显式指明对象是否能够为空（null），所以Kotlin是空类型安全的

3.它是函数式的，Kotlin是基于面向对象的语言。但是就如其他很多现代的语言那样，它使用了很多函数式编程的概念，比如，使用lambda表达式来更方便地解决问题。其中一个很棒的特性就是Collections的处理方式。

4.它可以扩展函数，这意味着我们可以扩展类的更多的特性，甚至我们没有权限去访问这个类




其次安装kotlin插件(安装后重启as生效)
-----------------------------


### 1.File ----》setting -----》plugins----》搜索kotlin，现在安装，重新启动studio

### 2.添加完你就会发现多了new file 时候多了两个选项，如下图![](https://github.com/libin-Android/KotlinStudyTwo/blob/master/a.png)

### 3.在studio中配置kotlin，如下图![](https://github.com/libin-Android/KotlinStudyTwo/blob/master/b.png)

### 4.配置kotlin完，查看project的build和module的build，如下图![](https://github.com/libin-Android/KotlinStudyTwo/blob/master/c.png) ![](https://github.com/libin-Android/KotlinStudyTwo/blob/master/d.png) ![](https://github.com/libin-Android/KotlinStudyTwo/blob/master/e.png)

### 5.最后介绍功能最强大的java代码转换成kotlin代码，，，而且studio自动转换，无需自己重写，如下图
![](https://github.com/libin-Android/KotlinStudyTwo/blob/master/f.png)

    `重点是转换完的文件上是.kt文件` `编译完的文件仍然是.class文件`
    
最后在代码中使用kotlin
==========================
### 1.转换后的MainActivity
   package com.example.administrator.kotlinstudy

import android.support.v7.app.AppCompatActivity

import android.os.Bundle

import kotlinx.android.synthetic.main.activity_main.*

class MainActivity : AppCompatActivity() {

    override fun onCreate(savedInstanceState: Bundle?) {
    
        super.onCreate(savedInstanceState)
        
        setContentView(R.layout.activity_main)
        
        tv.setText("kotlin Hello Word");
        
    }
    
}

 `不写findViewById.直接用布局中控件的id`

