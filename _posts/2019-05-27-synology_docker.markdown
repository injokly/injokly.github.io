---
layout: post
title:  "시놀로지에서 도커세팅하기"
date:   2019-05-27 00:22:33 +0900
categories: jekyll update
---
 
synology docker 세팅

ssh 로 터미널 접속
$ sudo su - 		//root 로 접속

pull 레지스트리
이미지 실행 -> 높은 권한으로 실행 클릭  -> 고급설정
- 볼륨 : 폴더추가 -> 로컬에 저장되있는 폴더추가, 마운트경로는 docker container에서 쓸 파일명으로 생성. 보통 로컬에서 하위 디렉토리 명과 일치하게 만듬
- 포트설정 : 로컬포트- 외부에서 접속할 포트번호, 컨테이너포트-컨테이너 포트번호
- 환경 : 실행명령 dockerfile에서 CMD 에 쓰이는 실행명령어 입력 (ex. node app.js)

$ docker exec -it container-id /bin/bash    //떠잇는 컨테이너 접속, exit 종료,



참고

https://www.raywenderlich.com/9159-docker-on-macos-getting-started
