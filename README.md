我只是在这里把我看到的，用到的Material Design 三方开源项目写在这里，我以后会把我了解到的继续推介，谢谢大牛们的专研和开源精神。
欢迎大家推荐好的 Android  Material Design开源项目，开源项目添加到 Android Android  Material Design开源项目集合，可以得到更多朋友的关注和反馈，欢迎Star、Fork :)
### 1.MaterialEditText
#### 作者：扔物线
####  [中文介绍地址](http://www.rengwuxian.com/post/materialedittext)
#### [源码地址](https://github.com/rengwuxian/MaterialEditText)
随着 Material Design 的到来， AppCompat v21 中也提供了 Material Design 的控件外观支持，其中包括 EditText 。但 AppCompat 中的 EditText 实在有点难用，因为它是通过 colorAccent 来自动为控件着色的，并没有提供设置颜色的api，因此需要通过为控件定制theme的方式来实现自定义控件颜色。 另外，除了外观上的变化， AppCompat 没有提供任何[ Google Material Design Spec ](http://www.google.com/design/spec/components/text-fields.html)中提到的特性。于是作者便做了这个库： MaterialEditText 。
效果和TextInputLayout+EditText看起来很像，但是这个三方控件多了很多可以定制的属性。
###  2 MaterialRippleLayout
#### 作者  balysv
#### [源码地址](https://github.com/balysv/material-ripple) 
用这个三方控件包裹着的控件点击时会有水波纹的效果。
效果图
![这里写图片描述](https://camo.githubusercontent.com/a39897ad0553f7c3e75fc9663af89afbab8c49d2/68747470733a2f2f7261772e6769746875622e636f6d2f62616c7973762f6d6174657269616c2d726970706c652f6d61737465722f6172742f64656d6f2e676966)
自定义属性如下：

```
app:mrl_rippleOverlay="true"              // if true, ripple is drawn in foreground; false - background

app:mrl_rippleColor="#ff0000"             // color of ripple

app:mrl_rippleAlpha="0.1"                 // alpha of ripple

app:mrl_rippleDimension="10dp"            // radius of hover and starting ripple

app:mrl_rippleHover="true"                // if true, a hover effect is drawn when view is touched

app:mrl_rippleRoundedCorners="10dp"       // radius of corners of ripples. Note: it uses software rendering pipeline for API 17 and below

app:mrl_rippleInAdapter="true"            // if true, MaterialRippleLayout will optimize for use in AdapterViews

app:mrl_rippleDuration="350"              // duration of ripple animation

app:mrl_rippleFadeDuration="75"           // duration of fade out effect on ripple

app:mrl_rippleDelayClick="true"           // if true, delays calls to OnClickListeners until ripple effect ends

app:mrl_rippleBackground="#FFFFFF"        // background under ripple drawable; used with rippleOverlay="false"

app:mrl_ripplePersistent="true"           // if true, ripple background color persists after animation, until setRadius(0) is called
```
使用例子：

```
<com.balysv.materialripple.MaterialRippleLayout
    android:id="@+id/ripple"
    android:layout_width="match_parent"
    android:layout_height="wrap_content">

    <Button
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_gravity="center"
        android:text="Button inside a ripple"/>

</com.balysv.materialripple.MaterialRippleLayout>
```
