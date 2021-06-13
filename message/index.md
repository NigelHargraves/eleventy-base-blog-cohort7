---
layout: layouts/post.njk
title: message
templateClass: tmpl-post
eleventyNavigation:
  key: message
  order: 5

---



<!--Form information for message-->
<form action="url here"  method="post" id="userform">
  <label for="fname">First name:</label><br>
  <input type="text" id="fname" name="fname" required><br>
  <br>
  <label for="sname">Sir name:</label><br>
  <input type="text" id="sname" name="sname" required><br>
  <br>
  <label for="email">Email:</label><br>
  <input type="email" id="email" name="email" required><br>
  <br>
  <textarea rows="4" cols="50" name="comment" form="userform" required>
  Enter message here...</textarea><br>
  <br>
  <input type="checkbox" id="t&c" name="t&c" required>
  <label for="t&c">Terms and Conditions</label><br>
  <br>
  <input type="submit"><br> 
</form>
