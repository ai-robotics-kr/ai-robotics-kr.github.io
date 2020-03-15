---
layout: post
title: "Windows에서 설치하기 따라하다 막힐 때"
description: "에러 문구가 나오지만 하라는데로 해서 해결 된.txt"
author: jeonghoon
date: 2020-03-15
tags: [test]
comments: true
subdir: presentation
thumbnail: mot_logo.jpg
share: true
---

## jekyll serve에서

jekyll serve를 통해 local에서 블로그를 확인하려고 커멘드를 입력하면 아래와 같은 에러가 나올 수 있다.

C:/Ruby26-x64/lib/ruby/gems/2.6.0/gems/bundler-2.1.4/lib/bundler/runtime.rb:312:in `check_for_activated_spec!': You have already activated public_suffix 4.0.3, but your Gemfile requires public_suffix 4.0.1. Prepending `bundle exec` to your command may solve this. (Gem::LoadError)  

이때 문구 처럼 `bundle exec`를 사용하면 잘 실행 된다.  

예시) C:\Users\Jeonghoon\blog_airoboticskr\ai-robotics-kr.github.io>bundle exec jekyll serve  
