---
layout: post
title: IntelliJ에서 React template 자동완성
subtitle: IntelliJ에서 React template 자동완성
categories: IDE
tags: [IntelliJ, React]
---

저는 IntelliJ를 주로 사용하는데 컴포넌트를 만들 때마다 필수 코드를 적는게 귀찮았습니다.
초기 template을 자동으로 만들어주는 플러그인을 찾아보다 보니 Live Templates에 이미 셋팅되어 있었네요.

> rsf  
> 어떤 단어의 약자인지 잘 모르겠습니다.  
> 저는 React Start Function으로 외웠습니다.

![img.png](/assets/images/post/2021/2021-12-31-IDE-intellij-react-format/01-rsp.png)
주로 React hook 형태로 작성하므로 위와 같이 rsf만 입력하면 알아서 function 형태로 생성됩니다.  
이 때 파일명을 따서 함수명도 지어주네요.

![img_1.png](/assets/images/post/2021/2021-12-31-IDE-intellij-react-format/02-completed.png)  
자동완성된 내용입니다.

![sc.png](/assets/images/post/2021/2021-12-31-IDE-intellij-react-format/03-live-templates.png)  
Live Templates에 가서 보면 이미 정의되어 있는걸 볼 수 있습니다.  
function이 아닌 const형태로 선언할 수도 있고 class형태로 사용하시는 분도 있을테니  
자주 쓰는 형태로 선택하시거나 편집하여 사용하시면 좋겠습니다.
