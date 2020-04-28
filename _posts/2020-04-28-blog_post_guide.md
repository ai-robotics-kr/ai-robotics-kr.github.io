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

Markdown 문법에 관련된 내용은 아래 사이트를 참조하시면 됩니다.

[Ref] https://gist.github.com/ihoneymon/652be052a0727ad59601



## 포스트 작성하기

ㅍ

```
git status

git add 파일명
git add .

git commit -m "커밋메세지"

git push origin master
```

이제는 http://ai-robotics-kr.github.io/ 에서 확인 가능합니다. 

git 이 없다면, 패키지 관리자 brew 를 이용해서 git 을 설치합니다. 
```
brew install -s git
```

깃이 설치 되었는지 아래 명령어로 확인합니다. 

```
git --version
```

![]({{ site.url }}/images/mac-inst₩all/5.png)

## 템플릿 가져오기

템플릿을 가져오기 전 cd 명령어를 이용해 작업할 폴더로 이동해 주세요.

예를 들어 아래 폴더라면 경로는 **F:\python\page**가 됩니다.

```
cd F:\python\page
```

아래 명령어로 템플릿을 가져옵니다.

clone 명령을 사용하기 전 폴더를 다시한번 확인해 주세요.

현재 폴더 내에 새로운 폴더가 생성됩니다.

```
git clone https://github.com/ai-robotics-kr/ai-robotics-kr.github.io.git
```

새로 생성된 폴더로 이동하여 아래 명령어로 필요한 패키지를 설치해 줍니다.

```
cd ai-robotics-kr.github.io   

bundle install
```

현재 페이지의 상태를 배포하기 전에 확인해 줍니다.

** bundle install 에서 아래과 같은 에러가 난다면

![]({{ site.url }}/images/mac-install/6.png)

해당 명령어로 업데이트 해준 후 다시 시도합니다.

```
bundle update --bundler
```
![]({{ site.url }}/images/mac-install/7.png)


이제 다 되었습니다! 블로그를 서빙해줍니다!

```
bundle exec jekyll serve
```

![]({{ site.url }}/images/mac-install/8.png)


만약 에러가 난다면 아래 패키지들을 설치해 주세요.

```
gem install tzinfo-data
gem install jekyll-seo-tag
gem install jekyll-admin
```

인터넷 창 열고 127.0.0.1:4000 를 클릭하면 해당 블로그를 볼수 있습니다. 


![]({{ site.url }}/images/window-install/13.png)

확인 후 글을 배포하기 위해 아래 git 명령어를 입력해 주세요.

```
git status

git add 파일명
git add .

git commit -m "커밋메세지"

git push origin master
```

이제는 http://ai-robotics-kr.github.io/ 에서 확인 가능합니다. 



