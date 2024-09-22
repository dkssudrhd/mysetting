
## 도커 이미지 만드는 방법
1. 사용하는 컨테이너에서 commit을 사용
2. 도커 파일을 작성하여 만들기
- 도커 파일을 빌드

> 커밋은 백업과 같은 느낌이 있고
>
> 빌드는 이미지를 새로 생성하는 느낌

#### 우분투 이미지 실행
```bash
docker run --name web-server -it ubuntu:20.04
```

#### commit 만들기
```bash
docker commit web-server web-server-commit
```

```Dockerfile
RUN apt update && intstall -y python3
```
> &&의 경우 앞에 있는 명령어가 실행되고 성공하면 뒤에 명령어가 실행

#### dokcer에서 디렉토리 만들기 + 이동하기
```Dockerfile
WORKDIR /var/www/html
```

### 명령어 실행
```Dockerfile
CMD ["python3", "-u", "-m", "http.server"]
```

### docker 컨테이너 삭제
```bash
docker rm --force web-server
```

### 도커 빌드
```bash
docker build -t web-server-build .
```

### 참고
> https://www.youtube.com/watch?v=0kQC19w0gTI