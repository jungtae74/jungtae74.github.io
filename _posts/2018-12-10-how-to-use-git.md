---
layout: post
title: git 사용법
categories: [Tools]
tags: [git, ssh]
---

## 변경 사항 확인하기

 * `git diff [파일명]`
  : 해당 파일의 변경 사항 보기 (Unstaged 상태)

 * `git diff --cached` or `git diff --staged`
  : Staged 상태의 파일 변경 사항 보기

 * `git show {COMMIT}`
  : 커밋된 파일 변경 사항 보기

## 되돌리기

 * `git checkout -f`
  : 변경된 모든 파일 되돌리기

 * `git reset HEAD^`
  : 최종 커밋 취소

<!--excerpt-->

## 커밋 로그 보기

 * `git log --name-status -1`
  : 커밋된 파일 목록 보기(상태 정보 포함)

## Push 안한 커밋 보기

 * `git log --branches --not --remotes`
  : 원격지(remote)에 없는 모든 커밋 보기1 (표준 형식: Author, Date, Commit message)

 * `git log --branches --not --remotes --oneline --graph --decorate`
  : 원격지(remote)에 없는 모든 커밋 보기2 (간략 형식: Commit hash, Lable, Commit message)

## 참고 링크

 * [Git 의 기초 - 되돌리기](https://git-scm.com/book/ko/v2/Git%EC%9D%98-%EA%B8%B0%EC%B4%88-%EB%90%98%EB%8F%8C%EB%A6%AC%EA%B8%B0)

 * [작업 취소하기](http://ecogeo.tistory.com/276)

 * [SSH Agent 사용하기](https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/#adding-your-ssh-key-to-the-ssh-agent)

