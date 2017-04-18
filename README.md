# Fragment嵌套的那些坑

## 其实一些小伙伴遇到的很多嵌套的坑，大部分都是由于对嵌套的栈视图产生混乱，只要理清栈视图关系，做好恢复相关工作以及正确选择是使用getFragmentManager()还是getChildFragmentManager()就可以避免这些问题。

这部分内容是我们感觉Fragment非常难用的一个点，我会在下一篇中，详细介绍使用Fragment嵌套的一些技巧，以及如何清晰分析各个层级的栈视图。

附：startActivityForResult接收返回问题
在support 23.2.0以下的支持库中，对于在嵌套子Fragment的startActivityForResult ()，会发现无论如何都不能在onActivityResult()中接收到返回值，只有最顶层的父Fragment才能接收到，这是一个support v4库的一个BUG，不过在前两天发布的support 23.2.0库中，已经修复了该问题，嵌套的子Fragment也能正常接收到返回数据了!
