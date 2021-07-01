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
5. Document.write the returned value

Example code:

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

1. Create a function that takes 1 argument (the array)
2. Create a variable inside the function called “totalPrice”
3. Loop through each item in the array and add the value of the item to the total price, remember to account for the quantity.
4. If the item has a type of “food” the total price is 20% less
5. Return the totalPrice Variable

Example code:

``` js

/*Create cart and string variable.
Create a function that takes 1 argument (cart),
Create a variable called totalPrice inside the function,
Loop through each item in the array
create itemPrice variable and multiply by quantity,
check if item is food type and add 20 % discount.
add itemPrice to totalPrice and return result.
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
  for (const item of cart){
    let itemPrice = item.price * item.quantity;//create variable and calc quantity.
    if (item.type === "food"){
      itemPrice -= (item.price * 20) / 100// add 20 % discount.
    }
   totalPrice += itemPrice;  //add to totalPrice.
  }
  return totalPrice;//return result.
}

document.write(getTotal(cart).toFixed(2));//call function, pass parameters and display result.
```


Part 3

1. Add 2 extra arguments to the function for “discountAmount” and “type”
2. Replace the logic that takes off 20% for object.type == “food” for object.type == type and allow the 20% to be the {discountAmount}%
3. Create logic so that if type == “any” all products have a discount applied

Example code:

```js
/*Create cart and string variable.
Create a function that takes 3
arguments (cart,discountAmount,type),
Create a variable called totalPrice inside the function,
Loop through each item in the array
check if we need to add a discount this can be set to any or an item.type
create variable itemPrice to equal price * quantity then check if we need to add
a discount, add itemPrice to totalPrice and return result.
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

let anyType = "any";//string variable.

//create function named addToCart.
function getTotal(cart,discountAmount,type){
  let totalPrice = 0;//integer variable.
  //loop through the items in cart.
  for (const item of cart){
    let itemPrice = item.price * item.quantity;//apply quantity
    //check to apply discount.
    if (type === "any" || type === item.type){
      itemPrice -= (itemPrice * discountAmount) / 100;
    }
     totalPrice += itemPrice;  //add to totalPrice.
  }
  return totalPrice;//return result.
}

document.write(getTotal(cart, 20, 'food').toFixed(2));//call function, pass parameters and display result.
```
Part 4

We are going to be using an array of objects provided as a simple shopping cart example.
We need to be able to work out which items cost between 2 price points. So for example, we need the cart to be returned by which products cost more than £2 but less than £5.
1. Create a function that has 3 arguments “cart”, “lowPrice” and “highPrice”.
2. Create an empty array called arrItems at the start of the function.
3. Loop through each item of the array.
4. If the price value is higher than or equal to the lowPrice and lower than or equal to the highPrice push to arrItems.

Example code:

```js
/*Create cart, create a function that takes 3
arguments (cart,lowPrice,highPrice),
Create an empty variable array called arrayItems inside the function,
Loop through each item in the cart and get the price
check if it is higher or equal to the low price and lower or equal to the high price.
If it is we can add various information to the new array i.e name, type, price, by useing .push.
Create another loop of arrayItems and display the items.*/

//cart object array.
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
]

//create function named getItem.
function getItem(cart,lowPrice,highPrice){
  let arrItems = []//create empty array.
  //loop for cart.
  for (const item of cart){
    //check if price is within the given values.
    if (item.price >= lowPrice && item.price <=highPrice){
      arrItems.push(`${item.name}  ${item.type}  £${item.price}`);//add the name,type and price to empty array.
    }
  }
  //loop for arrItems
  for (const item of arrItems){
    document.write(item + '</br>');//display array items.
  }
}

getItem(cart, 2, 5);//call function.
```

