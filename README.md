
























<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Be My Valentine?</title>
    <style>
        body {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
            margin: 0;
            background-color: #ffe4e1; /* Misty Rose */
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            text-align: center;
            overflow: hidden;
        }

        #container {
            background: white;
            padding: 3rem;
            border-radius: 20px;
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
            transition: all 0.3s ease;
        }

        h1 {
            color: #d63384;
            font-size: 2.5rem;
            margin-bottom: 2rem;
        }

        .buttons {
            display: flex;
            gap: 20px;
            justify-content: center;
            align-items: center;
        }

        button {
            padding: 15px 30px;
            font-size: 1.2rem;
            border: none;
            border-radius: 10px;
            cursor: pointer;
            transition: transform 0.2s;
        }

        #yesBtn {
            background-color: #ff4d6d;
            color: white;
            z-index: 1000;
        }

        #noBtn {
            background-color: #6c757d;
            color: white;
        }

        .hidden {
            display: none;
        }

        #successMessage {
            color: #d63384;
            font-size: 3rem;
            font-weight: bold;
            animation: heartBeat 1.5s infinite;
        }

        @keyframes heartBeat {
            0% { transform: scale(1); }
            50% { transform: scale(1.1); }
            100% { transform: scale(1); }
        }
    </style>
</head>
<body>

    <div id="container">
        <div id="quiz">
            <h1 id="question">Will you be my valentine? ❤️</h1>
            <div class="buttons">
                <button id="yesBtn" onclick="celebrate()">YES</button>
                <button id="noBtn" onclick="handleNo()">NO</button>
            </div>
        </div>

        <div id="success" class="hidden">
            <h1 id="successMessage">i love u sm sweetheart ❤️</h1>
            <div style="font-size: 50px;">🥰🌹✨</div>
        </div>
    </div>

    <script>
        let yesBtnSize = 1.2;
        let noClickCount = 0;
        
        const noResponses = [
            "Are you sure?",
            "baby u sure",
            "babyyyyyy",
            "just say yes baby",
            "baby pleaseeee"
        ];

        function handleNo() {
            const yesBtn = document.getElementById('yesBtn');
            const noBtn = document.getElementById('noBtn');
            
            // Increase Yes button size
            yesBtnSize += 0.5;
            yesBtn.style.fontSize = yesBtnSize + "rem";
            yesBtn.style.padding = (yesBtnSize * 10) + "px " + (yesBtnSize * 20) + "px";

            // Update No button text
            if (noClickCount < noResponses.length) {
                noBtn.innerText = noResponses[noClickCount];
                noClickCount++;
            } else {
                noBtn.innerText = "Please? 🥺";
            }
        }

        function celebrate() {
            document.getElementById('quiz').classList.add('hidden');
            document.getElementById('success').classList.remove('hidden');
            document.body.style.backgroundColor = "#ffb3c1";
        }
    </script>
</body>
</html>            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
            transition: all 0.3s ease;
        }

        h1 {
            color: #d63384;
            font-size: 2.5rem;
            margin-bottom: 2rem;
        }

        .buttons {
            display: flex;
            gap: 20px;
            justify-content: center;
            align-items: center;
        }

        button {
            padding: 15px 30px;
            font-size: 1.2rem;
            border: none;
            border-radius: 10px;
            cursor: pointer;
            transition: transform 0.2s;
        }

        #yesBtn {
            background-color: #ff4d6d;
            color: white;
            z-index: 1000;
        }

        #noBtn {
            background-color: #6c757d;
            color: white;
        }

        .hidden {
            display: none;
        }

        #successMessage {
            color: #d63384;
            font-size: 3rem;
            font-weight: bold;
            animation: heartBeat 1.5s infinite;
        }

        @keyframes heartBeat {
            0% { transform: scale(1); }
            50% { transform: scale(1.1); }
            100% { transform: scale(1); }
        }
    </style>
</head>
<body>

    <div id="container">
        <div id="quiz">
            <h1 id="question">Will you be my valentine? ❤️</h1>
            <div class="buttons">
                <button id="yesBtn" onclick="celebrate()">YES</button>
                <button id="noBtn" onclick="handleNo()">NO</button>
            </div>
        </div>

        <div id="success" class="hidden">
            <h1 id="successMessage">i love u sm sweetheart ❤️</h1>
            <div style="font-size: 50px;">🥰🌹✨</div>
        </div>
    </div>

    <script>
        let yesBtnSize = 1.2;
        let noClickCount = 0;
        
        const noResponses = [
            "Are you sure?",
            "baby u sure",
            "babyyyyyy",
            "just say yes baby",
            "baby pleaseeee"
        ];

        function handleNo() {
            const yesBtn = document.getElementById('yesBtn');
            const noBtn = document.getElementById('noBtn');
            
            // Increase Yes button size
            yesBtnSize += 0.5;
            yesBtn.style.fontSize = yesBtnSize + "rem";
            yesBtn.style.padding = (yesBtnSize * 10) + "px " + (yesBtnSize * 20) + "px";

            // Update No button text
            if (noClickCount < noResponses.length) {
                noBtn.innerText = noResponses[noClickCount];
                noClickCount++;
            } else {
                noBtn.innerText = "Please? 🥺";
            }
        }

        function celebrate() {
            document.getElementById('quiz').classList.add('hidden');
            document.getElementById('success').classList.remove('hidden');
            document.body.style.backgroundColor = "#ffb3c1";
        }
    </script>
</body>
</html>
