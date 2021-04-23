---
layout: post
title: Java中==与equals的匹配
categories: [Java, 基础]
description: Java中==与equals的匹配
keywords: java, Java, 基础,

---

#### 1、"=="的含义

1.1、基础数据类型：比较的是他们的值是否相等

1.2、引用数据类型：比较的是引用的地址是否相同

#### 2、理解equals的含义

2.1、equals方法是在Object中定义,比较的是当前对象的引用和obj的引用是否相同，代码如下：

```java
public boolean equals(Object obj){
	return (this == obj);
}
```

#### 3、重写equals

3.1、String中equals方法

```java
    public boolean equals(Object anObject) {
        if (this == anObject) {
            return true;
        }
        if (anObject instanceof String) {
            String aString = (String)anObject;
            if (coder() == aString.coder()) {
                return isLatin1() ? StringLatin1.equals(value, aString.value)
                                  : StringUTF16.equals(value, aString.value);
            }
        }
        return false;
    }
```

