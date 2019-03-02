

`tcpdump tcp -c 20` : capture 20 (c) tcp packets <br/>
`tcpdump -i eth0 port 80` : filter on port 80 <br/>
`tcpdump -i eth0 src|dst 192.168.1.1` filter on src or dest ip. <br/>
`tcpdump -i any|lo|eth0|docker0` Capture from specific interfaces, for any or loopback (localhost -> localhost)
