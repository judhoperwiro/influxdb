## InfluxDB Installation 
 
### 1.) Copy influxdb-1.8.3.rpm into /source 

### 2.) Install InfluDB 
user: root 
```
yum install -y /source/influxdb-1.8.3.x86_64.rpm 
```

### 3.)Edit /etc/influxdb/influxdb.conf 
user: root 

```
vi /etc/influxdb/influxdb.conf 

[meta]   

  dir = "/data/influxdb/meta" 

[data] 

  dir = "/data/influxdb/data" 

  wal-dir = "/data/influxdb/wal" 
```

### 4.) Start Influxdb 
user: root 

```
systemctl start influxdb 
```

### 5.) Create Database 
user: root 
```
$ influx 
> CREATE DATABASE telegraf 
> show databases 
```
