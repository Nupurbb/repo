---
toc: True
comments: false
layout: post
title:  login
description: review ticket
courses: {'compsci': {'week': 0}}
type: tangibles
---

<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Login Page</title>
<style>
    body {
        font-family: Arial, sans-serif;
        background-color: #f4f4f4;
    }
    .container {
        max-width: 400px;
        margin: 50px auto;
        padding: 20px;
        background: #fff;
        border-radius: 5px;
        box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    }
    .form-group {
        margin-bottom: 20px;
    }
    .form-group label {
        display: block;
        font-weight: bold;
    }
    .form-group input {
        width: 100%;
        padding: 8px;
        border: 1px solid #ccc;
        border-radius: 4px;
    }
    .btn {
        display: block;
        width: 100%;
        padding: 10px;
        background-color: #007bff;
        color: #fff;
        border: none;
        border-radius: 4px;
        cursor: pointer;
    }
    .btn:hover {
        background-color: #0056b3;
    }
</style>
</head>
<body>
<div class="container">
    <h2>Login</h2>
    <div class="form-group">
        <label for="backendLink">Backend Link:</label>
        <input type="text" id="backendLink" placeholder="Enter backend link...">
    </div>
    <div class="form-group">
        <label for="username">Username:</label>
        <input type="text" id="username" placeholder="Enter your username...">
    </div>
    <div class="form-group">
        <label for="password">Password:</label>
        <input type="password" id="password" placeholder="Enter your password...">
    </div>
    <button class="btn" onclick="login()">Login</button>
</div>

<script>
    function login() {
        var backendLink = document.getElementById("backendLink").value;
        var username = document.getElementById("username").value;
        var password = document.getElementById("password").value;

        // Send login request to backend
        // Example:
        fetch http://127.0.0.1:5000 {
            method: 'POST',
            headers: {
                'Content-Type': 'application/json'
            },
            body: JSON.stringify({
                username: username,
                password: password
            })
        }
        .then(response => {
            if (response.ok) {
                alert('Login successful!');
                // Redirect or do something else after successful login
            } else {
                alert('Login failed!');
            }
        })
        .catch(error => {
            console.error('Error:', error);
            alert('An error occurred, please try again later.');
        });
    }
</script>
</body>
</html>
