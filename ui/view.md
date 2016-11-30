#View

##事件分发
> 点击事件的持有对象是MotionEvent, 事件分发的过程就是对MotionEvent事件的分发, 把MotionEvent对象,一次传递给相关的View,就完成了本次的事件分发

##事件分发中的主要方法
###dispathTouchEvent(MotionEvent)
> 用来事件分发,如果事件能够传递给当前的View,那么此方法一定会调用,返回结果受当前View的onTouchEvent和下级View的dispatchTouchEvent方法的影响,表示是否消耗当前的事件

###onInterceptTouchEvent(MotionEvent)
> 在上述方法中调用,用来判断是否拦截某个事件,如果当前View拦截了某人事件,那么在同一个事件传递序列中,此方法不会再次调用,返回结果表示是否拦击当前事件

###onToucheEvent(MotionEvent)
> 在dispatchToucEvent方法中调用,用来处理点击事件,返回结果表示是否消耗当前事件,如果不消耗,则在同一个事件传递序列中,当前View无法再次接收到此事件

##三者之间的关系表述
>     public boolean dispatchTouchEvent(MotionEvent ev){
		boolean consume = false;
		if (onInterceptTouchEvent(ev)) {
			consume = onTouchEvent(ev); 
		} else {
			consume = child.dispatchTouchEvent(ev);
		}
		return consume;
	}
    

