# ๐ฅฐ Go Day-6

```javascript
//31. ๋ฐฐ์ด ๋ฉ์๋ find() : ๋ฐ์ดํฐ ์์ ์ฐพ๊ธฐ
      {
        const arr31 = [100, 200, 300, 400, 500];

        // const target1 = arr31.find(function(){});
        const target1 = arr31.find(element => {
          return element === 100;
          // return element === 600; undefined
        })
        const target2 = arr31.find(el => el == 200); //์ถ์ฝ

        document.write('*** 31. ๋ฐฐ์ด ๋ฉ์๋ find() ***<br>');
        document.write(target1,'<br>');
        document.write(target2,'<br>');
      }
      //32. ๋ฐฐ์ด ๋ฉ์๋ filter() : ๋ฐ์ดํฐ ์์ ์ฐพ๊ธฐ
      {
        const arr32 = [100, 200, 300, 400, 500];

        // const target1 = arr32.find(function(){});
        const target3 = arr32.filter(element => {
          return element === 100;
        })
        const target4 = arr32.filter(el => el == 200);

        document.write('*** 32. ๋ฐฐ์ด ๋ฉ์๋ filter() ***<br>');
        document.write(target3,'<br>');
        document.write(target4,'<br>');
      }
      //33. ๋ฐฐ์ด ๋ฉ์๋ reduce() : ๋ฐ์ดํฐ ๋ชจ๋  ๊ฐ์ ํฉ์ฐ
      {
        const arr33 = [100, 200, 300, 400, 500];

        const sum1 = arr33.reduce((prev, current) => {
          return prev + current;
        })
        const sum2 = arr33.reduce((p, c) => p + c);

        document.write('*** 33. ๋ฐฐ์ด ๋ฉ์๋ reduce() ***<br>');
        document.write(sum1,'<br>');
        document.write(sum2,'<br>');
      }

      //34. ๋ฐฐ์ด ๊ตฌ์กฐ ๋ถํด ํ ๋น
      {
        const arr34 = [100, 200, 'javescript'];

        // const num1 = arr[0];
        // const num1 = arr[0];
        // const num1 = arr[0];

        const [num1 , num2 , num3] = arr34;
        document.write('*** 34. ๋ฐฐ์ด ๊ตฌ์กฐ ๋ถํด ํ ๋น ***<br>');
        document.write(num1,'<br>');
        document.write(num2,'<br>');
        document.write(num3,'<br>');
      }

      //๋ณ์ : ๋ฐ์ดํฐ ์ ์ฅ์ (ํ๊ณ)
      // ๋ฐฐ์ด : ๋ฐ์ดํฐ ์ ์ฅ์ (ํ๊ฐ ์ด์)
      // ๊ฐ์ฒด : ๋ฐ์ดํฐ ์ ์ฅ์ (ํค์ ๊ฐ์ผ๋ก ์ ์ฅ)
      // ๋ด์ฅ ๊ฐ์ฒด : ์๋ฐ์คํฌ๋ฆฝํธ์์ ๋ง๋ค์ด์ง ๊ฐ์ฒด(๋งค์๋)
      // ํจ์ : ์คํ๋ฌธ, ์ฌํ์ฉ
      // ํด๋์ค : ์คํ๋ฌธ, ์ฌํ์ฉ, ํจ์์ ์งํฉ์ฒด

      //35. ๊ฐ์ฒด(๊ฐ์ฒด ์ ์ธํ๊ธฐ1)
      {
        const obj1 = new Object();

        obj1[0] = 100;
        obj1[1] = 200;
        obj1[2] = 'javescript';

        document.write('*** 35. ๊ฐ์ฒด(๊ฐ์ฒด ์ ์ธํ๊ธฐ1) ***<br>');
        document.write(obj1[0],'<br>');
        document.write(obj1[1],'<br>');
        document.write(obj1[2],'<br>');
      }

      //36. ๊ฐ์ฒด(๊ฐ์ฒด ์ ์ธํ๊ธฐ2)
      {
        const obj2 = new Object();

        obj2.a = 100;
        obj2.b = 200;
        obj2.c = 'javescript';

        document.write('*** 36. ๊ฐ์ฒด(๊ฐ์ฒด ์ ์ธํ๊ธฐ2) ***<br>');
        document.write(obj2.a,'<br>');
        document.write(obj2.b,'<br>');
        document.write(obj2.c,'<br>');
      }

      //37. ๊ฐ์ฒด(๊ฐ์ฒด ์ ์ธํ๊ธฐ3)
      {
        const obj3 = {}; //๋น ๊ฐ์ฒด์ ํค๊ฐ์ ๋ฃ์

        obj3.a = 100;
        obj3.b = 200;
        obj3.c = 'javescript';

        document.write('*** 37. ๊ฐ์ฒด(๊ฐ์ฒด ์ ์ธํ๊ธฐ3) ***<br>');
        document.write(obj3.a,'<br>');
        document.write(obj3.b,'<br>');
        document.write(obj3.c,'<br>');
      }

      //38. ๊ฐ์ฒด(๊ฐ์ฒด ์ ์ธํ๊ธฐ4)
      {
        const obj4 = {
          a : 100,
          b : 200,
          c : 'javescript'
        }; 


        document.write('*** 38. ๊ฐ์ฒด(๊ฐ์ฒด ์ ์ธํ๊ธฐ4) ***<br>');
        document.write(obj4.a,'<br>');
        document.write(obj4.b,'<br>');
        document.write(obj4.c,'<br>');
      }

      //39. ๊ฐ์ฒด(๊ฐ์ฒด ์ ์ธํ๊ธฐ5)
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


        document.write('*** 39. ๊ฐ์ฒด(๊ฐ์ฒด ์ ์ธํ๊ธฐ5) ***<br>');
        document.write(obj5[2].name,'<br>');
        document.write(obj5[2].age,'<br>');
      }

      //40. ๊ฐ์ฒด(๊ฐ์ฒด ์ ์ธํ๊ธฐ6)
      {
        const obj6 = {
          a :100,
          b :[200, 300],
          c :'javescript'
        }

        document.write('*** 40. ๊ฐ์ฒด(๊ฐ์ฒด ์ ์ธํ๊ธฐ6) ***<br>');
        document.write(obj6.a,'<br>');
        document.write(obj6.b[0],'<br>');
        document.write(obj6.b[1],'<br>');
        document.write(obj6.c,'<br>');
      }

      //41. ๊ฐ์ฒด( ๊ฐ์ฒด ์์ ๋ณ์)
      {
        const a = 100;
        const b = 200;
        const c = 'javescript';

        const obj7 = {a, b, c};
        document.write('*** 41. ๊ฐ์ฒด( ๊ฐ์ฒด ์์ ๋ณ์) ***<br>');
        document.write(obj7.a,'<br>');
        document.write(obj7.b,'<br>');
        document.write(obj7.c,'<br>');
      }

      //42.๊ฐ์ฒด (๊ฐ์ฒด ์์ ํจ์)
      {
        const obj8 = {
          a : 100,
          b : [200, 300],
          c : 'javescript',
          d : function(){
            document.write('์๋ฐ์คํฌ๋ฆฝํธ๊ฐ ์คํ๋์์ต๋๋ค.<br>')
          },
          e : function(){
            document.write( this.b[1] +'๊ฐ ์คํ๋์์ต๋๋ค.')
            // document.write( this.c +'๊ฐ ์คํ๋์์ต๋๋ค.')
          }
        };

        document.write('*** 42.๊ฐ์ฒด (๊ฐ์ฒด ์์ ํจ์) ***<br>');
        document.write(obj8.a,'<br>');
        document.write(obj8.b,'<br>');
        document.write(obj8.b[0],'<br>');
        document.write(obj8.b[1],'<br>');
        document.write(obj8.c,'<br>');
        obj8.d();
        obj8.e();
      }
```
