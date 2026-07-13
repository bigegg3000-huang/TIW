# 도커

## 용어정리

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
docker create <IMAGE>:<TAG>
```

도커 컨테이너 조회 명령어
```
docker ps -a
```
+ ps는 실행 중인 컨테이너만 조회한다.
+ ps **-a**는 중단된 컨테이너도 같이 조회한다


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
docker run <IMAGE>:<TAG>

# 예시
docker run -it --rm -v $PWD:/data rsactftool/rsactftool <arguments>
docker run -d -v ollama:/root/.ollama -p 11434:11434 --name ollama ollama/ollama
```
+ docker run은 foreground에서 실행되는데 background에서 실행하고 싶으면 **-d** 옵션으로 실행하면 됨
+ docker를 실행하면 80번 포트로 실행되는데 포트를 연결하기 위해서는 **-p <호스트포트>:<컨테이너포트>** 옵션으로 실행하면 됨


도커 컨테이너 중단 명령어
```
# 문법
docker stop <CONTAINER ID>
docker kill <CONTAINER ID>

# 예시
docker stop 1090f2a3b320
```

도커 컨테이너 삭제 명령어
```
# 문법
docker rm <CONTAINER ID>

# 예시
docker rm 1090f2a3b320
```
+ 도커 컨테이너 삭제는 중단 후에만 가능함


docker build -t rsactftool/rsactftool .


