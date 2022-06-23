
# 개요
* sonarqube 설치
> 개인생각: postgresql 선택이 어렵다.

# 준비
* pv생성
```sh
kubectl apply -f pv.yaml
```

# 설치
* helm chart 추가
```sh
helm repo add sonarqube https://SonarSource.github.io/helm-chart-sonarqube
helm repo update
```

* sonarqube 설치
```sh
kubectl create namespace infra
helm upgrade --install -n infra -f values.yaml sonarqube sonarqube/sonarqube
```

# 삭제
```sh
helm uninstall -n infra sonarqube
```


# 참고자료
* 공식문서: https://docs.sonarqube.org/latest/setup/sonarqube-on-kubernetes/
* helm charts: https://github.com/SonarSource/helm-chart-sonarqube/tree/master/charts/sonarqube
* 블로그: https://metleeha.tistory.com/36#Sonarqube%--%EB%-E%--%-F