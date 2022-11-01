# 🚗 클래스

****

**💡class**

* 객체를 손쉽게 만들 수 있는 템플릿(template) 객체
* `class` 키워드 사용
* 생성자 함수와 마찬가지로 함수명은 **파스칼 케이스** 사용
* 표현식으로도 클래스를 정의할 수 있다.

```javascript
// class: template
// object: class 안의 데이터 넣은 것
// 기존에 존재하던 프로토타입을 베이스로 한 것에 기반해서 추가한 것

// class 사용방법(정의)
class Person{
	constructor(name, age){
        // constructor:생성자를 이용해 object를 만들때 필요한 데이터 전달
    	// fields
        this.name = name;
        this.age = age;
    }
    
    // methods
    speak(){
    	console.log(`${this.name}:hello!`);
    }
}

const juhee = new Person('juhee',20);
console.log(juhee.name);
console.log(juhee.age);
juhee.speak();
```



**💡getter**

* 클래스 몸체의 메소드 이름 앞에 `get`키워드 사용
* 이때 메소드 이름은 클래스 필드(=멤버변수)의 이름처럼 사용됨
* 다시말해 getter는 호출이 아닌 프로퍼티처럼 참조형식이며, 참조 시 메서드가 호출됨
* **반드시 무언가를 반환해야 함**

**💡setter**

* 클래스 필드에 값을 할당할 때마다 클래스 필드의 값을 조작하는 행위가 필요할 때 사용
* `set`키워드 사용
* 다시말해 setter는 호출이 아닌 프로퍼티처럼 참조형식이며,
* **할당 시에 메소드가 호출된다.**

```javascript
// 2. Getter and setters
class User{ 
    constructor(firstName, lastName, age){ 
        this.firstName = firstName; 
        this.lastName = lastName; 
        this.age = age; 
    }
    //getter
    // user의  age가 -1인 것은 말이 안됨, get을 이용해 값을 return
    // 사용자가 this.age를 호출하면 우리는 get age를 return
    get age(){
    	// return this.age;
        return this._age;//call stack error 부분 방지
    }
    //setter
    set age(value){//set은 값을 설정하기 때문에 value를 받아와야함
    	// this.age = value;
        // this._age = value;//call stack error 부분 방지
        // if(value < 0){
        // throw Error('age can not be negative');
        // }
        //좀 더 젠틀하게
        this._age = value < 0 ? 0 : value; 
        // value의 값이 음수라면 0을, 아니면 지정된 value값
    }
    // ▶ 이러면 call stack 이 꽉 찼다고 할 것 그래서 이름을 약간씩 바꿔줌
};

const user1 = new User('steve', 'job', -1);// 나이는 0부터임
console.log(user1.age);
```



**💡Fields (public, private)**

```javascript
// 최근 추가되었음, 사파리에서도 지원이 되지 않음
class Experiment{
	publicField = 2;//생성자를 사용하지 않고 정의가 가능하고, 외부에서 접근이 가능
    #privateField = 0;//#을 쓰면 private로 사용할 수 있는데, 딱 class안에서만 사용 가능
}
const experiment = new Experiment();
console.log(experiment.publicField);
console.log(experiment.privateField);
```



**💡Static properties and methods**

```javascript
// 최근 추가되었음
// 클래스가 고유하게 가지고 있는 속성과 행동들
class Article {
	static publisher = 'Dream Coding';
    constructor(articleNumber){
    	this.aricleNumber = articleNumber;
    }
    
    static printPublisher(){
    	console.log(Article.publisher);
    }
}
const article1 = new Article(1);
const article2 = new Article(2);
console.log(article1.publisher);
// 값이 지정되지 않음 → class안에 있는 것이기 때문에
// console.log(Article.publisher)로 줘야함
// 그래서 static 함수의 호출은 클래스 명을 이용해서
// Article.printPublisher();로 해주면 됨
```

****

### 클래스 상속 <a href="#undefined" id="undefined"></a>

* 코드 재사용 관점에서 매우 유용한 것

**💡extends 키워드**

* 부모클래스를 상속받는 자식 클래스를 정의할 때 사용 \[확장(연결, 포함)]

**💡overriding 오버라이딩**

* 부모클래스가 가지고 있는 메서드를 하위 클래스에서 재정의 하는 것
* 필요한 함수만 바로 재정리해서 사용 가능

**💡super 키워드**

* 부모클래스를 참조할때 또는 부모클래스의 생성자를 호출할때 사용
* 부모의 method도 상속받고 싶다면 super.method();사용

```javascript
class Shape{
	constructor(width, height, color){
    	this.width = width;
        this.height = height;
        this.color = color;
    }
    
   //methods
   draw(){
		console.log(`drawing ${this.color} color of`);   
   }
   
   getArea(){//너비
		return this.width * this.height;
   }
}

//만약 여기서 다른 class에 위 Shap의 속성을 공통적으로 사용한다면
class Rectangle extends Shape{ //extends라는 키워드를 사용해 확장(연결, 포함)
}
class Triangle extends Shape{ //다양성: 필요한 함수만 바로 재정리해서 사용 가능 = 오버라이팅
	draw(){
    	super.draw();// 부모의 method도 상속받고 싶다면 super.method();사용
    	console.log('▲');
    }
    getArea(){//너비
		return (this.width * this.height) / 2;
   }
}

const rectangle = new Rectangle(20, 20, 'blue');
rectangle.draw();
console.log(rectangle.getArea());
const triangle = new Triangle(20, 20, 'red');
console.log(triangle.getArea());
```



**💡Class checking : instanceOf**

```javascript
console.log(rectangle instanceof Rectangle); //true
console.log(triangle instanceof Rectangle); //false
console.log(triangle instanceof Triangle); //true
console.log(triangle instanceof Shape); //true
console.log(triangle instanceof Object); //true 자바 스크립트에 만든 모든 object는 object를 다 상속한다.
// 왼쪽의 오브젝트가 오른쪽의 클래스로 만들어진 아이인지 아닌지 확인하는 것
```
