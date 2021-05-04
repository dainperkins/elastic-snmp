 1 create ilm policy (I used "standard-30d" as a 30 day delete, rollover @ 50GB. need to update it in the templates if you use something else)

 2 create snmp & snmp-asset index templates

 3 Bootstrap snmp indexes

In e.g. dev tools:

## load templates
PUT _index_template/snmp-assets
PUT _index_template/snmp

## Bootstrap indexes
PUT snmp-000001
{
  "aliases": {
    "snmp": {
      "is_write_index": true
    }
  }
}
PUT snmp-assets-000001
{
  "aliases": {
    "snmp-assets": {
      "is_write_index": true
    }
  }
}

output to snmp / snmp-assets indexes
