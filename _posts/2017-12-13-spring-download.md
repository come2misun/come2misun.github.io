---
layout: post
title: Spring Boot :: Download 서비스 구현
categories:
  - 개발팁
tags:
  - spring boot 
excerpt_separator:  <!--more-->
---

파일 다운로드 서비스 구현 샘플
<!--more-->


## Response 설정 
```java
Response.AddHeader("Content-Disposition", "attachment;filename=somefile.ext")


Response.AddHeader("Content-Disposition", "inline;filename=somefile.ext")
```

## 참고자료
* [샘플소스](https://www.boraji.com/spring-mvc-4-file-download-example)
* [Content-Disposition](https://stackoverflow.com/questions/1395151/content-dispositionwhat-are-the-differences-between-inline-and-attachment)
* [MIME 타입](https://developer.mozilla.org/ko/docs/Web/HTTP/Basics_of_HTTP/MIME_types)
