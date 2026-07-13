# 도커

## 컨테이너

컨테이너는 호스팅 컴퓨터에서 하는거

이미지는 다운받는거 dockerhub에서 

tag명은 이미지의 version을 나타내는 단어

## 도커 이미지 명령어

도커 이미지 다운로드 명령어

```
# 문법
docker pull <IMAGE>:<TAG>

# 예시
docker pull ngnix
docker pull ngnix:latest
docker pull ngnix:stable-alpine3.19-perl
```

도커 이미지 조회 명령어
```
docker image ls
```

도커 이미지 삭제 명령어
```
# 문법
docker image rm <IMAGE ID>

# 예시
docker image rm 456c0c9bd0d4
```


## 도커 컨테이너 명령어
도커 컨테이너 만드는 명령어
```
docker create <IMAGE>
```

도커 컨테이너 조회 명령어
```
docker ps -a
```


도커 컨테이너 실행 명령어
```
# 문법
docker start <CONTAINER ID>

# 예시
docker start 1090f2a3b320
```


도커 컨테이너 만들고 실행하는 명령어(create & start)
```
# 문법
docker run <IMAGE>

# 예시
docker run -it --rm -v $PWD:/data rsactftool/rsactftool <arguments>
docker run -d -v ollama:/root/.ollama -p 11434:11434 --name ollama ollama/ollama
```


docker build -t rsactftool/rsactftool .


