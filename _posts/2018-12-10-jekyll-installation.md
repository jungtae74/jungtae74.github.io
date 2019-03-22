---
layout: post
title: Jekyll 설치 및 실행
category: jekyll
tags: [gem, bundle]
---

## 설치 요구 사항

 1. 필요한 패키지 설치
    ~~~
    $ sudo apt-get install ruby-full build-essential zlib1g-dev
    ~~~

 1. 환경변수 설정
    ~~~
    $ echo >> ~/.bashrc
    $ echo '# Install Ruby Gems to ~/gems' >> ~/.bashrc
    $ echo 'export GEM_HOME="$HOME/gems"' >> ~/.bashrc
    $ echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.bashrc
    $ echo >> ~/.bashrc
    $ source ~/.bashrc
    ~~~

 1. 참고 링크
    * <https://jekyllrb.com/docs/installation/ubuntu/>

<!--excerpt-->

## Jekyll 설치

 1. Gem(Ruby) 업데이트 (필요한 경우)
    ~~~
    $ sudo gem update --system
    ~~~

 1. Jekyll 설치 (선택)

    * 선택1: __GitHub__ 호스팅을 위한 패키지 설치
    ~~~
    $ sudo gem install github-pages bundler
    ~~~

    * 선택2: 일반 설치 과정
    ~~~
    $ sudo gem install jekyll bundler
    ~~~

## Blog(site) 생성 & 실행, 설정 업데이트

 1. Blog 생성
    ~~~
    $ jekyll new myblog
    ~~~

 1. Blog 실행
    ~~~
    $ cd myblog

    $ bundle exec jekyll serve --host 192.168.0.10 --port 4000 --watch --safe
    ~~~
    * 옵션
      * --watch : 문서 변경(추가, 수정, 삭제) 시 자동 생성한다.
      * --safe : 커스텀 플러그인이나 심볼 링크 사용을 금지한다. (github-pages 호스팅을 위한 옵션)
      * --drafts : _drafts 디렉토리 문서도 생성한다.

 1. Blog 설정 업데이트

    **설정 파일(Gemfile)을 수정한 경우** Blog 실행 전에 설정 업데이트.
    ~~~
    $ cd myblog

    $ bundle update
    ~~~

## Jekyll 정보

 * jekyll 버전 확인
   ~~~
   $ jekyll --version
   ~~~

## RubyGems 사용법

 * 참고 링크
   * [RubyGems Command Reference](https://guides.rubygems.org/command-reference/)

 * 설치된 패키지 보기 (예: jekyll 단어 포함)
   ~~~
   $ gem list jekyll
   ~~~

 * 설치 가능한 패키지 보기 (예: jekyll 단어 포함)
   ~~~
   $ gem search jekyll --remote
   ~~~

 * 설치된 패키지 업데이트 (예: jekyll 패키지)
   ~~~
   $ sudo gem update jekyll
   ~~~

 * 설치된 패키지 삭제 (예: jekyll 패키지)
   ~~~
   $ sudo gem uninstall jekyll
   ~~~

