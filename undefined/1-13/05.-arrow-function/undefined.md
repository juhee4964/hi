# ๐ญ ํจ์

****

**๐กํจ์์ ์ ์์ ํธ์ถ**

* **ํจ์์ ์ ์ 3๊ฐ์ง ๋ฐฉ์**\
  1\. ํจ์ ์ ์ธ๋ฌธ\
  2\. ํจ์ ํํ์\
  3\. funtion ์์ฑ์ ํจ์

**๐กํจ์ ์ ์ธ๋ฌธ**

* `functionํค์๋ ํจ์๋ช (๋งค๊ฐ๋ณ์(=์ธ์)) { returnํค์๋ ๊ฐ๋ฐํ ํํ์; };`\
  **`function add(a,b){ return a+ b; };`**
* ํ๋์ ํจ์๋ ํ๋์ ์ผ๋ง
* ํจ์๋ช ์๋ต ๋ถ๊ฐ,`return`๋ฌธ์ผ๋ก ๊ฒฐ๊ณผ๊ฐ์ ๋ฐํํ  ์ ์์, ์ด๋ฅผ ๋ฐํ๊ฐ์ด๋ผ ํจ .
* ํจ์ ํธ์ด์คํ์ด ์ผ์ด๋  ์ ์๊ธฐ๋๋ฌธ์ ๊ฑฐ์ ์ฌ์ฉํ์ง ์์&#x20;
* **ํธ์ด์คํ ๊ฐ๋จ ์ค๋ช โจ**\
  : ํจ์ ์ ์ธ์ ์์น์๋ ์๊ด์์ด ์์ค ๋ด ์ด๋ ๊ณณ์์๋ ์ง ํธ์ถ์ด ๊ฐ๋ฅ

```javascript
function printHello(){
    console.log('hello');
}
printHello();

function log(message){
    console.log(message);
}
log('Hello');
log(1234); // type์ด ์ค์ํ ๊ฒฝ์ฐ์๋ ๋ํดํ  ์ ์์ 
```



**๐ก**Parameters**(=๋งค๊ฐ๋ณ์)**

* object parameters: ๋ฉ๋ชจ๋ฆฌ์ ๋ ํผ๋ฐ์ค๊ฐ ์ ๋ฌ
* premitive parameters: ๊ฐ์ด ๋ฐ๋ก ์ ๋ฌ
* ๋งค๊ฐ๋ณ์์ ๊ธฐ๋ณธ๊ฐ์ ๋ฌด์กฐ๊ฑด undefined
* ๋งค๊ฐ๋ณ์์ ์ ๋ณด๋ ํจ์ ๋ด๋ถ์์ ์ ๊ทผ์ด ๊ฐ๋ฅํ arguments ๊ฐ์ฒด์ ์ ์ฅ๋จ
* ๋งค๊ฐ๋ณ์ ๊ธฐ๋ณธ๊ฐ Default Parameter๋ฅผ ์ ํ  ์ ์๋ค.

```javascript
function changeName(obj){
    obj.name ='corder';
}
const ellie = {name: 'ellie'};
changeName(ellie);
console.log(ellie);//corder๋ผ๊ณ  ์ถ๋ ฅ

// Default parameters
//- ES6์์ ์ถ๊ฐ 
function showMessage(message, from = 'unknown'){
    console.log(`${message} by ${from}`);
}
showMessage('Hi');//consloe์ฐฝ์ Hi by unknown์ด๋ผ๊ณ  ๋ธ

//์ด์  ๋ฐฉ์: if(from === undefined){
//    from = 'unknown';
//}์ด๋ผ๊ณ  ์ผ์ผ์ด ์์ฑํ๋ค๋ฉด ์ง๊ธ์ ๋ฐ๋ก default๋ก ์ค์ ๊ฐ๋ฅ  

// Rest parameters
//- ES6์์ ์ถ๊ฐ
function printAll(...args){//๋ฐฐ์ด ํํ
    for(let i = 0; i < arg.length; i++){//arg.length ๊ฐฏ์
        console.log(args[i]);
    }
    //๋ ๋ค๋ฅธ ์ถ๋ ฅ ๋ฐฉ๋ฒ1(๋ฐฐ์ด)
    for(const arg of args){
        console.log(arg);
    }
    //๋ ๋ค๋ฅธ ์ถ๋ ฅ ๋ฐฉ๋ฒ2(๋ฐฐ์ด)
    args.forEach((arg) => console.log(arg));
}
printAll('dream','coding','ellie');
```



**๐ก**Return a value

* ํจ์๋ ์์ ์ ํธ์ถํ ์ฝ๋์๊ฒ ์ํํ ๊ฒฐ๊ณผ๋ฅผ ๋ฐํ(return)ํ  ์ ์์ \
  ๋ฐํ๋ ๊ฐ์ **๋ฐํ๊ฐ(return value)**๋ผ๊ณ  ๋ถ๋ฆ.
* `return` = `undefined`
* **๊ทธ๋ฅ `return`๋ง ์์ ๊ฒฝ์ฐ, ํจ์๊ฐ ์ฆ์ ์ข๋ฃ**โจ
* ๋ง์ผ `return` ์ดํ์ ๋ค๋ฅธ ๊ตฌ๋ฌธ์ด ์กด์ฌํ  ๊ฒฝ์ฐ,\
  ๊ทธ ๊ตฌ๋ฌธ์ ์คํ๋์ง ์์\
  ์ฌ์ฉ ์ :\
  ์กฐ๊ฑด์ด ๋ง์ง ์๋ ๊ฒฝ์ฐ ํจ์ ๋์๋ถ๋ถ์์ ํจ์๋ฅผ ์ผ์ฐ์ด ์ข๋ฃํ  ์ ์์

```javascript
function sum(a, b){
    return a + b;
}
const result = sum(1, 2);//3
console.log(`sum: ${sum(1, 2)}`);

// Early return, ealry exit
//bad
function upgradeUser(user){
    if(user.point > 10){
    //long upgrade logic - ๊ฐ๋์ฑ์ด ๋จ์ด์ง
    }
}

// good
function upgradeUser(user){
    if(user.point <= 10){
    return;
    // ์กฐ๊ฑด์ด ๋ง์ง ์๋ ๊ฒฝ์ฐ, ๊ฐ์ด undefined์ธ ๊ฒฝ์ฐ, -1์ธ ๊ฒฝ์ฐ
    // return์ ํด์ ๋นจ๋ฆฌ ํจ์๋ฅผ ์ข๋ฃ์ํด 
    }
    //long upgrade logic
}
```



**๐ก์ฝ๋ฐฑ ํจ์**

* ์ ๋ฌ๋  ๋น์์ ์ฝ๋ฐฑํจ์๋ฅผ ๋ฐ๋ก ํธ์ถํด์ ๋ฐํ๋ ๊ฐ์ ์ ๋ฌํ๋ ๊ฒ์ด ์๋๋ผ
* ์ฝ๋ฐฑํจ์๋ฅผ ๊ฐ๋ฆฌํค๊ณ  ์๋ ํจ์์ ๋ ํผ๋ฐ์ค(์ฐธ์กฐ๊ฐ)๊ฐ ์ ๋ฌ
* ๊ทธ๋์ ์ฝ๋ฐฑํจ์๋ ๊ณ ์ฐจํจ์์์์ ํ์ํ ์๊ฐ์ ํธ์ถ์ด ๋์ค์ ๋จ

```javascript
function randomQuiz(answer, printYes, printNo){
	if (answer === 'love you'){
    	printYes();
    }else{
    	printNo();
    }
}

const printYes = function(){
	console.log('yes!');
};

const printNO = function print(){
	// named function = ๊ธฐ๋ช ํจ์: ๋๋ฒ๊น์ ํจ์ ์ด๋ฆ์ด ๋์ค๊ฒ ํ๊ธฐ ์ํ ๊ฒ
	console.log('no!');
   	print();//ํจ์ ์์์ ํจ์ ์์ ์ ๊ณ์ ๋ถ๋ฌ๋ด๋ ๊ฒ๋ ๊ฐ๋ฅํ์ง๋ง
			//, ๋ฐ๋ณต๋๋ ํ๊ท ๊ฐ์ ๊ตฌํ๊ฑฐ๋ ์ด๋ด๋ ์ฌ์ฉ
};

randomQuiz('wrong', printYes, printNo);
randomQuiz('love you', printYes, printNo);
```

****

**๐ก**Arrow function

```javascript
const simplePrint = function(){
	console.log('simplePrint!');
};

//= const simplePrint = () => console.log('simplePrint!');

// Arrow function: ๊ฐ๊ฒฐํ๊ฒ ์ฝ๋๋ฅผ ๋ํ๋ผ ์ ์์
const add = (a, b) => a + b;
// function
const add = function(a, b){
	return a + b;
};

// Arrow function์์ ์ฌ๋ฌ๊ฐ์ง๋ฅผ ์คํํด์ผํด์ ๋ธ๋ญ์ ์ฌ์ฉํด์ผํ๋ค๋ฉด?
const simpleMultiply = (a, b) => {
	return a + b;
    // ๋ค๋ฅธ ๋์ํด์ผํ๋ ์ฝ๋
};j
```

****

**๐ก**IIFE

* Immediately Invoked Function Expression = ํจ์ ์ฆ์ ํธ์ถ

```javascript
function hello(){
	console.log('IIFE');
};
hello();

โถ 
(function hello(){
	console.log('IIFE');
 })();
```

