
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Jackpot Junction</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            display: flex;
            flex-direction: column;
            height: 100vh;
            justify-content: space-between;
            background: linear-gradient(to right, purple, red);
        }

        .container {
            text-align: center;
            margin-top: 50px;
            color: white;
        }

        .header {
            font-size: 36px;
            font-weight: bold;
        }

        .sub-header {
            font-size: 24px;
        }

        .slot-machine {
            font-size: 48px;
            margin: 20px 0;
            background-color: black;
            color: yellow;
            padding: 10px 20px;
            border-radius: 10px;
            display: inline-block;
        }

        .button {
            background-color: #4CAF50;
            border: none;
            color: white;
            padding: 20px 40px;
            text-align: center;
            text-decoration: none;
            display: inline-block;
            font-size: 24px;
            margin-bottom: 50px;
            cursor: pointer;
            border-radius: 10px;
        }

        .button:disabled {
            background-color: #cccccc;
            cursor: not-allowed;
        }

        .links {
            text-align: center;
            margin-bottom: 20px;
            color: white;
        }
    </style>
</head>

<body>
    <div class="container">
        <div class="header">Jackpot Junction</div>
        <div class="sub-header">Experience True Luxury</div>
        <div class="slot-machine" id="slotMachine">00</div>
        <button class="button" id="spinButton" onclick="spin()">Spin</button>
    </div>
    <div class="links">
        <a href="https://www.facebook.com/profile.php?id=61550062054004" target="_blank">Facebook Page</a> | <a href="https://www.facebook.com/lock.key.1656"
            target="_blank">Profile</a>
    </div>
</div> 
        <h2>Games Available:</h2>
        <ul>
            <li>Milkeyway</li>
            <li>Orinstar</li>
            <li>Firekrin</li>
            <li>Gamevault</li>
            <li>Vegassweeps</li>
            <li>Juwa</li>
            <li>Moolah</li>
        </ul>
</div>
    <script>
        function spin() {
            let randomNumber = Math.floor(Math.random() * 60) + 1;
            const slotMachine = document.getElementById('slotMachine');
            const spinButton = document.getElementById('spinButton');
            const maxIterations = 30;
            const delay = 100;
            spinButton.disabled = true;
            for (let i = 0; i < maxIterations; i++) {
                setTimeout(() => {
                    let currentNumber = i % 60 + 1;
                    slotMachine.innerText = currentNumber < 10 ? '0' + currentNumber : currentNumber;
                }, i * delay);
            }
            setTimeout(() => {
                slotMachine.innerText = randomNumber < 10 ? '0' + randomNumber : randomNumber;
            }, maxIterations * delay);
        }
    </script>
</body>

</html>
