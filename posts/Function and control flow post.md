---
title: This is my Programming Concepts - Task post.
description: This is a post on My Blog about Programming Concepts - Task.
date: 2021-06-18
tags: second tag
layout: layouts/post.njk
---
In this lesson I learnt about functions, the first function was just to write out a sentence. I created a function and gave it a name 'myFunction' then in side the function I used document.write to write out a sentence, the next step is to use the function this is done by typing the function name followed by parentheses, these are used to pass arguments to the function as you will see in the next function.

The next function is to take a first name and a last name and combine them to make a full name, the name of the function is 'combineNames' when the function is called the first name and last name are passed to it inside parentheses i.e. combineNames('Nigel','Hargraves');.The Nigel is passed to the firstName parameter and the Hargraves is passed to the lastName parameter inside the functions parentheses i.e. function combineNames(firstName, secondName), this so they can be used inside the function.thenext step is to write out the full name this is done inside the function using document.write i.e. document.write(firstName + ' ' + secondName);, notice that I have to add a space inbetween the first and last names.

As well as receiving parameters a function can also return them, I created a function called 'returnFunction' and inside the function I am going to square a number and return the result i.e. return number * number;. To call the function I have to pass it a number i.e. const multiplyNumber = returnFunction(3); so the variable name 'number' inside the function is given the value of 3, when the calculation has done the returning number will be 9 so the variable 'multiplyNumber' is given the value of 9 and then we write out the result i.e. document.write('this is the number: ' + multiplyNumber);.

The next function is going to use if else statments and the logical operator and'&&', first I pass the function the temperature i.e. temperature(-10); then inside the function named 'temperature' the variable 'tempnumber' is given the value of -10, inside the function I use if else and '&&' statments to calculate what range the temperature is at so I can decide to wear a coat or coat and hat or it's to cold or pants and vest is fine the code looks like this. 

function temperature(tempNumber){
  if (tempNumber < 50 && tempNumber >= 30)  {
    document.write('wear a coat: ');
  } else if (tempNumber < 30 && tempNumber >= 0) {
    document.write('wear a coat and a hat: ');
  }  else if (tempNumber < 0) {
    document.write('it is to cold stay inside') 
  } else {
    document.write('just pants and vest is fine')
  }  
} 

When the tempNumber variable falls inside the rage set in each if statment the message in the document.write is written out, if the variable tempNumber is not in any of the ranges then the last else statment is executed so the number must be 50 or above.