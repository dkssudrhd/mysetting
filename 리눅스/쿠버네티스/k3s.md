
### k3s 제거
> sudo rm -rf /var/lib/rancher/k3s
> sudo /usr/local/bin/k3s-uninstall.sh

### k3s 설치
> curl -sfL https://get.k3s.io | sh -


### 상태확인
> sudo systemctl status k3s.service
