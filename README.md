<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Be My Valentine?</title>
    <style>
        body {
            text-align: center;
            font-family: Arial, sans-serif;
            background-color: pink;
            margin-top: 100px;
        }
        #question, #dateInput, #thankYou {
            font-size: 24px;
            margin-bottom: 20px;
        }
        button {
            font-size: 20px;
            padding: 10px 20px;
            margin: 10px;
            border: none;
            cursor: pointer;
            border-radius: 10px;
        }
        #yesBtn { background-color: red; color: white; }
        #noBtn { background-color: gray; color: white; }
        #submitDate { background-color: purple; color: white; }
    </style>
</head>
<body>
    <div id="question">Will you be my Valentine? ❤️</div>
    <button id="yesBtn" onclick="showDateInput()">Yes</button>
    <button id="noBtn" onclick="alert('Oh no! 😢')">No</button>
    
    <div id="dateInput" style="display: none;">
        <p>Which day are you free? 📅</p>
        <input type="date" id="datePicker">
        <button id="submitDate" onclick="showThankYou()">Submit</button>
    </div>
    
    <div id="thankYou" style="display: none; font-size: 28px; color: darkred; font-weight: bold;">
        Thank you for being my girlfriend! ❤️
    </div>
    
    <script>
        function showDateInput() {
            document.getElementById('dateInput').style.display = 'block';
        }
        function showThankYou() {
            let date = document.getElementById('datePicker').value;
            if (date) {
                document.getElementById('thankYou').style.display = 'block';
                document.getElementById('dateInput').style.display = 'none';
                document.getElementById('question').style.display = 'none';
                document.getElementById('yesBtn').style.display = 'none';
                document.getElementById('noBtn').style.display = 'none';
            } else {
                alert('Please select a date!');
            }
        }
    </script>
</body>
</html>
