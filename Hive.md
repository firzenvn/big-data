https://www.tutorialspoint.com/hive/hive_installation.htm

### start mysql instance and config hive metastore hive-site.xml

#hive 3
  $ $HIVE_HOME/bin/schematool -dbType <db type> -initSchema


### start metastore service
$HIVE_HOME/bin/hive --service metastore &

### start HiveServer2
$HIVE_HOME/bin/hiveserver2 &
