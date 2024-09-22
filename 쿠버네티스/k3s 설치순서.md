## 준비
> sudo apt-get update
> sudo apt-get install -y curl

*******

## <b>도커 준비</b>

## docker 설치
> sudo apt install docker.io 

## docker 서비스 시작
> sudo systemctl start docker

## 부팅시 docker 서비스 시작
> sudo systemctl enable docker

*******

## k3s 설치 스크립트
> curl -sfL https://get.k3s.io | sh -
 
## 설치 되어있는지 확인
> sudo systemctl status k3s

## 노드 확인
> sudo kubectl get nodes

#### 마스터 노드 존재
NAME           STATUS   ROLES                  AGE    VERSION
<br>
raspberrypi1   Ready    control-plane,master   8m8s   v1.28.8+k3s1

## node-token 값 확인
> sudo cat /var/lib/rancher/k3s/server/node-token
<br>
나온 내용 전부를 복사 

## 워크 노드 만들기
> curl -sfL http://get.k3s.io | K3S_URL=https://<service-ip>:6443 K3S_TOKEN=<token값> sh -s - --docker

워크 노드에서 오류가 남....

## 삭제관련
> sudo /usr/local/bin/k3s-uninstall.sh

## 남은파일 삭제
> sudo rm -rf /etc/rancher/k3s /etc/systemd/system/k3s* /usr/local/bin/k3s*
