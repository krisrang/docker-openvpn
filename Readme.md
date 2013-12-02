```shell
CID=$(docker run -d -privileged -p 1194:1194/udp -p 442:442/tcp pebbles/openvpn)
docker run -t -i -p 8001:8001 -volumes-from $CID pebbles/openvpn serveconfig
```
