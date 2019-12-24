#Installation
https://hbase.apache.org/book.html#quickstart

##config hdfs datadir: copy url from hadoop/core-site.xml

#clear old zookeeper data
rm -rf ~/zookeeper_data

#edit $HBASE_HOME/bin/hbase
#http://92072234.wiz03.com/share/s/2i1O8Q1L1k042IDoOy3h7BgH2K4G6J2SoQv42Xc4b01xpCrj

CLASSPATH="${HBASE_CONF_DIR}"

CLASSPATH=${CLASSPATH}:$JAVA_HOME/lib/tools.jar:$HBASE_HOME/lib/*
