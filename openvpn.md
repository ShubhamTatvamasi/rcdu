# openvpn

start openvpn:
```bash
OVPN_DATA="ovpn-data-ramanujan"
docker run -v $OVPN_DATA:/etc/openvpn -d -p 1194:1194/udp --cap-add=NET_ADMIN kylemanna/openvpn
```
---

generate key
```bash
CLIENTNAME="anshul-ramanujan"
OVPN_DATA="ovpn-data-ramanujan"
docker run -v $OVPN_DATA:/etc/openvpn --rm -it kylemanna/openvpn easyrsa build-client-full ${CLIENTNAME} nopass
```

download key:
```bash
docker run -v $OVPN_DATA:/etc/openvpn --rm kylemanna/openvpn ovpn_getclient ${CLIENTNAME} > ${CLIENTNAME}.ovpn
```

