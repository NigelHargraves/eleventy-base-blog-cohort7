---
title: This is my Pseudocode post.
description: This is a post on My Blog about Pseudocode.
date: 2021-06-27
tags: second tag
layout: layouts/post.njk
---

## What is Pseudocode?

It is a simpler version of programming code - it is written plain English, basically it is the thoughts of the programer thinking of a solution written down at the start of the program.

Also in the program are comments that are used to explane to the programmer or any other programmer what a section of the program is doing or is ment to do, there are symbols to tell the computer that this is a comment but the syntax varies in different program languages, the syntax in javascript for a block of text is /* and closing with */, the syntax for a line comment is //.

Here is an example of a program with pseudocode and comments.

/*Create a function called fixStart. It should take a single argument, a
string, and return a version where all occurrences of its first character
have been replaced with ‘*****’, except for the first character itself. You
can assume that the string is at least one character long.*/


//declare variable firstLetter.
//create fixStart function add string (str).
//create loop to start at 0 and last for string length.
//set first letter in string to variable (firstLetter).
//check the rest of the letters against the variable.
//if a letter = the variable replace the letter with '*'.
//display to user.

var firstLetter = "";

function fixStart(str){
  //create loop to string length.
  for (let i = 0; i < (str.length) + 1; i++){
    //set firstLetter variable.
    if (i == 0) {
      firstLetter = str.charAt(i);
      document.write(firstLetter);
      //check if any letters are the same as the firstLetter and if so change it to '*'.
    }else if (firstLetter == str.charAt(i)) {
      document.write("*");
      //else just display the letter.
    }else {
      document.write(str.charAt(i));
    }
  }
}

//call the function with these words.
fixStart("babble");
document.write('<br>');
fixStart("turtle");
document.write('<br>');
fixStart("memories");
document.write('<br>');
fixStart("puppies");
document.write('<br>');
fixStart("mummies");
