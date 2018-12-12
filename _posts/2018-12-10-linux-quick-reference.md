---
layout: post
title: 간략한 Linux 사용법
category: linux
tags: [sudo, adduser, usermod, groups]
---

## 유저 관리

1. 유저 추가

    $ sudo adduser {계정명}

2. sudo 권한 부여

    $ sudo usermod -G sudo {계정명}

3. 유저 그룹 보기

    $ groups

