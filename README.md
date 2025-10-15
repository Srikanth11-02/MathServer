# Ex.05 Design a Website for Server Side Processing
## Date: 05-10-25

## AIM:
 To design a website to calculate the power of a lamp filament in an incandescent bulb in the server side. 


## FORMULA:
P = I<sup>2</sup>R
<br> P --> Power (in watts)
<br> I --> Intensity
<br> R --> Resistance

## DESIGN STEPS:

### Step 1:
Clone the repository from GitHub.

### Step 2:
Create Django Admin project.

### Step 3:
Create a New App under the Django Admin project.

### Step 4:
Create python programs for views and urls to perform server side processing.

### Step 5:
Create a HTML file to implement form based input and output.

### Step 6:
Publish the website in the given URL.

## PROGRAM :
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Lamp Power Calculator</title>
  <style>
    body {
      font-family: "Poppins", sans-serif;
      background: linear-gradient(135deg, #6a11cb, #2575fc);
      color: white;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      height: 100vh;
      margin: 0;
    }
    .container {
      background: rgba(255, 255, 255, 0.1);
      padding: 30px 40px;
      border-radius: 20px;
      box-shadow: 0 4px 20px rgba(0, 0, 0, 0.3);
      width: 320px;
      text-align: center;
    }
    h1 {
      font-size: 1.6em;
      margin-bottom: 15px;
    }
    label {
      display: block;
      margin: 10px 0 5px;
      font-weight: bold;
    }
    input {
      width: 100%;
      padding: 8px;
      border: none;
      border-radius: 5px;
      text-align: center;
      font-size: 1em;
    }
    button {
      margin-top: 20px;
      padding: 10px 20px;
      background-color: #ffcb05;
      border: none;
      border-radius: 10px;
      cursor: pointer;
      font-size: 1em;
      color: #333;
      transition: 0.3s;
    }
    button:hover {
      background-color: #ffd84d;
    }
    #result {
      margin-top: 20px;
      font-size: 1.2em;
      font-weight: bold;
    }
  </style>
</head>
<body>

  <div class="container">
    <h1>💡 Lamp Power Calculator</h1>

    <label for="current">Current (I) in Amperes:</label>
    <input type="number" id="current" placeholder="Enter current (I)" step="any">

    <label for="resistance">Resistance (R) in Ohms:</label>
    <input type="number" id="resistance" placeholder="Enter resistance (R)" step="any">

    <button onclick="calculatePower()">Calculate Power</button>

    <div id="result"></div>
  </div>

  <script>
    function calculatePower() {
      const I = parseFloat(document.getElementById("current").value);
      const R = parseFloat(document.getElementById("resistance").value);
      const resultDiv = document.getElementById("result");

      if (isNaN(I) || isNaN(R)) {
        resultDiv.innerHTML = "⚠️ Please enter both Current and Resistance values.";
        return;
      }

      const P = I * I * R;
      resultDiv.innerHTML = `🔹 Power (P) = ${P.toFixed(2)} watts`;
    }
  </script>

</body>
</html>
```

## SERVER SIDE PROCESSING:


## HOMEPAGE:
<img width="1365" height="595" alt="Screenshot 2025-10-05 111643" src="https://github.com/user-attachments/assets/b94ad354-974b-4487-b71d-f2c631e7cfeb" />


## RESULT:
The program for performing server side processing is completed successfully.
