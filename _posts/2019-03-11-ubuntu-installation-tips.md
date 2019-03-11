---
layout: post
title: Ubuntu 설치 팁
categories: [linux]
tags: [ubuntu, apt-get, wireless]
---

## 업데이트 저장소 변경

우분트 업데이트 저장소를 **ubuntu** 에서 **kakao**(kr) 로 변경

~~~
sudo vi /etc/apt/sources.list
~~~

* vi 에서 입력
~~~
:%s/archive.ubuntu.com/mirror.kakao.com/c
~~~


## 시스템 업데이트

~~~
sudo apt-get update && sudo apt-get -y upgrade
~~~

<!--excerpt-->

## 무선랜 설정

### STEP 1: 필요한 패키지 설치

~~~
sudo apt-get install wpasupplicant wireless-tools ifupdown
~~~

### STEP 2: 무선랜 장치 확인

~~~
ip link
~~~

### STEP 3: 무선랜 장치 구동

~~~
sudo ifconfig {무선랜 장치명} up
~~~

### STEP 4: 접속 가능 무선네트워크 확인 (ESSID 확인)

~~~
sudo iwlist {무선랜 장치명} scan
~~~

### STEP 5: 네트워크 설정 파일 수정

~~~
sudo vi /etc/network/interfaces
~~~

* **/etc/network/interfaces** 파일에 추가
~~~
auto {무선랜 장치명}
iface {무선랜 장치명} inet dhcp
        wpa-ssid "{ESSID: 무선네트워크명}"
        wpa-psk "{비밀번호}"
~~~

### STEP 6: 네트워크 재시작

~~~
sudo service networking restart
~~~

### STEP 7: 네트워크 정보 확인

~~~
ip addr
~~~


## 네트워크 설정으로 인한 부팅 지연 시 해결 방법

부팅 시 네트워크 설정을 대기하지 않도록 설정

~~~
sudo systemctl disable systemd-networkd-wait-online.service
sudo systemctl mask systemd-networkd-wait-online.service
~~~
