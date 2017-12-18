---
layout: post
title: "Spring Boot : Upload 서비스 구현"
categories:
  - 개발팁
tags:
  - spring boot 
excerpt_separator:  <!--more-->
---

파일 업로드 서비스 구현 샘플
<!--more-->


## MultipartFile 설정 
A representation of an uploaded file received in a multipart request.
The file contents are either stored in memory or temporarily on disk.
In either case, the user is responsible for copying file contents to a session-level or persistent store as and if desired. 
The temporary storages will be cleared at the end of request processing.

```
package org.springframework.web.multipart

public interface MultipartFile extends InputStreamSource {

}
``` 


## 참고자료
* [스프링 가이드 : Uploading Files](https://spring.io/guides/gs/uploading-files/)
 