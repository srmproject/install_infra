# 개요
* postgresql operator를 이용한 posrgresql 설치

# 상세내용
* operator 설치
```sh
helm repo add cnpg https://cloudnative-pg.github.io/charts
helm install cnpg cnpg/cloudnative-pg
```

* postgresql 클러스터를 위한 pv생성
```sh
kubectl apply -f pv.yaml
```

* secret 생성
```sh
kubectl apply -f secret.yaml
```

* cluster 설치
```sh
kubectl apply -f cluster.yaml
```
