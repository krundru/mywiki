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
`tcpdump -n dst net 192.168.1.0/24` catpure from cidr block ips <br/>
`tcpdump -i <interface> -s 65535 -w <some-file>` Capture full packet s "byte size" <br/>
`tcpdump -v -i eth0 -w dump.pcap` reporting <br/>
Keepalive packets:
```
tcpdump -pni $intf -v "tcp port $port and ( tcp[tcpflags] & tcp-ack != 0 and ( (ip[2:2] - ((ip[0]&0xf)<<2) ) - ((tcp[12]&0xf0)>>2) ) == 0 )"   - keepalive packets
```
Read headers:
```
tcpdump -n -S -s 0 -A 'tcp dst port 80' | grep -B3 -A10 "GET /some-path"
tcpdump -i any -nn -A -s 1492 dst port 8080 - on all network interfaces.
```

#### SS commands
`ss -tnn state established '( dport = :8080 or sport = :8080 )'` : list all open cx to 8080 <br/>
