
## Bcl数据格式

  目前我们给客户拷贝BCL数据主要包含各个Lane的数据和配置文件。

  各个Lane的数据解压后，目录格式为： Data/Intensities/BaseCalls/L00*

  配置文件解压后，目录格式分别为：
  InterOp
  RunInfo.xml
  runParameters.xml
  Data/Intensities/s.locs
  运行bcl2fastq时， 软件会自动在当前目录下寻找配置文件，进行数据拆分

