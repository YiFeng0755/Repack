命令行重打包源码



2018/1/11修改：

文件替换：

1. 使用sdk25的android.jar替换旧的
2. 使用apktool2.3.0替换2.0.2

代码修改：

1. 针对不同引擎版本，增加配置文件规则config.py:: self.__fileMap
2. 针对最新的apktool参数frame-path要求目录存在，反编译前确保目录存在
3. 命令执行统一为:   s = subprocess.Popen(cmd, shell=True)