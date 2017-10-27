---
layout: post
title: "Spring Boot 프로퍼티"
excerpt_separator: "<!--more-->"
categories:
  - 개발팁
tags:
  - Spring Boot
last_modified_at: 2017-10-26T15:33:37-04:00
---

Spring Boot 프로퍼티 만들기 

## 절차
* 프로퍼티 클래스 작성 
* 프로퍼티 활성화 
* 프로퍼티 설정 
* 프로퍼티 사용 


### 프로퍼티 클래스 작성 
```java


@Validated
@ConfigurationProperties("test.cust")
public class Test1Properties implements Serializable{

	private static final long serialVersionUID = 1L;

	/** 모드 */
	@NotEmpty
	private String mode ;
	
	/** 버전*/
	@NotEmpty
	private String version ;
	
	/** */
	@NotEmpty
	private String siteVersion ;

}

```

### 프로퍼티 활성화 
```

@Configuration
@EnableConfigurationProperties({Test1Properties.class, Test2Properties.class})
public class AppConfig {
	private static final Logger logger = LoggerFactory.getLogger(AppConfig.class);
	
 
}

```

### 참고자료
* [24. Externalized Configuration](https://docs.spring.io/spring-boot/docs/current/reference/html/boot-features-external-config.html)