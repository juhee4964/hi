# 🏩 JSON 변환

## 1. Object → JSON 변환 : JSON.stringify(obj)

Object를 직렬화 해서 JSON으로 변환

JSON.stringify(obj)

#### **💡**예1

```javascript
json = JSON.stringify(true);
console.log(json); // true
```

#### **💡**예2

```javascript
json = JSON.stringify(['apple', 'banana']);
console.log(json); // ["apple","banana"] "" - json규격사항
```

#### **💡**예

```javascript
const rabbit = {
  name: 'tori',
  color: 'white',
  size: null,
  // symbol: Symbol('id'), // 자바에만 있는 특별한 데이터도 JSON에 포함 X
  bithDate: new Date(), // 변환되어 포함.
  jump: () => {
    // 화살표 함수 경우 JSON에 포함 X, 만약 일반함수로 표현 시 JSON에 포함 O
    console.log(`${name} can jump!`);
  },
};

json = JSON.stringify(rabbit);
console.log(json); // {"name":"tori","color":"white","size":null,"bithDate":"2020-07-31T20:28:26.519Z"}

json = JSON.stringify(rabbit, ['name']);
console.log(json); // {"name":"tori"}

json = JSON.stringify(rabbit, ['name', 'color']);
console.log(json); // {"name":"tori","color":"white"}

json = JSON.stringify(rabbit, ['name', 'color', 'size']);
console.log(json); // {"name":"tori","color":"white","size":null}


json = JSON.stringify(rabbit, (key, value) => {
  console.log(`key: ${key}, value: ${value}`);
  return value; // 하단 주석의 결과값 참고.
});
console.log(json); // {"name":"tori","color":"white","size":null,"bithDate":"2020-07-31T21:03:46.990Z"}

/* 
※ 결과값: 
key: , value: [object Object]
key: name, value: tori
key: color, value: white
key: size, value: null
key: bithDate, value: 2020-07-31T21:08:45.393Z
key: jump, value: () => {
    // 화살표 함수 경우 JSON에 포함 X, 만약 일반함수로 표현 시 JSON에 포함 O
    console.log(`${name} can jump!`);
  }

※ 주의: 
처음엔 rabbit 객체 자체 정보 출력되고, 두 번째부터 rabbit 객체 안 key:value 출력.

※ Tip
rabbit 객체에서 jump 메서드를 화살표 함수 대신 일반 함수로 선언 시 name에 접근 가능.
객체의 메서드를 화살표 함수로 선언할 경우 this는 전역객체를 가리켜서 window가 출력됨.

(예제) 
jump: function() { console.log(`${this.name} can jump!`); } 
또는 
jump() { console.log(`${this.name} can jump!`); }
*/


json = JSON.stringify(rabbit, (key, value) => {
  console.log(`key: ${key}, value: ${value}`);
  return key === 'name' ? 'ellie' : value;
});
console.log(json); // {"name":"ellie","color":"white","size":null,"bithDate":"2020-07-31T21:21:17.267Z"}
```





## 2. JSON → Object변환 : JSON.parse(json)

```javascript
console.clear();
json = JSON.stringify(rabbit);
console.log(json);

const obj = JSON.parse(json);
console.log(obj); // {name: "tori", color: "white", size: null, birthDate: "2020-07-31T21:49:25.781Z"}

rabbit.jump(); // can jump!
// obj.jump(); // 에러 발생. (∵ JSON에서 변환된 객체엔 jump 메서드 포함 X)


console.log(rabbit.bithDate.getDate()); // 9  (※ 코드 테스트한 날의 일자)
// console.log(obj.birthDate.getDate()); // 에러 발생. (JSON에서 변환된 객체 경우, birthDate 값은 문자열이므로)


const obj2 = JSON.parse(json, (key, value) => {
  console.log(`key: ${key}, value: ${value}`);
  return value;
});
/* 
결과값:
key: name, value: tori
json.js:96 key: color, value: white
json.js:96 key: size, value: null
json.js:96 key: birthDate, value: 2020-07-31T23:34:05.781Z
json.js:96 key: , value: [object Object]
*/


const obj3 = JSON.parse(json, (key, value) => {
  console.log(`key: ${key}, value: ${value}`);
  return key === 'birthDate' ? new Date(value) : value;
});
/*
결과값:
key: name, value: tori
json.js:101 key: color, value: white
json.js:101 key: size, value: null
json.js:101 key: birthDate, value: 2020-07-31T23:34:05.781Z
json.js:101 key: , value: [object Object]
*/
console.log(rabbit.bithDate.getDate());
console.log(obj3.birthDate.getDate()); // 9
```
