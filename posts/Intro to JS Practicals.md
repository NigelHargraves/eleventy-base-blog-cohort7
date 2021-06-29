---
title: Intro to JS Practicals.
description: This is a post on My Blog about Intro to JS Practicals.
date: 2021-06-26
tags: second tag
layout: layouts/post.njk
---

## Task 1 - Percentage Calculator:

Create a function that is able to return a specific percentage of any number.
For example you want to know what 30% of 135 is,
1 Create a function named percentageCalculator,
2 Add 2 arguments for “number” and “percentage”,
3 Do the maths required to work out a percentage with the arguments,
4 Return the result of the maths,
5 Console.log the returned value.

example code:
``` text/2-3
//function to calculate percentage
function calcPercent(number, percent) {
    return (number / 100) * percent;
}

const result = calcPercent(135, 30); //declare variable and call function

console.log(result); //write result
```

## Task 2 - Switch Statement:

Customers can order 3 different types of drink and also select 3 sizes.
Cola, Lemonade, Orangeade, Small, Medium and Large.
The button they press have the values “cola”,”lemon”,”orange”
1 Create a function that will output the message “You have ordered a {size} of {softDrinkLabel}”,
2 Create a function named drinkOrder add 2 arguments for “size” and “drink”.
3 Use a switch statement to determine where the functional code needs to be written,
4 Create a message in each case statement to be returned.
5 Console.log the returned message.

example code:
``` text/2-3
//function to switch drinkType
function drinkOrder(size, type) {
    switch (type) {
        case "cola":
            drinkType = 'Cola';
            break;
        case "lemon":
            drinkType = 'Lemonade';
            break;
        case "orange":
            drinkType = 'Orangeade';
    }
    return `you have ordered a ${size} drink of ${drinkType}.`; //return result
}
//variables
var drinkSize = 'large',
    drinkType = 'lemon';

console.log(drinkOrder(drinkSize, drinkType)); //call function and pass parameters and write result
```


## Task 3 - Calculator:

We need to create a function capable of using the addition, subtraction, multiply, divider or modulus operator on 2 numbers provided.
1 Create a function named calculator
2 Add 3 arguments for “number1”, “number2” and “operator”
3 Use a switch statement to determine which operator to use
4 Add the math code for each operator in the case statement to return the value
5 Console.log a message “{number1} {operator} {number2} = {value}”

example code:
``` text/2-3
//function to calculate 2 numbers
function calculator(number1, number2, operator) {
    switch (operator) {
        case "+":
            value = number1 + number2;
            break;
        case "-":
            value = number1 - number2;
            break;
        case "*":
            value = number1 * number2;
            break;
        case "/":
            value = number1 / number2;
            break;
        case "%":
            value = number1 % number2;
    }
    return `${number1} ${operator} ${number2} = ${value}.`; //return result
}

//call function and pass parameters and write result
console.log(calculator(4, 3, "+"));
console.log(calculator(4, 3, "-"));
console.log(calculator(4, 3, "*"));
console.log(calculator(4, 3, "/"));
console.log(calculator(4, 3, "%"));
console.log(calculator(4, 2, "%"));
```
