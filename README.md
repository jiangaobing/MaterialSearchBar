# ExpandableTextView

**本项目基于开源项目android-materialshadowninepatch 进行鸿蒙化的移植和开发，可以通过项目标签以及github地址（<https://github.com/h6ah4i/android-materialshadowninepatch>）追踪到原安卓项目版本**

#### 项目介绍
- 项目名称：材料阴影
- 所属系列：鸿蒙的第三方组件适配移植
- 功能：实现可以给文本设置阴影效果
- 项目移植状态：主功能完成
- 调用差异：无
- 开发版本：sdk5，DevEco Studio2.1 beta3
- 项目作者和维护人：古天乐
- 联系方式：gutianle050@chinasoftinc.com
- 原项目Doc地址：<https://github.com/h6ah4i/android-materialshadowninepatch>

#### 效果演示
![效果演示](https://gitee.com/chinasoft_ohos/upload/raw/master/img/demo.gif "效果演示.gif")

#### 安装教程

1.下载library的har包library.har（位于:<https://gitee.com/chinasoft_ohos/ExpandableTextView/releases/v0.0.1_alpha>）。

2.启动 DevEco Studio，将下载的har包，导入工程目录“demo->libs”下。

 ```

在sdk4，DevEco Studio2.1 beta2下项目可直接运行
如无法运行，删除项目.gradle,.idea,build,gradle,build.gradle文件，
并依据自己的版本创建新项目，将新项目的对应文件复制到根目录下

#### 使用说明

使用该库非常简单，只需查看提供的示例的源代码。
```示例XML
<com.h6ah4i.android.materialshadowninepatch.MaterialShadowContainerView
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    style="@style/ms9_DefaultShadowStyle"
    android:id="@+id/shadow_item_container"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    app:ms9_shadowTranslationZ="2dp"
    app:ms9_shadowElevation="4dp">

    <!-- NOTE 1: only 1 child can be accepted -->
    <!-- NOTE 2: margins are required to draw shadow properly -->
    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginLeft="8dp"
        android:layout_marginTop="8dp"
        android:layout_marginRight="8dp"
        android:layout_marginBottom="8dp"
        android:background="@android:color/white"
        android:text="Inner content view" />

</com.h6ah4i.android.materialshadowninepatch.MaterialShadowContainerView>
```

```java
        MaterialShadowContainerView shadowView =
            (MaterialShadowContainerView) findViewById(R.id.shadow_item_container);

        float density = getResources().getDisplayMetrics().density;

        shadowView.setShadowTranslationZ(density * 2.0f); // 2.0 dp
        shadowView.setShadowElevation(density * 4.0f); // 4.0 dp
```
另外，您可以选择在布局xml文件中设置以下属性，以自定义ExpandableTextView的行为。
1. app:mrl_rippleAlpha 设置阴影的透明度

2. app:mrl_rippleColor 设置阴影的颜色

3. app:ms9_useAmbientShadow  指定是否使用环境阴影。

4. app:ms9_useSpotShadow 指定是否使用斑点阴影

5. ms9_forceUseCompatShadow 强制在棒棒糖上或以后使用兼容性阴影

#### 测试信息

CodeCheck代码测试无异常

CloudTest代码测试无异常

火绒安全病毒安全检测通过

当前版本demo功能与安卓原组件基本无差异

测试员：石凯月

#### 版本迭代

- v0.0.1_alpha

#### 版权和许可信息

    Copyright 2014 Manabu Shimobe
    
    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at
    
    http://www.apache.org/licenses/LICENSE-2.0
    
    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.

