---
toc: True
comments: True
layout: post
title:  Fitness Table
description: review ticket
courses: {'compsci': {'week': 0}}
type: hacks
---
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Data Table</title>
    <style>
        /* CSS styles for the table */
    </style>
</head>
<body>
    <h2> Data Table</h2>
    <table id="fitnessTable">
        <thead>
            <tr>
                <th>Name</th>
                <th>Fitness Type</th>
                <th>Age</th>
            </tr>
        </thead>
        <tbody>
            <!-- Data will be populated here -->
        </tbody>
    </table>

<script>
        // Retrieve user's data from localStorage
        const username = localStorage.getItem("username");

        // Example data, you would typically retrieve this from a server or other source
        const userData = [
            { name: "John Doe", fitnessType: "Cardio", age: 35 },
            { name: "Jane Smith", fitnessType: "Strength", age: 28 },
            { name: "toby", fitnessType: "Flexibility", age: 15 } // Using the username obtained from localStorage
        ];

        // Populate the table with user's data
        const tableBody = document.querySelector("#fitnessTable tbody");
        userData.forEach(user => {
            const row = document.createElement("tr");
            row.innerHTML = `
                <td>${user.name}</td>
                <td>${user.fitnessType}</td>
                <td>${user.age}</td>
            `;
            tableBody.appendChild(row);
        });
    </script>
</body>
</html>
