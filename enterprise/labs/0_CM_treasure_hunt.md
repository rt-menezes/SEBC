1. What is ubertask optimization?
Ubertask enables small jobs to run in a single JVM sequentially.

2. Where in CM is the Kerberos Security Realm value displayed?
Administration > Security

3. Which CDH service(s) host a property for enabling Kerberos authentication?
Hive, Zookeeper, Hue, Oozie, HDFS, YARN

4. How do you upgrade the CM agents?
The Cloudera Manager Agent is a Cloudera Manager component. The procedures for upgrading Cloudera Manager differ depending on the version of Cloudera Manager that you are upgrading from and whether you installed Cloudera Manager using packages or tarballs. 

5. Give the tsquery statement used to chart Hue's CPU utilization?
SELECT cpu_system_rate + cpu_user_rate WHERE entityName = "hue-HUE_SERVER-591786c5a4358d0013eb3b8ce44cdb11" AND category = ROLE

6. Name all the roles that make up the Hive service
Hive Gateway, Hive Metastore Server and HiveServer 2

7. What steps must be completed before integrating Cloudera Manager with Kerberos?
*Set up a working KDC. Cloudera Manager supports MIT KDC and Active Directory.                        
*The KDC should be configured to have non-zero ticket lifetime and renewal lifetime. CDH will not work properly if tickets are not renewable.                        
*OpenLdap client libraries should be installed on the Cloudera Manager Server host if you want to use Active Directory. Also, Kerberos client libraries should be installed on ALL hosts.                        
*Cloudera Manager needs an account that has permissions to create other accounts in the KDC.
