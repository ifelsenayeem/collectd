# Collectd

[Collectd](http://collectd.org) is a small daemon which collects system information periodically and provides mechanisms to store and monitor the values in a variety of ways.

## Usage

```
docker build -t collectd:v1 -f Dockerfile

docker run -d \
           -v collectd_config_path/collectd.conf:/etc/collectd/collectd.conf \
           --hostname collectd \
           --name collectd \
           collectd:v1
```

Change the Host in write_graphite plugin to receive the matrix in graphite.
