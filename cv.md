# [rsschool-cv](www.google.com)

# Grigory Sadovskiy

## Frontend Developer

## Contact information

- **Phone:** +7 965 144-67-07
- **E-mail:** sadovskiy.grigory@yandex.ru
- **Telegram:** @brgrigo
- **GitHub:** [GrigorySadovskiyxyz](https://github.com/GrigorySadovskiyxyz)

## About Me

## Tech skills:

- HTML5/CSS3
- JavaScript (ES5/6+, Asynchronous)
- Webpack
- Bootstrap
- React
- Redux
- Node.js
- Typescript
- Sass/Less
- MongoDB
- Express
- Pug
- Python3
- Git (GitLab, Github)
- VS Code
- Vim (basics)
- Figma

## Learning

Among all skills I want to **highlight:** googling information in obscure situations, touch typing (~100-110 WPM), critical thinking, code quality optimization, asking right questions and solving thing on my own independetly.

I have a willingness to increase my competencies in the field of Frontend Development and MERN stack as well as in digitalization of the companies in industrial sector. Happy to solve complex tasks and ready for the new challenges.

## Code Examples

There is an array with information about payments:

```
const payments = [
  { createdAt: 1623456006400, sum: 300 },
  { createdAt: 1602374400000, sum: 144 },
  { createdAt: 1607731200320, sum: 300 },
  { createdAt: 1602374400300, sum: 20 },
  { createdAt: 1589155200000, sum: 10 },
  { createdAt: 1589155200020, sum: 250 },
  { createdAt: 1623456000000, sum: 170 },
  { createdAt: 1589155200000, sum: 300 },
  { createdAt: 1620691200100, sum: 40 },
  { createdAt: 1607731200010, sum: 200 },
  { createdAt: 1620691204100, sum: 15 },
  { createdAt: 1620691254500, sum: 15 },
  { createdAt: 1623456000400, sum: 37 },
  { createdAt: 1623456006800, sum: 200 },
  { createdAt: 1607731208320, sum: 400 },
];
```

There is an array with information about payments: where **_createdAt_** - time of payment in timestamp format, **_sum_** - amount of payment.

You need to write a function which will receive an array of payments and return the three most profitable days in descending order in the form:
**_"yyyyy-mm-dd": N_**
(**_"yyyyyy-mm-dd"_** is the date of payments, **_N_** is the sum of payments for this date)
(data structure for the result is at candidate's discretion).

```
let transformDatePayments = (arg) => arg.map(item => {
    const container = {};

    container.createdAt = newDate(item);
    container.sum = item.sum;

    return container;
})

function newDate(number) {
    let date = new Date(parseInt(number.createdAt));
    let formatYmd = date.toISOString().slice(0, 10);

    return formatYmd;
}

function getThreeMostProfitableDays(data) {
    if (typeof data === "undefined") {
        throw new Error("Invoked without arguments.")
    }
    if (data.length < 1) return []

    let arrayOfPayments = transformDatePayments(data);
    let resMap = new Map();
    let result = [];
    arrayOfPayments.map((x) => {
        if (!resMap.has(x.createdAt))
            resMap.set(x.createdAt, x.sum);
        else
            resMap.set(x.createdAt, (x.sum + resMap.get(x.createdAt)));
    })
    resMap.forEach((value, key) => {
        result.push({
            [key]: value
        })
    })

    result.sort((a, b) => b[Object.keys(b)[0]] - a[Object.keys(a)[0]]);

    return result.slice(0, 3);
}

getThreeMostProfitableDays(payments)
```

## Education

- **Lappeenranta-Lahti University of Technology, LUT.**
  Master's Programme in Global Management of Innovation and Technology 2019
- **Bauman Moscow State Technical University, BMSTU.** PhD Programme in 

- Courses:

  - [FreeCodeCamp](https://www.freecodecamp.org/)
  - [SICP JS](https://sourceacademy.org/sicpjs/index)
  - [Hexlet](https://en.hexlet.io/)
  - [The Odin Project](https://www.theodinproject.com/)
  - [Udemy](https://www.udemy.com/)

  ***

## Languages

Russian - native speaker.
English - C2 proficiency.
