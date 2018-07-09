# TabLayout
可自定义下标宽度的TabLayout 根据 com.android.support:design   TabLayout 的源码进行修改而来

[![Release](https://jitpack.io/v/UMoonlitDropOfBlood/TabLayout.svg)]
(https://jitpack.io/#MoonlitDropOfBlood/TabLayout)

看到网上博客都是反射修改，而且减少了Tab的可点击范围，体验十分不友好
所以特地修改了一份源码供使用，本项目依赖了V7包的样式（其实只使用了文本样式）
现在因为保持API一直 暂不提供直接设置文字大小的属性及方法 可通过 app:tabTextAppearance 进行设置

PROJECT_DIR/build.gradle

allprojects {
		repositories {
			...
			maven { url 'https://jitpack.io' }
		}
	}


mainMule/build.gradle

dependencies {
	        implementation 'com.github.MoonlitDropOfBlood:TabLayout:1.0.0'
	}

xml、java 中替换

android.support.design.widget.TabLayout ->  com.wwhbygx.tablayout.TabLayout
android.support.design.widget.TabItem   ->  com.wwhbygx.tablayout.TabItem

属性、方法与 api27.1.1版本保持一致

新增方法 setSelectedTabIndicatorWidth 方法（动态改变宽度）
新增 tabIndicatorWidth 属性 可在xml中直接定义属性 如 app:tabIndicatorWidth="30dp"

TabLayout详细用法 请查看http://www.google.com/design/spec/components/tabs.html
