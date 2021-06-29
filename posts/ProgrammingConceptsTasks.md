---
title: This is my Programming Concepts - Task post.
description: This is a post on My Blog about Programming Concepts - Task.
date: 2021-06-15
tags: second tag
layout: layouts/post.njk
---
At the end of this lesson the take home task was to calculate a tip amount from a bill, I started with 2 functions one to calculate the tip as 2% of the bill and the other to add the bill and the tip to give the total bill. I then declared the variables like the pre tip bill, the tip percentage, first and last name, full name and a variable totalTip to call the tipTotal function. Then the last thing to do was to write out the results using document.write of full name total bill and tip amount.


example code:

``` js/2/4
//a function to return the value of the tip
function tipTotal() {
    return tipPercentage / 100 * preTipTotal; //calc tip;
}

//a function to calculate the total bill
function calcBill() {
    return preTipTotal + totalTip; //calc bill
}

//set variables
var preTipTotal = 19.74;
const tipPercentage = 2;
var firstName = ('Nigel');
var lastName = ('Hargraves');
var fullName = (firstName + ' ' + lastName);

var totalTip = tipTotal() //call tipTotal function

document.write(fullName + '<br>'); //display name
document.write('Your total bill, with tip, is £' + calcBill().toFixed(2) + '<br>'); //call calcBill function and display Bill to 2 decimal places
document.write('Your tip amount is £' + totalTip.toFixed(2)); //display tip amount to 2 decimal places
```
