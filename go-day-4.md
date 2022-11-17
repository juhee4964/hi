# 🙃 Go Day-4

```javascript
//20. 배열 메서드 reverse() : 배열 요소의 순서를 반대로 할 때
    {
      const arr17 = [100, 200, 300, 400, 500];

      document.write('*** 20. 배열 메서드 reverse() ***<br>');
      document.write(arr17.reverse(), '<br><br>');
    }

    //21. 배열 메서드 sort() : 배열 요소를 정렬할 때
    {
      const arr18 = [100, 200, 300, 400, 500];

      document.write('*** 21. 배열 메서드 sort() ***<br>');
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

    //22. 배열 메서드 slice() : 원하는 배열 요소를 가져올 때
    {
      const arr19 = [100, 200, 300, 400, 500];

      document.write('*** 22. 배열 메서드 slice() ***<br>');
      document.write(arr19.slice(1, 3), '<br>');
      document.write(arr19.slice(1, 4), '<br>');
      document.write(arr19.slice(1, 5), '<br>');
      document.write(arr19.slice(1, -1), '<br>');
      document.write(arr19.slice(1, -2), '<br>');
      document.write(arr19.slice(1, -3), '<br><br>');
    }

    //23. 배열 메서드 concat() : 배열을 결합할 때
    {
      const arr20 = [100, 200, 300];
      const arr21 = [400, 500, 600];

      document.write('*** 23. 배열 메서드 concat() ***<br>');
      document.write(arr20.concat(arr21), '<br><br>');
    }

    //24. 배열 메서드 shift() : 배열의 첫 번째 요소를 제거할 때
    {
      const arr22 = [100, 200, 300, 400, 500];

      document.write('*** 24. 배열 메서드 shift() ***<br>');
      document.write(arr22.shift(), '<br>');
      document.write(arr22, '<br><br>');
    }

    //25. 배열 메서드 unshift() : 배열의 앞 부분에 요소를 추가할 때
    {
      const arr23 = [200, 300, 400, 500];

      document.write('*** 25. 배열 메서드 unshift() ***<br>');
      document.write(arr23.unshift(100), '<br>');
      document.write(arr23, '<br><br>');
    }

    //26. 배열 메서드 pop() : 배열 마지막 요소를 제거할 때
    {
      const arr24 = [100, 200, 300, 400, 500];

      document.write('*** 26. 배열 메서드 pop() ***<br>');
      document.write(arr24.pop(), '<br>');
      document.write(arr24, '<br><br>');
    }

    //27. 배열 메서드 push() : 배열 마지막 요소에 추가할 때
    {
      const arr25 = [100, 200, 300, 400];

      document.write('*** 27. 배열 메서드 push() ***<br>');
      document.write(arr25.push(500), '<br>');
      document.write(arr25, '<br><br>');
    }

    //28. 배열 메서드 splice() : 배열 요소를 다른 요소로 변경
    {
      const arr26 = [100, 200, 300, 400, 500];

      document.write('*** 28. 배열 메서드 splice() ***<br>');
      //document.write(arr26.splice(1), "<br>");
      //document.write(arr26.splice(2), "<br>");
      //document.write(arr26.splice(3), "<br>");
      //document.write(arr26.splice(1,2), "<br>");
      //document.write(arr26.splice(1,3), "<br>");
      document.write(arr26.splice(1, 2, 201, 301), '<br>');
      document.write(arr26, '<br><br>');
    }

    //29. 배열 메서드 indexOf() : 배열 요소를 검색
    {
      const arr27 = [100, 200, 300, 400, 500];

      document.write('*** 29. 배열 메서드 indexOf() ***<br>');
      document.write(arr27.indexOf(200), '<br>');
      document.write(arr27.indexOf(300), '<br>');
      document.write(arr27.indexOf(400), '<br><br>');
    }

    //30. 배열 메서드 includes() : 데이터 요소 포함 여부 확인
    {
      const arr28 = [100, 200, 300, 400, 500];

      document.write('*** 30. 배열 메서드 indexOf() ***<br>');
      document.write(arr28.includes(200), '<br>');
      document.write(arr28.includes(300), '<br>');
      document.write(arr28.includes(600), '<br><br>');
    }
```
