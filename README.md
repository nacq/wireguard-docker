### Wireguard vps setup

#### Dependencies

- nginx
- docker compose

#### Instructions

- link the nginx configs
```sh
ln -s /path/to/wireguard/wg-nginx-conf /etc/nginx/sites-available/wg
```

```sh
ln -s /etc/nginx/sites-available/wg /etc/nginx/sites-enabled/wg
```

- test the new nginx config
```sh
nginx -t
```

- reload nginx
```sh
systemctl reload nginx
```

- link the service
```sh
ln -s /path/to/wireguard/wireguard.service /etc/systemd/system/wireguard.service
```

- reload daemon
```sh
systemctl daemon-reload
```

- enable service
```sh
systemctl enable wireguard.service
```

- start service
```sh
systemctl start wireguard.service
```
