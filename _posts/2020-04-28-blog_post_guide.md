---
layout: post
title: "Github Blog Post 작성하기"
description: "Github Blog Post 작성하기"
author: stella
date: 2020-04-28
tags: [presentation, airoboticskr, TechTalk]
comments: true
subdir: presentation
thumbnail: mot_logo.jpg
share: true
---

# Blog Post 작성하는 법

ai robotics kr 의 블로그에 글을 포스팅 하는 법을 소개합니다.


## jekyll 을 os 에 맞게 설치하기

먼저, 앞에 글들인 

1. window 에서 jekyll 설치하기
2. mac 에서 jekyll 설치하기

를 참고해서 jekyll 을 os에 알맞게 설치해줍니다. 

## 포스트 작성 환경 설치 (IDE, Markdown)

git clone 한 코드를 editor 로 열어줍니다. 

저는 주로 pycharm 을 사용합니다.
저희 Github blog 는 markdown 을 이용하여 작성합니다.
markdown 문법으로 작성하며 preview 하면서 작성하면 좋기 때문에
저는 pycharm 에서 지원하는 markdown plugin 을 사용합니다.
이외에 여러 markdown IDE 가 존재하니, 원하시는 에디터를 사용하셔서
포스트를 작성하시면 되겠습니다.

![]({{ site.url }}/images/user-install/9.png)

## 포스트 작성하기

포스트를 쓰기 위해서는 _post 폴더 내에 design 에 아래와 같은 이름의 md 파일을 작성합다. 

```
YYYY-MM-DD-제목(underbar 띄어쓰기).md
예 : 2020-03-09-jekyll_install_window.md
```
이제 해당 .md 파일에 포스트를 작성할 수 있습니다.

제일 윗부분에 포스트에 관련된 정보를 반드시 기입하고 시작합니다.

```

---
layout: post
title: "포스트 제목"
description: "포스트에 대한 한줄 설명"
author: 저자이름
date: YYYY-MM-DD
tags: [달고싶은태그1, 달고싶은태그2, 달고싶은태그3]
comments: true
subdir: presentation
thumbnail: mot_logo.jpg
share: true
---

```

그 다음은 원하는 포스트 내용을 마음 껏 작성 하시면 됩니다.

작성 문법은 위에서 언급드린 markdown 문법을 사용합니다.

Markdown 문법에 관련된 내용은 아래 사이트를 참조하시면 됩니다.

[[Ref]https://gist.github.com/ihoneymon/652be052a0727ad59601](https://gist.github.com/ihoneymon/652be052a0727ad59601)
 


이미지를 삽입하고 싶으실 경우, 

images 폴더 내부 user install 폴더에 번호 순서에 맞게 이름을 바꾸어

png 파일을 추가해주신 후 아래와 같은 문법을 사용하여 이미지를 중간에

첨부해주시면 됩니다.

```
![]({{ site.url }}/images/user-install/1.png)
```

![]({{ site.url }}/images/user-install/10.png)

블로그에는 줄글로 설명하는 형식으로 포스팅을 작성하며,

발표자료는 Slide 로, Code 는 Github Code 로 가져와서 엮는 식으로

블로깅을 해 나가시면 됩니다. 모두 작성하셨으면 

git commit 및 pull request 해주시면 됩니다.

pull request 하시는 방법은 아래의 사이트를 참조해 주세요.


[[Ref]https://wayhome25.github.io/git/2017/07/08/git-first-pull-request-story/](https://wayhome25.github.io/git/2017/07/08/git-first-pull-request-story/)

[[Ref]https://velog.io/@zansol/Pull-Request-%EC%9D%B4%ED%95%B4%ED%95%98%EA%B8%B0](https://velog.io/@zansol/Pull-Request-%EC%9D%B4%ED%95%B4%ED%95%98%EA%B8%B0)
 

 
pull request 가 관리자에 의해서 승인되면, serving 되게 되고

이제는 http://ai-robotics-kr.github.io/ 에서 포스트를 확인 가능합니다. 


