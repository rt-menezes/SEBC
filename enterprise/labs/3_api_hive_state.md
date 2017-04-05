curl -u admin:admin 'http://10.230.82.86:7180/api/v1/clusters/silas.tailer.cluster/services/hive'
```
{
  "name" : "hive",
  "type" : "HIVE",
  "clusterRef" : {
    "clusterName" : "cluster"
  },
  "serviceUrl" : "http://ip-10-230-82-86.ec2.internal:7180/cmf/serviceRedirect/hive",
  "serviceState" : "STARTED",
  "healthSummary" : "GOOD",
  "healthChecks" : [ {
    "name" : "HIVE_HIVEMETASTORES_HEALTHY",
    "summary" : "GOOD"
  }, {
    "name" : "HIVE_HIVESERVER2S_HEALTHY",
    "summary" : "GOOD"
  } ],
  "configStale" : false
```

curl -X POST -H "Content-Type:application/json" -u admin:'admin' 'http://10.230.82.86:7180/api/v12/clusters/silas.tailer.cluster/services/hive/commands/stop'
```
{
  "id" : 451,
  "name" : "Stop",
  "startTime" : "2017-04-05T14:03:07.493Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }
```

curl -X POST -H "Content-Type:application/json" -u admin:'admin' 'http://10.230.82.86:7180/api/v12/clusters/silas.tailer.cluster/services/hive/commands/start'
```
{
  "id" : 455,
  "name" : "Start",
  "startTime" : "2017-04-05T14:03:52.676Z",
  "active" : true,
  "serviceRef" : {
    "clusterName" : "cluster",
    "serviceName" : "hive"
  }

```