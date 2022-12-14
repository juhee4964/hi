# ๐ฉ JSON ๋ณํ

## 1. Object โ JSON ๋ณํ : JSON.stringify(obj)

Object๋ฅผ ์ง๋ ฌํ ํด์ JSON์ผ๋ก ๋ณํ

JSON.stringify(obj)

#### **๐ก**์1

```javascript
json = JSON.stringify(true);
console.log(json); // true
```

#### **๐ก**์2

```javascript
json = JSON.stringify(['apple', 'banana']);
console.log(json); // ["apple","banana"] "" - json๊ท๊ฒฉ์ฌํญ
```

#### **๐ก**์

```javascript
const rabbit = {
  name: 'tori',
  color: 'white',
  size: null,
  // symbol: Symbol('id'), // ์๋ฐ์๋ง ์๋ ํน๋ณํ ๋ฐ์ดํฐ๋ JSON์ ํฌํจ X
  bithDate: new Date(), // ๋ณํ๋์ด ํฌํจ.
  jump: () => {
    // ํ์ดํ ํจ์ ๊ฒฝ์ฐ JSON์ ํฌํจ X, ๋ง์ฝ ์ผ๋ฐํจ์๋ก ํํ ์ JSON์ ํฌํจ O
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
  return value; // ํ๋จ ์ฃผ์์ ๊ฒฐ๊ณผ๊ฐ ์ฐธ๊ณ .
});
console.log(json); // {"name":"tori","color":"white","size":null,"bithDate":"2020-07-31T21:03:46.990Z"}

/* 
โป ๊ฒฐ๊ณผ๊ฐ: 
key: , value: [object Object]
key: name, value: tori
key: color, value: white
key: size, value: null
key: bithDate, value: 2020-07-31T21:08:45.393Z
key: jump, value: () => {
    // ํ์ดํ ํจ์ ๊ฒฝ์ฐ JSON์ ํฌํจ X, ๋ง์ฝ ์ผ๋ฐํจ์๋ก ํํ ์ JSON์ ํฌํจ O
    console.log(`${name} can jump!`);
  }

โป ์ฃผ์: 
์ฒ์์ rabbit ๊ฐ์ฒด ์์ฒด ์ ๋ณด ์ถ๋ ฅ๋๊ณ , ๋ ๋ฒ์งธ๋ถํฐ rabbit ๊ฐ์ฒด ์ key:value ์ถ๋ ฅ.

โป Tip
rabbit ๊ฐ์ฒด์์ jump ๋ฉ์๋๋ฅผ ํ์ดํ ํจ์ ๋์  ์ผ๋ฐ ํจ์๋ก ์ ์ธ ์ name์ ์ ๊ทผ ๊ฐ๋ฅ.
๊ฐ์ฒด์ ๋ฉ์๋๋ฅผ ํ์ดํ ํจ์๋ก ์ ์ธํ  ๊ฒฝ์ฐ this๋ ์ ์ญ๊ฐ์ฒด๋ฅผ ๊ฐ๋ฆฌ์ผ์ window๊ฐ ์ถ๋ ฅ๋จ.

(์์ ) 
jump: function() { console.log(`${this.name} can jump!`); } 
๋๋ 
jump() { console.log(`${this.name} can jump!`); }
*/


json = JSON.stringify(rabbit, (key, value) => {
  console.log(`key: ${key}, value: ${value}`);
  return key === 'name' ? 'ellie' : value;
});
console.log(json); // {"name":"ellie","color":"white","size":null,"bithDate":"2020-07-31T21:21:17.267Z"}
```





## 2. JSON โ Object๋ณํ : JSON.parse(json)

```javascript
console.clear();
json = JSON.stringify(rabbit);
console.log(json);

const obj = JSON.parse(json);
console.log(obj); // {name: "tori", color: "white", size: null, birthDate: "2020-07-31T21:49:25.781Z"}

rabbit.jump(); // can jump!
// obj.jump(); // ์๋ฌ ๋ฐ์. (โต JSON์์ ๋ณํ๋ ๊ฐ์ฒด์ jump ๋ฉ์๋ ํฌํจ X)


console.log(rabbit.bithDate.getDate()); // 9  (โป ์ฝ๋ ํ์คํธํ ๋ ์ ์ผ์)
// console.log(obj.birthDate.getDate()); // ์๋ฌ ๋ฐ์. (JSON์์ ๋ณํ๋ ๊ฐ์ฒด ๊ฒฝ์ฐ, birthDate ๊ฐ์ ๋ฌธ์์ด์ด๋ฏ๋ก)


const obj2 = JSON.parse(json, (key, value) => {
  console.log(`key: ${key}, value: ${value}`);
  return value;
});
/* 
๊ฒฐ๊ณผ๊ฐ:
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
๊ฒฐ๊ณผ๊ฐ:
key: name, value: tori
json.js:101 key: color, value: white
json.js:101 key: size, value: null
json.js:101 key: birthDate, value: 2020-07-31T23:34:05.781Z
json.js:101 key: , value: [object Object]
*/
console.log(rabbit.bithDate.getDate());
console.log(obj3.birthDate.getDate()); // 9
```
