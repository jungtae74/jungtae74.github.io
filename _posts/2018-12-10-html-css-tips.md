---
layout: post
title: HTML 과 CSS 팁 모음
category: web
tags: [html, css]
---

### id 와 class 속성 차이

* id 속성
 : 단일 태그에 속성을 부여한다.
 : CSS 형식: `#id { ... }`

* class 속성
 : 복수(그룹) 태그에 속성을 부여한다.
 : CSS 형식: `.class { ... }`

### \<div\> 와 \<span\> 태그 차이

* \<div\> 태그
 : 단락 단위로 묶을 때 사용
 : 태그(단락)가 끝날 때 줄바꿈이 기본값

* \<span\> 태그
 : 개별 요소(Element, 또는 단어) 단위로 묶을 때 사용
 : 태그가 끝날 때 줄바꿈 없음

* \<div\>가 \<span\> 보다 상위 집합으로 볼 수 있음

### CSS 계층적 구조

* Descendant Selector
 : 형식: `tag1 tag2 { ... }`
 : 공백(space) 로 구분, `tag1` 에 포함된 모든 `tag2` 선택 (계층 깊이에 상관 없음)

* Child Selector
 : 형식: `tag1 > tag2 { ... }`
 : `>` 로 구분, `tag1` 아래에 포함된 `tag2`만 선택 (자식 태그만 선택, 계층 깊이를 주의해야 함)

* 참고> [CSS Combinators](http://www.w3schools.com/css/css_combinators.asp)

### 웹 아이콘 폰트

* 링크1> [Font Awesome Icons (Free)](https://fontawesome.com/icons?d=gallery&m=free)
  * [Cheatsheet](https://fontawesome.com/cheatsheet)
  * [Font Awesome's Free CDN Link (HTML Tag)](https://fontawesome.com/start)

* 링크2> [Bootstrap - Glyphicons](http://getbootstrap.com/components/#glyphicons)

### HTML 레퍼런스

* [Enter HTML5 structural elements](https://www.w3.org/wiki/HTML_structural_elements#Enter_HTML5_structural_elements)

* [HTML Element Reference](http://www.w3schools.com/tags/)

* [HTML Color Names](http://www.w3schools.com/tags/ref_colornames.asp)
