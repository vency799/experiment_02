

## 实验二

1、线性布局实验

代码：

> ```
> <LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
>     android:orientation="vertical" android:layout_width="match_parent"
>     android:layout_height="match_parent"
>     >
>     <!--父标签设置为垂直布局-->
>     <LinearLayout
>         android:layout_width="match_parent"
>         android:layout_height="wrap_content"
>         android:orientation="horizontal">
>         <!--子标签设置为水平布局-->
>         <Button
>             android:id="@+id/button1"
>             android:layout_width="wrap_content"
>             android:layout_height="wrap_content"
>             android:text="@string/button1" />
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
(用到了4个子标签<LinearLayout>)
运行结果：

![image](https://github.com/vency799/experiment_02/blob/master/lineartest.png)

