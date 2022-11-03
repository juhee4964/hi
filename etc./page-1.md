# Page 1



### **💡for …in 문**

* 객체의 열거 가능한 '속성들'을 순회할 수 있도록 해줌
* 객체의 key값에 접근 가능, value값에는 직접 접근 불가
* 모든 객체에서 사용 가능

for ...in문은 객체의 '열거할 수 있는 **** 모든 속성들'을 순회할 수 있도록 해줌&#x20;

(keys는 열거 가능한 속성, valueOf는 열거 불가능한 속성 - [링크 참고](https://itboxs.tistory.com/353)) 따라 for ...in 문은 객체의 key 값에는 접근 가능하지만, value 값에 직접적으로 접근하는 방법은 제공하지 않는음

위에서 언급했듯이 key 값에만 접근이 가능하기 때문에 :star:배열에서는 index에, :star:객체에서는 key값에 접근하게 됨

&#x20;value값이 궁금하다면 arr\[i], obj\[prop]과 같이 key를 이용하는 방식을 사용해 간접적으로 접근할 수도 있음 (수업때 했던 방법)&#x20;

#### for ...in 문을 사용해 배열과 객체의 요소에 접근하는 예제&#x20;

```javascript
var arr = ['a', 'b', 'c']; 
for (var i in arr) {
	console.log(i, arr[i]); 
}
//arr[i] 간접적인 접근 
// 0 a, 1 b, 2 c 

var obj = { a: 1, b: 2, c: 3 }; 
for (var prop in obj) { 
	console.log(prop, obj[prop]); 
} 
// a 1, b 2, c 3
```

#### &#x20;for...in 문 주의할 점&#x20;

* for ...in문에서는 순서가 보장되지 않기 때문에 속성들 간의 순서가 중요한 경우에는 for...in문을 사용하지 않는 것이 좋음&#x20;
* &#x20;length 연산자를 사용 할 수 없음
* alue값은 string이라 연산이 불가능하다는 것이다

&#x20;

### **💡for …of 문**

* 반복 가능한 객체(iterable)를 순회할 수 있도록 해줌
* &#x20;Array, Map, Set, arguments 등이 해당됨 (Object는 해당 X)

&#x20;

> for ...of 반복문은 ES6에 추가된 새로운 컬렉션 전용 반복 구문
>
> &#x20;for ...of구문을 사용하기 위해선 컬렉션 객체가 \[Symbol.iterator] 속성을 가지고 있어야만 **함** (직접 명시 가능)

&#x20;

for ...of 문은 반복 가능한 객체(iterable)를 순회할 수 있도록 해줌

&#x20;Iterator 속성이 있는 객체인 Array, Map, Set, String, TypedArray, arguments 등의 값을 반복할 수 있으며, string 문자열에도 적용할 수 있.&#x20;

다시 언급하겠지만, for ...in문이 객체의 모든 열거 가능한 속성을 대상으로 하는 것과 달리, for ...of문은 \[Symbol.iterator] 속성을 가지는 것들만을 대상으로 함&#x20;

아래 예제들 중 맨 아래를 보면, 객체는 이에 해당하지 않기 때문에 for ...of문을 사용하면 TypeError를 발생시킴

&#x20;

#### for ...of 문을 사용한 예제&#x20;

```javascript
// Array 
for (const val of ['a', 'b', 'c']) {
	console.log(val); // 'a','b','c' 
} 

// String 
for (const val of 'abc') { 
	console.log(val); // 'a','b','c' 
} 

// Object 
for ( let val of {1 :'a', 2 :'b', 3 :'c'} ) {
	console.log(val); // TypeError: object is not iterable 
}
```



### **💡for... in문 vs for... of문**

{% tabs %}
{% tab title="for ...in문" %}
✔️ Iterable object이면 모두 대상으로 함

✔️ 객체의 모든 열거 가능한 속성에 대해 반복

✔️ key를 리턴 (배열의 경우에는 index)
{% endtab %}

{% tab title="for ...of문" %}
✔️ \[Symbol.iterator] 속성을 가지는 collection만 대상으로 함

✔️ Iterable object이지만, prototype chain에 의한 Iterable은 대상에서 제외

&#x20;      → Array, Map, Set, String, TypedArray, arguments 등

✔️ value를 리턴
{% endtab %}
{% endtabs %}

{% hint style="info" %}
for/in - loops through the properties of an object&#x20;

for/of - loops through the values of an iterable object
{% endhint %}
