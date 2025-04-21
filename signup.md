---
layout: page
title: signup
permalink: /signup/
---

<style>
.signup-form {
  max-width: 400px;
  margin: 2rem auto;
  padding: 1.5rem;
  border: 1px solid #ccc;
  border-radius: 12px;
  font-family: sans-serif;
}
.signup-form h2 {
  text-align: center;
  margin-bottom: 1rem;
}
.signup-form label {
  display: block;
  margin-bottom: 0.25rem;
  font-weight: bold;
}
.signup-form input {
  width: 100%;
  padding: 0.5rem;
  margin-bottom: 1rem;
  border-radius: 6px;
  border: 1px solid #ddd;
}
.signup-form button {
  width: 100%;
  padding: 0.6rem;
  background-color: #007bff;
  color: white;
  font-weight: bold;
  border: none;
  border-radius: 6px;
  cursor: pointer;
}
.signup-form button:hover {
  background-color: #0056b3;
}
.message {
  text-align: center;
  font-weight: bold;
  margin-top: 1rem;
  display: none;
}
.message.success {
  color: green;
}
.message.error {
  color: red;
}
</style>

<form class="signup-form" id="blogSignupForm">
  <h2>Sign up for our newsletter</h2>
  <label for="name">Name:</label>
  <input type="text" id="name" name="name" placeholder="Your name" required>

  <label for="email">Email:</label>
  <input type="email" id="email" name="email" placeholder="you@example.com" required>

  <button type="submit">Subscribe</button>

  <div class="message" id="formMessage"></div>
</form>

<script>
document.getElementById("blogSignupForm").addEventListener("submit", async function(e) {
  e.preventDefault();
  
  const form = e.target;
  const name = form.name.value;
  const email = form.email.value;
  const messageBox = document.getElementById("formMessage");

  try {
    const response = await fetch("https://script.google.com/macros/s/AKfycbzW8YJ3ZRjmYg8-qqXYFOjzxTdlJ2ufpWvrVhIPZlWV6joJ5-cOFepbGTDGP8d_wL0J/exec", {
      method: "POST",
      body: new URLSearchParams({ name, email })
    });

    if (response.ok) {
      form.reset();
      messageBox.textContent = "🎉 Thanks for signing up!";
      messageBox.className = "message success";
      messageBox.style.display = "block";
    } else {
      throw new Error("Network error");
    }
  } catch (error) {
    messageBox.textContent = "Sorry, an error occured.  Don't worry, it's not you, it's us!  Please try again later.";
    messageBox.className = "message error";
    messageBox.style.display = "block";
  }
});
</script>