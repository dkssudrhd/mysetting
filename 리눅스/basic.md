
### 사용중인 포트 확인하는 명령어

```bash
sudo netstat -tuln
```

### 사용중인 램 확인

```bash
free -h
```

### 권한 변경

```bash
sudo usermod -aG <권한을 변경할 명령어> ${USER}
groups ${user}
```

> reboot를 해야 적용이 된다.


### OS 버전 정보 확인

```bash
cat /etc/*release*
```

### clear 단축기

> 컨트롤 + L


### 새로운 유저 만들기
```bash
adduser ${USER_NAME}
```

> sodu 권한이 있어야 한다. 그리고 USER_NAME을 입력하고 그 이후에는 password를 입력한다.
