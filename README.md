```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>For Api Umaima 💛</title>

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: Georgia, serif;
            background: linear-gradient(135deg, #fffdf2, #fff4bf);
            color: #5c4a1f;
            overflow-x: hidden;
        }

        /* NAVIGATION */
        nav {
            position: fixed;
            top: 0;
            width: 100%;
            padding: 18px 8%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            background: rgba(255, 252, 230, 0.94);
            backdrop-filter: blur(10px);
            z-index: 1000;
            box-shadow: 0 3px 18px rgba(100, 75, 10, 0.08);
        }

        .logo {
            font-size: 22px;
            font-weight: bold;
            color: #a87900;
        }

        nav a {
            text-decoration: none;
            color: #6d581d;
            margin-left: 22px;
            font-size: 15px;
            transition: 0.3s;
        }

        nav a:hover {
            color: #d39e00;
        }

        /* HERO */
        .hero {
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 110px 20px 70px;
            position: relative;
        }

        .hero-content {
            max-width: 850px;
            animation: fadeUp 1.5s ease;
        }

        .main-flower {
            font-size: 75px;
            animation: floatFlower 3s ease-in-out infinite;
            margin-bottom: 15px;
        }

        .small-title {
            letter-spacing: 5px;
            text-transform: uppercase;
            font-size: 13px;
            color: #a57b00;
            margin-bottom: 18px;
        }

        h1 {
            font-size: clamp(48px, 9vw, 90px);
            color: #8a6500;
            margin-bottom: 12px;
        }

        .hero h2 {
            font-size: 25px;
            font-weight: normal;
            color: #6d581d;
            margin-bottom: 25px;
        }

        .hero p {
            max-width: 700px;
            margin: auto;
            line-height: 1.9;
            font-size: 18px;
        }

        /* BUTTON */
        .button {
            display: inline-block;
            margin-top: 32px;
            padding: 15px 32px;
            border-radius: 35px;
            background: #e4b800;
            color: white;
            border: none;
            font-size: 16px;
            cursor: pointer;
            transition: 0.3s;
            box-shadow: 0 8px 22px rgba(170, 130, 0, 0.22);
        }

        .button:hover {
            transform: translateY(-5px) scale(1.03);
            background: #c99f00;
        }

        /* SECTIONS */
        section {
            padding: 95px 8%;
            text-align: center;
        }

        .section-title {
            font-size: 39px;
            color: #8a6500;
            margin-bottom: 18px;
        }

        .section-subtitle {
            max-width: 700px;
            margin: 0 auto 45px;
            line-height: 1.9;
            color: #75612a;
            font-size: 17px;
        }

        /* MESSAGE CARD */
        .message-card {
            max-width: 850px;
            margin: auto;
            background: rgba(255, 255, 255, 0.72);
            padding: 48px;
            border-radius: 28px;
            box-shadow: 0 15px 45px rgba(120, 90, 20, 0.1);
            border: 1px solid #f0d778;
            line-height: 2;
            font-size: 18px;
        }

        .message-icon {
            font-size: 55px;
            margin-bottom: 20px;
        }

        /* CARDS */
        .cards {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 25px;
            max-width: 1050px;
            margin: auto;
        }

        .card {
            background: #fffdf2;
            padding: 32px 24px;
            border-radius: 22px;
            border: 1px solid #efd46a;
            transition: 0.4s;
            box-shadow: 0 8px 25px rgba(100, 80, 20, 0.07);
        }

        .card:hover {
            transform: translateY(-9px);
            box-shadow: 0 18px 35px rgba(100, 80, 20, 0.14);
        }

        .card span {
            font-size: 40px;
        }

        .card h3 {
            margin: 15px 0 12px;
            color: #8a6500;
            font-size: 21px;
        }

        .card p {
            line-height: 1.75;
            font-size: 15px;
        }

        /* STUDIES SECTION */
        .study-section {
            background: rgba(255, 239, 151, 0.28);
        }

        /* WORDS SECTION */
        .words-section {
            background: rgba(255, 248, 214, 0.65);
        }

        .quote-box {
            max-width: 800px;
            margin: auto;
            padding: 45px;
            background: #fffdf4;
            border-radius: 25px;
            border-left: 6px solid #e3b600;
            box-shadow: 0 10px 30px rgba(120, 90, 20, 0.1);
        }

        .quote-box p {
            font-size: 23px;
            line-height: 1.8;
            font-style: italic;
        }

        /* APPRECIATION LIST */
        .appreciation-list {
            max-width: 750px;
            margin: auto;
            text-align: left;
        }

        .appreciation-item {
            background: #fffdf3;
            margin: 14px 0;
            padding: 18px 22px;
            border-radius: 15px;
            border: 1px solid #efd878;
            transition: 0.3s;
        }

        .appreciation-item:hover {
            transform: translateX(7px);
        }

        /* SURPRISE */
        #surprise {
            display: none;
            max-width: 800px;
            margin: 35px auto 0;
            padding: 38px;
            background: #fffdf0;
            border-radius: 25px;
            border: 2px dashed #dfb300;
            animation: fadeUp 1s ease;
            line-height: 1.9;
            font-size: 18px;
        }

        /* FALLING FLOWERS */
        .floating-flower {
            position: fixed;
            top: -60px;
            font-size: 25px;
            pointer-events: none;
            animation: fall linear infinite;
            z-index: 999;
        }

        .flower1 {
            left: 8%;
            animation-duration: 9s;
        }

        .flower2 {
            left: 27%;
            animation-duration: 12s;
            animation-delay: 2s;
        }

        .flower3 {
            left: 52%;
            animation-duration: 8s;
            animation-delay: 1s;
        }

        .flower4 {
            left: 78%;
            animation-duration: 11s;
            animation-delay: 3s;
        }

        .flower5 {
            left: 92%;
            animation-duration: 10s;
            animation-delay: 4s;
        }

        /* FOOTER */
        footer {
            padding: 40px;
            text-align: center;
            background: #ffefa5;
            color: #70591b;
            line-height: 1.8;
        }

        /* ANIMATIONS */
        @keyframes fadeUp {
            from {
                opacity: 0;
                transform: translateY(35px);
            }

            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes floatFlower {
            0%, 100% {
                transform: translateY(0) rotate(-5deg);
            }

            50% {
                transform: translateY(-14px) rotate(5deg);
            }
        }

        @keyframes fall {
            0% {
                transform: translateY(-60px) rotate(0deg);
                opacity: 0;
            }

            15% {
                opacity: 1;
            }

            100% {
                transform: translateY(110vh) rotate(360deg);
                opacity: 0;
            }
        }

        /* MOBILE */
        @media (max-width: 650px) {

            nav {
                padding: 15px 5%;
            }

            .logo {
                font-size: 17px;
            }

            nav a {
                margin-left: 8px;
                font-size: 12px;
            }

            section {
                padding: 70px 6%;
            }

            .message-card,
            .quote-box {
                padding: 30px 22px;
            }

            .hero p {
                font-size: 16px;
            }

            .quote-box p {
                font-size: 19px;
            }
        }
    </style>
</head>

<body>

    <!-- FALLING FLOWERS -->
    <div class="floating-flower flower1">🌼</div>
    <div class="floating-flower flower2">🌸</div>
    <div class="floating-flower flower3">🌻</div>
    <div class="floating-flower flower4">🌼</div>
    <div class="floating-flower flower5">🌸</div>


    <!-- NAVIGATION -->
    <nav>

        <div class="logo">
            Api Umaima 💛
        </div>

        <div>
            <a href="#home">Home</a>
            <a href="#about">About</a>
            <a href="#words">Words</a>
        </div>

    </nav>


    <!-- HERO -->
    <section class="hero" id="home">

        <div class="hero-content">

            <div class="main-flower">
                🌼
            </div>

            <div class="small-title">
                A Little Something For You
            </div>

            <h1>
                Api Umaima
            </h1>

            <h2>
                A Guide, A Friend & Someone I Truly Appreciate
            </h2>

            <p>
                Some people come into our lives and make ordinary moments
                feel a little brighter. You are one of those people.
                Your kindness, your words, your help with my studies,
                and your friendly nature are things I genuinely appreciate.
            </p>

            <button class="button" onclick="showSurprise()">
                ✨ Open My Surprise
            </button>

        </div>

    </section>


    <!-- ABOUT -->
    <section id="about">

        <h2 class="section-title">
            You Are More Than Someone Who Teaches Me 🌼
        </h2>

        <p class="section-subtitle">
            You help me learn, but you also make learning feel comfortable,
            enjoyable, and much less stressful.
        </p>

        <div class="message-card">

            <div class="message-icon">
                📚💛
            </div>

            <p>
                Api Umaima, sometimes it is difficult to put appreciation
                into words because some people simply mean a lot to us.
                You are one of those people.
                <br><br>

                You are someone who helps me with my studies, explains things
                when I don't understand, and encourages me to keep trying.
                But what makes you especially memorable is how friendly you are.
                <br><br>

                I can learn from you, ask questions, have a laugh, and enjoy
                the little moments along the way.
                <br><br>

                That combination of guidance and friendship is something
                I really value.
            </p>

        </div>

    </section>


    <!-- THINGS I APPRECIATE -->
    <section>

        <h2 class="section-title">
            Things I Appreciate About You 💛
        </h2>

        <p class="section-subtitle">
            There are so many little things that make you someone
            I will always remember.
        </p>

        <div class="cards">

            <div class="card">
                <span>📚</span>
                <h3>You Help Me Learn</h3>
                <p>
                    You explain things patiently and help me understand
                    my studies when something feels difficult.
                </p>
            </div>

            <div class="card">
                <span>🌼</span>
                <h3>You Are Friendly</h3>
                <p>
                    You make conversations comfortable and make it easy
                    to talk and share a laugh.
                </p>
            </div>

            <div class="card">
                <span>💡</span>
                <h3>Your Advice</h3>
                <p>
                    The advice you give often makes me think differently
                    and helps me when I need encouragement.
                </p>
            </div>

            <div class="card">
                <span>😊</span>
                <h3>You Bring Joy</h3>
                <p>
                    You have a way of making ordinary moments happier
                    and more memorable.
                </p>
            </div>

            <div class="card">
                <span>✨</span>
                <h3>Your Encouragement</h3>
                <p>
                    Your encouraging words can make me feel more confident
                    when I am struggling.
                </p>
            </div>

            <div class="card">
                <span>💛</span>
                <h3>Your Kindness</h3>
                <p>
                    Your patience, understanding, and kindness are things
                    I genuinely appreciate.
                </p>
            </div>

        </div>

    </section>


    <!-- STUDIES -->
    <section class="study-section">

        <h2 class="section-title">
            Thank You For Helping Me With My Studies 📖
        </h2>

        <p class="section-subtitle">
            Learning is not always easy, but having someone who is willing
            to explain, encourage, and help makes a big difference.
        </p>

        <div class="message-card">

            <p>
                Thank you for answering my questions and explaining things
                when I don't understand something.
                <br><br>

                Thank you for being patient when I need something explained
                more than once.
                <br><br>

                Thank you for reminding me that mistakes are simply part
                of learning.
                <br><br>

                And thank you for making studying feel a little easier
                and a lot more comfortable.
            </p>

        </div>

    </section>


    <!-- HER WORDS -->
    <section class="words-section" id="words">

        <h2 class="section-title">
            Your Words Stay With Me 💬
        </h2>

        <p class="section-subtitle">
            There are some things people say that we remember for a long time.
        </p>

        <div class="quote-box">

            <p>
                "I really like the words you say, the advice you give,
                and the little things you tell me. Even simple words from you
                can make my day better."
            </p>

        </div>

        <br><br>

        <div class="message-card">

            <p>
                Sometimes your words make me smile.
                Sometimes they make me think.
                Sometimes they encourage me when I need it.
                <br><br>

                You may not always realize it, but the little things you say
                can stay in someone's mind for a long time.
                <br><br>

                That is why I genuinely appreciate your words.
            </p>

        </div>

    </section>


    <!-- APPRECIATION -->
    <section>

        <h2 class="section-title">
            A Few More Thank Yous 🌻
        </h2>

        <div class="appreciation-list">

            <div class="appreciation-item">
                🌼 Thank you for your patience.
            </div>

            <div class="appreciation-item">
                📚 Thank you for helping me learn.
            </div>

            <div class="appreciation-item">
                💛 Thank you for your encouraging words.
            </div>

            <div class="appreciation-item">
                😊 Thank you for making me laugh.
            </div>

            <div class="appreciation-item">
                ✨ Thank you for making ordinary moments special.
            </div>

            <div class="appreciation-item">
                🌻 Thank you for always being so friendly.
            </div>

            <div class="appreciation-item">
                💡 Thank you for the advice you give.
            </div>

            <div class="appreciation-item">
                🤍 Thank you for being someone I can appreciate and remember.
            </div>

        </div>

    </section>


    <!-- SURPRISE -->
    <section>

        <h2 class="section-title">
            One Last Little Surprise ✨
        </h2>

        <p class="section-subtitle">
            There is one more message hidden here just for you.
        </p>

        <button class="button" onclick="showSurprise()">
            🌼 Click To Open
        </button>

        <div id="surprise">

            <p>
                <strong>Api Umaima,</strong>
                <br><br>

                If you are reading this, then you reached the end of my
                little website.
                <br><br>

                I just want to say one more thing:
                <br><br>

                <strong>
                    I really appreciate you.
                </strong>

                <br><br>

                I appreciate your words, your help, your kindness,
                your advice, your jokes, and all the little moments
                that make you such a memorable person.
                <br><br>

                Thank you for being someone who can make studying feel
                easier and everyday moments feel happier.
                <br><br>

                Keep smiling, keep being amazing, and never forget that
                the little things you do can mean a lot to someone.
                <br><br>

                <strong>
                    Happy Teacher's Day, Api Umaima! 🌼💛✨
                </strong>
            </p>

        </div>

    </section>


    <!-- FOOTER -->
    <footer>

        Made with appreciation for Api Umaima 🌼
        <br>

        💛 Thank you for all the little things you do. 💛

    </footer>


    <!-- JAVASCRIPT -->
    <script>

        function showSurprise() {

            const message = document.getElementById("surprise");

            if (message.style.display === "block") {

                message.style.display = "none";

            } else {

                message.style.display = "block";

                message.scrollIntoView({
                    behavior: "smooth",
                    block: "center"
                });

            }

        }

    </script>

</body>
</html>
```
