---
layout: post
title: Linux Shell 프로그래밍 팁
category: linux
tags: [bash, shell]
---
### 확장자를 뺀 파일명 얻기

```
$ basename -s .{확장자} {파일명(경로포함)}
```

### 환경 변수

* 환경 변수 설정: ```$ export {변수명}={변수값}```
* 환경 변수 제거: ```$ unset {변수명}```
* 환경 변수 보기: ```$ env```
