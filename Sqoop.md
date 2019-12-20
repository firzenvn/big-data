# Install
https://www.tutorialspoint.com/sqoop/sqoop_installation.htm

Download and copy the commons-lang-2.6.jar to /usr/local/sqoop/lib

edit $JAVA_HOME/lib/security/java.policy, add to "grant" block to allow permission to run sqoop-import:

permission org.apache.derby.security.SystemPermission "engine", "usederbyinternals";
