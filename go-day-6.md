# 🥰 Go Day-6

```javascript
//31. 배열 메서드 find() : 데이터 요소 찾기
      {
        const arr31 = [100, 200, 300, 400, 500];

        // const target1 = arr31.find(function(){});
        const target1 = arr31.find(element => {
          return element === 100;
          // return element === 600; undefined
        })
        const target2 = arr31.find(el => el == 200); //축약

        document.write('*** 31. 배열 메서드 find() ***<br>');
        document.write(target1,'<br>');
        document.write(target2,'<br>');
      }
      //32. 배열 메서드 filter() : 데이터 요소 찾기
      {
        const arr32 = [100, 200, 300, 400, 500];

        // const target1 = arr32.find(function(){});
        const target3 = arr32.filter(element => {
          return element === 100;
        })
        const target4 = arr32.filter(el => el == 200);

        document.write('*** 32. 배열 메서드 filter() ***<br>');
        document.write(target3,'<br>');
        document.write(target4,'<br>');
      }
      //33. 배열 메서드 reduce() : 데이터 모든 값을 합산
      {
        const arr33 = [100, 200, 300, 400, 500];

        const sum1 = arr33.reduce((prev, current) => {
          return prev + current;
        })
        const sum2 = arr33.reduce((p, c) => p + c);

        document.write('*** 33. 배열 메서드 reduce() ***<br>');
        document.write(sum1,'<br>');
        document.write(sum2,'<br>');
      }

      //34. 배열 구조 분해 할당
      {
        const arr34 = [100, 200, 'javescript'];

        // const num1 = arr[0];
        // const num1 = arr[0];
        // const num1 = arr[0];

        const [num1 , num2 , num3] = arr34;
        document.write('*** 34. 배열 구조 분해 할당 ***<br>');
        document.write(num1,'<br>');
        document.write(num2,'<br>');
        document.write(num3,'<br>');
      }

      //변수 : 데이터 저장소 (한계)
      // 배열 : 데이터 저장소 (한개 이상)
      // 객체 : 데이터 저장소 (키와 값으로 저장)
      // 내장 객체 : 자바스크립트에서 만들어진 객체(매서드)
      // 함수 : 실행문, 재활용
      // 클래스 : 실행문, 재활용, 함수의 집합체

      //35. 객체(객체 선언하기1)
      {
        const obj1 = new Object();

        obj1[0] = 100;
        obj1[1] = 200;
        obj1[2] = 'javescript';

        document.write('*** 35. 객체(객체 선언하기1) ***<br>');
        document.write(obj1[0],'<br>');
        document.write(obj1[1],'<br>');
        document.write(obj1[2],'<br>');
      }

      //36. 객체(객체 선언하기2)
      {
        const obj2 = new Object();

        obj2.a = 100;
        obj2.b = 200;
        obj2.c = 'javescript';

        document.write('*** 36. 객체(객체 선언하기2) ***<br>');
        document.write(obj2.a,'<br>');
        document.write(obj2.b,'<br>');
        document.write(obj2.c,'<br>');
      }

      //37. 객체(객체 선언하기3)
      {
        const obj3 = {}; //빈 객체에 키값을 넣음

        obj3.a = 100;
        obj3.b = 200;
        obj3.c = 'javescript';

        document.write('*** 37. 객체(객체 선언하기3) ***<br>');
        document.write(obj3.a,'<br>');
        document.write(obj3.b,'<br>');
        document.write(obj3.c,'<br>');
      }

      //38. 객체(객체 선언하기4)
      {
        const obj4 = {
          a : 100,
          b : 200,
          c : 'javescript'
        }; 


        document.write('*** 38. 객체(객체 선언하기4) ***<br>');
        document.write(obj4.a,'<br>');
        document.write(obj4.b,'<br>');
        document.write(obj4.c,'<br>');
      }

      //39. 객체(객체 선언하기5)
      {
        const obj5 = [
          {
            name : 'juhee',
            age : 27
          }, 
          {
            name : 'juhee22',
            age : 250
          },
          {
            name : 'juhee33',
            age : 500
          }
        ]


        document.write('*** 39. 객체(객체 선언하기5) ***<br>');
        document.write(obj5[2].name,'<br>');
        document.write(obj5[2].age,'<br>');
      }

      //40. 객체(객체 선언하기6)
      {
        const obj6 = {
          a :100,
          b :[200, 300],
          c :'javescript'
        }

        document.write('*** 40. 객체(객체 선언하기6) ***<br>');
        document.write(obj6.a,'<br>');
        document.write(obj6.b[0],'<br>');
        document.write(obj6.b[1],'<br>');
        document.write(obj6.c,'<br>');
      }

      //41. 객체( 객체 속에 변수)
      {
        const a = 100;
        const b = 200;
        const c = 'javescript';

        const obj7 = {a, b, c};
        document.write('*** 41. 객체( 객체 속에 변수) ***<br>');
        document.write(obj7.a,'<br>');
        document.write(obj7.b,'<br>');
        document.write(obj7.c,'<br>');
      }

      //42.객체 (객체 속에 함수)
      {
        const obj8 = {
          a : 100,
          b : [200, 300],
          c : 'javescript',
          d : function(){
            document.write('자바스크립트가 실행되었습니다.<br>')
          },
          e : function(){
            document.write( this.b[1] +'가 실행되었습니다.')
            // document.write( this.c +'가 실행되었습니다.')
          }
        };

        document.write('*** 42.객체 (객체 속에 함수) ***<br>');
        document.write(obj8.a,'<br>');
        document.write(obj8.b,'<br>');
        document.write(obj8.b[0],'<br>');
        document.write(obj8.b[1],'<br>');
        document.write(obj8.c,'<br>');
        obj8.d();
        obj8.e();
      }
```
