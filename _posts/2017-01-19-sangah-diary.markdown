---
layout: post
title:  JAVA
date:   2017-01-19 12:00:00 +0900
categories: Diary
---

## Java

{% highlight javascript %}
public Document() {
		super();
	}

public Document(Map container) {
		super(container);
	}

public boolean hasTag( String searchtag ){
	if( Strings.isBlank(searchtag) ) return false;
	
	String tags = getMapValue( DB_FIELD_TAGS );
	if( Strings.hasText( tags ) ) {
		String[] t = tags.split("\\s*,\\s*");
		for (int i = 0; i < t.length; i++) {
			String tag = t[i];
			if( tag.equals( searchtag ) ) {
				return true;
			}
		}
	}
	return false;
}
{% endhighlight %}

## JSP

{% highlight javascript %}
<c:if test="${bod.hasTag('withacl')}">
			<tr>
          	<th class="label_top"><label><sangah:msg id='label.1705'/></label></th>
          	<td colspan="7">
          		<input type="hidden" name="issueForm.privacy" value="2" >
          		<div style="margin: 10px 0;"><%@ include file="/pmis/STND_PMIS/board/issue/IssueAccess.jsp"%></div>
          	</td>
          </tr>
          </c:if>
{% endhighlight %}  