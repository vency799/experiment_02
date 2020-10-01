

## 实验二

实验内容：根据图片要求，完成Android布局

实验步骤：

1、线性布局实验

代码：

```
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
 android:orientation="vertical" android:layout_width="match_parent"
 android:layout_height="match_parent"
 >
 <!--父标签设置为垂直布局-->
 <LinearLayout
     android:layout_width="match_parent"
     android:layout_height="wrap_content"
     android:orientation="horizontal">
     <!--子标签设置为水平布局-->
     <Button
         android:id="@+id/button1"
         android:layout_width="wrap_content"
         android:layout_height="wrap_content"
         android:text="@string/button1" />
...
```

设置两个<LinearLayout>，第一个<LinearLayout>作为父标签，第二个<LinearLayout>作为子标签，子标签在父标签内。父标签设置为垂直布局，子标签设置为水平布局。结构如下：

```
<LinearLayout ...>
	<LinearLayout ...>
		...
	</LinearLayout>
</LinearLayout>
```

(用到了4个<LinearLayout>子标签)

string内定义的button：

```
 	<string name="button1">One,One</string>
    <string name="button2">One,Two</string>
    <string name="button3">One,Three</string>
    <string name="button4">One,Four</string>

    <string name="button5">Two,One</string>
    <string name="button6">Two,Two</string>
    <string name="button7">Two,Three</string>
    <string name="button8">Two,Four</string>

    <string name="button9">Three,One</string>
    <string name="button10">Three,Two</string>
    <string name="button11">Three,Three</string>
    <string name="button12">Three,Four</string>

    <string name="button13">Four,One</string>
    <string name="button14">Four,Two</string>
    <string name="button15">Four,Three</string>
    <string name="button16">Four,Four</string>
```

运行结果：

![image](https://github.com/vency799/experiment_02/blob/master/lineartest.png)

![image](https://github.com/vency799/experiment_02/blob/master/phonepage.png)

2、约束布局实验

代码：

```
<?xml version="1.0" encoding="utf-8"?>
<android.support.constraint.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent">

    <Button
        android:id="@+id/button"
        android:layout_width="96dp"
        android:layout_height="72dp"
        android:backgroundTint="#F44336"
        android:text="@string/button_red"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

    <Button
        android:id="@+id/button17"
        android:layout_width="96dp"
        android:layout_height="72dp"
        android:backgroundTint="#FF9800"
        android:text="@string/button_orange"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.498"
        app:layout_constraintStart_toStartOf="@+id/button"
        app:layout_constraintTop_toTopOf="parent" />

    <Button
        android:id="@+id/button18"
        android:layout_width="101dp"
        android:layout_height="72dp"
        android:backgroundTint="#FFEB3B"
        android:text="@string/button_yellow"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

    <Button
        android:id="@+id/button19"
        android:layout_width="92dp"
        android:layout_height="78dp"
        android:backgroundTint="#3F51B5"
        android:text="@string/button_blue"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/button17"
        app:layout_constraintVertical_bias="0.106" />

    <Button
        android:id="@+id/button20"
        android:layout_width="92dp"
        android:layout_height="78dp"
        android:layout_marginTop="60dp"
        android:backgroundTint="#4CAF50"
        android:text="@string/button_green"
        app:layout_constraintEnd_toStartOf="@+id/button19"
        app:layout_constraintHorizontal_bias="0.835"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/button17" />

    <Button
        android:id="@+id/button22"
        android:layout_width="92dp"
        android:layout_height="78dp"
        android:layout_marginTop="60dp"
        android:backgroundTint="#7F1C8F"
        android:text="@string/button_indigo"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.154"
        app:layout_constraintStart_toEndOf="@+id/button19"
        app:layout_constraintTop_toBottomOf="@+id/button17" />

    <Button
        android:id="@+id/button23"
        android:layout_width="408dp"
        android:layout_height="53dp"
        android:backgroundTint="#D55AEA"
        android:text="@string/button_violet"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="1.0"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="@+id/button17"
        app:layout_constraintVertical_bias="0.39" />
</android.support.constraint.ConstraintLayout>
```

代码中的“toStartof"、”toEndof“、”toTopof“等都为约束布局的条件，由”app“控制。

RED、YELLOW按钮：

RED按钮添加一个水平约束和一个垂直约束，水平约束连接到窗口左边框，垂直约束连接到窗口上边框；YELLOW按钮同理，垂直约束连接到右边框。调整按钮尺寸与颜色，完成。

![image](https://github.com/vency799/experiment_02/blob/master/button_red.png)

![image](https://github.com/vency799/experiment_02/blob/master/button_yellow.png)



ORANGE按钮：

ORANGE按钮添加两个水平约束和一个垂直约束，达到水平居中，在窗口最上方。

![image](https://github.com/vency799/experiment_02/blob/master/button_orange.png)

BLUE按钮：

BLUE按钮添加两个水平约束和两个垂直约束。

![image](https://github.com/vency799/experiment_02/blob/master/button_blue.png)

GREEN、INDIGO按钮：

GREEN按钮添加两个水平约束和一个垂直约束，左水平约束连接到窗口左边框，右水平约束连接到BLUE按钮左边；INDIGO按钮同理，左水平约束连接到BLUE按钮右边，右水平约束连接到窗口右边框。两个按钮的垂直约束均连接到ORANGE按钮的下约束。

![image](https://github.com/vency799/experiment_02/blob/master/button_green.png)

![image](https://github.com/vency799/experiment_02/blob/master/button_indigo.png)

VIOLET按钮：

VIOLET按钮添加两个水平约束和两个垂直约束，个方向约束连接到对应方向的窗口边框。

![image](https://github.com/vency799/experiment_02/blob/master/button_violet.png)

运行结果：

![image](https://github.com/vency799/experiment_02/blob/master/result_constr.png)
