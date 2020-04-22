# Pgpool-II Exporter

Prometheus exporter for [Pgpool-II](https://pgpool.net) metrics.

Supported Pgpool-II 3.6 and later.


## Building and running

### Build
```
$ make
```

### Running

Running using an environment variable:
```
$ export DATA_SOURCE_NAME="postgresql://user:password@hostname:port/dbname"
$ ./pgpool2_exporter <flags>
```
    
To see all available configuration flags:
```
$ ./pgpool2_exporter --help
```
    
 ### Flags

* `version`
  Print version information.
  
* `web.listen-address`
  Address on which to expose metrics and web interface. (default ":9719").

* `web.telemetry-path`
  Path under which to expose metrics. (default "/metrics")
  
## Metrics

### Collector Flags
name | Description
:---|:---
pgpool2_frontend_total | Number of total child processed
pgpool2_frontend_used | Number of used child processes
pgpool2_pool_nodes_replication_delay | Replication delay
pgpool2_pool_nodes_select_cnt | SELECT query counts issued to each backend
pgpool2_pool_cache_cache_hit_ratio | Query cache hit ratio
pgpool2_pool_cache_num_cache_entries | Number of used cache entries
pgpool2_pool_cache_num_hash_entries | Number of total hash entries
pgpool2_pool_cache_used_hash_entries | Number of used hash entries

