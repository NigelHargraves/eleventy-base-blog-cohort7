---
title: Loops, Arrays and Objects - Practical lesson tasks post.
description: This is a post on My Blog about Loops, Arrays and Objects - Practical lesson tasks.
date: 2021-07-01
tags: second tag
layout: layouts/post.njk
---

## Task 1 - Shopping Cart

We are going to be using an array of objects provided as a simple shopping cart example,
We need to work out the total cost of the items in the shopping cart.

Part 1
1. Create a function that takes 1 argument (the array)
2. Create a variable inside the function called “totalPrice”
3. Loop through each item in the array and add the value of the item to the total price, remember to account for the quantity.
4. Return the totalPrice Variable
5. Console.log the returned value

example code:

``` js
/*Create cart and string variable.
Create a function that takes 1 argument (cart),
Create a variable called totalPrice inside the function,
Loop through each item in the array
add itemPrice to totalPrice and account for quantity and return result.
document.write() the returned value.*/

let cart = [
  { name: "loaf of bread", type: "food", quantity: 1, price: 0.85 },
  { name: "multipack beans", type: "food", quantity: 1, price: 1 },
  { name: "mushrooms", type: "food", quantity: 10, price: 0.1 },
  { name: "can of beer", type: "alcohol", quantity: 4, price: 1.1 },
  { name: "prosecco", type: "alcohol", quantity: 1, price: 8.99 },
  { name: "steak", type: "food", quantity: 2, price: 3.99 },
  { name: "blue cheese", type: "food", quantity: 1, price: 2.99 },
  { name: "candles", type: "home", quantity: 3, price: 1.99 },
  { name: "cheesecake", type: "food", quantity: 1, price: 4.99 },
  { name: "onions", type: "food", quantity: 3, price: 0.4 },
];

//create function named addToCart.
function getTotal(cart){
  let totalPrice = 0;//integer variable.
  //loop through the items in cart.
  for (i = 0; i < cart.length; i++){
    totalPrice += (cart[i].price * cart[i].quantity);  //add to totalPrice and acount for quantity.
  }
  return totalPrice;
}

document.write(getTotal(cart).toFixed(2));//call function, pass parameter and display result.
```


Part 2
