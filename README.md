<!DOCTYPE html> 
<html lang="en"> 
<head> 
<meta charset="UTF-8"> 
<title>Task Progress</title> 
<style> body {     font-family: Arial, sans-serif; 
    background: #ffffff; 
} 
/* Main box */ .box {     width: 650px;     margin: 50px auto; 
    border: 2px solid #3f7f3f; 
} 
/* Title */ 
.title { 
    background: #4f8f4f;     color: white;     text-align: center;     font-size: 24px;     font-weight: bold;     padding: 10px;     border-bottom: 4px solid #dcdcdc; 
} 
/* Table */ table {     width: 100%;     border-collapse: collapse; 
} 
/* Header */ th { 
    background: #5a9e5a;     color: white;     padding: 12px;     font-size: 18px;     border-right: 1px solid #4a8a4a; 
} 
th:last-child {     border-right: none; 
} 
/* Cells */ td {     padding: 14px;     font-size: 16px;     text-align: center;     border-top: 1px solid #cfcfcf; 
    border-right: 1px solid #cfcfcf; 
} 
td:last-child {     border-right: none; 
} 
/* Alternate row */ tr:nth-child(3) {     background: #e6e6e6; 
} 
/* Status labels */ span {     padding: 6px 18px;     border-radius: 10px;     color: white; 
    font-weight: bold; 
} 
/* Colors */ .completed {     background: #4CAF50; 
} 
.progress {     background: #e0a800; 
} 
.pending {     background: #d32f2f; 
} 
</style> 
</head> <body> 
<div class="box"> 
    <div class="title">Task Progress</div> 
    <table> 
        <tr> 
            <th>Task</th> 
            <th>Status</th> 
            <th>Deadline</th> 
        </tr> 
        <tr> 
            <td>Design Mockup</td> 
            <td><span class="completed">Completed</span></td> 
            <td>August 15</td> 
        </tr> 
        <tr> 
            <td>Write Documentation</td> 
            <td><span class="progress">In Progress</span></td> 
            <td>August 20</td> 
        </tr> 
        <tr> 
            <td>Testing Phase</td> 
            <td><span class="pending">Pending</span></td> 
            <td>August 25</td> 
        </tr> 
    </table> </div> 
</body> 
</html>



<!DOCTYPE html> 
<html lang="en"> 
<head> 
    <meta charset="UTF-8"> 
    <title>Weekly Schedule</title> 
</head> 
<body style="font-family: Arial, sans-serif; background-color: #f5f5f5;"> 
<div style="width: 650px; margin: 50px auto; border: 2px solid #e66a2c;"> 
    <!-- Title --> 
    <div style="background-color: #e66a2c; color: white; text-align: center;                  font-size: 26px; font-weight: bold; padding: 10px; 
                border-bottom: 4px solid #ffffff;"> 
        Weekly Schedule 
    </div> 
    <!-- Table --> 
    <table style="width: 100%; border-collapse: collapse; text-align: center;"> 
        <!-- Header --> 
        <tr style="background-color: #e66a2c; color: white; font-size: 18px;"> 
            <th style="padding: 12px; border-right: 1px solid #d45c24;">Day</th> 
            <th style="padding: 12px; border-right: 1px solid #d45c24;">Task</th> 
            <th style="padding: 12px;">Time</th> 
        </tr> 
        <!-- Row 1 --> 
        <tr style="background-color: #f3e2c7;"> 
            <td style="padding: 14px; border-top: 1px solid #ccc; border-right: 1px solid 
#ccc;">Monday</td> 
            <td style="padding: 14px; border-top: 1px solid #ccc; border-right: 1px solid #ccc;">Code 
Practice</td> 
            <td style="padding: 14px; border-top: 1px solid #ccc;">10:00 AM</td> 
        </tr> 
        <!-- Row 2 --> 
        <tr style="background-color: #e0e0e0;"> 
            <td style="padding: 14px; border-top: 1px solid #ccc; border-right: 1px solid 
#ccc;">Wednesday</td> 
            <td style="padding: 14px; border-top: 1px solid #ccc; border-right: 1px solid #ccc;">Team 
Meeting</td> 
            <td style="padding: 14px; border-top: 1px solid #ccc;">2:00 PM</td> 
        </tr> 
        <!-- Row 3 --> 
        <tr style="background-color: #f3e2c7;"> 
            <td style="padding: 14px; border-top: 1px solid #ccc; border-right: 1px solid 
#ccc;">Friday</td> 
            <td style="padding: 14px; border-top: 1px solid #ccc; border-right: 1px solid 
#ccc;">Project Review</td> 
            <td style="padding: 14px; border-top: 1px solid #ccc;">4:00 PM</td> 
        </tr> 
    </table> </div> 
</body> 
</html>


<!DOCTYPE html> 
<html lang="en"> 
<head> 
    <meta charset="UTF-8"> 
    <title>Form Validation</title> 
    <!-- Bootstrap CSS --> 
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet"> 
    <script> 
        function validateForm() { 
            let name = document.getElementById("name").value.trim();             let email = document.getElementById("email").value.trim();             let password = document.getElementById("password").value.trim();             let emailPattern = /^[^ ]+@[^ ]+\.[a-z]{2,3}$/; 
            // Empty field validation 
            if (name === "" || email === "" || password === "") { 
                document.getElementById("msg").innerHTML = "All fields are required!";                 return false;             } 
            // Email validation 
            if (!email.match(emailPattern)) { 
                document.getElementById("msg").innerHTML = "Enter valid email!";                 return false;             } 
            // Password length validation             if (password.length < 6) { 
                document.getElementById("msg").innerHTML = "Password must be at least 6 characters!"; 
                return false; 
            } 
            alert("Form submitted successfully!");             return true; 
        } 
    </script> 
    <style>         body { 
            background-color: #f2f2f2; 
        } 
        .form-box {             background: white;             padding: 25px;             border-radius: 10px; 
            box-shadow: 0px 0px 10px gray; 
        }         .error {             color: red;             text-align: center; 
        } 
    </style> 
</head> 
<body> 
<div class="container mt-5"> 
    <div class="row justify-content-center"> 
        <div class="col-md-5"> 
            <div class="form-box"> 
                <h3 class="text-center mb-3">Registration Form</h3> 
                <form onsubmit="return validateForm()"> 
                    <div class="mb-3"> 
                        <label>Name</label> 
                        <input type="text" id="name" class="form-control"> 
                    </div> 
                    <div class="mb-3"> 
                        <label>Email</label> 
                        <input type="text" id="email" class="form-control">                     </div> 
                    <div class="mb-3"> 
                        <label>Password</label> 
                        <input type="password" id="password" class="form-control"> 
                    </div> 
                    <p id="msg" class="error"></p> 
                    <button type="submit" class="btn btn-primary w-100">Submit</button> 
                </form> 
            </div> 
        </div> 
    </div> </div> 
</body> 
</html>


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Simple Calculator</title>
    <style>
        body {
            font-family: Arial;
            background: #f4f4f4;
            text-align: center;
            margin-top: 50px;
        }

        .calculator {
            background: #fff;
            padding: 20px;
            width: 250px;
            margin: auto;
            border-radius: 10px;
            box-shadow: 0 0 10px gray;
        }

        input, select, button {
            width: 90%;
            padding: 10px;
            margin: 10px 0;
            font-size: 16px;
        }

        button {
            background: #007BFF;
            color: white;
            border: none;
            cursor: pointer;
        }

        button:hover {
            background: #0056b3;
        }

        #result {
            font-weight: bold;
            margin-top: 10px;
        }
    </style>
</head>
<body>

<div class="calculator">
    <h2>Calculator</h2>

    <input type="number" id="num1" placeholder="Enter first number">
    <input type="number" id="num2" placeholder="Enter second number">

    <select id="operator">
        <option value="+">Addition (+)</option>
        <option value="-">Subtraction (-)</option>
        <option value="*">Multiplication (*)</option>
        <option value="/">Division (/)</option>
    </select>

    <button onclick="calculate()">Calculate</button>

    <div id="result"></div>
</div>

<script>
    function calculate() {
        let num1 = parseFloat(document.getElementById("num1").value);
        let num2 = parseFloat(document.getElementById("num2").value);
        let operator = document.getElementById("operator").value;

        let result;

        switch (operator) {
            case '+':
                result = add(num1, num2);
                break;
            case '-':
                result = subtract(num1, num2);
                break;
            case '*':
                result = multiply(num1, num2);
                break;
            case '/':
                if (num2 === 0) {
                    result = "Cannot divide by zero";
                } else {
                    result = divide(num1, num2);
                }
                break;
            default:
                result = "Invalid operator";
        }

        document.getElementById("result").innerText = "Result: " + result;
    }

    function add(a, b) {
        return a + b;
    }

    function subtract(a, b) {
        return a - b;
    }

    function multiply(a, b) {
        return a * b;
    }

    function divide(a, b) {
        return a / b;
    }
</script>

</body>
</html>
