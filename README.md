<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Waiting for Grades</title>
    <style>
        body {
            background: linear-gradient(to bottom, #ffecd2, #fcb69f);
            font-family: "Poppins", sans-serif;
            color: #333;
            text-align: center;
            padding: 20px;
            overflow-x: hidden;
        }

        h1 {
            font-size: 3rem;
            color: #ff6b6b;
            text-shadow: 3px 3px #f8b195;
            animation: shake 1.5s infinite alternate;
        }

        p {
            font-size: 1.2rem;
            margin: 20px auto;
            max-width: 600px;
            line-height: 1.5;
        }

        button {
            font-size: 1.2rem;
            padding: 10px 20px;
            margin: 20px;
            border: 3px solid #ff6b6b;
            background: #fff;
            color: #333;
            border-radius: 8px;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        button:hover {
            background: #ff6b6b;
            color: white;
            transform: scale(1.1);
        }

        @keyframes shake {
            0% { transform: rotate(-3deg); }
            100% { transform: rotate(3deg); }
        }

        .hidden {
            display: none;
        }

        .animated-text {
            animation: fadeIn 1.5s;
        }

        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
    </style>
</head>
<body>
    <h1>Kinakabahan ka ba sa releasing of grades, pre?</h1>
    <p id="story-text" class="animated-text">
        The grades are coming out soon. Yii, kakain ng Graham nang may ngiti sa mga labi o may luha sa mga pisngi? <br> (Huwag naman sana iyong pangalawa, ne?) Click below to continue.
    </p>
    <button onclick="nextPart()">below to continue, hahahaha.</button>

    <script>
        let currentPart = 0;

        const storyParts = [
            "Iyong may nag-notify sa iyo. Akala mo may grade nang na-release pero kaibigan mo lang pala na nag-send ng meme about failing together. (Omay, nandamay pa talaga.)",
            "Anyway, I would like to assure you all na makapapasa tayong lahat. Deserve nating makapasa!",
            "Don’t doubt yourself, hindi ka magiging irreg.",
            "Siya nga pala. Thank you for helping me survive this sem. If you didn’t update me about what you’d been doing while I was away for the competition sa CAASUC III, I wouldn’t be able to comply with anything.",
            "You all made my life a little bit easy. You saved me! (wow, life savior pala kau).",
            "Labyu all, mga pre, hindi niyo ako pinabayaan, whahahahhaha."
        ];

        function nextPart() {
            const storyText = document.getElementById("story-text");
            if (currentPart < storyParts.length) {
                storyText.innerHTML = storyParts[currentPart];
                currentPart++;
            } else {
                storyText.innerHTML = "Tara at sabay-sabay na lang humiling ng 1.00, 1.25, 1.50, at 1.75 sa portal. Good luck sa atin sa second sem! Panibagong hell na naman, mga ya";
                document.querySelector("button").style.display = "none";
            }
        }
    </script>
</body>
</html>
