docker run --name influxdb -d -p 8086:8086 -v "C:\Privat\Workspace\snmp\influxdb:/var/lib/influxdb" -e INFLUXDB_ADMIN_USER=admin -e INFLUXDB_ADMIN_PASSWORD=admin influxdb:1.8
docker run --name grafana  -d -p 3000:3000 -v "C:\Privat\Workspace\snmp\grafana:/var/lib/grafana" --link influxdb grafana/grafana:9.5.3
docker run --name telegraf -d              -v "C:\Privat\Workspace\snmp\telegraf\telegraf.conf:/etc/telegraf/telegraf.conf:ro" --link influxdb telegraf:1.26.3



https://gist.github.com/agent4788/438639df3c5f2801038123de3f916d1d
https://h30434.www3.hp.com/t5/Printer-Setup-Software-Drivers/Web-interface-showing-different-toner-level-than-SNMP/td-p/6310044