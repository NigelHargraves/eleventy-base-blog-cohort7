---
layout: layouts/post.njk
title: message
templateClass: tmpl-post
eleventyNavigation:
  key: message
  order: 5

---




<form action="urlhere" id="usrform">
  <label for="fname">First name:</label><br>
  <input type="text" id="fname" name="fname" required><br>
  <br>
  <label for="sname">Sir name:</label><br>
  <input type="text" id="sname" name="sname" required><br>
  <br>
  <label for="email">Email:</label><br>
  <input type="email" id="email" name="email" required><br>
  <br>
  <textarea rows="4" cols="50" name="comment" form="usrform" required>
  Enter message here...</textarea><br>
  <input type="submit"><br> 
</form>
