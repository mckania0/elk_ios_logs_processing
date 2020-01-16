# Elastic stack (ELK) on Docker for Cisco Logs processing

Whole stack forked from https://github.com/deviantony/docker-elk

Network topology was built in eve-ng with logging to external server, which in our case was Logstash listening on specific ports.


## Sample queries for update, delete, display indices

### GET /_index/_type/_id
```
GET /ciscolog/_doc/egMPr28B4Tf2r4l9ih0O
```

### POST vs PUT: 
* POST will create doc with id 
* PUT will update doc with id that we will specify


#### POST /_index/_type
#### PUT /_index/_type/_id
```
POST /ciscolog/_doc
{
    "@timestamp" : "2020-01-16T15:26:18.723Z",
    "facility_mnemonic" : "DUPADDR",
    "facility" : "IP",
    "tags" : [
      "cisco"
    ],
    "severity_level" : "4 - Warning",
    "host" : "192.168.64.1",
    "fingerprint" : "0ceaab2f4a850aadb22a6f591a1b1b604e879e2455cc936c5a0658a99cc2ba96",
    "message" : "Duplicate address 192.168.1.2 on Ethernet0/1, sourced by 0050.56fd.6892",
    "log_date" : "Jan 16 15:26:18.723 UTC",
    "type" : "syslog-cisco"
}
```

### DELETE /_index/_type/_id
```
DELETE /ciscolog/_doc/egMPr28B4Tf2r4l9ih0O
```
