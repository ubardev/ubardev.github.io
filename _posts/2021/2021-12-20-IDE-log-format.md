---
layout: post
title: IntelliJ에서 console.log()편하게 사용하기
subtitle: IntelliJ에서 console.log()편하게 사용하기
categories: IDE
tags: [IntelliJ]
---

IntelliJ계열 IDE에서 js파일을 개발하다보면 console.log()를 많이 사용하게 됩니다.  
하지만 기본으로 설정된 shortcut이 없어 로그를 찍으려면 번거롭습니다.  
![default shortcut list](/assets/images/post/2021/2021-12-20-IDE-log-format/01-default-shortcut-list.png)

IntelliJ계열 IDE에는 shortcut을 커스터마이징 하는 기능을 제공하기 있기에 자주 사용하는 문자열을 등록할 수 있습니다

> <shortcut등록 메뉴>  
> Preferences > Editor > Live Templates

등록 방법을 알아보겠습니다.

![JavaScript shortcut 등록 메뉴](/assets/images/post/2021/2021-12-20-IDE-log-format/02-add-javascript-shortcut.png)
*JavaScript shortcut 등록 메뉴*

![Live template추가](/assets/images/post/2021/2021-12-20-IDE-log-format/03-add-live-template.png)
*console.log();를 등록할 Live Template추가 버튼 클릭*

사용할 단축어와 설명, 텍스트를 입력합니다.
> Abbreviation: 사용할 단축어(저는 console, log의 앞글자를 따서 cl로 정했습니다)  
> Description: 설명  
> Template text: 사용할 텍스트 console.log();

![사용할 단축어와 설명 입력](/assets/images/post/2021/2021-12-20-IDE-log-format/04-input-shortcut-and-description.png)
*사용할 단축어와 설명 입력*

![추가한 단축어를 사용할 언어 정의](/assets/images/post/2021/2021-12-20-IDE-log-format/05-set-shortcut-info.png)
*추가한 단축어를 사용할 언어 정의*

![JavaScript와 TypeScript선택](/assets/images/post/2021/2021-12-20-IDE-log-format/06-select-javascript-and-typescript.png)
*JavaScript와 TypeScript선택*

등록이 완료됐습니다.
실제 에디터에서 사용해보겠습니다.

![설정 확인](/assets/images/post/2021/2021-12-20-IDE-log-format/07-confirm-setting.png)
*설정 확인*

위와 같이 cl만 입력하면 console.log();가 입력되도록 shortcut이 설정됐습니다.
다른 자주 쓰는 텍스트도 위와 같이 등록해놓으면 더 편하게 개발할 수 있습니다.
