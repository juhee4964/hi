# 🚀 자바스크립트 함수 기본편

## **💡**함수 선언 & 호출

{% tabs %}
{% tab title="함수 선언" %}
```javascript
function doSomething(){
    console.log('hello');
}

function add(a , b){
    const sum = a + b;
    return sum;
}

```
{% endtab %}

{% tab title="함수 호출" %}
```javascript
doSomething();

const result = add(1 ,2);
console.log(result);
```
{% endtab %}
{% endtabs %}

```javascript
//함수 선언
function doSomething(){
    console.log('hello');
}

function add(a , b){
    const sum = a + b;
    return sum;
}

//함수 호출
doSomething();

const result = add(1 ,2);
console.log(result);
```



:thumbsup:함수를 인자로 전달, 함수를 변수에 할당

```javascript
function doSomething2(add2){
    console.log(add2);
    const result2 = add2(2 , 3);
    console.log(result2);
}

function add2(a , b){
    const sum2 = a + b;
    return sum2;
}

//함수 호출
doSomething2(add2);
//doSomething2(add2()); 함수를 전달할때 함수의 이름만 전달


// 함수를 변수에 할당
const addFun = add;
console.log(add);
addFun(1 ,2);
```

* 함수에는 선언과 호출이 있음.&#x20;
* 선언을 할때에는 어떤 값을 전달 받아 올건지 인자들을 정의하고 나서 코드블럭을 작성.&#x20;
* 선언만 하면 작성한 코드가 수행되지 않음.&#x20;
* 우리가 정의한 선언한 함수를 수행하기 위해서는 함수를 호출해야 함.&#x20;
* 함수를 호출하기 위해서는 함수이름 옆에 ()를 이용해서 함수에서 원하는 정의된 인자값을 전달하면서 호출해야 함.
