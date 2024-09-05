젠킨스 공식 홈페이지

> https://www.jenkins.io/doc/book/installing/linux/

```bash
sudo wget -O /usr/share/keyrings/jenkins-keyring.asc \
  https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key
echo "deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc]" \
  https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null
sudo apt-get update
sudo apt-get install jenkins
```

### 시작 및 설치 완료 확인
```bash
sudo systemctl start jenkins
sudo systemctl status jenkins
```
> error가 없다면 잘 성공한 것이다.

### 포트에서 잘 돌아가는지 확인
```bash
sudo netstat -tnlp
```
