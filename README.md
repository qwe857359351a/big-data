# big-data
在Windows 10上安装Hadoop 3.2.1时，尝试格式化HDFS namnode时可能会遇到以下错误：
java.lang.UnsupportedOperationException
        java.nio.file.Files.setPosixFilePermissions（Files.java:2044）
        org.apache.hadoop.hdfs.server.common.Storage $ StorageDirectory.clearDirectory（Storage.java:452）
        org.apache.hadoop.hdfs.server.namenode.NNStorage.format（NNStorage.java:591）
        org.apache.hadoop.hdfs.server.namenode.NNStorage.format（NNStorage.java:613）
        org.apache.hadoop.hdfs.server.namenode.FSImage.format（FSImage.java:188）
        org.apache.hadoop.hdfs.server.namenode.NameNode.format（NameNode.java:1206）
        org.apache.hadoop.hdfs.server.namenode.NameNode.createNameNode（NameNode.java:1649）
        org.apache.hadoop.hdfs.server.namenode.NameNode.main（NameNode.java:1759）
解决方法：
下载hadoop-hdfs-3.2.1.jar，
将文件夹％HADOOP_HOME％\share\hadoop\hdfs中的文件名hadoop-hdfs-3.2.1.jar重命名为hadoop-hdfs-3.2.1.bk。
将下载的hadoop-hdfs-3.2.1.jar复制到文件夹％HADOOP_HOME％\share\hadoop\hdfs
