# 🐭 함수

****

**💡함수의 정의와 호출**

* **함수의 정의 3가지 방식**\
  1\. 함수 선언문\
  2\. 함수 표현식\
  3\. funtion 생성자 함수

**💡함수 선언문**

* `function키워드 함수명 (매개변수(=인자)) { return키워드 값반환 표현식; };`\
  **`function add(a,b){ return a+ b; };`**
* 하나의 함수는 하나의 일만
* 함수명 생략 불가,`return`문으로 결과값을 반환할 수 있음, 이를 반환값이라 함 .
* 함수 호이스팅이 일어날 수 있기때문에 거의 사용하지 않음&#x20;
* **호이스팅 간단 설명 ✨**\
  : 함수 선언의 위치와는 상관없이 소스 내 어느 곳에서든지 호출이 가능

```javascript
function printHello(){
    console.log('hello');
}
printHello();

function log(message){
    console.log(message);
}
log('Hello');
log(1234); // type이 중요한 경우에는 난해할 수 있음 
```



**💡**Parameters**(=매개변수)**

* object parameters: 메모리의 레퍼런스가 전달
* premitive parameters: 값이 바로 전달
* 매개변수의 기본값은 무조건 undefined
* 매개변수의 정보는 함수 내부에서 접근이 가능한 arguments 객체에 저장됨
* 매개변수 기본값 Default Parameter를 정할 수 있다.

```javascript
function changeName(obj){
    obj.name ='corder';
}
const ellie = {name: 'ellie'};
changeName(ellie);
console.log(ellie);//corder라고 출력

// Default parameters
//- ES6에서 추가 
function showMessage(message, from = 'unknown'){
    console.log(`${message} by ${from}`);
}
showMessage('Hi');//consloe창에 Hi by unknown이라고 뜸

//이전 방식: if(from === undefined){
//    from = 'unknown';
//}이라고 일일이 작성했다면 지금은 바로 default로 설정가능  

// Rest parameters
//- ES6에서 추가
function printAll(...args){//배열 형태
    for(let i = 0; i < arg.length; i++){//arg.length 갯수
        console.log(args[i]);
    }
    //또 다른 출력 방법1(배열)
    for(const arg of args){
        console.log(arg);
    }
    //또 다른 출력 방법2(배열)
    args.forEach((arg) => console.log(arg));
}
printAll('dream','coding','ellie');
```



**💡**Return a value

* 함수는 자신을 호출한 코드에게 수행한 결과를 반환(return)할 수 있음 \
  반환된 값을 **반환값(return value)**라고 부름.
* `return` = `undefined`
* **그냥 `return`만 있을 경우, 함수가 즉시 종료**✨
* 만일 `return` 이후에 다른 구문이 존재할 경우,\
  그 구문은 실행되지 않음\
  사용 예 :\
  조건이 맞지 않는 경우 함수 도입부분에서 함수를 일찍이 종료할 수 있음

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
    //long upgrade logic - 가독성이 떨어짐
    }
}

// good
function upgradeUser(user){
    if(user.point <= 10){
    return;
    // 조건이 맞지 않는 경우, 값이 undefined인 경우, -1인 경우
    // return을 해서 빨리 함수를 종료시킴 
    }
    //long upgrade logic
}
```



**💡콜백 함수**

* 전달될 당시에 콜백함수를 바로 호출해서 반환된 값을 전달하는 것이 아니라
* 콜백함수를 가리키고 있는 함수의 레퍼런스(참조값)가 전달
* 그래서 콜백함수는 고차함수안에서 필요한 순간에 호출이 나중에 됨

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
	// named function = 기명 함수: 디버깅시 함수 이름이 나오게 하기 위한 것
	console.log('no!');
   	print();//함수 안에서 함수 자신을 계속 불러내는 것도 가능하지만
			//, 반복되는 평균값을 구하거나 이럴때 사용
};

randomQuiz('wrong', printYes, printNo);
randomQuiz('love you', printYes, printNo);
```

****

**💡**Arrow function

```javascript
const simplePrint = function(){
	console.log('simplePrint!');
};

//= const simplePrint = () => console.log('simplePrint!');

// Arrow function: 간결하게 코드를 나타낼 수 있음
const add = (a, b) => a + b;
// function
const add = function(a, b){
	return a + b;
};

// Arrow function에서 여러가지를 실행해야해서 블럭을 사용해야한다면?
const simpleMultiply = (a, b) => {
	return a + b;
    // 다른 동작해야하는 코드
};j
```

****

**💡**IIFE

* Immediately Invoked Function Expression = 함수 즉시 호출

```javascript
function hello(){
	console.log('IIFE');
};
hello();

▶ 
(function hello(){
	console.log('IIFE');
 })();
```

