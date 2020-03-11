---
layout: post
title: "Mac에서 jekyll 설치하기"
description: "Mac OS에서 Ruby, jekyll, git 설치하기"
author: stella
date: 2020-03-11
tags: [presentation, NAVER, TechTalk]
comments: true
subdir: presentation
thumbnail: mot_logo.jpg
share: true
---

# mac os jekyll 설치방법



## RUBY 설치하기

ruby 를 설치하기 위해 패키지 관리자 brew 를 다운받는다. 
```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```
(설치 중간에 비밀번호를 치라고 나옵니다.)

![]({{ site.url }}/images/mac-install/1.png)

설치가 잘 되면 위와 같은 문구가 나옵니다.

이제 설치된 brew 를 이용해 ruby 를 설치해 줍니다. 
```
brew install ruby
```
homebrew 루비의 경로를 쉘 환경 설정에 추가한다. 
```
echo 'export PATH="/usr/local/opt/ruby/bin:$PATH"' >> ~/.bash_profile
```

터미널을 다시 껐다가 켜줍니다. 


```
ruby -v
```
이 명령어를 쳤을때, 버전 확인이 가능하면 됩니다. ruby 2.6.5-1 이상 버전이면 됩니다. 

![]({{ site.url }}/images/mac-install/2.png)


```
gem --version
```

을 입력하여 gem 설치가 되어 있는지 확인해 줍니다.

![]({{ site.url }}/images/mac-install/3.png)

## jekyll 설치하기

설치가 잘 되어있다면 jekyll을 설치해 줍니다.

1) mojave (10.14) version

```
sudo gem install bundler
sudo gem install -n /usr/local/bin/ jekyll
```
2) mojave 이전 버전 (<10.14)
```
sudo gem install bundler jekyll
```

설치가 완료되면 아래 명령어를 입력하여 설치를 확인해 줍니다.

```
jekyll -v
```

![]({{ site.url }}/images/mac-install/4.png)

## git 설치하기

git 이 없다면, 패키지 관리자 brew 를 이용해서 git 을 설치합니다. 
```
brew install -s git
```

깃이 설치 되었는지 아래 명령어로 확인합니다. 

```
git --version
```

![]({{ site.url }}/images/mac-install/5.png)

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

인터넷 창 열고 127.0.0.1:4000 
또는 http://ai-robotics-kr.github.io/ 에서 확인 가능합니다. 

![]({{ site.url }}/images/window-install/13.png)

확인 후 글을 배포하기 위해 아래 git 명령어를 입력해 주세요.

```
git status

git add 파일명
git add .

git commit -m "커밋메세지"

git push origin master
```




