#android contacts数据分析
>Uri: content://com.android.contacts/data
>[数据结构表分析请点击](http://blog.csdn.net/kafka_88/article/details/50670406)
> contacts 数据表
> ![数据表](http://i.imgur.com/oBt5ByK.png)
> 主要的两个表:
> # data
> ![](http://i.imgur.com/2hcUQna.png)
> # raw_contacts
> ![raw_contatcts](http://i.imgur.com/yxO0Luf.png)

##ContentProvider
> 插入数据执行的方法, 拿到Activity中ContentResolver(),
> getContentResolver().insert(Uri,ContentValues)
> 其真正的实现方法是IContentProvider
> ContentResolver类中有个hide(隐藏) 方法
> public final IContentProvder acquireProvider(Uri)
> 最终调用的其抽象方法,
> protected abstract IContentProvider acquireProvider(Context,String)

#Providers实现方法
> 其实实在