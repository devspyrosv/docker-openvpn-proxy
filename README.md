# docker-openvpn-proxy
Docker OpenVPN Client and Squid Proxy Server

Build based on
* [schmas/docker-openvpn-client](https://github.com/schmas/docker-openvpn-proxy)

## Run container from Docker registry
To run the container use this command:

```
$ docker run --privileged  -d \
              -e "OPENVPN_PROVIDER=PIA" \
              -e "OPENVPN_CONFIG=Netherlands" \
              -e "OPENVPN_USERNAME=user" \
              -e "OPENVPN_PASSWORD=pass" \
              -p 1022:22 \
              -p 3128:3128 \
              --dns 1.1.1.1 \
              devspyrosv/openvpn-proxy:1.0
```

Now you can connect your application to a proxy `localhost:3128`.


