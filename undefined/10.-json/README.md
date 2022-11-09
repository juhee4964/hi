# ➡ 10. JSON 개념 정리와 활용방법

**💡join**

* make a string out of an array
* arr.join() : (array → string) 변환
* array를 구분자를 넣어 문자열로 바꿀 수 있음&#x20;
* 배열에 있는 모든 것을 string으로 만들어 줌
* 구분자를 생략 시, 콤마,가 기본값

```javascript
{
  const fruits = ['apple', 'banana', 'orange'];
  const res1 = fruits.join();
  console.log(res1);
  const res2 = fruits.join('|');
  console.log(res2);
}
```



**💡split**

* make an array out of a string
* str.split() : (string → array) 변환
* 주어진 string을 array로 변환
* 구분자는 문자열 또는 정규표현식
* 구분자를 꼭 전달해 줘야함

```javascript
{
  const fruits = 'apple🍎, kiwi🥝, banana🍌, cherry🍒';
  const res1 = fruits.split(',');
  console.log(res1); // ["apple", " kiwi", " banana", " cherry"]
  const res2 = fruits.split(',', 2);
  console.log(res2); // ["apple", " kiwi"]
  const res3 = fruits.split();
  console.log(res3); // ["apple, kiwi, banana, cherry"]
}
```



**💡reverse**

* make this array look like this: \[5, 4, 3, 2, 1]
* arr.reverse() : 배열 자체의 순서 뒤집기

```javascript
{
  const array = [1, 2, 3, 4, 5];
  const res = array.reverse();
  console.log(res); // [5, 4, 3, 2, 1]
  console.log(array); // [5, 4, 3, 2, 1] 배열 자체를 변화시킴
}
```



**💡splice, slice**

* make new array without the first two elements
* `array.splice();` : 배열 자체에서 데이터를 삭제, 배열 자체 변화 O
* `array.slice();` : 배열의 특정한 부분을 리턴함. 배열 자체는 변화 X (∴ 이것을 사용해야 함.)

```javascript
{
  const array = [1, 2, 3, 4, 5];
  const res1 = array.splice(0, 2);
  console.log(res1); // [1, 2]
  console.log(array); // [3, 4, 5]

  const res2 = array.slice(2, 5);
  console.log(res2); // [3, 4, 5]
  console.log(array); // [1, 2, 3, 4, 5]
}
```



**💡find**

* find a student with the score 90
* array에서 특정 조건을 만족하는 첫번째 item을 반환
* 찾지 못하면 undefined를 반환
* 콜백함수는 array의 모든 item마다 호출이 됨
* 호출된 콜백함수가 true이면 해당 item을 반환
* 콜백함수는 boolean을 반환해야 함

```javascript
class Student {
    constructor(name, age, enrolled, score) {
      this.name = name;
      this.age = age;
      this.enrolled = enrolled;
      this.score = score;
    }
  }
  
  const students = [
    new Student('A', 29, true, 45),
    new Student('B', 28, false, 80),
    new Student('C', 30, true, 90),
    new Student('D', 40, false, 66),
    new Student('E', 18, true, 88),
  ];


{
  /*
  const res = students.find(function (student,index) {
   // console.log(student,index);
   return student.score === 90;
  });
  */
  const res = students.find((student) => student.score === 90);
  console.log(res);
}
```



**💡filter**

* make an array of enrolled students
* 콜백함수를 true로 만족하는 item을 모아 array로 생성

```javascript
class Student {
    constructor(name, age, enrolled, score) {
      this.name = name;
      this.age = age;
      this.enrolled = enrolled;
      this.score = score;
    }
  }
  
  const students = [
    new Student('A', 29, true, 45),
    new Student('B', 28, false, 80),
    new Student('C', 30, true, 90),
    new Student('D', 40, false, 66),
    new Student('E', 18, true, 88),
  ];


{
    const res = students.filter((student) => student.enrolled);
    console.log(res);
}
```



**💡map**

* make an array containing only the students' scores
* .map() : map은 배열안에 들어있는 모든 요소들을 원하는 함수를 이용해서 리턴되어진 값들로 대체함

```javascript
class Student {
    constructor(name, age, enrolled, score) {
      this.name = name;
      this.age = age;
      this.enrolled = enrolled;
      this.score = score;
    }
  }
  
  const students = [
    new Student('A', 29, true, 45),
    new Student('B', 28, false, 80),
    new Student('C', 30, true, 90),
    new Student('D', 40, false, 66),
    new Student('E', 18, true, 88),
  ];


{
    const res4 = students.map((student) => student.score);
    console.log(res4);
}
```



**💡some,  every**

* check if there is a student with the score lower than 50
* .some() : 배열중에 어떤것이라도 하나 만족되는 것이 있는지 없는지 검사할떄는 some
* .every() : 모든 배열의 조건이 만족되야할 때 every

```javascript
class Student {
    constructor(name, age, enrolled, score) {
      this.name = name;
      this.age = age;
      this.enrolled = enrolled;
      this.score = score;
    }
  }
  
  const students = [
    new Student('A', 29, true, 45),
    new Student('B', 28, false, 80),
    new Student('C', 30, true, 90),
    new Student('D', 40, false, 66),
    new Student('E', 18, true, 88),
  ];


{
    console.clear();
    const res5 = students.some((student) => student.score < 50);
    console.log(res5); //true 배열중에 어떤것이라도 하나 만족되는 것이 있는지 없는지 검사할떄는 some

    const res55 = students.every((student) => student.score < 50);
    console.log(res55); //false 모든 배열의 조건이 만족되야할 때 every
}
```



**💡reduce**

* compute students' average score
* 배열에 있는 모든 요소들의 값을 누적하는, 함께 모아놓을때 쓰는구나
* 배열 하나하나를 돌면서 무언가 값을 누적할때 쓰는 것
* reduceRight은 array의 제일 뒤부터 시작
* 콜백함수와 초기값을 전달
* 콜백함수는 array의 모든 item에서 실행

```javascript
class Student {
    constructor(name, age, enrolled, score) {
      this.name = name;
      this.age = age;
      this.enrolled = enrolled;
      this.score = score;
    }
  }
  
  const students = [
    new Student('A', 29, true, 45),
    new Student('B', 28, false, 80),
    new Student('C', 30, true, 90),
    new Student('D', 40, false, 66),
    new Student('E', 18, true, 88),
  ];


{
    console.clear();
    const result = students.reduce((prev, curr) => {
        console.log(prev);
        console.log(curr);
        return prev + curr.score;
    }, 0);
    console.log(result / students.length);
    // const res6 = students.reduce((prev, curr) => prev + curr.score, 0);
}
```



**💡sort**

* sorted in ascending order
* result should be: '45, 66, 80, 88, 90'
* 콜백 함수에 a, b(이전값, 현재값)이 전달
* 값을 return하면 첫번째가 뒤보다 작다고 간주되어 정렬

```javascript
class Student {
    constructor(name, age, enrolled, score) {
      this.name = name;
      this.age = age;
      this.enrolled = enrolled;
      this.score = score;
    }
  }
  
  const students = [
    new Student('A', 29, true, 45),
    new Student('B', 28, false, 80),
    new Student('C', 30, true, 90),
    new Student('D', 40, false, 66),
    new Student('E', 18, true, 88),
  ];


{
    const res = students.map(student => student.score)
    .sort((a,b)=>a-b)
    .join();
    console.log(res)
}
```
