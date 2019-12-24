# Install
Install sqoop for hadoop from: https://www.tutorialspoint.com/sqoop/sqoop_installation.htm

Download and copy the commons-lang-2.6.jar to /usr/local/sqoop/lib

Add derby.jar to $SQOOP_HOME/lib

edit $JAVA_HOME/lib/security/java.policy, add to "grant" block to allow permission to run sqoop-import:

permission org.apache.derby.security.SystemPermission "engine", "usederbyinternals";

#import example
$SQOOP_HOME/bin/sqoop-import --connect jdbc:mysql://18.140.29.203:3306/adventureworksdw --username root --password root --driver com.mysql.jdbc.Driver \
--table factinternetsales \
--split-by ProductKey \
--target-dir /user/admin/adventureworks/dw/internetsales \
--fields-terminated-by "," \
--hive-import \
--create-hive-table \
--hive-table test.internetsales
