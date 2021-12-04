# 개요
* helm promtail 차트로 promtail설치

# helm repo 추가
```sh
helm repo add grafana https://grafana.github.io/helm-charts
helm repo update
```

# 설치
```sh
helm install -n infra -f values.yaml promtail grafana/promtail
```

# 참고자료
* 공식문서: https://github.com/grafana/helm-charts/tree/main/charts/promtail