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
> ContentImpl.ApplicationContentResolver中
> 由mMainThread.acquireProvider(context,String,userID,stable)生成

##ContentResolver和ContentProvider

##ContactsProvider2
> insertInTransaction(Uri,ContentValues)
> swtich(uri)
> insertRawContact
> 

##ContactsDatabaseHelper

##ProfileProvider

## ContactLocaleUtils
> getBucketIndex(name)
> getBucketLabel(index)

##两个关键的key
> phonebook_label_alt
> phonebook_bucket_alt
> sort_key_alt

##Bucket
> 每个对象就是一个字符
> label 字符的实际内容
> displayIndex 在所有bucket中的位置

##AlphabeticIndex
> 实现了Interable借口,有iterator()函数
> 里面可以存放所有语言的Bucket
> bucketList/immutableVisibleList中存放所有的Bucket
> bucketList/ 中文中是51个/ 第一遍的缺少ijk等字母
> immutableVisibleList/中文28个
> ##内部类 ImmutableIndex 正真含有Bucket的对象
> AlphabeticIndex.buildImmutableIndex()返回每个语言的字符(日文12个,前缀和后缀)
> 