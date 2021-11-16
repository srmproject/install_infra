- [개요](#--)
- [helm 저장소 추가](#helm-------)
- [설치](#--)
- [참고자료](#----)

# 개요
* nginx ingress controller 설치방법을 설명합니다.

<br>

# helm 저장소 추가
```sh
helm repo add nginx-stable https://helm.nginx.com/stable
helm repo update
```

<br>

# 설치
* infra namespace에 설치했습니다.
> metallb설치가 필요합니다.
```sh
kubectl create ns infra
helm install -n infra nginx-ingress nginx-stable/nginx-ingress
```

![installed](./imgs/installed.png)

<br>

# 참고자료
* 공식문서: https://docs.nginx.com/nginx-ingress-controller/installation/installation-with-helm/
