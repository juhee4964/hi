# 🤩 Go Day-2

```javascript
// 11. 배열 데이터 불러오기 (forEach)
{
    const arr8 = [100, 200, 300, 400, 500]
    document.write('*********** 11. 배열 불러오기 ***********<br>')
    // arr8. forEach(function(){}); - this 불러오기 가능
    // arr8. forEach(() => {}); - this 불러올 수 없음
    // arr8.forEach(function(element){
    //     document.write(element, '<br>')
    // })

    document.write('*********** 11-1. 배열 불러오기 ***********<br>')
    arr8.forEach(function(element, index, array){
        document.write(element, '<br>')
        // element 해당 요소 찾는거
        document.write(index, '<br>')
        // index 순서 찾는거
        document.write(array, '<br>')
        // array 배열 가저옴
    })

    document.write('<br>')
}

// 12. 배열 데이터 불러오기 (map) : 배열 요소를 추출하여 새 배열을 만듦
{
    const arr9 = [111, 222, 333, 444, 555]

    document.write('*********** 12. 배열 불러오기 ***********<br>')
    arr9.map((element, index, array) => {
        document.write(index, '<br>')
    })
    // 화살표 함수를 씀 즉, 익명 함수 
    document.write('<br>')
}
// 13. 배열 데이터 불러오기 (fon in 문)
{
    const arr10  = [111, 222, 333, 444, 555]

    document.write('*********** 13. 배열 불러오기 ***********<br>')
    for(let i in arr10){
        document.write(arr10[i], '<br>')
        document.write(i, '<br>')// index가 나옴 0,1,2,3,4
    }
    document.write('<br>')
}
// 14. 배열 데이터 불러오기 (fon of 문)
{
    const arr11  = [111, 222, 333, 444, 555]

    document.write('*********** 14. 배열 불러오기 ***********<br>')
    for(let i of arr11){
        document.write(i, '<br>')
    }
    document.write('<br>')
}

//  (fon in 문) (fon of 문) 차이 적기 


// test
{
    const a = 1;
    const b = 2;

    if(a == b){
        document.write(1);
    }else{
        document.write(-1);
    }

    document.write('<br>')
}

{
    let a = 95;

    if(a <= 100 && a >= 90){
        document.write("A")
    }else if(a <= 89 && a >= 70){
        document.write("B")
    }else if(a <= 69 && a >= 50){
        document.write("C")
    }else if(a <= 49 && a >= 40){
        document.write("D")
    }else if(a <= 39){
        document.write("B")
    }else{
        
    }
    
    
// 시험성적 A 90 ~ 100점
// 시험성적 B 70 ~ 89점
// 시험성적 C 50 ~ 69점
// 시험성적 D 40 ~ 49점
// 시험성적 F 그 이하 점수

// 시험성적은 0 ~ 100 점 까지며
// 각 상황별로 등급표가 나오게 코드를 작성해주세요
// 0 ~ 100 외의 값일 경우 "점수를 다시입력해주세요" 를 리턴해주세요.
let answer = 0;
document.write('<br>')
}
```
