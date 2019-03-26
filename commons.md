## Common commands

##### curl
`curl -m|--max-time 5 -i -v -k url`: fetch response from url <br/>
`   -k`: insecure certs<br/>
`   -i`: fetch only headers <br/>
`   -v`: enable verbose mode <br/>
`   -m <sec>`: max time to spend to fetch res <br/>
`   -H "key: value"`: to send http header <br/>

#### misc

`uuidgen --time` : Generate uuid <br/>

#### systemctl
`systemctl list-units --type service` : list all services <br/>
`systemctl list-units --type mount` : list all mount paths <br/>
`systemctl list-unit-files` : List all service unit files<br/>

#### Envoy
`curl localhost:9001/stats`: for all stats <br/>
`curl localhost:9001/logs` <br/>
`curl localhost:9001/clusters`<br/>
`curl -X POST localhost:9001/logging` <br/>
`   /logging?<name>=<level> (change singlelevel)` <br/>
`   /logging?level=<level> (change all levels)` <br/>

#### No of threads
`cat /proc/<PROCESS_PID>/status | grep Threads`
