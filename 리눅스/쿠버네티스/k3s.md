
### k3s 제거
> sudo rm -rf /var/lib/rancher/k3s
> sudo /usr/local/bin/k3s-uninstall.sh

### k3s 설치
> curl -sfL https://get.k3s.io | sh -


### 상태확인
> sudo systemctl status k3s

### 재시작
> sudo systemctl restart k3s

### k3s 설정확인
>  sudo cat /etc/rancher/k3s/k3s.yaml

### 실행중인 node 보기 
> sudo kubectl get node -o wide

### 클러스터 정보 보기
> sudo kubectl cluster-info
