# 개요
* 그라파나 helm설정

# pv, pvc생성
* pv.yaml, pvc.yaml 참고

# override_valeus.yaml
```yaml

ingress:
enabled: true
annotations:
    nginx.ingress.kubernetes.io/rewrite-target: /$2
# change here
path: /test(/|$)(.*)
hosts:
    - choilab.com
grafana.ini:
server:
    # change here
    domain: choilab.com
    root_url: http://choilab/test/
    serve_from_sub_path: true
persistence:
  enabled: true
  type: pvc
```

# 참고자료
* 공식문서: https://github.com/grafana/helm-charts/blob/main/charts/grafana/README.md
* https://medium.com/@kevincoakley/reusable-persistent-volumes-with-the-existingclaim-option-for-the-grafana-prometheus-operator-84568b96315