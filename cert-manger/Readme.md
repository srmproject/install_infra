# helm 저장소 추가
```sh
helm repo add cert-manager https://charts.jetstack.io
helm repo update
```

# helm 차트 설치
```sh
helm install \
cert-manager cert-manager/cert-manager \
--namespace cert-manager \
--create-namespace \
--version v1.6.1 \
--set installCRDs=true
```

# 참고자료
* cert-manager helm 공식문서: https://artifacthub.io/packages/helm/cert-manager/cert-manager
* helm 설치: https://itnext.io/setting-up-self-signed-https-access-to-local-dev-k8s-cluster-in-minikube-539bc62ad62f
* helm 설치: https://docs.solo.io/gloo-mesh-enterprise/main/setup/certs/aws-certs/acm-cert-manager/
* helm arguments: https://issueexplorer.com/issue/jetstack/cert-manager/4405