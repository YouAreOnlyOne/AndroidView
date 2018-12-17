# AndroidView
Android中自定义控件的使用与封装，包括各种原形图片、柱状图、折线图、饼图、组合图形以及复杂的控件特效等等，是现在在Android开发中直接引用。


# 最新版本

版本号：[![](https://www.jitpack.io/v/YouAreOnlyOne/AndroidView.svg)](https://www.jitpack.io/#YouAreOnlyOne/AndroidView)

使用自行替换下面的版本号，以获得最新版本。

# 使用方法

后期会介绍在不同的项目开发环境中，如何快速的使用该库。

## Android中使用：

方法一：

1.第一步，在项目的build.gradle下配置，注意是项目的build.gradle：

     allprojects {
		repositories {
			...
			maven { url 'https://www.jitpack.io' }
		}
	}
    
    
2.第二步,在app的build.gradle下添加如下依赖：

    dependencies {
            ...
            implementation 'com.github.YouAreOnlyOne:AndroidView:版本号'
            ...
     }
    
# 使用示例

在任何布局文件中，即Activity所装载的 xml 文件中进行引用，跟普通的View控件没有什么区别，举例如下：

## 圆形图片自动转换：

	<com.frank.ycj520.customview.CircleImageView
      		 <!--设置控件高度-->
      		 android:layout_height="wrap_content"
       		 <!--设置控件高度-->
       		 android:layout_width="wrap_content"
       		 <!--设置要显示的图片资源，这里不止这一种方法，根据需要进行使用-->
        		 app:imageSrc="@drawable/test"
        		<!--设置模糊程度，数值越大，越模糊，1代表不模糊-->
        		app:inSampleSize="1">

   	 </com.frank.ycj520.customview.circleImageView>
	 
	 注意：使用时候，可能要去掉注释内容，以免编译出错。
	 
## 折线图动态显示：

在xml文件中引用View：

	<com.frank.ycj520.customview.BrokenLineView1
       	android:layout_width="wrap_content"
        	android:layout_height="wrap_content" />
		 
		 
在Activity中加载数据：

	BrokenLineView brokenview= (BrokenLineView) findViewById(R.id.chartView);
	brokenview.SetInfo(
                new String[]{"周一","周二","周三","周四","周五","周六","周日"},   //X轴刻度
                new String[]{"","50","100","150","200","250","300","350"},   //Y轴刻度
                new String[]{"150","230","10","136","45","40","112","313"},  //数据
                "图标的标题"
        );

# 主要控件

CircleImageView  自动把图片转换为圆形图片

BrokenLineView1  数据自动生成折线图，风格1

BrokenLineView2  数据自动生成折线图，风格2

MyRadioGroup  自动对RadioGroup中的RadioButton进行按行或者按列排列

RenderViewForWave  

WaveView 单曲线水波纹效果➕图像跳动

WaveViewForDouble 双曲线水波纹滑动效果➕渐变填充

