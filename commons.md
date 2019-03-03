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
`systemctl list-units --type service` : list all services
`systemctl list-units --type mount` : list all mount paths 
`systemctl list-unit-files` : List all service unit files
