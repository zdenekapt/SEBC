# /api/v2/cm/deployment

[centos@ip-172-31-37-70 ~]$ curl -u admin:admin 'http://localhost:7180/api/v2/cm/deployment'
{
  "timestamp" : "2019-02-15T12:51:54.171Z",
  "clusters" : [ {
    "name" : "zdenekapt",
    "version" : "CDH5",
    "services" : [ {
      "name" : "hive",
      "type" : "HIVE",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "HIVEMETASTORE",
          "items" : [ {
            "name" : "hive_metastore_java_heapsize",
            "value" : "1099956224"
          }, {
            "name" : "hive_metastore_server_max_message_size",
            "value" : "109995622"
          } ]
        }, {
          "roleType" : "HIVESERVER2",
          "items" : [ {
            "name" : "hiveserver2_java_heapsize",
            "value" : "860880896"
          }, {
            "name" : "hiveserver2_spark_driver_memory",
            "value" : "966367641"
          }, {
            "name" : "hiveserver2_spark_executor_cores",
            "value" : "4"
          }, {
            "name" : "hiveserver2_spark_executor_memory",
            "value" : "951897292"
          }, {
            "name" : "hiveserver2_spark_yarn_driver_memory_overhead",
            "value" : "102"
          }, {
            "name" : "hiveserver2_spark_yarn_executor_memory_overhead",
            "value" : "160"
          } ]
        } ],
        "items" : [ {
          "name" : "hive_metastore_database_host",
          "value" : "ip-172-31-37-70.eu-central-1.compute.internal"
        }, {
          "name" : "hive_metastore_database_name",
          "value" : "hive"
        }, {
          "name" : "hive_metastore_database_password",
          "value" : "cloudera"
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hive-GATEWAY-720ff148adb6e50839b928b7fe7f42cc",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "2f708c23-ecee-46ca-93a8-e79969f1ecb2"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-7c563c0a16a29c7aefa51eb19467b5b9",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "2bd6c763-8faf-4ef1-aa12-43e5ea4c5e0c"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-b3b2dbfd3af0436695f16d3e77d22da3",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "1770e495-5e30-4f8a-8566-f0ae81b97750"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-bc148c046060d290126bd892cf268ba2",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "69c4db24-91ab-4ea0-893b-e7c8fb2f9ee6"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-GATEWAY-cfaedf65fe631a3797a87a24f9d677e8",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "f1d86679-d68f-4b62-8137-7be90cb3ddf5"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-HIVEMETASTORE-cfaedf65fe631a3797a87a24f9d677e8",
        "type" : "HIVEMETASTORE",
        "hostRef" : {
          "hostId" : "f1d86679-d68f-4b62-8137-7be90cb3ddf5"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "30wz89a9b3prcb0dmo9wnmctx"
          } ]
        }
      }, {
        "name" : "hive-HIVESERVER2-7c563c0a16a29c7aefa51eb19467b5b9",
        "type" : "HIVESERVER2",
        "hostRef" : {
          "hostId" : "2bd6c763-8faf-4ef1-aa12-43e5ea4c5e0c"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "fp379pqwzdet0bgghxskt71a"
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
            "value" : "860880896"
          } ]
        } ],
        "items" : [ ]
      },
      "roles" : [ {
        "name" : "zookeeper-SERVER-720ff148adb6e50839b928b7fe7f42cc",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "2f708c23-ecee-46ca-93a8-e79969f1ecb2"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "t6ivrs4vatt3qjlolw8981cl"
          }, {
            "name" : "serverId",
            "value" : "3"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-7c563c0a16a29c7aefa51eb19467b5b9",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "2bd6c763-8faf-4ef1-aa12-43e5ea4c5e0c"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "cu8l260nxxqxrrx37uap42nf1"
          }, {
            "name" : "serverId",
            "value" : "2"
          } ]
        }
      }, {
        "name" : "zookeeper-SERVER-cfaedf65fe631a3797a87a24f9d677e8",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "f1d86679-d68f-4b62-8137-7be90cb3ddf5"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "cv7c320qe6w0nkq97a61b7mdg"
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
          "value" : "ip-172-31-37-70.eu-central-1.compute.internal"
        }, {
          "name" : "database_password",
          "value" : "cloudera"
        }, {
          "name" : "database_type",
          "value" : "mysql"
        }, {
          "name" : "hive_service",
          "value" : "hive"
        }, {
          "name" : "hue_webhdfs",
          "value" : "hdfs-NAMENODE-cfaedf65fe631a3797a87a24f9d677e8"
        }, {
          "name" : "oozie_service",
          "value" : "oozie"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hue-HUE_LOAD_BALANCER-7c563c0a16a29c7aefa51eb19467b5b9",
        "type" : "HUE_LOAD_BALANCER",
        "hostRef" : {
          "hostId" : "2bd6c763-8faf-4ef1-aa12-43e5ea4c5e0c"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "54j8wttldomyrcat1xds5e55y"
          } ]
        }
      }, {
        "name" : "hue-HUE_SERVER-cfaedf65fe631a3797a87a24f9d677e8",
        "type" : "HUE_SERVER",
        "hostRef" : {
          "hostId" : "f1d86679-d68f-4b62-8137-7be90cb3ddf5"
        },
        "config" : {
          "items" : [ {
            "name" : "navmetadataserver_cmdb_password",
            "value" : "919ef545-0ab2-481f-a5c8-dd2a0e741c68"
          }, {
            "name" : "role_jceks_password",
            "value" : "8szr4p5n4prc89ty9ddmroz1m"
          }, {
            "name" : "secret_key",
            "value" : "RL0THXqSICWTKk5N9xbyMOmBcE4n8t"
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
            "value" : "ip-172-31-37-70.eu-central-1.compute.internal"
          }, {
            "name" : "oozie_database_password",
            "value" : "cloudera"
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
        "name" : "oozie-OOZIE_SERVER-cfaedf65fe631a3797a87a24f9d677e8",
        "type" : "OOZIE_SERVER",
        "hostRef" : {
          "hostId" : "f1d86679-d68f-4b62-8137-7be90cb3ddf5"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "blvsl91ciz6qc34j6jnj9nie1"
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
            "value" : "8"
          }, {
            "name" : "mapred_submit_replication",
            "value" : "3"
          } ]
        }, {
          "roleType" : "JOBHISTORY",
          "items" : [ {
            "name" : "mr2_jobhistory_java_heapsize",
            "value" : "860880896"
          } ]
        }, {
          "roleType" : "NODEMANAGER",
          "items" : [ {
            "name" : "yarn_nodemanager_heartbeat_interval_ms",
            "value" : "100"
          }, {
            "name" : "yarn_nodemanager_local_dirs",
            "value" : "/yarn/nm"
          }, {
            "name" : "yarn_nodemanager_log_dirs",
            "value" : "/yarn/container-logs"
          }, {
            "name" : "yarn_nodemanager_resource_cpu_vcores",
            "value" : "4"
          }, {
            "name" : "yarn_nodemanager_resource_memory_mb",
            "value" : "5578"
          } ]
        }, {
          "roleType" : "RESOURCEMANAGER",
          "items" : [ {
            "name" : "yarn_scheduler_maximum_allocation_mb",
            "value" : "5578"
          }, {
            "name" : "yarn_scheduler_maximum_allocation_vcores",
            "value" : "4"
          } ]
        } ],
        "items" : [ {
          "name" : "hdfs_service",
          "value" : "hdfs"
        }, {
          "name" : "rm_dirty",
          "value" : "true"
        }, {
          "name" : "zk_authorization_secret_key",
          "value" : "rH1o5i5naoi0XnRadmSZcScvD0g6W7"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "yarn-JOBHISTORY-7c563c0a16a29c7aefa51eb19467b5b9",
        "type" : "JOBHISTORY",
        "hostRef" : {
          "hostId" : "2bd6c763-8faf-4ef1-aa12-43e5ea4c5e0c"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "9vphy80z55l466lasbumylmq0"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-720ff148adb6e50839b928b7fe7f42cc",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "2f708c23-ecee-46ca-93a8-e79969f1ecb2"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "b7g2rdo2cj69snlxtmnnnk4tv"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-7c563c0a16a29c7aefa51eb19467b5b9",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "2bd6c763-8faf-4ef1-aa12-43e5ea4c5e0c"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "2oi47ubov2l6581qln1idsbqx"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-b3b2dbfd3af0436695f16d3e77d22da3",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "1770e495-5e30-4f8a-8566-f0ae81b97750"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "7tt8jiajsrkb3opw9asas95bc"
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-bc148c046060d290126bd892cf268ba2",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "69c4db24-91ab-4ea0-893b-e7c8fb2f9ee6"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "3l5ryp65offb5llz7a26vmdli"
          } ]
        }
      }, {
        "name" : "yarn-RESOURCEMANAGER-cfaedf65fe631a3797a87a24f9d677e8",
        "type" : "RESOURCEMANAGER",
        "hostRef" : {
          "hostId" : "f1d86679-d68f-4b62-8137-7be90cb3ddf5"
        },
        "config" : {
          "items" : [ {
            "name" : "rm_id",
            "value" : "117"
          }, {
            "name" : "role_jceks_password",
            "value" : "ztrqbxo4hfqlsw57mjpoiukr"
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
            "value" : "860880896"
          } ]
        }, {
          "roleType" : "DATANODE",
          "items" : [ {
            "name" : "dfs_data_dir_list",
            "value" : "/dfs/dn"
          }, {
            "name" : "dfs_datanode_data_dir_perm",
            "value" : "755"
          }, {
            "name" : "dfs_datanode_du_reserved",
            "value" : "3220069990"
          } ]
        }, {
          "roleType" : "GATEWAY",
          "items" : [ {
            "name" : "dfs_client_use_trash",
            "value" : "true"
          } ]
        }, {
          "roleType" : "NAMENODE",
          "items" : [ {
            "name" : "dfs_name_dir_list",
            "value" : "/dfs/nn"
          }, {
            "name" : "dfs_namenode_servicerpc_address",
            "value" : "8022"
          }, {
            "name" : "namenode_java_heapsize",
            "value" : "860880896"
          } ]
        }, {
          "roleType" : "SECONDARYNAMENODE",
          "items" : [ {
            "name" : "fs_checkpoint_dir_list",
            "value" : "/dfs/snn"
          }, {
            "name" : "secondary_namenode_java_heapsize",
            "value" : "860880896"
          } ]
        } ],
        "items" : [ {
          "name" : "dfs_ha_fencing_cloudera_manager_secret_key",
          "value" : "L9RY1DUYO51oRfrrOCrrQwb5crB8zy"
        }, {
          "name" : "fc_authorization_secret_key",
          "value" : "jyajUe9gk31HvIvAEgfv9hczXUFxRD"
        }, {
          "name" : "http_auth_signature_secret",
          "value" : "oQDuH8A7aTy3rD96VlEnLBkgcahOOL"
        }, {
          "name" : "rm_dirty",
          "value" : "true"
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper"
        } ]
      },
      "roles" : [ {
        "name" : "hdfs-BALANCER-7c563c0a16a29c7aefa51eb19467b5b9",
        "type" : "BALANCER",
        "hostRef" : {
          "hostId" : "2bd6c763-8faf-4ef1-aa12-43e5ea4c5e0c"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-DATANODE-720ff148adb6e50839b928b7fe7f42cc",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "2f708c23-ecee-46ca-93a8-e79969f1ecb2"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "aqe9x4cwusnlf91wahjk1s54v"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-7c563c0a16a29c7aefa51eb19467b5b9",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "2bd6c763-8faf-4ef1-aa12-43e5ea4c5e0c"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "et6gwytlci6wn9fcg3spo9v2q"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-b3b2dbfd3af0436695f16d3e77d22da3",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "1770e495-5e30-4f8a-8566-f0ae81b97750"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "1dja6cckpj5d5mqgznnlnad2s"
          } ]
        }
      }, {
        "name" : "hdfs-DATANODE-bc148c046060d290126bd892cf268ba2",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "69c4db24-91ab-4ea0-893b-e7c8fb2f9ee6"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "ehj7n3hew43oes9jc95mtbd16"
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-cfaedf65fe631a3797a87a24f9d677e8",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "f1d86679-d68f-4b62-8137-7be90cb3ddf5"
        },
        "config" : {
          "items" : [ {
            "name" : "namenode_id",
            "value" : "119"
          }, {
            "name" : "role_jceks_password",
            "value" : "3qz8ys0if2uy2f1gf3s8xc89m"
          } ]
        }
      }, {
        "name" : "hdfs-SECONDARYNAMENODE-7c563c0a16a29c7aefa51eb19467b5b9",
        "type" : "SECONDARYNAMENODE",
        "hostRef" : {
          "hostId" : "2bd6c763-8faf-4ef1-aa12-43e5ea4c5e0c"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "4ikrib1crob7vcoeqm03khywl"
          } ]
        }
      } ],
      "displayName" : "HDFS"
    }, {
      "name" : "impala",
      "type" : "IMPALA",
      "config" : {
        "roleTypeConfigs" : [ {
          "roleType" : "CATALOGSERVER",
          "items" : [ {
            "name" : "catalogd_embedded_jvm_heapsize",
            "value" : "332398592"
          } ]
        }, {
          "roleType" : "IMPALAD",
          "items" : [ {
            "name" : "impalad_embedded_jvm_heapsize",
            "value" : "52428800"
          }, {
            "name" : "impalad_memory_limit",
            "value" : "268435456"
          }, {
            "name" : "scratch_dirs",
            "value" : "/impala/impalad"
          } ]
        } ],
        "items" : [ {
          "name" : "hdfs_service",
          "value" : "hdfs"
        }, {
          "name" : "hive_service",
          "value" : "hive"
        }, {
          "name" : "llama_am_ha_zk_auth_secret_key",
          "value" : "t5BVNPFsbHlFvb14fdN0NtksaDho9N"
        }, {
          "name" : "rm_dirty",
          "value" : "true"
        } ]
      },
      "roles" : [ {
        "name" : "impala-CATALOGSERVER-cfaedf65fe631a3797a87a24f9d677e8",
        "type" : "CATALOGSERVER",
        "hostRef" : {
          "hostId" : "f1d86679-d68f-4b62-8137-7be90cb3ddf5"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "5ayvkrfl2kpoxtnqu1yi65uw8"
          } ]
        }
      }, {
        "name" : "impala-IMPALAD-720ff148adb6e50839b928b7fe7f42cc",
        "type" : "IMPALAD",
        "hostRef" : {
          "hostId" : "2f708c23-ecee-46ca-93a8-e79969f1ecb2"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "aujnjfl7r72c48lfcaahk6aw5"
          } ]
        }
      }, {
        "name" : "impala-IMPALAD-7c563c0a16a29c7aefa51eb19467b5b9",
        "type" : "IMPALAD",
        "hostRef" : {
          "hostId" : "2bd6c763-8faf-4ef1-aa12-43e5ea4c5e0c"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "3gwjjxhhilrqtxsherdvxmenb"
          } ]
        }
      }, {
        "name" : "impala-IMPALAD-b3b2dbfd3af0436695f16d3e77d22da3",
        "type" : "IMPALAD",
        "hostRef" : {
          "hostId" : "1770e495-5e30-4f8a-8566-f0ae81b97750"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "dyhpmid5a0pjpryljal2tq7oa"
          } ]
        }
      }, {
        "name" : "impala-IMPALAD-bc148c046060d290126bd892cf268ba2",
        "type" : "IMPALAD",
        "hostRef" : {
          "hostId" : "69c4db24-91ab-4ea0-893b-e7c8fb2f9ee6"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "cfzimmyyosbsyfyjah8aedtu8"
          } ]
        }
      }, {
        "name" : "impala-STATESTORE-7c563c0a16a29c7aefa51eb19467b5b9",
        "type" : "STATESTORE",
        "hostRef" : {
          "hostId" : "2bd6c763-8faf-4ef1-aa12-43e5ea4c5e0c"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "5ilnuay5ss5jv2m21hty37u3z"
          } ]
        }
      } ],
      "displayName" : "Impala"
    } ]
  } ],
  "hosts" : [ {
    "hostId" : "2bd6c763-8faf-4ef1-aa12-43e5ea4c5e0c",
    "ipAddress" : "172.31.33.116",
    "hostname" : "ip-172-31-33-116.eu-central-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "2f708c23-ecee-46ca-93a8-e79969f1ecb2",
    "ipAddress" : "172.31.33.93",
    "hostname" : "ip-172-31-33-93.eu-central-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "f1d86679-d68f-4b62-8137-7be90cb3ddf5",
    "ipAddress" : "172.31.37.70",
    "hostname" : "ip-172-31-37-70.eu-central-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "1770e495-5e30-4f8a-8566-f0ae81b97750",
    "ipAddress" : "172.31.42.17",
    "hostname" : "ip-172-31-42-17.eu-central-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "69c4db24-91ab-4ea0-893b-e7c8fb2f9ee6",
    "ipAddress" : "172.31.47.155",
    "hostname" : "ip-172-31-47-155.eu-central-1.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  } ],
  "users" : [ {
    "name" : "__cloudera_internal_user__hue-HUE_SERVER-cfaedf65fe631a3797a87a24f9d677e8",
    "roles" : [ "ROLE_NAVIGATOR_ADMIN" ],
    "pwHash" : "d13263655337449841fecfdb8d077aaada22f5a4e44c52bcbd6509f36ea89616",
    "pwSalt" : 1190931583643722098,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-EVENTSERVER-cfaedf65fe631a3797a87a24f9d677e8",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "694606e2726364d794dc0b7635b36322c7e1a703853b3898815921fd05adda2f",
    "pwSalt" : 7902739594185369095,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-HOSTMONITOR-7c563c0a16a29c7aefa51eb19467b5b9",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "6bacb6e27ccbb919995ad20daa9ad035f01d7f8efaf9b965750020743583b797",
    "pwSalt" : 4622741702756646704,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-REPORTSMANAGER-cfaedf65fe631a3797a87a24f9d677e8",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "b46788088cebe083b30c5920ac47f0c61f8fdf0e62d1695fbfcf6d54e4adf9ee",
    "pwSalt" : -277475105275568155,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-SERVICEMONITOR-cfaedf65fe631a3797a87a24f9d677e8",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "84a5fa9bf7f943394a31b90363a64fa6165ede209938e4e852ddc9fd0d40a6d1",
    "pwSalt" : 2665097519141819720,
    "pwLogin" : true
  }, {
    "name" : "admin",
    "roles" : [ "ROLE_ADMIN" ],
    "pwHash" : "b7de433f5efea22138eb3aa320dee7abec2a166f214c36c4e4f007ec7d8ec452",
    "pwSalt" : 8637793172570324140,
    "pwLogin" : true
  }, {
    "name" : "minotaur",
    "roles" : [ "ROLE_CONFIGURATOR" ],
    "pwHash" : "29c17ead4c325372ed567d09edfb119c895c941d12451bb9fa16f69a22b790c5",
    "pwSalt" : -5744751946634269811,
    "pwLogin" : true
  } ],
  "versionInfo" : {
    "version" : "5.16.1",
    "buildUser" : "jenkins",
    "buildTimestamp" : "20181120-1809",
    "gitHash" : "6a13b87a6fcdf4afad6d4474a68a9434b24d6c67",
    "snapshot" : false
  },
  "managementService" : {
    "name" : "mgmt",
    "type" : "MGMT",
    "config" : {
      "roleTypeConfigs" : [ {
        "roleType" : "HOSTMONITOR",
        "items" : [ {
          "name" : "firehose_heapsize",
          "value" : "860880896"
        }, {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "1119879168"
        } ]
      }, {
        "roleType" : "REPORTSMANAGER",
        "items" : [ {
          "name" : "headlamp_database_host",
          "value" : "ip-172-31-37-70.eu-central-1.compute.internal"
        }, {
          "name" : "headlamp_database_name",
          "value" : "rman"
        }, {
          "name" : "headlamp_database_password",
          "value" : "cloudera"
        }, {
          "name" : "headlamp_database_user",
          "value" : "rman"
        } ]
      }, {
        "roleType" : "SERVICEMONITOR",
        "items" : [ {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "1430257664"
        } ]
      } ],
      "items" : [ ]
    },
    "roles" : [ {
      "name" : "mgmt-ALERTPUBLISHER-7c563c0a16a29c7aefa51eb19467b5b9",
      "type" : "ALERTPUBLISHER",
      "hostRef" : {
        "hostId" : "2bd6c763-8faf-4ef1-aa12-43e5ea4c5e0c"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "6dsyscp7ww9y386cyzccafi7h"
        } ]
      }
    }, {
      "name" : "mgmt-EVENTSERVER-cfaedf65fe631a3797a87a24f9d677e8",
      "type" : "EVENTSERVER",
      "hostRef" : {
        "hostId" : "f1d86679-d68f-4b62-8137-7be90cb3ddf5"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "bd20b84hexr6grldt2boy382b"
        } ]
      }
    }, {
      "name" : "mgmt-HOSTMONITOR-7c563c0a16a29c7aefa51eb19467b5b9",
      "type" : "HOSTMONITOR",
      "hostRef" : {
        "hostId" : "2bd6c763-8faf-4ef1-aa12-43e5ea4c5e0c"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "21tejle0wr9poxc9qc3buo3d3"
        } ]
      }
    }, {
      "name" : "mgmt-REPORTSMANAGER-cfaedf65fe631a3797a87a24f9d677e8",
      "type" : "REPORTSMANAGER",
      "hostRef" : {
        "hostId" : "f1d86679-d68f-4b62-8137-7be90cb3ddf5"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "2lgxyjulq0ub9hpzoi2ttoud2"
        } ]
      }
    }, {
      "name" : "mgmt-SERVICEMONITOR-cfaedf65fe631a3797a87a24f9d677e8",
      "type" : "SERVICEMONITOR",
      "hostRef" : {
        "hostId" : "f1d86679-d68f-4b62-8137-7be90cb3ddf5"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "f4d3jl2kapkm8oqdroh7kee1y"
        } ]
      }
    } ],
    "displayName" : "Cloudera Management Service"
  },
  "managerSettings" : {
    "items" : [ {
      "name" : "CLUSTER_STATS_START",
      "value" : "10/25/2012 4:50"
    }, {
      "name" : "PUBLIC_CLOUD_STATUS",
      "value" : "ON_PUBLIC_CLOUD"
    }, {
      "name" : "REMOTE_PARCEL_REPO_URLS",
      "value" : "https://archive.cloudera.com/cdh5/parcels/{latest_supported}/,https://archive.cloudera.com/cdh4/parcels/latest/,https://archive.cloudera.com/impala/parcels/latest/,https://archive.cloudera.com/search/parcels/latest/,https://archive.cloudera.com/accumulo/parcels/1.4/,https://archive.cloudera.com/accumulo-c5/parcels/latest/,https://archive.cloudera.com/kafka/parcels/latest/,http://archive.cloudera.com/kudu/parcels/latest/,https://archive.cloudera.com/spark/parcels/latest/,https://archive.cloudera.com/sqoop-connectors/parcels/latest/"
    } ]
  }


  