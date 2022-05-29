# 개요
* JCP 앱 배포

# front-end core
## 배포방법
* `kustomize`로 공통 템플릿을 관리하고 `argocd`로 배포
* kustomized템플릿 stdout출력 
```sh
git clone https://github.com/srmproject/JCP-Front-Core.git
# 개발환경
kubectl kustomize ./dev
```

## nodeselector
* nfs서버가 없어서 특정노드(`node2`)의 hostpath로 관리
* 노드 라벨 설정
```sh
kubectl create label node role=infra
```
