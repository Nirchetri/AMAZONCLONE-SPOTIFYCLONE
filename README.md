PRACTICAL 1 - WAP TO MAKE A ORDERED LIST
<!DOCTYPE html>
<html>
<head>
<title>Ordered List Example</title>
</head>
<body>
<h2>Example Ordered List</h2>
<ol>
<li>HTML</li>
<li>CSS</li>
<li>JAVASCRIPT</li>
<li>XML</li>
</ol>
</body>
</html>
*********************************************
PRACTICAL 2 - WAP TO MAKE A UNORDERED LIST
<!DOCTYPE html>
<html>
<head>
<title>Unordered List Example</title>
</head>
<body>
<h2>Web Technology</h2>
<ul>
<li>HTML</li>
<li>CSS</li>
<li>JAVASCRIPT</li>
<li>XML</li>
</ul>
</body>
</html>
*********************************************
PRACTICAL 3 - WAP TO MAKE A FORM HTML, CSS
<!DOCTYPE html>
<html>
<head>
<title>Simple Form</title>
<style>
body {
font-family: Arial, sans-serif;
background-color:#2f4f4f;
margin: 0;
padding: 0;
display: flex;
align-items: center;
justify-content: center;
height: 100vh;
}
form {
background-color: #fff;
padding: 20px;
border-radius: 8px;
box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
width: 300px;
}
label {
display: block;
margin-bottom: 8px;
}
input {
width: 100%;
padding: 8px;
margin-bottom: 16px;
box-sizing: border-box;
}
button {
background-color: #4caf50;
color: #fff;
padding: 10px;
border: none;
border-radius: 4px;
cursor: pointer;
width: 50%;
margin-left: 70px;
}
button:hover {
background-color: #45a049;
}
</style>
</head>
<body>
<form>
<label for="name">Name:</label>
<input type="text" id="name" name="name" required>
<label for="email">Email:</label>
<input type="email" id="email" name="email" required>
<label for="password">Password:</label>
<input type="password" id="password" name="password" required>
<button type="submit">Submit</button>
</form>
</body>
</html>
*********************************************
PRACTICAL 4 - WAP TO MAKE A TABLE
<!DOCTYPE html>
<html lang="en">
<head>
<title>Simple Table</title>
<style>
table {
border-collapse: collapse;
width: 50%;
margin: 20px auto;
}
th, td {
border: 1px solid #d9d8d8;
text-align: left;
padding: 8px;
}
th {
background-color: #f2f2f2;
}
</style>
</head>
<body>
<table border="1">
<thead>
<tr>
<th>Name</th>
<th>Age</th>
<th>City</th>
</tr>
</thead>
<tbody>
<tr>
<td>Peter Parker</td>
<td>23</td>
<td>New York</td>
</tr>
<tr>
<td>Mary Jane</td>
<td>23</td>
<td>Los Angeles</td>
</tr>
<tr>
<td>Harry Osborn</td>
<td>23</td>
<td>Chicago</td>
</tr>
</tbody>
</table>
</body>
</html>
*********************************************
PRACTICAL 5 - WA JS PROGRAM FOR SUM OF DIGITS OF A NUMBER
<!DOCTYPE html>
<html>
<head>
<title>Sum Of Digits Of Number</title>
<script>
function sum() {
var n = parseInt(document.getElementById("numberInput").value, 10),
sum = 0;
while (n) sum += n % 10, n = Math.floor(n / 10);
document.write("Sum of Digits: " + sum);
}
</script>
</head>
<body>
<label for="numberInput">Enter a number:</label>
<input type="text" id="numberInput" placeholder="Enter a number">
<br>
<input type="button" value="Display" onclick="sum()">
</body>
</html>
*********************************************
PRACTICAL 6 - WA JS PROGRAM TO DETERMINE WHETHER THE NUMBER IS
EVEN/ODD
<!DOCTYPE html>
<html>
<head>
<title>Even or Odd Checker</title>
<script>
function checkEvenOdd() {
var n = parseInt(document.getElementById("numberInput").value, 10);
document.getElementById('result').innerText = isNaN(n) ? 'Invalid input.
Please enter a number.' : `${n} is ${n % 2 ? "Odd" : "Even"}.`;
}
</script>
</head>
<body>
<label for="numberInput">Enter a number:</label>
<input type="text" id="numberInput" placeholder="Enter a number">
<br>
<button onclick="checkEvenOdd()">Check Even/Odd</button>
<p id="result"></p>
</body>
</html>
*********************************************
PRACTICAL 7 - WA JS PROGRAM TO CONVERT CELSIUS TO FAHRENHEIT
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Celsius to Fahrenheit Converter</title>
<script>
document.addEventListener('DOMContentLoaded', function() {
const celsius = 25; // Predefined Celsius temperature
document.getElementById('result').innerText = `${celsius}°C is ${(celsius *
9/5 + 32).toFixed(2)}°F.`;
});
</script>
</head>
<body>
<p id="result"></p>
</body>
</html>
*********************************************
PRACTICAL 8 - WA JS PROGRAM TO DETERMINE PRIME NUMBER
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Prime Number Checker</title>
<script>
document.addEventListener('DOMContentLoaded', () => {
const num = 17; // Predefined number
const isPrime = Array.from({ length: Math.sqrt(num) }, (_, i) => num % (i +
2) !== 0).every(Boolean);
document.getElementById('result').innerText = `${num} is ${isPrime ?
'prime' : 'not prime'}.`;
});
</script>
</head>
<body>
<p id="result"></p>
</body>
</html>
*********************************************
PRACTICAL 9 -
<!-- HTML -->
<!DOCTYPE html>
<html>
<head>
<title>Styled Form</title>
<link rel="stylesheet" href="style.css">
</head>
<body>
<div class="container">
<form>
<label for="name">Name:</label>
<input type="text" id="name" name="name" required>
<label for="email">Email:</label>
<input type="email" id="email" name="email" required>
<label for="password">Password:</label>
<input type="password" id="password" name="password" required>
<input type="submit" value="Submit">
</form>
</div>
</body>
</html>
/* style.css */
body {
font-family: 'Arial', sans-serif;
background-color: #f4f4f4;
margin: 0;
padding: 0;
}
.container {
width: 50%;
margin: auto;
}
form {
background-color: #fff;
padding: 20px;
margin-top: 50px;
box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
border-radius: 5px;
}
label {
display: block;
margin-bottom: 8px;
}
input[type="text"],
input[type="email"],
input[type="password"] {
width: 100%;
padding: 10px;
margin-bottom: 15px;
box-sizing: border-box;
border: 1px solid #ccc;
border-radius: 4px;
}
input[type="submit"] {
background-color: #4caf50;
color: #fff;
padding: 10px 15px;
border: none;
border-radius: 4px;
cursor: pointer;
}
input[type="submit"]:hover {
background-color: #45a049;
}
*********************************************
