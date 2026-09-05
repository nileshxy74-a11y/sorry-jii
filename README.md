<!DOCTYPE html>

<html lang="en">
<head>

```
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>For You ❤️ khushiii </title>

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>

<link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@400;500;600;700&family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">

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
        font-family: "Poppins", sans-serif;
        background: #0f0814;
        color: white;
        overflow-x: hidden;
    }


    /* ========================================
       LOADING SCREEN
    ======================================== */

    #loader {
        position: fixed;
        inset: 0;
        background: #0f0814;

        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;

        z-index: 9999;

        transition: opacity 1s ease;
    }

    .loader-heart {
        font-size: 70px;
        animation: heartbeat 1s infinite;
    }

    #loader p {
        margin-top: 20px;
        color: #ffc5dd;
        font-size: 15px;
    }

    @keyframes heartbeat {

        0%, 100% {
            transform: scale(1);
        }

        50% {
            transform: scale(1.25);
        }

    }


    /* ========================================
       FLOATING HEARTS
    ======================================== */

    .hearts-container {
        position: fixed;
        inset: 0;

        pointer-events: none;

        overflow: hidden;

        z-index: 1;
    }

    .heart {
        position: absolute;

        bottom: -50px;

        color: #ff6fae;

        font-size: 20px;

        opacity: 0.5;

        animation: floatHeart linear infinite;
    }

    @keyframes floatHeart {

        0% {
            transform: translateY(0) rotate(0deg);
            opacity: 0;
        }

        20% {
            opacity: 0.7;
        }

        100% {
            transform: translateY(-110vh) rotate(360deg);
            opacity: 0;
        }

    }


    /* ========================================
       GENERAL
    ======================================== */

    section {
        min-height: 100vh;

        padding: 90px 20px;

        position: relative;

        z-index: 2;

        display: flex;

        align-items: center;

        justify-content: center;
    }

    .container {
        width: 100%;

        max-width: 1050px;

        margin: auto;

        text-align: center;
    }


    /* ========================================
       HERO
    ======================================== */

    .hero {

        background:

            radial-gradient(
                circle at 20% 30%,
                #5b1647 0%,
                transparent 30%
            ),

            radial-gradient(
                circle at 80% 70%,
                #33134c 0%,
                transparent 35%
            ),

            #0f0814;
    }

    .small-text {

        color: #ff9ec7;

        letter-spacing: 3px;

        font-size: 13px;

        text-transform: uppercase;

        margin-bottom: 20px;
    }

    .hero h1 {

        font-family: "Dancing Script", cursive;

        font-size: clamp(55px, 10vw, 110px);

        line-height: 1;

        background:
            linear-gradient(
                90deg,
                #fff,
                #ff9fc8,
                #fff
            );

        -webkit-background-clip: text;

        -webkit-text-fill-color: transparent;
    }

    .hero h2 {

        margin-top: 25px;

        font-weight: 300;

        font-size: clamp(18px, 3vw, 28px);

        color: #ffd9e8;
    }

    .hero-description {

        max-width: 650px;

        margin: 30px auto;

        color: #cdbdca;

        line-height: 1.8;

        font-size: 15px;
    }

    .main-button {

        border: none;

        background:
            linear-gradient(
                135deg,
                #ff4f91,
                #c52cff
            );

        color: white;

        padding: 15px 32px;

        border-radius: 50px;

        font-size: 16px;

        cursor: pointer;

        box-shadow:
            0 10px 30px
            rgba(255, 79, 145, 0.3);

        transition: 0.3s;
    }

    .main-button:hover {

        transform:
            translateY(-4px)
            scale(1.03);

        box-shadow:
            0 15px 40px
            rgba(255, 79, 145, 0.5);
    }

    .scroll-text {

        margin-top: 55px;

        font-size: 12px;

        color: #867681;
    }


    /* ========================================
       SECTION TITLE
    ======================================== */

    .section-title {

        font-family:
            "Dancing Script",
            cursive;

        font-size:
            clamp(45px, 7vw, 75px);

        color: #ffb2d2;

        margin-bottom: 15px;
    }

    .section-subtitle {

        color: #a99ba7;

        margin-bottom: 45px;
    }


    /* ========================================
       APOLOGY
    ======================================== */

    .apology-card {

        max-width: 750px;

        margin: auto;

        padding: 45px;

        border:
            1px solid
            rgba(255,255,255,0.1);

        border-radius: 25px;

        background:
            rgba(255,255,255,0.04);

        backdrop-filter: blur(15px);

        box-shadow:
            0 20px 60px
            rgba(0,0,0,0.25);
    }

    .apology-card .emoji {

        font-size: 55px;

        margin-bottom: 20px;
    }

    .apology-card p {

        color: #ddd0da;

        line-height: 2;

        font-size: 16px;
    }

    .signature {

        margin-top: 30px;

        font-family:
            "Dancing Script",
            cursive;

        color: #ff9fc7;

        font-size: 30px;
    }


    /* ========================================
       MEMORIES
    ======================================== */

    .memory-grid {

        display: grid;

        grid-template-columns:
            repeat(3, 1fr);

        gap: 20px;
    }

    .memory-card {

        background:
            rgba(255,255,255,0.05);

        border-radius: 20px;

        overflow: hidden;

        border:
            1px solid
            rgba(255,255,255,0.08);

        transition: 0.4s;
    }

    .memory-card:hover {

        transform:
            translateY(-10px);
    }

    .memory-card img {

        width: 100%;

        height: 300px;

        object-fit: cover;

        display: block;
    }

    .memory-content {

        padding: 20px;
    }

    .memory-content h3 {

        color: #ffb0d0;

        margin-bottom: 8px;
    }

    .memory-content p {

        color: #aaa0aa;

        font-size: 13px;

        line-height: 1.6;
    }


    /* ========================================
       VIDEO
    ======================================== */

    .video-section {

        background:

            radial-gradient(
                circle at center,
                #35102e,
                transparent 50%
            ),

            #0f0814;
    }

    .video-card {

        max-width: 800px;

        margin: auto;

        padding: 15px;

        background:
            rgba(255,255,255,0.05);

        border:
            1px solid
            rgba(255,255,255,0.1);

        border-radius: 25px;

        backdrop-filter: blur(15px);

        box-shadow:
            0 25px 70px
            rgba(0,0,0,0.4);
    }

    .video-card video {

        width: 100%;

        max-height: 600px;

        display: block;

        border-radius: 18px;

        background: #000;
    }

    .video-caption {

        padding:
            25px 15px 15px;
    }

    .video-caption h3 {

        color: #ffb2d2;

        font-family:
            "Dancing Script",
            cursive;

        font-size: 32px;

        margin-bottom: 8px;
    }

    .video-caption p {

        color: #aaa0aa;

        font-size: 14px;
    }


    /* ========================================
       LOVE REASONS
    ======================================== */

    .reasons-grid {

        display: grid;

        grid-template-columns:
            repeat(3, 1fr);

        gap: 20px;
    }

    .reason {

        padding: 30px 20px;

        border-radius: 20px;

        background:
            linear-gradient(
                145deg,
                rgba(255,255,255,0.06),
                rgba(255,255,255,0.02)
            );

        border:
            1px solid
            rgba(255,255,255,0.07);

        transition: 0.3s;
    }

    .reason:hover {

        transform: scale(1.04);

        border-color:
            rgba(255,159,199,0.4);
    }

    .reason span {

        font-size: 40px;
    }

    .reason h3 {

        margin: 15px 0 10px;

        color: #ffc0d9;
    }

    .reason p {

        color: #aaa0aa;

        font-size: 13px;

        line-height: 1.6;
    }


    /* ========================================
       MUSIC
    ======================================== */

    .music-box {

        max-width: 600px;

        margin: auto;

        padding: 35px;

        border-radius: 25px;

        background:
            rgba(255,255,255,0.05);

        border:
            1px solid
            rgba(255,255,255,0.1);
    }

    .music-icon {

        font-size: 60px;

        animation:
            musicPulse 2s infinite;
    }

    @keyframes musicPulse {

        0%,100% {
            transform: scale(1);
        }

        50% {
            transform: scale(1.1);
        }

    }

    .music-box h3 {

        margin: 15px 0 5px;
    }

    .music-box p {

        color: #9f929d;

        margin-bottom: 20px;
    }

    audio {

        width: 100%;
    }


    /* ========================================
       FINAL QUESTION
    ======================================== */

    .question-section {

        background:

            radial-gradient(
                circle,
                #4d143e,
                transparent 45%
            ),

            #0f0814;
    }

    .question {

        font-family:
            "Dancing Script",
            cursive;

        font-size:
            clamp(45px, 8vw, 85px);

        color: #fff;

        margin-bottom: 20px;
    }

    .question-subtitle {

        color: #bbaab6;

        margin-bottom: 40px;
    }

    .buttons {

        display: flex;

        justify-content: center;

        gap: 15px;

        flex-wrap: wrap;
    }

    .answer-button {

        padding:
            14px 30px;

        border-radius: 50px;

        border:
            1px solid
            rgba(255,255,255,0.15);

        background:
            rgba(255,255,255,0.05);

        color: white;

        cursor: pointer;

        transition: 0.3s;
    }

    .answer-button:hover {

        background: #ff5797;

        transform:
            translateY(-4px);
    }


    /* ========================================
       FINAL MESSAGE
    ======================================== */

    .final-message {

        display: none;

        margin-top: 40px;

        animation:
            fadeUp 1s ease;
    }

    .final-message h2 {

        font-family:
            "Dancing Script",
            cursive;

        font-size: 60px;

        color: #ff9fc7;
    }

    .final-message p {

        max-width: 600px;

        margin: 20px auto;

        line-height: 1.8;

        color: #d4c6d0;
    }

    @keyframes fadeUp {

        from {

            opacity: 0;

            transform:
                translateY(30px);
        }

        to {

            opacity: 1;

            transform:
                translateY(0);
        }

    }


    /* ========================================
       FOOTER
    ======================================== */

    footer {

        position: relative;

        z-index: 2;

        padding: 40px 20px;

        text-align: center;

        color: #776b75;

        font-size: 12px;
    }

    footer span {

        color: #ff6fae;
    }


    /* ========================================
       MOBILE
    ======================================== */

    @media (max-width: 750px) {

        section {

            padding:
                70px 18px;
        }

        .memory-grid,
        .reasons-grid {

            grid-template-columns: 1fr;
        }

        .memory-card img {

            height: 350px;
        }

        .apology-card {

            padding:
                30px 22px;
        }

        .hero h1 {

            font-size: 65px;
        }

    }

</style>
```

</head>

<body>

<!-- ========================================
     LOADING
======================================== -->

<div id="loader">

```
<div class="loader-heart">
    ❤️
</div>

<p>
    Preparing something special for you...
</p>
```

</div>

<!-- ========================================
     FLOATING HEARTS
======================================== -->

<div
    class="hearts-container"
    id="hearts">
</div>

<!-- ========================================
     HERO
======================================== -->

<section class="hero">

```
<div class="container">

    <div class="small-text">
        A little something from me to you
    </div>


    <!-- CHANGE HER NAME HERE -->

    <h1>
        For You, khushiii 
    </h1>


    <h2>
        I know you're angry with me... 🥺
    </h2>


    <p class="hero-description">

        I could write a hundred messages,
        call you a thousand times,
        or say sorry again and again...

        <br><br>

        But instead, I made this little
        corner of the internet just for you. ❤️

    </p>


    <button
        class="main-button"
        onclick="scrollToSection('apology')">

        Give Me 2 Minutes ❤️

    </button>


    <div class="scroll-text">

        ↓ Keep scrolling ↓

    </div>

</div>
```

</section>

<!-- ========================================
     APOLOGY
======================================== -->

<section id="apology">

```
<div class="container">

    <h2 class="section-title">
        I'm Sorry...
    </h2>

    <p class="section-subtitle">
        And this time, I really mean it.
    </p>


    <div class="apology-card">

        <div class="emoji">
            🥺❤️
        </div>


        <p>

            I know I made you upset.

            <br><br>

            I'm not going to make excuses
            or try to prove that I was right.

            <br><br>

            If I hurt you, then I'm sorry.

            <br><br>

            Your feelings matter to me more
            than winning an argument ever could.

            <br><br>

            I know a simple "sorry" can't magically
            fix everything, but I hope you can see
            that I genuinely care about you.

            <br><br>

            You mean way more to me than I sometimes
            know how to express.

        </p>


        <div class="signature">

            — Your Idiot ❤️

        </div>

    </div>

</div>
```

</section>

<!-- ========================================
     MEMORIES
======================================== -->

<section>

```
<div class="container">

    <h2 class="section-title">
        Our Little Memories
    </h2>

    <p class="section-subtitle">
        Some moments I never want to forget.
    </p>


    <div class="memory-grid">


        <!-- MEMORY 1 -->

        <div class="memory-card">

            <img
                src="assets\photo1.jpeg"
                alt="Our memory">


            <div class="memory-content">

                <h3>
                    That First Moment ❤️
                </h3>

                <p>

                    Replace this with the story
                    of your first meeting or
                    first special memory.

                </p>

            </div>

        </div>


        <!-- MEMORY 2 -->

        <div class="memory-card">

            <img
                src="assets\photo14.jpeg"
                alt="Our memory">


            <div class="memory-content">

                <h3>
                    That Crazy Day 😂
                </h3>

                <p>

                    Write something funny
                    or cute about this memory.

                </p>

            </div>

        </div>


        <!-- MEMORY 3 -->

        <div class="memory-card">

            <img
                src="assets\photo5.jpeg"
                alt="Our memory">


            <div class="memory-content">

                <h3>
                    My Favorite Memory 🥹
                </h3>

                <p>

                    Write why this moment
                    is special to you.

                </p>

            </div>

        </div>

    </div>

</div>
```

</section>

<!-- ========================================
     VIDEO
======================================== -->

<section class="video-section">

```
<div class="container">

    <h2 class="section-title">
        A Little Video For You 🎬❤️
    </h2>


    <p class="section-subtitle">

        Some moments are better shown
        than explained.

    </p>


    <div class="video-card">


        <video
            id="ourVideo"
            controls
            playsinline
            poster="assets/photo1.jpg">


            <!-- YOUR VIDEO -->

            <source
                src="assets\our-video.mp4"
                type="video/mp4">


            Your browser does not support video.

        </video>


        <div class="video-caption">

            <h3>
                Our Little Story ❤️
            </h3>


            <p>

                Every second with you is a memory
                I want to keep forever.

            </p>

        </div>

    </div>

</div>
```

</section>

<!-- ========================================
     WHY SHE IS SPECIAL
======================================== -->

<section>

```
<div class="container">

    <h2 class="section-title">
        Why You Are Special
    </h2>


    <p class="section-subtitle">

        Just in case you forgot...

    </p>


    <div class="reasons-grid">


        <div class="reason">

            <span>😊</span>

            <h3>
                Your Smile
            </h3>

            <p>

                Your smile can literally
                change my mood in seconds.

            </p>

        </div>


        <div class="reason">

            <span>🫶</span>

            <h3>
                Your Care
            </h3>

            <p>

                The little ways you care
                about me mean more than
                you realize.

            </p>

        </div>


        <div class="reason">

            <span>🥰</span>

            <h3>
                Just You
            </h3>

            <p>

                Honestly, I don't need
                a reason. I just love
                having you in my life.

            </p>

        </div>


        <div class="reason">

            <span>😂</span>

            <h3>
                Your Craziness
            </h3>

            <p>

                Life is definitely more
                fun and chaotic with you.

            </p>

        </div>


        <div class="reason">

            <span>❤️</span>

            <h3>
                Your Heart
            </h3>

            <p>

                You have a beautiful heart
                and I hope you always
                remember that.

            </p>

        </div>


        <div class="reason">

            <span>🌎</span>

            <h3>
                My Person
            </h3>

            <p>

                Out of all the people in
                the world, I'm grateful
                that I found you.

            </p>

        </div>

    </div>

</div>
```

</section>

<!-- ======================================== MUSIC ======================================== -->

<section>

<div class="container">

    <h2 class="section-title">
        One Song For You 🎵
    </h2>


    <p class="section-subtitle">

        Because sometimes a song says
        what words can't.

    </p>


    <div class="music-box">

        <div class="music-icon">
            🎧
        </div>


        <!-- CHANGE SONG NAME -->

        <h3>
            Our Special Song
        </h3>


        <p>
            Replace this with your song name ❤️
        </p>


        <!-- YOUR SONG -->

        <audio
            id="music"
            controls>

            <source
                src="assets\song.mp3"
                type="audio/mpeg">

            Your browser does not support audio.

        </audio>

    </div>

</div>

</section>

<!-- ========================================
     FINAL QUESTION
======================================== -->

<section class="question-section">

```
<div class="container">


    <div class="small-text">

        Okay... one last thing

    </div>


    <h2 class="question">

        Are you still angry with me? 🥺

    </h2>


    <p class="question-subtitle">

        Be honest... 😭

    </p>


    <div class="buttons">


        <button
            class="answer-button"
            onclick="answer('yes')">

            YES 😤

        </button>


        <button
            class="answer-button"
            onclick="answer('maybe')">

            Maybe... 🥺

        </button>


        <button
            class="answer-button"
            onclick="answer('no')">

            No ❤️

        </button>

    </div>


    <!-- YES -->

    <div
        id="yesMessage"
        class="final-message">


        <h2>
            Okay... 🥺
        </h2>


        <p>

            I'll wait.

            <br><br>

            Take your time.

            <br><br>

            I'm not going anywhere. ❤️

        </p>

    </div>


    <!-- MAYBE -->

    <div
        id="maybeMessage"
        class="final-message">


        <h2>
            That's Progress! 🥹
        </h2>


        <p>

            I'll take "maybe" 😂❤️

            <br><br>

            Now I just have to
            make you smile again.

        </p>

    </div>


    <!-- NO -->

    <div
        id="noMessage"
        class="final-message">


        <h2>
            You Forgave Me! 🥹❤️
        </h2>


        <p>

            I promise I'm going to try
            my best to make you smile
            more than I make you angry.

            <br><br>

            Thank you for being you.

            <br><br>

            I love you. ❤️

        </p>

    </div>

</div>
```

</section>

<!-- ========================================
     FOOTER
======================================== -->

<footer>

```
Made with too much love

<span>❤️</span>

just for you.
```

</footer>

<script>


/* ========================================
   LOADING SCREEN
======================================== */

window.addEventListener("load", function() {

    setTimeout(function() {

        const loader =
            document.getElementById("loader");


        loader.style.opacity = "0";


        setTimeout(function() {

            loader.style.display = "none";

        }, 1000);


    }, 1500);

});



/* ========================================
   SMOOTH SCROLL
======================================== */

function scrollToSection(id) {

    document
        .getElementById(id)
        .scrollIntoView({

            behavior: "smooth"

        });

}



/* ========================================
   FLOATING HEARTS
======================================== */

const heartsContainer =
    document.getElementById("hearts");


function createHeart() {

    const heart =
        document.createElement("div");


    heart.classList.add("heart");


    const hearts = [

        "❤️",
        "💕",
        "💗",
        "💖",
        "💘",
        "💓"

    ];


    heart.innerHTML =
        hearts[
            Math.floor(
                Math.random() *
                hearts.length
            )
        ];


    heart.style.left =
        Math.random() * 100 + "%";


    heart.style.fontSize =
        Math.random() * 20 + 12 + "px";


    heart.style.animationDuration =
        Math.random() * 5 + 5 + "s";


    heartsContainer.appendChild(heart);


    setTimeout(function() {

        heart.remove();

    }, 10000);

}


setInterval(
    createHeart,
    700
);



/* ========================================
   ANSWER BUTTONS
======================================== */

function answer(type) {


    document
        .getElementById("yesMessage")
        .style.display = "none";


    document
        .getElementById("maybeMessage")
        .style.display = "none";


    document
        .getElementById("noMessage")
        .style.display = "none";


    if (type === "yes") {

        document
            .getElementById("yesMessage")
            .style.display = "block";

    }


    if (type === "maybe") {

        document
            .getElementById("maybeMessage")
            .style.display = "block";

    }


    if (type === "no") {

        document
            .getElementById("noMessage")
            .style.display = "block";


        celebration();

    }

}



/* ========================================
   HEART CELEBRATION
======================================== */

function celebration() {


    for (
        let i = 0;
        i < 40;
        i++
    ) {

        setTimeout(
            function() {

                createHeart();

            },
            i * 50
        );

    }

}



/* ========================================
   MUSIC ANIMATION
======================================== */

const music =
    document.getElementById("music");


music.addEventListener(
    "play",
    function() {

        document
            .querySelector(".music-icon")
            .style.animationDuration =
            "0.7s";

    }
);


music.addEventListener(
    "pause",
    function() {

        document
            .querySelector(".music-icon")
            .style.animationDuration =
            "2s";

    }
);



/* ========================================
   VIDEO
======================================== */

const video =
    document.getElementById("ourVideo");


video.addEventListener(
    "play",
    function() {

        console.log(
            "Our video is playing ❤️"
        );

    }
);


</script>

</body>
</html>
