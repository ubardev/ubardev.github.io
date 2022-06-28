---
layout: post
title: Javascript Array sort()
subtitle: Javascript의 Array 내장함수 중 sort에 관한 내용입니다.
categories: Javascript
tags: [Javascript]
---

Javascript의 Array 내장함수 중 sort()에 관해 정리해보고자 합니다.

## 기본 구문
```javascript
arr.sort([compareFunction])
```
### parameter
#### compareFunction(optional)
정렬 순서를 정의하는 함수.  
생략하면 배열은 각 요소의 문자열 변환에 따라 각 문자의 유니코드 값에 따라 정렬됩니다.
#### return value
정렬한 배열. 원 배열(original)이 정렬됩니다.
```javascript
const numbers = [2, 1, 6, 4, 9];
numbers.sort();
console.log(`numbers: ${numbers}`); // numbers: 1,2,4,6,9

const strings = ['zoo', 'king', 'car', 'orange'];
strings.sort();
console.log(`strings: ${strings}`); // strings: car,king,orange,zoo
```

## 숫자
### 1, 10의 단위 구분
`[2, 1, 3, 10]` 배열의 경우 10이 2보다 유니코드가 앞서기 때문에  
`[1, 2, 3, 10]`이 아닌 `[1, 10, 2, 3]`으로 정렬됩니다.
원하는 결과값을 얻기 위해서는 아래 function을 정의해줍니다.

### 오름차순
```javascript
const numbers = [5, 7, 2, 23, 10];
numbers.sort((a, b) => a - b);
console.log(`numbers: ${numbers}`); // numbers: 2,5,7,10,23
````

### 내림차순
```javascript
const numbers = [5, 7, 2, 23, 10];
numbers.sort((a, b) => b - a);
console.log(`numbers: ${numbers}`); // numbers: 23,10,7,5,2
````

## 문자
### 대소문자 구분
대문자가 소문자보다 유니코드가 앞서기 때문에 대문자가 소문자보다 앞에 정렬됩니다.
#### 오름차순
```javascript
const strings = ['g', 'green', 'car', 'orange'];
strings.sort();
console.log(`strings: ${strings}`); // strings: car,g,green,orange
````

#### 내림차순
```javascript
const strings = ['g', 'green', 'car', 'orange'];
strings.sort((a, b) => {
  if (a > b) return -1;
  else if (b > a) return 1;
  else return 0;
});
console.log(`strings: ${strings}`); // strings: orange,green,g,car
````

### 대소문자 구분 없이
대문자가 소문자보다 유니코드가 앞서기 때문에 대문자가 소문자보다 앞에 정렬됩니다.
```javascript
const strings = ['g', 'Green', 'car', 'orange'];
strings.sort();
console.log(`strings: ${strings}`); // strings: Green,car,g,orange
````
#### 오름차순
대소문자 구분 없이 정렬하기 위해서는 모두 대문자 or 소문자로 변환하여 정렬합니다.
```javascript
const strings = ['g', 'Green', 'car', 'orange'];
strings.sort((a, b) => {
  const convertedA = a.toUpperCase();
  const convertedB = b.toUpperCase();

  if (convertedA > convertedB) return 1;
  else if (convertedA < convertedB) return -1;
  else return 0;
});
console.log(`strings: ${strings}`); // strings: car,g,Green,orange
````
#### 내림차순
대소문자 구분 없이 정렬하기 위해서는 모두 대문자 or 소문자로 변환하여 정렬합니다.
그리고 조건을 오름차순의 반대로 적어줍니다.
```javascript
const strings = ['g', 'Green', 'car', 'orange'];
strings.sort((a, b) => {
  const convertedA = a.toUpperCase();
  const convertedB = b.toUpperCase();

  if (convertedA < convertedB) return 1;
  else if (convertedA > convertedB) return -1;
  else return 0;
});
console.log(`strings: ${strings}`); // strings: orange,Green,g,car
````

## 객체(Object)
객체 내 정렬하고자 하는 값을 추출하여 비교합니다.
### 오름차순
```javascript
const fruits = [
  { name: 'mango', price: 3000},
  { name: 'apple', price: 1000},
  { name: 'tomato', price: 500},
];
fruits.sort((a, b) => a.price - b.price);
console.log(`fruits: ${JSON.stringify(fruits)}`);
// fruits: [{"name":"tomato","price":500},{"name":"apple","price":1000},{"name":"mango","price":3000}]
```
### 내림차순
```javascript
const fruits = [
  { name: 'mango', price: 3000},
  { name: 'apple', price: 1000},
  { name: 'tomato', price: 500},
];
fruits.sort((a, b) => b.price - a.price);
console.log(`fruits: ${JSON.stringify(fruits)}`);
// fruits: [{"name":"mango","price":3000},{"name":"apple","price":1000},{"name":"tomato","price":500}]
```