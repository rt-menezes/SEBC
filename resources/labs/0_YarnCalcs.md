# OS
Will have only one vcore because it will not be running any kind of heavy load process.

# NodeManager
32 GB so it can match the number of memory in DN, the same goes for the number of vcores

# DataNode
The capacity of memory that manages metadata for block allocation.

# Impalad
May run heavy SQL queries

# YARM RM Properties
yarn.scheduler.maximum-allocation-vcores is set to 6 so that one container may run with the maximum number os cores available

