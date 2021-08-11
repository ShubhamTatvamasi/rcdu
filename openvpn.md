# openvpn

generate key
```bash
OVPN_DATA="ovpn-data-ramanujan"
CLIENTNAME="anshul-ramanujan"
docker run -v $OVPN_DATA:/etc/openvpn --rm -it kylemanna/openvpn easyrsa build-client-full ${CLIENTNAME} nopass
```

download key:
```bash
docker run -v $OVPN_DATA:/etc/openvpn --rm kylemanna/openvpn ovpn_getclient ${CLIENTNAME} > ${CLIENTNAME}.ovpn
```

