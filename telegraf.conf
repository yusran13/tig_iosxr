
## This section defines the  settings for the router that Telegraf will dial-in or connect to.
[[inputs.gnmi]]                                                       
   addresses = ["172.17.6.237:57344"]     
   username = "cisco"                      
   password = "cisco123"

   ## This section defines the metric that Telegraf wants router to stream.
   [[inputs.gnmi.subscription]]
      name = "ifcounters"                                                                   
      origin = "Cisco-IOS-XR-infra-statsd-oper"							  
      path = "/infra-statistics/interfaces/interface/latest/generic-counters"
      subscription_mode = "sample"    # (one of: "target_defined", "sample", "on_change")
      sample_interval = "10s"		   # Cadence between two consecutive samples.

## This section defines where will Telegraf to store the metric.
[[outputs.influxdb]]

   # urls = ["http://localhost:8086"]
   urls = ["http://influxdb:8086"]
   database = "mdt-db"
   username = "admin"
   password = "admin"
