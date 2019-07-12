# telegraf_influxdb_grafana

## step 1
```
docker run --rm -e INFLUXDB_DB=telegraph -e INFLUXDB_ADMIN_ENABLED=true -e INFLUXDB_ADMIN_USER=admin -e INFLUXDB_ADMIN_PASSWORD=secretpassword -e INFLUXDB_USER=telegraph -e INFLUX_USER_PASSWORD=secretpassword  influxdb /init-influxdb.sh
```

## step 2
Download and install telegraf
```
wget https://dl.influxdata.com/telegraf/releases/telegraf_1.11.2-1_amd64.deb
```
```
sudo dpkg -i telegraf_1.11.2-1_amd64.deb
```
## step 3
Copy telegraf.conf to the specified location from where you wan to use

## step 4
Test the telegraf settings:
```telegraf -config telegraf.conf --test```

## step 5
Start telegraf:
```
telegraf -config telegraf.conf
```

## step 6
Start the influxDB and Grafana containers
```
docker-compose up -d
```
