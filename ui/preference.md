#android preference 偏好设置
> 几乎每个app都会有设置, 而且一般设置的条目还会很多很多,你一般是怎么写的呢?
> 刚开始不太了解, 然后就傻傻的一股脑搞了个LinerLayout,里面嵌套好多Layout和View, 各种view啊,有木有.....当时写的就想吐,,能不能找个优雅的写法,,,然而并没有找到
> 然而现在有幸工作中与android framework层有一定的接触,看到系统setting中的优雅写法,毕竟是Google大腿,怎能和我等写法一致
> 什么是preference, preference字面是解释就是偏好的意思, android 手机自带的系统设置除了主界面和一些需要提供隐式跳转的action的功能外的界面是使用activity来实现的, 其他的一律是使用PreferenceFragment实现的
> 使用其实还有个PreferenceActivity这货, 不过,从5.0后,好像就不推荐使用了,而是推荐使用PreferenceFragment这种更加优雅和艺术的方式来实现的
> 在使用过程中,总会遇到不一样的需求,而Android自带的preference的样式,只是类似于ListView的样式,每个item的View都是一个水平的线性布局, 这种东西肯定就不能满足我们自己的需求了, 于是就要拿出Androi的杀手锏了----自定义Preference
> 刚开始也是一脸懵逼, 这货只能显示成水平的布局,这不胡扯么,说好的Androi的最大的优势就是可以自定义呢
> 