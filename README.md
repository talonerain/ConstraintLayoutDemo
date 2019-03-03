ConstraintLayout
1. 当我们希望控件A与控件B左侧对齐时，就可以使用下面的属性。   
        ```
        app:layout_constraintLeft_toLeftOf="@id/viewB"
        ```
2. 当希望控件填满剩余部分时，除需要设置对齐属性外，还需要将控件宽度设置0dp，在ConstraintLayout中0代替match\_parent，所以不支持match\_parent这个值，官网就是这样说的。
    	```
    	android:layout_width="0dp"  
    	app:layout_constraintLeft_toRightOf="@+id/id_btn01"  
    	app:layout_constraintRight_toRightOf="parent"
    	```
3. 希望控件宽高保持比例可以通过设置下面这个属性设置宽高比：
	```
	app:layout_constraintDimensionRatio="16.6"
	```
	这点在其他布局中很难做到，除非通过代码
4. 比例设置：  
	```
	app:layout_constrainVertical_bias="0.9"
	app:layout_constrainHorizontal_bias="0.9"
	```
	以上两行代码分别将垂直方向和水平方向两侧的间隙比例设置为90%和10%
5. 辅助线，布局中不显示：  
	```
	<android.support.constraint.Guideline
        android:id="@+id/guideline_h"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:orientation="horizontal"
        app:layout_constraintGuide_percent="0.8"/>
	```
