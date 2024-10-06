# PayPal-surveys-and-money-clicker-

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Your App</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
            margin: 0;
            background-color: #f5f5f5; /* Light background for contrast */
        }
        .header {
            display: flex;
            justify-content: space-between;
            width: 100%;
            padding: 10px;
            background-color: #007BFF; /* Header background color */
            color: white;
        }
        .coins {
            display: flex;
            flex-direction: column;
            align-items: flex-start;
        }
        .button {
            margin: 5px;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            background-color: #007BFF;
            color: white;
            cursor: pointer;
            transition: background-color 0.3s;
        }
        .button:hover {
            background-color: #0056b3; /* Darker blue on hover */
        }
        .cashout-options {
            display: none;
            flex-direction: column;
            align-items: flex-start;
            margin-top: 10px;
        }
        #cashoutOptions span {
            margin-bottom: 5px;
        }
    </style>
</head>
<body>

<div class="header">
    <div class="coins">
        <span id="coins">Coins: 100</span>
        <button class="button" id="convertButton">Convert</button>
        <button class="button" id="clickerButton">Click for Coins!</button> <!-- Clicker Button -->
    </div>
    <div>
        <span id="balance">£0.00</span>
        <button class="button" id="cashoutButton">Cashout</button>
    </div>
</div>

<div>
    <button class="button" id="googleButton">Sign in with Google</button>
    <button class="button" id="facebookButton">Sign in with Facebook</button>
</div>

<div class="cashout-options" id="cashoutOptions">
    <span>Choose Cashout Option:</span>
    <button class="button" id="bankTransferButton">Bank Transfer</button>
    <button class="button" id="paypalButton">PayPal</button>
</div>

<script>
    let coinCount = 100; // Initial coin count
    document.getElementById('coins').innerText = `Coins: ${coinCount}`;

    // Clicker button to increase coins
    document.getElementById('clickerButton').addEventListener('click', function() {
        coinCount += 1; // Increase coin count by 1
        document.getElementById('coins').innerText = `Coins: ${coinCount}`;
    });

    document.getElementById('cashoutButton').addEventListener('click', function() {
        document.getElementById('cashoutOptions').style.display = 'flex';
    });

    document.getElementById('convertButton').addEventListener('click', function() {
        // Logic to convert coins to actual money goes here
        alert('Converting coins...');
    });

    document.getElementById('bankTransferButton').addEventListener('click', function() {
        // Logic for bank transfer cashout goes here
        alert('Bank Transfer Selected');
    });

    document.getElementById('paypalButton').addEventListener('click', function() {
        // Logic for PayPal cashout goes here
        alert('PayPal Selected');
    });

    // Add your Google and Facebook sign-in logic here
</script>

</body>
</html>
