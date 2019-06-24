## Overview
project prometheus-lua-nginx is a complete solution for openresty based api gateway monitoring, prometheus-lua-nginx use prometheus lua lib and openresty http request life cycle to inject monitoring code, it is async, high performance, and business awareness, it also have built-in grafana dashboard out of box, please see [Snapshots](https://github.com/zrbcool/prometheus-lua-nginx/blob/master/Snapshots.md)
## Architecture

## Features
- Base on promethues pull mode to collect metrics
- Multiple dimension latency metrics collection(host,status code,schema,etc.)
- Out-of-box grafana dashboards
- LUA based latency metrics collection, high performance, low memory use, async
## Getting started
### Quickly start up a demo by docker-compose
```shell
# please instal docker-ce, docker-compose correctly
docker-compose up
```
this compose will install a set of containers for a demo use:
- a grafana has built in dashboards
- a backend services for mock latency and the real workload
- a openresty as proxy with counter.lua and promethues.lua integrated, can collect latency metrics, and expose them by :9145/metrics endpoint
- a promethues has pre configured previous oprenresty as scrape target

how to asscess:
- access grafana by [hostip]:3000
- access promethues by [hostip]:9090
- access openresty exposed metrics by [hostip]:9145/metrics
- access [hostip]:8081/latency/[latency]/bytes/[bytes] to mock a api call, for instance -> :8081/latency/100/bytes/10
## Building
## Contact

