---
layout: page
title: Contact Me
description: Drop me a line...
---

Have a question you want answered? Is there something you would like me to write about on the blog? Just use the form below to reach out to me. I can’t promise I will respond to every question, but I will try to either respond or post an entry to the blog relating to your inquiry.


<style>
label {
	display: inline-block;
	width: 300px;
	padding-bottom:15px;
}
input[type=text], input[type=email], input[type=textarea] {
	width: 300px;
}
input[type=submit] {
	margin-top:25px;
}
textarea {
	width: 100%;
}
</style>

<form name="submitContact" netlify-honeypot="bot-field" action="/thankyou" netlify>
  <p style="display:none;">
    <label>Don’t fill this out: <input name="bot-field"></label>
  </p>
  <p>
    <label>Name: <input type="text" name="name" size="40" required></label>
  </p>
  <p>
    <label>Email: <input type="text" name="email" size="40" required></label>
  </p>
  <p>
    <label>Comments: <textarea name="comments" rows="4" required></textarea></label>
  </p>
  <p>
    <button type="submit">Send</button>
  </p>
</form>
