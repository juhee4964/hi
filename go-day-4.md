# π Go Day-4

```javascript
//20. λ°°μ΄ λ©μλ reverse() : λ°°μ΄ μμμ μμλ₯Ό λ°λλ‘ ν  λ
    {
      const arr17 = [100, 200, 300, 400, 500];

      document.write('*** 20. λ°°μ΄ λ©μλ reverse() ***<br>');
      document.write(arr17.reverse(), '<br><br>');
    }

    //21. λ°°μ΄ λ©μλ sort() : λ°°μ΄ μμλ₯Ό μ λ ¬ν  λ
    {
      const arr18 = [100, 200, 300, 400, 500];

      document.write('*** 21. λ°°μ΄ λ©μλ sort() ***<br>');
      document.write(arr18.sort(), '<br>');
      document.write(
        arr18.sort(function (a, b) {
          return b - a;
        }),
        '<br>'
      );
      document.write(
        arr18.sort(function (a, b) {
          return a - b;
        }),
        '<br><br>'
      );
    }

    //22. λ°°μ΄ λ©μλ slice() : μνλ λ°°μ΄ μμλ₯Ό κ°μ Έμ¬ λ
    {
      const arr19 = [100, 200, 300, 400, 500];

      document.write('*** 22. λ°°μ΄ λ©μλ slice() ***<br>');
      document.write(arr19.slice(1, 3), '<br>');
      document.write(arr19.slice(1, 4), '<br>');
      document.write(arr19.slice(1, 5), '<br>');
      document.write(arr19.slice(1, -1), '<br>');
      document.write(arr19.slice(1, -2), '<br>');
      document.write(arr19.slice(1, -3), '<br><br>');
    }

    //23. λ°°μ΄ λ©μλ concat() : λ°°μ΄μ κ²°ν©ν  λ
    {
      const arr20 = [100, 200, 300];
      const arr21 = [400, 500, 600];

      document.write('*** 23. λ°°μ΄ λ©μλ concat() ***<br>');
      document.write(arr20.concat(arr21), '<br><br>');
    }

    //24. λ°°μ΄ λ©μλ shift() : λ°°μ΄μ μ²« λ²μ§Έ μμλ₯Ό μ κ±°ν  λ
    {
      const arr22 = [100, 200, 300, 400, 500];

      document.write('*** 24. λ°°μ΄ λ©μλ shift() ***<br>');
      document.write(arr22.shift(), '<br>');
      document.write(arr22, '<br><br>');
    }

    //25. λ°°μ΄ λ©μλ unshift() : λ°°μ΄μ μ λΆλΆμ μμλ₯Ό μΆκ°ν  λ
    {
      const arr23 = [200, 300, 400, 500];

      document.write('*** 25. λ°°μ΄ λ©μλ unshift() ***<br>');
      document.write(arr23.unshift(100), '<br>');
      document.write(arr23, '<br><br>');
    }

    //26. λ°°μ΄ λ©μλ pop() : λ°°μ΄ λ§μ§λ§ μμλ₯Ό μ κ±°ν  λ
    {
      const arr24 = [100, 200, 300, 400, 500];

      document.write('*** 26. λ°°μ΄ λ©μλ pop() ***<br>');
      document.write(arr24.pop(), '<br>');
      document.write(arr24, '<br><br>');
    }

    //27. λ°°μ΄ λ©μλ push() : λ°°μ΄ λ§μ§λ§ μμμ μΆκ°ν  λ
    {
      const arr25 = [100, 200, 300, 400];

      document.write('*** 27. λ°°μ΄ λ©μλ push() ***<br>');
      document.write(arr25.push(500), '<br>');
      document.write(arr25, '<br><br>');
    }

    //28. λ°°μ΄ λ©μλ splice() : λ°°μ΄ μμλ₯Ό λ€λ₯Έ μμλ‘ λ³κ²½
    {
      const arr26 = [100, 200, 300, 400, 500];

      document.write('*** 28. λ°°μ΄ λ©μλ splice() ***<br>');
      //document.write(arr26.splice(1), "<br>");
      //document.write(arr26.splice(2), "<br>");
      //document.write(arr26.splice(3), "<br>");
      //document.write(arr26.splice(1,2), "<br>");
      //document.write(arr26.splice(1,3), "<br>");
      document.write(arr26.splice(1, 2, 201, 301), '<br>');
      document.write(arr26, '<br><br>');
    }

    //29. λ°°μ΄ λ©μλ indexOf() : λ°°μ΄ μμλ₯Ό κ²μ
    {
      const arr27 = [100, 200, 300, 400, 500];

      document.write('*** 29. λ°°μ΄ λ©μλ indexOf() ***<br>');
      document.write(arr27.indexOf(200), '<br>');
      document.write(arr27.indexOf(300), '<br>');
      document.write(arr27.indexOf(400), '<br><br>');
    }

    //30. λ°°μ΄ λ©μλ includes() : λ°μ΄ν° μμ ν¬ν¨ μ¬λΆ νμΈ
    {
      const arr28 = [100, 200, 300, 400, 500];

      document.write('*** 30. λ°°μ΄ λ©μλ indexOf() ***<br>');
      document.write(arr28.includes(200), '<br>');
      document.write(arr28.includes(300), '<br>');
      document.write(arr28.includes(600), '<br><br>');
    }
```
