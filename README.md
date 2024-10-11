# one-string-code

Задача перемішування ряду чисел.  Данний підхід може використовуватися:
- при генерації (вибору з наявних) випадкових кодів підтвердження або активації для смс та месендерів
- для швидкого перебору рядків таблиці без повтору в псеводвипадковому порядку
- для перемішування даних

В якості кроку S рекомедовано використовувати просте число, яке лежить близько до золотого перетину відрізку [0, L-1]. В цьому випадку числа, які мало відрізняються одне від одного, в переборі будуть стояти далеко від одного.

Код на js у файлі index.html. Запускається в браузері, результат виводиться в консоль браузеру.





const L = 100; // Number of values, starting from 0

const S = 3; // Step. L and S must have the greatest common divisor == 1

//Outputs values from 0 to L-1 in a pdeudo-random order (with step = S)

Array.apply(null,Array(L)).forEach((a,i)=>console.log((i*S%L)))

