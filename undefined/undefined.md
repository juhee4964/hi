# π μλ°μ€ν¬λ¦½νΈ ν¨μ κΈ°λ³ΈνΈ

## **π‘**ν¨μ μ μΈ & νΈμΆ

{% tabs %}
{% tab title="ν¨μ μ μΈ" %}
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

{% tab title="ν¨μ νΈμΆ" %}
```javascript
doSomething();

const result = add(1 ,2);
console.log(result);
```
{% endtab %}
{% endtabs %}

```javascript
//ν¨μ μ μΈ
function doSomething(){
    console.log('hello');
}

function add(a , b){
    const sum = a + b;
    return sum;
}

//ν¨μ νΈμΆ
doSomething();

const result = add(1 ,2);
console.log(result);
```



:thumbsup:ν¨μλ₯Ό μΈμλ‘ μ λ¬, ν¨μλ₯Ό λ³μμ ν λΉ

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

//ν¨μ νΈμΆ
doSomething2(add2);
//doSomething2(add2()); ν¨μλ₯Ό μ λ¬ν λ ν¨μμ μ΄λ¦λ§ μ λ¬


// ν¨μλ₯Ό λ³μμ ν λΉ
const addFun = add;
console.log(add);
addFun(1 ,2);
```

* ν¨μμλ μ μΈκ³Ό νΈμΆμ΄ μμ.&#x20;
* μ μΈμ ν λμλ μ΄λ€ κ°μ μ λ¬ λ°μ μ¬κ±΄μ§ μΈμλ€μ μ μνκ³  λμ μ½λλΈλ­μ μμ±.&#x20;
* μ μΈλ§ νλ©΄ μμ±ν μ½λκ° μνλμ§ μμ.&#x20;
* μ°λ¦¬κ° μ μν μ μΈν ν¨μλ₯Ό μννκΈ° μν΄μλ ν¨μλ₯Ό νΈμΆν΄μΌ ν¨.&#x20;
* ν¨μλ₯Ό νΈμΆνκΈ° μν΄μλ ν¨μμ΄λ¦ μμ ()λ₯Ό μ΄μ©ν΄μ ν¨μμμ μνλ μ μλ μΈμκ°μ μ λ¬νλ©΄μ νΈμΆν΄μΌ ν¨.
