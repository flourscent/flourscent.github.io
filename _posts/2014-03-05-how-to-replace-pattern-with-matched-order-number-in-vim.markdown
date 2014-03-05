---
layout: post
title:  "vim 에서 패턴을 텍스트 내에서 일치한 순서의 번호로 subsitute 하기"
date:   2014-03-05 10:10:00
categories: hack
---

요즘 텍스트 파일을 수정할 일이 많은데, 특정 패턴을 나타나는 순서대로 번호로 바꾸어야 하는 경우가 있었다. 
그렇게 긴 텍스트 파일은 아니라 손으로 했어도 됐겠지만, 웬지 방법이 있을 것 같아 몇번 검색을 해서 나온 커맨드를 약간 수정하여 원하는 결과를 얻을 수 있었다.  

{% highlight sh %}
:let counter=0|g/패턴/let counter=counter+1|s/^\n/\="번호앞패턴".counter."번호뒤패턴"
{% endhighlight %}

설명은 나중에 추가하겠음.
