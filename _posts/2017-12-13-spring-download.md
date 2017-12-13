---
layout: post
title: "Spring Boot :: Download 서비스 구현"
excerpt_separator: "<!--more-->"
categories:
  - 개발팁
tags:
  - spring boot 
last_modified_at: 2017-12-12T15:33:37-04:00
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
