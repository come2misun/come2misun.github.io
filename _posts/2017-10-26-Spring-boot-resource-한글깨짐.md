---
layout: post
title: "Spring Boot Resource 한글깨짐"
excerpt_separator: "<!--more-->"
categories:
  - 개발팁
tags:
  - Spring Boot
last_modified_at: 2017-03-23T15:33:37-04:00
---

다른 웹어플리케이션에서 가져온 html의 한글이 깨지는 현상이 발견돼었다.
```
<ng-include src="'/public/app/html/rms/drctMng/module/DRCT.RECIPES.html'"></ng-include>
```

<!--more-->
```java
public class WebSecurityConfig extends WebSecurityConfigurerAdapter {

    @Override
    protected void configure(HttpSecurity http) throws Exception {
        
		//여기를 삽입하니까 해결됨..
    	CharacterEncodingFilter filter = new CharacterEncodingFilter();
        filter.setEncoding("UTF-8");
        filter.setForceEncoding(true);
        http.addFilterBefore(filter,CsrfFilter.class);
        //여기를 삽입하니까 해결됨..
		
		
        http
        	.csrf().disable()
            .authorizeRequests()
            	.antMatchers( "/home", "/login").permitAll()
            	.antMatchers( "/cmm").hasRole("ADMIN")
            	.anyRequest().authenticated()
            	.and()
....
    }
	...
}
```