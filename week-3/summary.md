# WRITING TEST WEEK 3

03 Oktober 2022 - 07 Oktober 2022
***

## Javascript Intermediate - Array & Multidimensional Array

### Array

Salah satu cara untuk mengakses array adalah menggunakan perulangan (array), bisa menggunakan for, while atau do while. Berikut cara mengakses array menggunakan for loop.

```js
    let arr = [1, 2, 3, 4, 5];
    for (let i = 0; i < arr.length; i++) {
        console.log(arr[i]);
    }

    /* output
    1
    2
    3
    4
    5
    */
```

Ada juga beberapa built-in method yang bisa digunakan untuk mengakses array, berikut contohnya:

```js
    // forEach()
    let colors = ['blue', 'red', 'yellow', 'green'];

    colors.forEach(data => {
        console.log(data)
    });

    /* output
    blue
    red
    yellow
    green
    */
```

```js
    // map()
    let input = [100, 50, 60, 10]

    let output = input.map(item => {
        return item;
    })

    // output [100, 50, 60, 10]

```

### Array Multidimensional

Array multidimensi merupakan array biasa yang di dalamnya terdapat data array, atau biasa dibilang array di dalam array.

berikut contoh array multidimensi:

```js
    let inventory = [
        ["kaos polos", 21],
        ["jaket hoodie", 13],
        ["topi", 7]
    ];
```

## Object & Array of Object

Array of object merupakan data data object yang berada di dalam array, berikut contohnya:

```js
    const flowerGarden = [
        {
            name: "jasmine",
            color: "white"
        },
        {
            name: "rose",
            color: "red"
        },
        {
            name: "violet",
            color: "blue"
        }
    ];

    console.log(flowerGarden);
```