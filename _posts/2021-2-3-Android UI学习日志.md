---
layout: post
title: Android UI学习日志
categories: [Android]
description: Android UI学习日志
keywords: Android, android, java, ui, UI
---

## 0、布局常用属性

```xml
<!--xml约束-->
xmlns:android="http://schemas.android.com/apk/res/android"
```

android:gravity:文字对齐方式

android:layout_gravity：布局对齐方式

match_parent:属性值表示和父组件一样的宽度或高度

wrap_content:属性值表示和自身一样的的宽度或高度

layout_weight:值表示线性分割原本应有长度的权重，要和上面两个属性值配合使用

* 和wrap_content配合：先按照内容的多少去设定空间大小，然后按照权重的比例分配剩余控件

* 和match_parent配合：空间计算方式：空间大小=父容器大小+权重比例*剩余空间大小

* 和0dp配合：将layout_weight或者layout_height设为0dp，将直接按照layout_weight权重的比例分配空间，且不会被内容撑大

    

## 1、常用控件

### 1.1、TextView

### 1.2、Button

### 1.3、EditText

### 1.4、ImageView

### 1.5、ProgressBar

### 1.6、AlertDialog

### 1.7、ListView

### 1.8、RecyclerView

## 2、三种基本布局

### 2.1、LinearLayout

线性布局（水平或垂直方向布局，默认水平方向）

* android:orientation属性设置水平方向（horizontal) ,垂直方向（vertical）
* 如果布局为水平方向布局，内部的控件绝对不能将宽度指定为match_parent，否则一个控件就会将整个水平方向占满；同样，如果布局为垂直方向布局，内容的控件就不能将高度设置为match_parent
* 如果布局为水平方向，则对齐方式（layout_gravity)只有垂直方向的方式生效，垂直同理
* layout_weight属性：设置控件的宽度或高度的比例权重，前提要将layout_width设置为0dp



### 2.2、RealtiveLayout

相当布局（通过相对定位的方式让控件出现在布局的任何位置）

* 默认方式是在左上角，后声明的控件在最上面

* 基于父布局定位

    ```
    android:layout_alignParentBottom="true" //父布局底部对齐
    android:layout_alignParentTop="true" //父布局顶部对齐
    android:layout_alignParentRight="true" //父布局右对齐
    android:layout_alignParentLeft="true" //父布局左对齐
    ```

* 基于控件进行定位

    ```
    android:layout:above="控件id" 让一个控件位于另一个控件的上方
    android:layout:below"控件id" 让一个控件位于另一个控件的下方
    android:layout:toLeftOf"控件id" 让一个控件位于另一个控件的左侧
    android:layout:toRightOf"控件id" 让一个控件位于别一个控件的右侧
    注意：当一个控件去引用一另一个控件的id时，该控件一定要定义在引用控件的后面，否则会出现找不到id情况
    ```

    ```
    android:layout_alignLeft="控件id" 让一个控件的左边缘和另一个控件的左边缘对齐
    android:layout_alignRight="控件id" 让一个控件的左边缘和另一个控件的左边缘对齐
    android:layout_alignTop="控件id" 让一个控件的左边缘和另一个控件的左边缘对齐
    android:layout_alignBottom="控件id" 让一个控件的左边缘和另一个控件的左边缘对齐
    ```

### 2.3、FrameLayout

帧布局

* 没有丰富的定位方式，所有控件都会默认摆放在布局的左上角
* 可以通过android:layout_gravity进行定位对齐
* 配合Fragment使用

### 2.4、自定义控件

### 3、Fragment

