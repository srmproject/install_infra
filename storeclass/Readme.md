# 개요
* storageclass 정의

# 내용
## local-storage 리소스 생성
* 
```sh
apiVersion: storage.k8s.io/v1
kind: StorageClass
metadata:
  name: local-storage-retain
reclaimPolicy: "Retain"
provisioner: kubernetes.io/no-provisioner
volumeBindingMode: WaitForFirstConsumer
```
