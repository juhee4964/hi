# 🥳 Go Day-3

<pre class="language-javascript"><code class="lang-javascript">// 15. 배열 조회하기
{
    const arr15  = [111, 222, 333, 444,'javascript' ]
    // => let arr = document.querySelectorAll('요소');
    const search = 'javascript'

    document.write('*********** 15. 배열 조회하기 ***********&#x3C;br>')
    for(let i=0; i &#x3C; arr15.length; i++){
        if(search == arr15[i])
        document.write(search + '를 찾았습니다.');
    }
    document.write('&#x3C;br>')
    
<strong>    // forEach
</strong>    arr15.forEach(element => {
        if(element == search)
            document.write(search + '를 찾았습니다.');
    });

<strong>    // map
</strong>    arr15.map(element => {
        if(element == search)
            document.write(search + '를 찾았습니다.');
    });
}

// 16. 배열 펼침 연산자
{
    document.write('*********** 16. 배열 펼침 연산자 ***********&#x3C;br>')
    const arr16 = [1, 2, 3, 4, 5];

    document.write('&#x3C;br>&#x3C;br>');
    document.write(arr16);

    document.write(...arr16);
    document.write('&#x3C;br>')
}

// 17. 배열 최댓값 구하기

document.write('*********** 17. 배열 최댓값 구하기 ***********&#x3C;br>')
const arr17 = [100, 200, 300, 400, 500]
let max = 0;

for(let i = 0; i &#x3C; arr17.length; i++){
    if(max &#x3C; arr17[i]){
        max = arr17[i];// 총 4번 변함
    }
}
document.write('&#x3C;br>')


// 포이치는 => 자바스크립트 문법 (제이쿼리랑 같이 쓰면 에러남)
// 이치는 => 제이쿼리 문법

// 18. Math로 최댓값,최솟값(min) 구하기
document.write('*********** 18. Math로 최댓값,최솟값(min) 구하기 ***********&#x3C;br>')
const arr18 = [100, 200, 300, 400, 500]
let Max = Math.max(...arr18);
let Min = Math.min(...arr18);

console.log(max)
console.log(Min)

// 19. 배열 매서드 join() : 배열 요소 결합하여 문자열 만들기
document.write('*********** 19. 배열 매서드 join() : 배열 요소 결합하여 문자열 만들기 ***********&#x3C;br>')
const arr19 = [100, 200, 300, 400, 500]
document.write(arr19.join('*'))


// 숙제 
{
    const arr17 = [100, 200, 300, 400, 500]
    let max = 0;
    arr17.map((value) => {
        if(max &#x3C; value){
            max = value  
        };
    });
    console.log(max)
    console.log(arr17)
}
{
    const arr18 = [100, 200, 300, 400, 500]
    let max = 0;
    arr18.forEach((value) => {
        if(max &#x3C; value){
            max = value
        };
    });
    console.log(max);
    console.log(arr18);
}</code></pre>

```html
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>

    <script src="https://code.jquery.com/jquery-3.6.1.js" integrity="sha256-3zlB5s2uwoUzrXK3BT7AX3FyvojsraNFxCc2vC/7pNI=" crossorigin="anonymous"></script>
    <style>
        div a {display: block; width: 100px; height: 100px; margin-bottom: 10px; background-color: aqua;}
    </style>
</head>
<body>
    <div>
        <a href="#" class="a"></a>
        <a class="a"></a>
        <a href="#" class="a"></a>
        <a class="a"></a>
    </div>
    
</body>
<script>
    let a = $('.a');
    console.log(a);
    $('.a').each(function(index,value){
        let aA = $(value).attr('href');
        if(aA === undefined){
            $(value).on('click',function(){
                alert('준비중')
            });
        };
    });



    let aState = $('.arl');

    aState.each(function(idx, el){
      let aa = $(el).attr('href');
      if(aa === undefined){
        $(el).on('click', function(){
          alert('Coming soon');
        });
      }
    });
</script>
</html>
```
