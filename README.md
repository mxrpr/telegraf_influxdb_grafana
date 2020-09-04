# telegraf_influxdb_grafana

## step 1
Start the influxDB and Grafana containers
```
docker-compose up -d
```

## step 2
Download and install telegraf
On Linux
```
wget https://dl.influxdata.com/telegraf/releases/telegraf_1.11.2-1_amd64.deb
```
```
sudo dpkg -i telegraf_1.11.2-1_amd64.deb
```

On Mac:
```
brew install telegraf
```
## step 3
Copy telegraf.conf to the specified location from where you wan to use. Update url, username, password and the plugins you wish to use

## step 4
Test the telegraf settings:
```telegraf -config telegraf.conf```


## step 5
Start telegraf:
```
telegraf -config telegraf.conf
```
