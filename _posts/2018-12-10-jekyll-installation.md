---
layout: post
title: Jekyll 설치 및 실행
category: jekyll
tags: [sudo, apt-get, gem, jekyll, bundle]
---

## 설치 요구 사항

1. 필요한 패키지 설치
~~~
$ sudo apt-get install -y ruby-full build-essential
~~~

2. 환경변수 설정
~~~
$ echo '# Install Ruby Gems to ~/gems' >> ~/.bashrc
$ echo 'export GEM_HOME=$HOME/gems' >> ~/.bashrc
$ echo 'export PATH=$HOME/gems/bin:$PATH' >> ~/.bashrc
$ source ~/.bashrc
~~~

3. 참고 링크
  * [https://jekyllrb.com/docs/installation/ubuntu/](https://jekyllrb.com/docs/installation/ubuntu/)


## Jekyll 설치

1. Gem(Ruby) 업데이트

    $ sudo gem update --system

1. Jekyll 설치1 (__GitHub__ 호스팅을 위한 패키지)

    $ sudo gem install github-pages

1. Jekyll 설치2 (일반 설치 과정)

    $ sudo gem install jekyll bundler

## Blog(site) 생성 & 실행

1. Blog 생성

    $ jekyll new myblog

1. Blog 실행

    $ cd myblog

    $ bundle exec jekyll serve --host 192.168.0.10 --port 4000 --watch --safe

## Jekyll 정보

* 버전 확인

    $ jekyll --version

* 설치된 패키지 보기

    $ gem list jekyll

* 설치 가능한 패키지 보기

    $ gem search jekyll --remote

* Jekyll 업데이트

    $ sudo gem update jekyll