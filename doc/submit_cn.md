## 运行提交参数

[**English Document**](./submit.md)

在XLearning客户端，使用`$XLEARNING_HOME/bin/xl-submit`命令，将作业提交至Yarn集群进行调度执行。提交命令使用说明请见[README运行示例](../README_CN.md)部分，详细提交参数说明如下：

参数名称 | 含义  
---------------- | ---------------  
app-name | 指定作业名称  
app-type | 指定作业类型，默认为XLearning，可根据使用深度学习平台设置为TensorFlow、Caffe、XGBoost等  
input | 输入文件路径，格式为 HDFS路径#本地文件夹名称  
output | 输出文件路径，格式为 HDFS路径#本地文件夹名称  
files | 指定作业执行所需本地文件
cacheArchive | 指定作业执行所需相关HDFS压缩文件  
cacheFile | 指定作业执行所需相关HDFS文件  
launch-cmd | 作业执行命令  
user-path | 用户追加环境变量$PATH  
conf | 设置系统配置  
am-cores | 指定AM申请使用的CPU核数，默认个数为系统配置xlearning.am.cores  
am-memory | 指定AM申请使用的内存大小，默认单位MB，默认大小为系统配置xlearning.am.memory  
ps-num | 指定ps申请数目，默认个数为系统配置xlearning.ps.num  
ps-cores | 指定ps申请的CPU核数，默认个数为系统配置xlearning.ps.cores  
ps-memory | 指定ps申请的内存大小，默认单位为MB，默认大小为系统配置xlearning.ps.memory  
worker-num | 指定worker申请数目，默认个数为系统配置xlearning.worker.num  
worker-cores | 指定worker申请的CPU核数，默认个数为系统配置xlearning.worker.cores  
worker-memory | 指定worker申请内存，默认单位为MB，默认大小为系统配置xlearning.worker.memory  
queue | 指定作业提交队列，默认为系统配置xlearning.app.queue  
priority | 指定作业提交优先级，默认为系统配置xlearning.app.priority对应级别  
board-enable | 是否开启TensorBoard服务，默认为系统配置xlearning.tf.board.enable  
board-index | 指定开启TensorBoard服务的work index，默认为系统配置xlearning.tf.board.worker.index  
board-logdir | TensorBoard日志存放路径，默认为系统配置xlearning.tf.board.log.dir  
board-reloadinterval | TensorBoard数据加载时间间隔，默认为系统配置xlearning.tf.board.reload.interval  
board-historydir | TensorBoard日志HDFS上传路径，默认为系统配置xlearning.tf.board.history.dir
input-strategy | 输入文件加载策略，默认为系统配置xlearning.input.strategy  
inRenameInputFile | 当输入文件加载策略为DOWNLOAD时，设置是否对下载后的文件进行重命名，默认为系统配置xlearning.inputfile.rename  
stream-epoch | 当输入文件加载策略为STREAM时，流式数据读取次数，默认为系统配置xlearning.stream.epoch  
inputformat | 当输入文件加载策略为STREAM时，指定inputformat类，默认为系统配置xlearning.inputformat.class  
inputformat-shuffle | 当输入文件加载策略为STREAM时，指定inputformat输入是否需要shuffle操作，默认为系统配置xlearning.input.stream.shuffle  
output-strategy | 输出文件加载策略，默认为系统配置xlearning.output.strategy  
outputformat | 当输出文件加载模式为STREAM时，指定outputformat类，默认为系统配置xlearning.outputformat.class  

