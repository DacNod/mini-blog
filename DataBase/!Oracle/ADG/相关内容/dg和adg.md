**一、ADG主要解决了DG时代读写不能并行的问题**

DG时代的数据同步方式如采用Redo Log的物理方式，则数据库同步数据快、耗用资源低，但存在一个大问题。

Oracle 11G以前的Data Guard物理备份数据库，可以以只读的方式打开数据，但这时日志的数据同步过程就停止了。而如果日志的数据同步处于执行过程中，则数据库就不能打开。**也就是日志读、写两个状态是互相排斥的**。而Active Data Guard则是主要解决这个问题。

