---
layout: page
title: signup
permalink: /signup/
---

<!-- Blog Sign-up Form -->
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
</style>

<form class="signup-form" action="https://script.google.com/macros/s/AKfycbzW8YJ3ZRjmYg8-qqXYFOjzxTdlJ2ufpWvrVhIPZlWV6joJ5-cOFepbGTDGP8d_wL0J/exec" method="post">
  <h2>Sign up to our newsletter</h2>
  <label for="name">Name:</label>
  <input type="text" id="name" name="name" placeholder="Your name" required>

  <label for="email">Email:</label>
  <input type="email" id="email" name="email" placeholder="you@example.com" required>

  <button type="submit">Subscribe</button>
</form>