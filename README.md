# π Go Day-1

```javascript
// 01. λ³μ : λ°μ΄ν° μ μ₯μ, λ°μ΄ν° λ³κ²½, λ°μ΄ν° μΆκ°
{
    var x = 100;
    var y = 200;
    var z = 'js';

    document.write('*********** 01. λ³μ ***********<br>');
    document.write(x, '<br>');
    document.write(y, '<br>');
    document.write(z, '<br>');
    document.write(x + y, '<br>');
    document.write(x % y, '<br><br>');
    // λͺ«μ κ΅¬νλ λ°©λ²
    document.write(Math.floor (y / x), '<br><br>'); 
}

// 02. λ³μ : λ³νλ λ°μ΄ν°
{
    let x = 100;
    let y = 200;
    let z = 'js';
    
    x = 200;
    y = 300;
    z = 'javascript';

    document.write('*********** 02. λ³μ ***********<br>');
    document.write(x, '<br>');
    document.write(y, '<br>');
    document.write(z, '<br>');
    document.write(x + y, '<br>');
    document.write(x % y, '<br><br>');
    // λͺ«μ κ΅¬νλ λ°©λ²
    document.write(Math.floor (y / x), '<br><br>'); 
}

// 03. μμ : λ°μ΄ν° μ μ₯μ, λ³νμ§ μλ λ°μ΄ν°
{
    const x = 100;
    const y = 200;
    const z = 'js';
    
    document.write('*********** 03. μμ ***********<br>');
    document.write(x, '<br>');
    document.write(y, '<br>');
    document.write(z, '<br>');
    document.write(x + y, '<br>');
    document.write(x % y, '<br><br>');
    // λͺ«μ κ΅¬νλ λ°©λ²
    document.write(Math.floor (y / x), '<br><br>'); 
}


// 04. λ°°μ΄ : λ°μ΄ν° μ μ₯μ, μ¬λ¬κ°λ₯Ό μ μ₯, λ°°μ΄ μ μΈ1
{
    const arr1 = new Array();
    arr1[0] = 100;
    arr1[1] = 200;
    arr1[2] = 'javascript';

    document.write('*********** 04. λ°°μ΄ ***********<br>');
    document.write(arr1[0], '<br><br>');
}

// 05. λ°°μ΄ : λ°μ΄ν° μ μ₯μ, μ¬λ¬κ°λ₯Ό μ μ₯, λ°°μ΄ μ μΈ2
{
    const arr2 = new Array(100, 200, 'javascript')
    document.write('*********** 05. λ°°μ΄ ***********<br>');
    document.write(arr2[0], '<br>');
    document.write(arr2[1], '<br>');
    document.write(arr2[2], '<br><br>');
}

// 06. λ°°μ΄ : λ°μ΄ν° μ μ₯μ, μ¬λ¬κ°λ₯Ό μ μ₯, λ°°μ΄ μ μΈ3
{
    const arr3 = []
    arr3[0] = 100;
    arr3[1] = 200;
    arr3[2] = 'javascript';
    document.write('*********** 06. λ°°μ΄ ***********<br>');
    document.write(arr3[0], '<br>');
    document.write(arr3[1], '<br>');
    document.write(arr3[2], '<br><br>');
}

// 07. λ°°μ΄ : λ°μ΄ν° μ μ₯μ, μ¬λ¬κ°λ₯Ό μ μ₯, λ°°μ΄ μ μΈ4
{
    const arr4 = [100, 200, 'javascript']

    document.write('*********** 07. λ°°μ΄ ***********<br>');
    document.write(arr4[0], '<br>');
    document.write(arr4[1], '<br>');
    document.write(arr4[2], '<br><br>');
}

// 08. 2μ°¨ λ°°μ΄
{
    const arr5 = [100, 200, ['javascript' , 'react'] ];

    document.write('*********** 08. 2μ°¨ λ°°μ΄ ***********<br>');
    document.write(arr5[2][1], '<br><br>');
}

// 09. λ°°μ΄ κ°―μ
{
    const arr6 = [100, 200, 300, 400, 500];
    document.write('*********** 09. λ°°μ΄ κ°―μ ***********<br>');
    document.write(arr6.length, '<br><br>');
}

// 10. λ°°μ΄ λΆλ¬μ€κΈ°
{
    const arr7 = [100, 200, 300, 400, 500];


    document.write('*********** 10. λ°°μ΄ λΆλ¬μ€κΈ° ***********<br>');
    for (let i = 0; i < arr7.length; i++){
        document.write(arr7[i], '<br>')
    }
}
```
