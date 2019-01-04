---
layout: post
title: 간략한 Linux 사용법
category: linux
tags: [user, group, process, kill, nohup]
---

## 유저 관리

 1. 유저 추가
    ~~~
    $ sudo adduser {계정명}
    ~~~

 2. sudo 권한 부여
    ~~~
    $ sudo usermod -G sudo {계정명}
    ~~~

 3. 유저 그룹 보기
    ~~~
    $ groups
    ~~~

## 프로세스 관리

 1. 백그라운드 실행
    ~~~
    $ nohup {명령어} &

    $ tail -f {파일명}
    ~~~

 1. 프로세스 정보 확인
    * 참고 링크: <https://zetawiki.com/wiki/%EB%A6%AC%EB%88%85%EC%8A%A4_ps>

    * 프로세스 정보 확인1

      PID, CPU/MEM 사용률, 프로세스 상태코드 표시
      ~~~
      $ ps aux
      ~~~

    * 프로세스 정보 확인2

      PID, PPID 표시
      ~~~
      $ ps -ef
      ~~~

    * 프로세스 정보 확인(계층구조)
      ~~~
      $ pstree
      ~~~

    * 프로세스 이름으로 PID 찾기
      ~~~
      $ pgrep {프로세스명}

      $ pidof {프로세스명}
      ~~~

 1. 프로세스 강제 종료
    ~~~
    $ kill -9 `pidof {프로세스명}`

    $ pkill {프로세스명}

    $ killall {프로세스명}
    ~~~
