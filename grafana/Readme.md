- [개요](#--)
- [pv, pvc생성](#pv--pvc--)
- [override_valeus.yaml](#override-valeusyaml)
- [설치](#--)
- [초기 비밀번호](#-------)
- [참고자료](#----)

# 개요
* helm grafana chart를 이용하여 grafana 설치

# 목표
* ingress subpath 설정
* pv, pvc.yaml 설정과 연동

# pv, pvc생성
* [pv.yaml](./pv.yaml), [pvc.yaml](./pvc.yaml) 참고

# override_valeus.yaml
* [values.yaml](./values.yaml)파일 참고

# 설치
```sh
helm install -n infra -f values.yaml grafana grafana/grafana
```

# 초기 비밀번호
```sh
kubectl get secret --namespace infra grafana -o jsonpath="{.data.admin-password}" | base64 --decode ; echo
```

# 참고자료
* 공식문서: https://github.com/grafana/helm-charts/blob/main/charts/grafana/README.md
* https://medium.com/@kevincoakley/reusable-persistent-volumes-with-the-existingclaim-option-for-the-grafana-prometheus-operator-84568b96315
* nginx-ingress 공식문서: https://kubernetes.github.io/ingress-nginx/examples/rewrite/#rewrite-target
* https://www.jacobbaek.com/1175