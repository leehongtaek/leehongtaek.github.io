---
layout: post
title:  170110 JSP
date:   2017-01-10 18:15:29 +0900
categories: basic
---
Bad
``` js
var type = "${param.type}"; 

Good
``` js
var type = setDecode2("<c:out value="${param.type}" />");

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