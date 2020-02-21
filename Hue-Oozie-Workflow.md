# Manage workflows by Hue user instead of admin user

# Shell action, to prevent permission error, add env variable
<env-var>HADOOP_USER_NAME=${wf:user()}</env-var>
