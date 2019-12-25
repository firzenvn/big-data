https://www.tutorialspoint.com/hive/hive_installation.htm

### start mysql instance and config hive metastore hive-site.xml

### start metastore service
bin/hive --service metastore &

### start HiveServer2
$HIVE_HOME/bin/hiveserver2 &
