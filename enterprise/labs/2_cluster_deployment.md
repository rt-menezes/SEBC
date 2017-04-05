{
  "timestamp" : "2017-04-05T13:39:02.667Z",
  "clusters" : [ {
    "name" : "silas.tailer.cluster",
    "version" : "CDH5",
    "services" : [ {
      "name" : "hive",
      "type" : "HIVE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "HIVEMETASTORE",
          "items" : [ {
            "name" : "hive_metastore_java_heapsize",
            "value" : "1712324608"
          }, {
            "name" : "hive_metastore_server_max_message_size",
            "value" : "171232460"
          } ]
        }, {
          "roleType" : "HIVESERVER2",
          "items" : [ {
            "name" : "hiveserver2_java_heapsize",
            "value" : "1712324608"
          }, {
            "name" : "hiveserver2_spark_driver_memory",
            "value" : "966367641"
          }, {
            "name" : "hiveserver2_spark_executor_cores",
            "value" : "4"
          }, {
            "name" : "hiveserver2_spark_executor_memory",
            "value" : "3432356249"
          }, {
            "name" : "hiveserver2_spark_yarn_driver_memory_overhead",
            "value" : "102"
          }, {
            "name" : "hiveserver2_spark_yarn_executor_memory_overhead",
            "value" : "577"
          } ]
        } ],
        "items" : [ {
          "name" : "hive_metastore_database_host",
          "value" : "ip-10-230-82-86.ec2.internal"
        }, {
          "name" : "hive_metastore_database_password",
          "value" : "hive"
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hive-GATEWAY-0fd28be3b4dc492f049eea4a98198d8f",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "089eec3b-f092-44c9-9f36-909cae651ad8"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-44970eef589b1fcb63cbcacdf2216b57",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "a5d6f5d8-251a-402f-ab26-76f68c9aeb07"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-591786c5a4358d0013eb3b8ce44cdb11",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "46d1a6f0-038b-45af-8384-ca7b66d67c66"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-924553c3dcfafa91329af66926cf9d83",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "cac5ad98-ea5d-4a43-b490-724aa6292266"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-ef30eaf9d75c32c16a37b6fb5af76960",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "58b485cd-ab5f-4ef0-9624-d1d44a33331d"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-HIVEMETASTORE-ef30eaf9d75c32c16a37b6fb5af76960",
        "type" : "HIVEMETASTORE",
        "hostRef" : {
          "hostId" : "58b485cd-ab5f-4ef0-9624-d1d44a33331d"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "eb8po9mla8zzs389iagrm6yt7"
          } ]
        }
      }, {
        "name" : "hive-HIVESERVER2-ef30eaf9d75c32c16a37b6fb5af76960",
        "type" : "HIVESERVER2",
        "hostRef" : {
          "hostId" : "58b485cd-ab5f-4ef0-9624-d1d44a33331d"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "40cmzh8lyzzhtienpftbxzehy"
          } ]
        }
      } ],
      "displayName" : "Hive"
    }, {
      "name" : "zookeeper",
      "type" : "ZOOKEEPER",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "SERVER",
          "items" : [ {
            "name" : "zookeeper_server_java_heapsize",
            "value" : "895483904"
          } ]
        } ],
        "items" : [ ]
      },
      "roles" : [ {
        "name" : "zookeeper-SERVER-0fd28be3b4dc492f049eea4a98198d8f",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "089eec3b-f092-44c9-9f36-909cae651ad8"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "9dza7wzjal7m2sepz5pzy8vp3"
          }, {
            "name" : "serverId",
            "value" : "3"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-591786c5a4358d0013eb3b8ce44cdb11",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "46d1a6f0-038b-45af-8384-ca7b66d67c66"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "b50dctk7mj77uskvb36fqfphn"
          }, {
            "name" : "serverId",
            "value" : "2"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-ef30eaf9d75c32c16a37b6fb5af76960",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "58b485cd-ab5f-4ef0-9624-d1d44a33331d"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "x43j5uw80j421ieaudvq21yp"
          }, {
            "name" : "serverId",
            "value" : "1"
          } ]
        }
      } ],
      "displayName" : "ZooKeeper"
    }, {
      "name" : "hue",
      "type" : "HUE",
      "config" : {
        "roleTypeConfigs" : [ ],
        "items" : [ {
          "name" : "database_host",
          "value" : "ip-10-230-82-86.ec2.internal"
        }, {
          "name" : "database_password",
          "value" : "hue"
        }, {
          "name" : "database_type",
          "value" : "mysql"
        }, {
          "name" : "hive_service",
          "value" : "hive"
        }, {
          "name" : "hue_webhdfs",
          "value" : "hdfs-NAMENODE-591786c5a4358d0013eb3b8ce44cdb11"
        }, {
          "name" : "oozie_service",
          "value" : "oozie"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hue-HUE_SERVER-591786c5a4358d0013eb3b8ce44cdb11",
        "type" : "HUE_SERVER",
        "hostRef" : {
          "hostId" : "46d1a6f0-038b-45af-8384-ca7b66d67c66"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "9d9rovv002bp214m7pph5qws9"
          }, {
            "name" : "secret_key",
            "value" : "m5RuWUvlDzMCiLRfbp435aHDm5gxu3"
          } ]
        }
      } ],
      "displayName" : "Hue"
    }, {
      "name" : "oozie",
      "type" : "OOZIE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "OOZIE_SERVER",
          "items" : [ {
            "name" : "oozie_database_host",
            "value" : "ip-10-230-82-86.ec2.internal"
          }, {
            "name" : "oozie_database_password",
            "value" : "oozie"
          }, {
            "name" : "oozie_database_type",
            "value" : "mysql"
          }, {
            "name" : "oozie_database_user",
            "value" : "oozie"
          } ]
        } ],
        "items" : [ {
          "name" : "hive_service",
          "value" : "hive"
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "oozie-OOZIE_SERVER-ef30eaf9d75c32c16a37b6fb5af76960",
        "type" : "OOZIE_SERVER",
        "hostRef" : {
          "hostId" : "58b485cd-ab5f-4ef0-9624-d1d44a33331d"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "422x1jmi5p2t8qv1sv05c63g5"
          } ]
        }
      } ],
      "displayName" : "Oozie"
    }, {
      "name" : "yarn",
      "type" : "YARN",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "GATEWAY",
          "items" : [ {
            "name" : "mapred_reduce_tasks",
            "value" : "6"
          }, {
            "name" : "mapred_submit_replication",
            "value" : "1"
          } ]
        }, {
          "roleType" : "NODEMANAGER",
          "items" : [ {
            "name" : "rm_cpu_shares",
            "value" : "1800"
          }, {
            "name" : "rm_io_weight",
            "value" : "900"
          }, {
            "name" : "yarn_nodemanager_heartbeat_interval_ms",
            "value" : "100"
          }, {
            "name" : "yarn_nodemanager_local_dirs",
            "value" : "/data/yarn/nm"
          }, {
            "name" : "yarn_nodemanager_log_dirs",
            "value" : "/yarn/container-logs,/data/yarn/container-logs"
          }, {
            "name" : "yarn_nodemanager_resource_cpu_vcores",
            "value" : "3"
          }, {
            "name" : "yarn_nodemanager_resource_memory_mb",
            "value" : "4938"
          } ]
        }, {
          "roleType" : "RESOURCEMANAGER",
          "items" : [ {
            "name" : "yarn_scheduler_maximum_allocation_mb",
            "value" : "4938"
          }, {
            "name" : "yarn_scheduler_maximum_allocation_vcores",
            "value" : "3"
          } ]
        } ],
        "items" : [ {
          "name" : "hdfs_service",
          "value" : "hdfs"
        }, {
          "name" : "rm_dirty",
          "value" : "false"
        }, {
          "name" : "rm_last_allocation_percentage",
          "value" : "90"
        }, {
          "name" : "yarn_service_cgroups",
          "value" : "false"
        }, {
          "name" : "yarn_service_lce_always",
          "value" : "false"
        }, {
          "name" : "zk_authorization_secret_key",
          "value" : "RVS4Tf1jhnzzhRg5V0l7qKJzgX4D5M"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "yarn-JOBHISTORY-ef30eaf9d75c32c16a37b6fb5af76960",
        "type" : "JOBHISTORY",
        "hostRef" : {
          "hostId" : "58b485cd-ab5f-4ef0-9624-d1d44a33331d"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "aahk31kshg8ibvy60ns0baek9"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-0fd28be3b4dc492f049eea4a98198d8f",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "089eec3b-f092-44c9-9f36-909cae651ad8"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "5aphl2k3p7xjdf2yzqta6i4a9"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-44970eef589b1fcb63cbcacdf2216b57",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "a5d6f5d8-251a-402f-ab26-76f68c9aeb07"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "1p8lov11p82xg99o4atlex6dr"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-924553c3dcfafa91329af66926cf9d83",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "cac5ad98-ea5d-4a43-b490-724aa6292266"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "5ne23bjuhubpm8oonevnl7ju6"
          } ]
        }
      }, {
        "name" : "yarn-RESOURCEMANAGER-ef30eaf9d75c32c16a37b6fb5af76960",
        "type" : "RESOURCEMANAGER",
        "hostRef" : {
          "hostId" : "58b485cd-ab5f-4ef0-9624-d1d44a33331d"
        },
        "config" : {
          "items" : [ {
            "name" : "rm_id",
            "value" : "81"
          }, {
            "name" : "role_jceks_password",
            "value" : "dn4mco7a3yp3n32kbvs8ayrin"
          } ]
        }
      } ],
      "displayName" : "YARN (MR2 Included)"
    }, {
      "name" : "hdfs",
      "type" : "HDFS",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "BALANCER",
          "items" : [ {
            "name" : "balancer_java_heapsize",
            "value" : "895483904"
          } ]
        }, {
          "roleType" : "DATANODE",
          "items" : [ {
            "name" : "datanode_java_heapsize",
            "value" : "1073741824"
          }, {
            "name" : "dfs_data_dir_list",
            "value" : "/data/dfs/dn"
          }, {
            "name" : "dfs_datanode_du_reserved",
            "value" : "4293264998"
          }, {
            "name" : "dfs_datanode_max_locked_memory",
            "value" : "4294967296"
          }, {
            "name" : "rm_cpu_shares",
            "value" : "200"
          }, {
            "name" : "rm_io_weight",
            "value" : "100"
          } ]
        }, {
          "roleType" : "GATEWAY",
          "items" : [ {
            "name" : "dfs_client_use_trash",
            "value" : "true"
          } ]
        }, {
          "roleType" : "JOURNALNODE",
          "items" : [ {
            "name" : "dfs_journalnode_edits_dir",
            "value" : "/data/dfs/jn"
          } ]
        }, {
          "roleType" : "NAMENODE",
          "items" : [ {
            "name" : "dfs_name_dir_list",
            "value" : "/data/dfs/nn"
          }, {
            "name" : "dfs_namenode_servicerpc_address",
            "value" : "8022"
          } ]
        }, {
          "roleType" : "SECONDARYNAMENODE",
          "items" : [ {
            "name" : "fs_checkpoint_dir_list",
            "value" : "/data/dfs/snn"
          }, {
            "name" : "secondary_namenode_java_heapsize",
            "value" : "895483904"
          } ]
        } ],
        "items" : [ {
          "name" : "dfs_ha_fencing_cloudera_manager_secret_key",
          "value" : "vBGppyW2ucaxzk1WCefrXCVl7iCbxp"
        }, {
          "name" : "dfs_ha_fencing_methods",
          "value" : "shell(true)"
        }, {
          "name" : "fc_authorization_secret_key",
          "value" : "XHEc3bCzdzRibtPCVzcKXh0KUNb4Rs"
        }, {
          "name" : "http_auth_signature_secret",
          "value" : "2Qb4Xs0CyQiCPJAYB3tP5M1NY4nDYR"
        }, {
          "name" : "rm_dirty",
          "value" : "false"
        }, {
          "name" : "rm_last_allocation_percentage",
          "value" : "10"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hdfs-BALANCER-591786c5a4358d0013eb3b8ce44cdb11",
        "type" : "BALANCER",
        "hostRef" : {
          "hostId" : "46d1a6f0-038b-45af-8384-ca7b66d67c66"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-DATANODE-0fd28be3b4dc492f049eea4a98198d8f",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "089eec3b-f092-44c9-9f36-909cae651ad8"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "7gpas05renakrmofpqqoi6s6i"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-44970eef589b1fcb63cbcacdf2216b57",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "a5d6f5d8-251a-402f-ab26-76f68c9aeb07"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "dmya9u5aj7o8ou0pfohir9wce"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-924553c3dcfafa91329af66926cf9d83",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "cac5ad98-ea5d-4a43-b490-724aa6292266"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "2868ftv9jgb5rfhsybdlmpn92"
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-591786c5a4358d0013eb3b8ce44cdb11",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "46d1a6f0-038b-45af-8384-ca7b66d67c66"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "4hpb47edk8j63l1iv160uiamp"
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-ef30eaf9d75c32c16a37b6fb5af76960",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "58b485cd-ab5f-4ef0-9624-d1d44a33331d"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "6x3zmt2s16x0s32voa46lrypl"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-0fd28be3b4dc492f049eea4a98198d8f",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "089eec3b-f092-44c9-9f36-909cae651ad8"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "c5r72o3dn5bokc2uduamj6vkk"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-591786c5a4358d0013eb3b8ce44cdb11",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "46d1a6f0-038b-45af-8384-ca7b66d67c66"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "2lq8braxe0kee74fzsyl1uk67"
          } ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-ef30eaf9d75c32c16a37b6fb5af76960",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "58b485cd-ab5f-4ef0-9624-d1d44a33331d"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "2muj8ai9k4z6481uxcoc9f0bz"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-591786c5a4358d0013eb3b8ce44cdb11",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "46d1a6f0-038b-45af-8384-ca7b66d67c66"
        },
        "config" : {
          "items" : [ {
            "name" : "autofailover_enabled",
            "value" : "true"
          }, {
            "name" : "dfs_federation_namenode_nameservice",
            "value" : "nameservice1"
          }, {
            "name" : "dfs_namenode_quorum_journal_name",
            "value" : "nameservice1"
          }, {
            "name" : "namenode_id",
            "value" : "83"
          }, {
            "name" : "role_jceks_password",
            "value" : "aedkaiv2odqprxzscv9nk4brt"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-ef30eaf9d75c32c16a37b6fb5af76960",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "58b485cd-ab5f-4ef0-9624-d1d44a33331d"
        },
        "config" : {
          "items" : [ {
            "name" : "autofailover_enabled",
            "value" : "true"
          }, {
            "name" : "dfs_federation_namenode_nameservice",
            "value" : "nameservice1"
          }, {
            "name" : "dfs_namenode_quorum_journal_name",
            "value" : "nameservice1"
          }, {
            "name" : "namenode_id",
            "value" : "88"
          }, {
            "name" : "role_jceks_password",
            "value" : "5t6y04cshf19tr51f6aqnzhjr"
          } ]
        }
      } ],
      "displayName" : "HDFS"
    } ]
  } ],
  "hosts" : [ {
    "hostId" : "58b485cd-ab5f-4ef0-9624-d1d44a33331d",
    "ipAddress" : "10.146.179.98",
    "hostname" : "ip-10-146-179-98.ec2.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "089eec3b-f092-44c9-9f36-909cae651ad8",
    "ipAddress" : "10.203.227.13",
    "hostname" : "ip-10-203-227-13.ec2.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "46d1a6f0-038b-45af-8384-ca7b66d67c66",
    "ipAddress" : "10.230.82.86",
    "hostname" : "ip-10-230-82-86.ec2.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ {
        "name" : "memory_overcommit_threshold",
        "value" : "0.5"
      } ]
    }
  }, {
    "hostId" : "a5d6f5d8-251a-402f-ab26-76f68c9aeb07",
    "ipAddress" : "10.61.160.149",
    "hostname" : "ip-10-61-160-149.ec2.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "cac5ad98-ea5d-4a43-b490-724aa6292266",
    "ipAddress" : "10.95.161.53",
    "hostname" : "ip-10-95-161-53.ec2.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  } ],
  "users" : [ {
    "name" : "__cloudera_internal_user__a2e77c1a-93ad-4c7c-8fad-96808ad4267f",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "b9e4506b03326966f723c909ffbe1b49d70fc43c5981537495e71b39bf8f4ff0",
    "pwSalt" : 5942224656270468868,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-ACTIVITYMONITOR-591786c5a4358d0013eb3b8ce44cdb11",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "be445cbd1a5acf7e6ab10bc887bd5fb17fee0b244ce0cc68c849463238be9c60",
    "pwSalt" : 7889933450026480558,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-EVENTSERVER-591786c5a4358d0013eb3b8ce44cdb11",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "0121ba97b799c4d4b40243055925fbd53c1b05ee0abf9cf92fb95fa530aac30c",
    "pwSalt" : 5523722280730016636,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-HOSTMONITOR-591786c5a4358d0013eb3b8ce44cdb11",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "136e15a68f90e7e605a097e60034711187f0f87e2c3ea6e03dd92652584f143b",
    "pwSalt" : -4061398958210451345,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-REPORTSMANAGER-591786c5a4358d0013eb3b8ce44cdb11",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "374165315168202df15aead00abedb303a85464f48df67d473cac26e909c046e",
    "pwSalt" : -2716328672945565679,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-SERVICEMONITOR-591786c5a4358d0013eb3b8ce44cdb11",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "a937f32934f246b128db771c16f51130e844698bc4dff60c52ddd1ec6e522ed6",
    "pwSalt" : -3947413046533468923,
    "pwLogin" : true
  }, {
    "name" : "admin",
    "roles" : [ "ROLE_LIMITED" ],
    "pwHash" : "ea296b39868fd60c6ee964d11136d78f628def903aecd2cd8cc90642154e0970",
    "pwSalt" : 1421690873962718090,
    "pwLogin" : true
  }, {
    "name" : "minotaur",
    "roles" : [ "ROLE_CONFIGURATOR" ],
    "pwHash" : "f7173cce82a8f51e1a306f98f11cbb3a1c133c5bf269444cc5345a401d627c78",
    "pwSalt" : 4174012066774862876,
    "pwLogin" : true
  }, {
    "name" : "stailer",
    "roles" : [ "ROLE_ADMIN" ],
    "pwHash" : "ce2e56f50b348bdcc896eec29111a7739f10c4860200cdb3b236c583d2878492",
    "pwSalt" : 8838432418776203098,
    "pwLogin" : true
  } ],
  "versionInfo" : {
    "version" : "5.10.1",
    "buildUser" : "jenkins",
    "buildTimestamp" : "20170319-2001",
    "gitHash" : "f226435f6fa5f545543c00245900ae43bea7a29c",
    "snapshot" : false
  },
  "managementService" : {
    "name" : "mgmt",
    "type" : "MGMT",
    "config" : {
      "roleTypeConfigs" : [ {
        "roleType" : "ACTIVITYMONITOR",
        "items" : [ {
          "name" : "firehose_database_host",
          "value" : "ip-10-230-82-86.ec2.internal"
        }, {
          "name" : "firehose_database_name",
          "value" : "amon"
        }, {
          "name" : "firehose_database_password",
          "value" : "amon"
        }, {
          "name" : "firehose_database_user",
          "value" : "amon"
        }, {
          "name" : "firehose_heapsize",
          "value" : "895483904"
        } ]
      }, {
        "roleType" : "EVENTSERVER",
        "items" : [ {
          "name" : "event_server_heapsize",
          "value" : "895483904"
        } ]
      }, {
        "roleType" : "HOSTMONITOR",
        "items" : [ {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "1614807040"
        } ]
      }, {
        "roleType" : "REPORTSMANAGER",
        "items" : [ {
          "name" : "headlamp_database_host",
          "value" : "ip-10-230-82-86.ec2.internal"
        }, {
          "name" : "headlamp_database_name",
          "value" : "rman"
        }, {
          "name" : "headlamp_database_password",
          "value" : "rman"
        }, {
          "name" : "headlamp_database_user",
          "value" : "rman"
        }, {
          "name" : "headlamp_heapsize",
          "value" : "895483904"
        } ]
      }, {
        "roleType" : "SERVICEMONITOR",
        "items" : [ {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "1614807040"
        } ]
      } ],
      "items" : [ ]
    },
    "roles" : [ {
      "name" : "mgmt-ACTIVITYMONITOR-591786c5a4358d0013eb3b8ce44cdb11",
      "type" : "ACTIVITYMONITOR",
      "hostRef" : {
        "hostId" : "46d1a6f0-038b-45af-8384-ca7b66d67c66"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "dn0rcc0a98vt2x2gzpsrosdai"
        } ]
      }
    }, {
      "name" : "mgmt-ALERTPUBLISHER-591786c5a4358d0013eb3b8ce44cdb11",
      "type" : "ALERTPUBLISHER",
      "hostRef" : {
        "hostId" : "46d1a6f0-038b-45af-8384-ca7b66d67c66"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "4l6m0ojziirxstdbu3p5ph6oi"
        } ]
      }
    }, {
      "name" : "mgmt-EVENTSERVER-591786c5a4358d0013eb3b8ce44cdb11",
      "type" : "EVENTSERVER",
      "hostRef" : {
        "hostId" : "46d1a6f0-038b-45af-8384-ca7b66d67c66"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "9vgoncsl8krghg2zaekv92nhh"
        } ]
      }
    }, {
      "name" : "mgmt-HOSTMONITOR-591786c5a4358d0013eb3b8ce44cdb11",
      "type" : "HOSTMONITOR",
      "hostRef" : {
        "hostId" : "46d1a6f0-038b-45af-8384-ca7b66d67c66"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "athep4tlmx4mpvqp7n17dhwkz"
        } ]
      }
    }, {
      "name" : "mgmt-REPORTSMANAGER-591786c5a4358d0013eb3b8ce44cdb11",
      "type" : "REPORTSMANAGER",
      "hostRef" : {
        "hostId" : "46d1a6f0-038b-45af-8384-ca7b66d67c66"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "3vjsjy1sjtoq8xgnh1b7uw0c"
        } ]
      }
    }, {
      "name" : "mgmt-SERVICEMONITOR-591786c5a4358d0013eb3b8ce44cdb11",
      "type" : "SERVICEMONITOR",
      "hostRef" : {
        "hostId" : "46d1a6f0-038b-45af-8384-ca7b66d67c66"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "6dqjuceoq3205k8ivutr5f1vz"
        } ]
      }
    } ],
    "displayName" : "Cloudera Management Service"
  },
  "managerSettings" : {
    "items" : [ {
      "name" : "CLUSTER_STATS_START",
      "value" : "10/22/2012 9:40"
    }, {
      "name" : "PUBLIC_CLOUD_STATUS",
      "value" : "ON_PUBLIC_CLOUD"
    }, {
      "name" : "REMOTE_PARCEL_REPO_URLS",
      "value" : "http://10.230.82.86/parcels"
    } ]
  }
}