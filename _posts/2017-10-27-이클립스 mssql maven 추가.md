---
layout: post
title: "이클립스 mssql maven 추가"
excerpt_separator: "<!--more-->"
categories:
  - 개발팁
tags:
  - 이클립스
  - maven
  - mssql
last_modified_at: 2017-10-27T15:33:37-04:00
---

```
maven com.mssql:sqljdbc4:jar:1.0
```


이클립스에 mave install 시 에러 발생..
레파지토리에서 lib를 못가져오는 상황
로컬에 추가한다. 

<!--more-->

## 절차
* JAR 다운로드(https://www.microsoft.com/ko-kr/download/confirmation.aspx?id=11774) 
* mave jar 추가 
* pom.xml 확인 
* maven install


### 이클립스에서 jar를 추가한다. 
<img alt="jar 추가 home page" src="/assets/images/eclipse-import-maven-jar.png" width="300px" />

### 등록한 jar를 pom.xml에 설정한다. 
```
		<dependency>
    		<groupId>com.microsoft.sqlserver</groupId>
    		<artifactId>sqljdbc4</artifactId>
    		<version>4.0</version>
   		</dependency>
```		
 
### maven install 확인 
```
[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
[INFO] Total time: 6.123 s
[INFO] Finished at: 2017-10-27T17:16:21+09:00
[INFO] Final Memory: 45M/345M
[INFO] ------------------------------------------------------------------------

``` 