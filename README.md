# elastic-snmp

Logstash configs, ingest pipelines, and dashboards for SNMP data ingested into Elastic search

### Warning - part of the reason I started working thru this was to get a feel for likely ECS additions for interface metrics.  
The interface.xxx fields are custom, don't follow the ECS rules, and could very well be changed.

There seems to be a timing issue in logstash where the 60s interval **appears** to be from the time the last execution ended, I see a ~ 4s drift.  
Easy enough to adjust for in the snmp input config, but adjustment will be specific to your environment

Theres also 2 community snmp beats that could probably be used with ingest pipelines, probably worth a look

https://github.com/sydneybrokeit/netbeat   - I think this one looks the most promising 
https://github.com/isalgueiro/otilio
https://github.com/hoat23/snmpbeat
