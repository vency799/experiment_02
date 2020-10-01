

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

设置两个 LinearLayout ，第一个 LinearLayout 作为父标签，第二个 LinearLayout 作为子标签，子标签在父标签内。父标签设置为垂直布局，子标签设置为水平布局。结构如下：

```
<LinearLayout ...>
	<LinearLayout ...>
		...
	</LinearLayout>
</LinearLayout>
```

(用到了4个 LinearLayout 子标签)

strings配置：

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

strings配置：

```
    <string name="button_red">RED</string>
    <string name="button_orange">ORANGE</string>
    <string name="button_yellow">YELLOW</string>
    <string name="button_blue">BLUE</string>
    <string name="button_green">GREEN</string>
    <string name="button_indigo">INDIGO</string>
    <string name="button_violet">VIOLET</string>
```

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

3、表格布局实验

代码：

```
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:background="#6C6A6A"
    android:orientation="vertical">

    <TableRow
        android:layout_width="match_parent"
        android:layout_height="wrap_content">

        <TextView
            android:id="@+id/textView5"
            android:layout_width="194dp"
            android:layout_height="match_parent"
            android:text="@string/open"
            android:textColor="#FFFFFF"
            android:textSize="24sp" />

        <TextView
            android:id="@+id/textView6"
            android:layout_width="201dp"
            android:layout_height="match_parent"
            android:gravity="right"
            android:text="@string/cto"
            android:textColor="#FFFFFF"
            android:textSize="24sp" />
    </TableRow>

    <TableRow
        android:layout_width="match_parent"
        android:layout_height="wrap_content">

        <TextView
            android:id="@+id/textView7"
            android:layout_width="194dp"
            android:layout_height="match_parent"
            android:text="@string/save"
            android:textColor="#FFFFFF"
            android:textSize="24sp" />

        <TextView
            android:id="@+id/textView9"
            android:layout_width="201dp"
            android:layout_height="match_parent"
            android:gravity="right"
            android:text="@string/cts"
            android:textColor="#FFFFFF"
            android:textSize="24sp" />

    </TableRow>

    <TableRow
        android:layout_width="match_parent"
        android:layout_height="wrap_content">

        <TextView
            android:id="@+id/textView10"
            android:layout_width="194dp"
            android:layout_height="match_parent"
            android:text="@string/save_as"
            android:textColor="#FFFFFF"
            android:textSize="24sp" />

        <TextView
            android:id="@+id/textView11"
            android:layout_width="197dp"
            android:layout_height="match_parent"
            android:gravity="right"
            android:text="@string/ctfs"
            android:textColor="#FFFFFF"
            android:textSize="24sp" />
    </TableRow>

    <TableRow
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:background="#ACA8A8"
        android:paddingTop="10dp">

        <TextView
            android:id="@+id/textView12"
            android:layout_width="match_parent"
            android:layout_height="match_parent"
            android:background="#6C6A6A"
            android:text="@string/imp"
            android:textColor="#FFFFFF"
            android:textSize="24sp" />
    </TableRow>

    <TableRow
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:background="#ACA8A8"
        android:paddingBottom="10dp">

        <TextView
            android:id="@+id/textView13"
            android:layout_width="194dp"
            android:layout_height="wrap_content"
            android:background="#6C6A6A"
            android:text="@string/emp"
            android:textColor="#FFFFFF"
            android:textSize="24sp" />

        <TextView
            android:id="@+id/textView14"
            android:layout_width="199dp"
            android:layout_height="wrap_content"
            android:background="#6C6A6A"
            android:gravity="right"
            android:text="@string/cte"
            android:textColor="#FFFFFF"
            android:textSize="24sp" />
    </TableRow>

    <TableRow
        android:layout_width="match_parent"
        android:layout_height="wrap_content">

        <TextView
            android:id="@+id/textView15"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:background="#6C6A6A"
            android:text="@string/quit"
            android:textColor="#FFFFFF"
            android:textSize="24sp" />
    </TableRow>

</LinearLayout>
```

strings配置：

```
    <string name="open">&#32;&#32;&#32;&#32;Open...</string>
    <string name="cto">Ctrl+O</string>
    <string name="save">&#32;&#32;&#32;&#32;Save...</string>
    <string name="cts">Ctrl+S</string>
    <string name="save_as">&#32;&#32;&#32;&#32;Save As...</string>
    <string name="ctfs">Ctrl+Shift+S</string>
    <string name="imp">× Import...</string>
    <string name="emp">× Export...</string>
    <string name="cte">Ctrl+E</string>
    <string name="quit">&#32;&#32;&#32;&#32;Quit</string>
```

关于边框颜色设置：

在Import、Export两行处，上下各有颜色较背景颜色浅色的横条，实现方法是：Import的 TableRow 设置paddingTop=10dp，Export的 TableRow 设置paddingBottom=10dp

![image](https://github.com/vency799/experiment_02/blob/master/padding_setting.png)

设置 TextView 的背景颜色与窗口背景颜色一致(#6C6A6A)，所以Import TableRow 上方有10dp的空余区域，Export TableRow 下方有10dp的空余区域，将两个 TableRow 的背景颜色设置为浅一点的颜色(#ACA8A8)，完成。

![image](https://github.com/vency799/experiment_02/blob/master/edge_color.png)

其他：

同一行中的右边内容都设置了

> ```
> android:gravity="right"
> ```

效果如图：

![image](https://github.com/vency799/experiment_02/blob/master/gravity_setting.png)

运行结果：

![image](https://github.com/vency799/experiment_02/blob/master/design.png)

![image](https://github.com/vency799/experiment_02/blob/master/result_table.png)
