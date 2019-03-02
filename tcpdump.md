## tcpdump commands

#### How to install
`yum install tcpdump`

#### Regular commands

`tcpdump tcp -c 20` : capture 20 (c) tcp packets <br/>
`tcpdump -i eth0 port 80` : filter on port 80 <br/>
`tcpdump -i eth0 src|dst 192.168.1.1` filter on src or dest ip. <br/>
`tcpdump -i any|lo|eth0|docker0` Capture from specific interfaces, for any or loopback (localhost -> localhost)<br/>
`-nn` - single n for hostnames - nn for hostname & port<br/>
`-s0` - unlimited snap size (capture packets for all traffic)<br/>
`-v` - verbose<br/>
`sudo tcpdump host 10.10.1.1` capture on host ip (to & from packets)<br/>

