$ kubectl create secret docker-registry docker-pull-secret \
--docker-server=https://index.docker.io/v1/ \
--docker-username=myid \
--docker-password=mypassword \
--docker-email=myemail@example.com \
-n inferno


inferno 이미지에 접근 권한이 있는 docker 계정 인증 정보를 secret으로 등록 후 helm install


$ helm install my-inferno . --namespace inferno --create-namespace


삭제 시에는


$ helm delete my-inferno --namespace inferno
