## Qalarm

Qalarm 是一个专注于实时监控的业务监控报警系统，能快速发现并帮助定位线上突发故障,你值得拥有。通过在程序异常处埋点[Qalarm数据格式]，输出到文件系统，再使用flume、kafka等日志收集工具把数据收集到中心节点进行报警、统计、图表展示等。能做到线上问题秒级发现，帮助应用快速定位故障。

总结实践经验，我们发现大多数线上异常都是由于调用外部模块引发，如访问redis，mysql等存储，调用第三方应用服务，还有少量的程序内部错误，所以Qalarm把异常数据分四个维度：项目、模块、错误类型、环境，环境维度是为了区分sit、test、prod的报警。


能解决的问题：

1、线上故障实时发现并告警；
2、报错信息聚合，全局决策；
3、灵活报警阈值和策略，避免误报；
4、直观图表反映实时线上情况；

设计原理如下图：
![avatar](http://on-img.com/chart_image/5779fcaae4b08b6f0224e0f9.png)
