---
layout: post
title: Javascript map() vs forEach()
subtitle: Javascript map() vs forEach()
categories: Javascript
tags: [Javascript]
published: false
---
개발하면서 많이 쓰는 map(), forEach() 사용법이 비슷해서 왜 나눠놨을까 궁금증이 생겼습니다.
어떤 차이가 있는지 비교해 보겠습니다.

어떤 특징을 가진 메서드인가?
-
map()과 forEach() 모두 Array 관련 메서드들로써, ES5 부터 등장하였습니다.  
forEach()가 배열 요소마다 한 번씩 주어진 함수(콜백)를 실행하는 것과 달리, map()은 배열 내의 모든 요소 각각에 대하여 주어진 함수(콜백)를 호출한 결과를 모아 새로운 배열을 반환한다는 특징을 가지고 있습니다.  
그리고, 그 함수는  
1. currentValue (배열 원소의 값)
2. index (현재 요소의 인덱스)
3. array (현재 배열)

이 세 개의 인자를 가지고 호출됩니다.

# This is a H1
## This is a H2
### This is a H3
#### This is a H4
##### This is a H5
###### This is a H6

> This is a first blockqute.  
> This is a first blockqute.
>> This is a second blockqute.
>>> This is a third blockqute.

- 1단계
    - 2단계
        - 3단계 
        - 4단계

This is a normal paragraph:

    This is a code block. asdflkasdlfkj
    asdflkjalskdjf;lasdjf;ladsjfl;asdflkjalskdjf
    aslkdjf;alsdjf;lasdjf;lasdjfl;sadjflsajdfl;

end code block.

```javascript
public class BootSpringBootApplication {
  public static void main(String[] args) {
    System.out.println("Hello, Honeymon");
  }
}
```

---