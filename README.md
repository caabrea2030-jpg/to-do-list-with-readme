# to-do-list-with-readme
This code helps you confirm your student eligibility card. It helps you verify your student enrollment allowing you to access carious benefits such as discounts. library access, and more. 

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Discount Eligibility</title>
</head>
<body>
    <h2>Check Discount Eligibility</h2>

    <label for="student">Are you a student?</label>
    <input type="text" id="student" placeholder="yes or no"><br><br>

    <label for="age">Enter your age:</label>
    <input type="number" id="age" placeholder="Your age"><br><br>

    <label for="card">Do you have a membership card?</label>
    <input type="text" id="card" placeholder="yes or no"><br><br>

    <button onclick="checkDiscount()">Check Eligibility</button>

    <p id="result"></p>

    <script>
        function checkDiscount() {
            // get values from input fields
            const student = document.getElementById("student").value.toLowerCase();
            const age = parseInt(document.getElementById("age").value);
            const card = document.getElementById("card").value.toLowerCase();

            let result = "";

            // check discount eligibility
            if (card === "yes") {
                result = "You are eligible for a discount.";
            } else if (card === "no") {
                result = "You are not eligible for a discount.";
            } else {
                result = "Please answer 'yes' or 'no' for the membership card.";
            }

            // show the result
            document.getElementById("result").innerText = result;
        }
    </script>
</body>
</html>
