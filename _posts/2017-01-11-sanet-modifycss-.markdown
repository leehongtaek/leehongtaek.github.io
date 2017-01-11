---
layout: post
title:  Change CSS list
date:   2017-01-11 11:00:00 +0900
categories: work
---

### 상아넷 디자인 변경

+메인 화면 css변경
+로그인 화면 css변경
+메뉴구성 재검토 및 모듈검증
+새로운 메신저와의 소켓통신 확인 후 모듈수정

## 상아넷 수정사항
Login
:temp_image 삭제

Main
:메인에서 디자인 변경이 필요한 요소들이 있음.[Main - user profile picture](http://www.bypeople.com/css-profile/  "고고")

Modules
:기타 모듈들이 정상적으로 작동하는지 체크 후 디자인 변경. (STANDARD 기준으로)

# 상아넷 추후 작업예정
많음. 많다!

###### 인용문구 쓰는법
>이것은 인용문을 쓸 때 사용하는 것입니다.
> '>'을 넣으면 자동적으로 indent가 됩니다.
>>경우에 따라서 아주 많은 곳에서 좋은 소스를 참고하여 이 페이지에 저장할 때 주로 쓰이게 될 것입니다.
>
>Markdown 문법 적응을 위해 연습으로 작성 중인 텍스트 입니다.

>### Header에서도 인용문이 적용되는지 Test
>
>Sangah
>
>Management
>
>Colsulting
>
>Yeah!

#### 리스트를 표현해 봅시다.
1. 번호식
2. 으로도
3. 표현가능

- 이렇게
- 표시도
- 가능합니다.

Note These are some changes required to correct some of the problems above:
{% highlight javascript %}
\$\(document\)(\.on\(["'].*["'],[\s]*function\()(?:[\s]*e,[\s]*)?(.*\)) => pmis$1$2
(\$\([\s]*window[\s]*\)\.on\(["'])resize(\..*)?(["'],[\s]*function\(.*\)) => $1resize.pmis$3
(\$\([\s]*window[\s]*\)\.)resize\(([\s]*function[\s]*\(\)) => $1on('resize.pmis', $2
{% endhighlight %}
You should replace the left regular expression with the right replacement string