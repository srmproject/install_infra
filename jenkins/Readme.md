# 개요
* 젠킨스 설치 메뉴얼입니다.

<br>

# ingress 설정
* subpath 설정

# 설치
> 빠른 개발을 위해 helm을 사용하지 않았습니다.
* persistentvolume은 hostpath를 사용하고 Retain정책을 갖습니다.
* 젠킨스 컨테이너 이미지는 커스텀을 사용했습니다.
    * 커스텀이지미: choisunguk/jenkins:jdk11
* node2을 대상으로 nodeselector을 사용했습니다.

# 참고자료
* https://stackoverflow.com/questions/45959056/change-jenkins-container-deployment-root-path
* https://stackoverflow.com/questions/51751462/nginx-ingress-jenkins-path-rewrite-configuration-not-working
* jenkin helm subpath: https://github.com/jenkinsci/helm-charts/blob/main/charts/jenkins/templates/jenkins-controller-statefulset.yaml#L190