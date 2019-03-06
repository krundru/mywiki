
splunk complex query: 
```
index=os AND sourcetype=linux_secure AND source="/var/lib/docker-latest/volumes/gateway/_data/envoy_access.log" Application=<> AND EnvironmentGroup::<> AND Environment::<>
| rex "\"(?P<req_method>\w*)\s*(?P<req_path>[^\s]*)\s*(?P<req_protocol>[^\"]*)\"\s*(?P<status_code>\S*)\s*(?P<envoy_flags>[\S]*)\s*(?P<bytes_received>\S*)\s*(?P<bytes_sent>\S*)\s*(?P<duration>\S*)\s*(?P<upstream_duration>\S*)\s\"([^\"]*)\"\s\"([^\"]*)\"\s\"(?P<req_id>[\S]*)\"\s\"(?P<upstream_host>[\S]*)\"\s\"(?P<upstream_ip>[\S]*)\"(\s\"(?P<rc>[\S]*)\"\s\"(?P<ri>[\S]*)\")?"

```
