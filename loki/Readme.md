- [개요](#--)
- [사전준비](#----)
- [helm 저장소 업데이트](#helm---------)
- [설치](#--)
- [추가 작업](#-----)
- [참고자료](#----)

# 개요
* helm loki chart를 이용하여 loki 설치

# 사전준비
* node labeling
* pv, pvc
    * [pv.yaml](./pv.yaml), [pvc.yaml](./pvc.yaml) 설치

# helm 저장소 업데이트
```sh 
helm repo add grafana https://grafana.github.io/helm-charts
helm repo update
```

# 설치
* loki-stack은 여러 솔루션을 한번에 설치
* grafana 설치 비활성화
* prometheus 설치 비활성화
* 
```sh
helm upgrade --install -n infra -f values.yaml loki grafana/loki
```

# 추가 작업
* grafana 대시보드 설치 후 연결
    * [helm을 이용한 grafana 설치](../grafana/Readme.md)


# 참고자료
* 공식문서: https://grafana.com/docs/loki/latest/installation/helm/