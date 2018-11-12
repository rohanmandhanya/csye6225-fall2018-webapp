# csye6225-fall2018-webapp

```
{
    "agent": {
        "metrics_collection_interval": 10,
        "logfile": "/var/logs/amazon-cloudwatch-agent.log"
    },
    "logs": {
        "logs_collected": {
            "files": {
                "collect_list": [
                    {
                        "file_path": "/opt/tomcat/logs/csye6225.log",
                        "log_group_name": "csye6225_fall2018",
                        "log_stream_name": "webapp",
                        "timestamp_format": "%H:%M:%S %y %b %-d"
                    }
                ]
            }
        },
        "log_stream_name": "cloudwatch_log_stream"
    },
    "metrics":{
      "metrics_collected":{
         "statsd":{
            "service_address":":8125",
            "metrics_collection_interval":10,
            "metrics_aggregation_interval":0
         }
      }
    }
}
```