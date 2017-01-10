---
layout: post
title:  170110 JSP
date:   2017-01-10 18:15:29 +0900
categories: basic
---

## Code

Bad

``` js
var type = "${param.type}"; 
```
Good

``` js
var type = setDecode2("<c:out value="${param.type}" />");
```
DECODE HASH

``` js
function setDecode2(formNm)
{
	formNm = formNm || "";
    return formNm.replace(/&amp;/g, "&")
                        .replace(/&lt;/g, "<")
                        .replace(/&gt;/g, ">")
                        .replace(/&quot;/g, "\"")
                        .replace(/&#039;/g, "`")
                        .replace(/&#034;/g, "\"");
}
```

## 테이블 테스트

| 테스트 	 | 설명 		   				|
| ------ | -------------------------|
|1   	 | 안녕하세요. 					|
|2		 | 마크다운 언어로 작성하는 테이블 입니다.| 
|3		 | 상당히 어렵습니다.				|