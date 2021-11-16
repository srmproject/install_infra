- [loadbalancer 설정](#loadbalancer---)

# loadbalancer 설정
* aws ELB같은 역할을 담당합니다.
* haproxy가 nginx-ingress controller로 로드밸런싱 합니다.

```sh
# vi /etc/haproxy/haproxy.cfg

frontend http_front
  bind *:80
  stats uri /haproxy?stats
  default_backend http_back

backend http_back
  balance roundrobin
  server kube 10.10.20.170:80
```

```sh
systemctl restart haproxy
```
