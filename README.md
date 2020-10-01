

## 实验二

1、线性布局实验

代码：

> ```
> <LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
>  android:orientation="vertical" android:layout_width="match_parent"
>  android:layout_height="match_parent"
>  >
>  <!--父标签设置为垂直布局-->
>  <LinearLayout
>      android:layout_width="match_parent"
>      android:layout_height="wrap_content"
>      android:orientation="horizontal">
>      <!--子标签设置为水平布局-->
>      <Button
>          android:id="@+id/button1"
>          android:layout_width="wrap_content"
>          android:layout_height="wrap_content"
>          android:text="@string/button1" />
> ...
> ```

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
