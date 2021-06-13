---
layout: layouts/post.njk
title: message
templateClass: tmpl-post
eleventyNavigation:
  key: message
  order: 5

---




<form action="/action_page.php" id="usrform">
  <label for="fname">First name:</label><br>
  <input type="text" id="fname" name="fname"><br>
  <label for="sname">Sir name:</label><br>
  <input type="text" id="sname" name="sname"><br>
  <label for="email">Email:</label><br>
  <input type="email" id="email" name="email"><br>

  --- 
  
  <textarea rows="4" cols="50" name="comment" form="usrform">
  Enter text here...</textarea><br>
  <input type="submit"><br> 
</form>
