# MINER 子命令

### 用法

```
xfsgo miner [options] <sub-command>
```

### 子命令列表

*   **start \[--workers \<num>]**

    启动工作线程，开始封装区块。使用 workers 选项可以指定启动的工作线程数量
*   **status**

    查询服务状态以及参数指标
*   **setworkers \<number>**

    设置工作线程的数量，该值可以在运行过程中动态调整
*   **setgasprice \<value>**

    设置 “矿工” 接受的最低交易燃烧费价格
*   **stop**

    停止所有的工作线程
