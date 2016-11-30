#android
> 1 Android vector Path Data
##android不错的开源资源
>[打开](http://www.open-open.com/lib/view/open1411443332703.html)

##Android默认的资源文件
> sdk/platforms/android-24/data/res
##看了好久的android preference,还是不太明白到底要怎么用
> 不懂就看源码,android源码永远是最好的解释, 这点毋庸置疑,
> 
> 而且提示信息多,

> 从命名规范中大致去猜测是什么意思,

	> 比如View 和ViewGroup的关系,Fragment和PreferenceFragment的关系
	> Activity和FragmentActivity的关系

> 不会就多看源码, 一定要多看, 哪怕英语不好, 看多了你会发现英文变得不错, 其实,对英语阅读能力并不是很大, 会常见的单词, 然后,一个有道词典,一个不错的宽带就好
> 
##android sdk目录结构
* add-ons 
	> google apis map等,里面有doc文件夹,有相关的介绍

* build-tools 
	> 各个版本的build工具都在这个文件夹下
	
* docs
	 >这个文件夹,实际上就是android developers的离线网站,挺好的,可以多看看,英文不好的更要多看了,比如我
* extras 
	> 这个文件夹放的都是一些外部的资源,经常用的supperv4,v
	> 7gridView RecyclerView PreferencV7等等,都在改目录下
	> extras\android\m2repository\com\android\support

* licenses 
	> 看名字应该是存放许可密匙类似的文件的吧,对于开发者没有什么意义
* platforms
	> 这个也是最重要的,没有之一,android所有下载过的版本都在这里面,里面有android.jar 和android 的res文件等,sdk中最重要的,毕竟我们写的代码都是android.jar和android res所提供的
* platform-tools
	> 这个应该不陌生,配置adb命令就是配置的改文件地址,里面有adb.exe等工具
* skins
	> 顾名思义,存放皮肤资源的,当然是模拟器的资源图片了
* sources
	> 开发看的最多的源码了吧, 安装ctrl点进源码看的就是这里的文件,当然是存在的情况,反编译的不算
* temp 
	> 存放各个平台如x86,x64,arm的cup镜像
* tools
	> 这个应该也很重要的了,存放个有辅助开发的工具,ddms draw9patch,hierarchyviewer布局分析,uiautomatorviewer等


##SetupWizardLayout 

##TemplateLayout

##Illustration

#数据库查询

Order by
用途：

指定结果集的排序

语法：

SELECT column-name(s) FROM table-name ORDER BY { order_by_expression [ ASC | DESC ] }
 

解释：

 指定结果集的排序，可以按照ASC(递增方式排序，从最低值到最高值)或者DESC(递减方式排序，从最高值到最低值)的方式进行排序，默认的方式是ASC

## android Preconditions工具类
> 路径: com.android.internal.util
> checkStringNoEmpty(T)
> CheckStringNotEmpty(T,Object)
> 各种检查参数是否正确

## PermissionUtil 权限工具

