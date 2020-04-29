---
layout: post
title: "윈도우에서 jekyll 설치하기"
description: "윈도우 10에서 Ruby, jekyll, git 설치하기"
author: bill
date: 2020-03-08
tags: [presentation, NAVER, TechTalk]
comments: true
subdir: presentation
thumbnail: mot_logo.jpg
share: true
---

windows 10 jekyll 설치방법

jekyll이란 텍스트를 정적 사이트(static websites)로 만들어주는 변환기(생성기)입니다.

ruby 기반으로 되어있어 jekyll을 사용하기 위해서는 ruby를 먼저 설치해야 합니다.

## RUBY 설치하기

아래 사이트에서 ruby를 다운로드 합니다.

[https://rubyinstaller.org/downloads/](https://rubyinstaller.org/downloads/)

2020/03/08 기준으로 ruby에서 추천하는 2.6.5-1 버전을 설치하였습니다.

다운로드 할 때 WITH DEVKIT 을 선택해야 합니다.

gem이라는 패키지 관리자(python의 pip)를 이용하기 위함입니다.

![]({{ site.url }}/images/window-install/1.png)

설치중에 **Add Ruby executables to your PATH**는 반드시 체크해 주시기 바랍니다.

체크가 되어있지 않다면 PATH 설정을 별도로 해주어야 합니다.

![]({{ site.url }}/images/window-install/3.png)

MSYS2는 윈도우용 소프트웨어 배포, 구축 플랫폼입니다.

이미 설치가 되어있다면 넘어가도 되지만, 아니라면 1을 눌러 설치해 주세요.

![]({{ site.url }}/images/window-install/6.png)

설치가 완료되었으면 터미널(cmd or powershell)을 열어 확인해 줍니다.

```
gem --version
```

을 입력하여 설치가 되어 있는지 확인해 줍니다.

![]({{ site.url }}/images/window-install/8.png)

## jekyll 설치하기

설치가 잘 되어있다면 jekyll을 설치해 줍니다.

```
gem install jekyll bundler
```

설치가 완료되면 아래 명령어를 입력하여 설치를 확인해 줍니다.

```
jekyll -v
```

![]({{ site.url }}/images/window-install/9.png)

## git 설치하기

아래 링크에서 setup파일을 다운로드합니다.

[https://git-scm.com/download/win](https://git-scm.com/download/win)

![]({{ site.url }}/images/window-install/10.png)

특별한 것 없이 기본 체크대로 넘어가 주시면 됩니다.

설치가 완료되면 아래 명령어로 설치를 확인합니다.

```
git --version
```

![]({{ site.url }}/images/window-install/11.png)

## 템플릿 가져오기

템플릿을 가져오기 전 cd 명령어를 이용해 작업할 폴더로 이동해 주세요.

예를 들어 아래 폴더라면 경로는 **F:\python\page**가 됩니다.

```
cd F:\python\page
```

아래 명령어로 템플릿을 가져옵니다.

clone 명령을 사용하기 전 폴더를 다시한번 확인해 주세요.

현재 폴더 내에 새로운 폴더가 생성됩니다.

관리자가 아닌경우 먼저 

https://github.com/ai-robotics-kr/ai-robotics-kr.github.io

의 repository 를 fork 한후 clone 하여 자신의 로컬 저장소에 저장해줍니다. 
```
git clone https://github.com/아이디/ai-robotics-kr.github.io.git
```
 
 
새로 생성된 폴더로 이동하여 아래 명령어로 필요한 패키지를 설치해 줍니다.

```
cd ai-robotics-kr.github.io   

bundle install
```

현재 페이지의 상태를 배포하기 전에 확인해 줍니다.

```
jekyll serve
```

![]({{ site.url }}/images/window-install/12.png)

만약 에러가 난다면 아래 패키지들을 설치해 주세요.

```
gem install tzinfo-data
gem install jekyll-seo-tag
gem install jekyll-admin
```

인터넷 창 열고 127.0.0.1:4000 클릭하여 들어가면 확인할 수 있습니다.

![]({{ site.url }}/images/window-install/13.png)






