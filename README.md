# PieView
一个自定义的饼状表格图View

#效果图

###PieView效果图
<div>
<img src="https://github.com/zhijieeeeee/PieView/blob/master/screenshot/pre1.png" width = "270" height = "480" alt="PieView" />
<img src="https://github.com/zhijieeeeee/PieView/blob/master/screenshot/pre2.png" width = "270" height = "480" alt="PieView" />
</div>

###PieView2效果图
<div>
<img src="https://github.com/zhijieeeeee/PieView/blob/master/screenshot/pieview2_pre1.png" width = "270" height = "480" alt="PieView2" />
<img src="https://github.com/zhijieeeeee/PieView/blob/master/screenshot/pieview2_pre2.png" width = "270" height = "480" alt="PieView2" />
</div>
#基本使用

###1.在gradle中添加依赖
	
	compile 'com.don:pieviewlibrary:2.0.0'

###2.布局中使用

使用默认的样式，其中宽高可根据自己的需求设置，支持wrap\_content，match\_parent，固定尺寸。


折现类型显示数据：

	<com.don.pieviewlibrary.PieView
        android:id="@+id/pieView"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />

百分比类型显示数据	：

	<com.don.pieviewlibrary.PieView2
        android:id="@+id/pieView2"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />

自定义样式，根据自己的需求设置各种颜色：
	
	<com.don.pieviewlibrary.PieView
        android:id="@+id/pieView"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        don:centerTextColor="#000000"
        don:centerTextSize="24sp"
        don:circleWidth="20dp"
        don:dataTextColor="#ff00ff"
        don:dataTextSize="12sp" />

	<com.don.pieviewlibrary.PieView2
        android:id="@+id/pieView2"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        don:centerTextColor="#000000"
        don:centerTextSize="24sp"
        don:circleWidth="40dp"
        don:dataTextColor="#ffffff"
        don:dataTextSize="10sp" />


* centerTextColor：中间字体颜色

* centerTextSize：中间字体大小

* circleWidth：圆圈的厚度

* dataTextColor：数据字体颜色

* dataTextSize：数据字体大小

###3.代码中设置数据源

PieView和PieView2的使用方式相同

	int[] data = new int[]{10, 10, 10, 40};
    String[] name = new String[]{"兄弟", "姐妹", "情侣", "基友"};

    PieView pieView = (PieView) findViewById(R.id.pieView);
    pieView.setData(data, name);

	PieView2 pieView2 = (PieView2) findViewById(R.id.pieView2);
    pieView2.setData(data, name);

#更新日志

### V2.0.0
* 添加PieView2，使用百分比形式显示
* 重构代码
### V1.0.0
* 饼状表格图View


#License
        Copyright 2016 zhijieeeeee

        Licensed under the Apache License, Version 2.0 (the "License");
        you may not use this file except in compliance with the License.
        You may obtain a copy of the License at

          http://www.apache.org/licenses/LICENSE-2.0

        Unless required by applicable law or agreed to in writing, software
        distributed under the License is distributed on an "AS IS" BASIS,
        WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
        See the License for the specific language governing permissions and
        limitations under the License.
