https://www.tutorialspoint.com/hive/hive_installation.htm

### start mysql instance and config hive metastore hive-site.xml

#hive 3
  $ $HIVE_HOME/bin/schematool -dbType <db type> -initSchema


### start metastore service
$HIVE_HOME/bin/hive --service metastore &

### start HiveServer2
$HIVE_HOME/bin/hiveserver2 &

### backup hive database to s3
s3-dist-cp --src=/user/hive/warehouse --dest s3://magestore-retail-assistant/user/hive/warehouse

### restore hive database from s3
CREATE TABLE KYLIN_ACCOUNT
(
ACCOUNT_ID bigint
,ACCOUNT_BUYER_LEVEL int COMMENT 'Account Buyer Level'
,ACCOUNT_SELLER_LEVEL int COMMENT 'Account Seller Level'
,ACCOUNT_COUNTRY string COMMENT 'Account Country'
,ACCOUNT_CONTACT string COMMENT 'Account Contact Info'
)
ROW FORMAT DELIMITED FIELDS TERMINATED BY ','
STORED AS TEXTFILE
LOCATION 's3://magestore-retail-assistant/user/hive/warehouse/kylin_account/';
