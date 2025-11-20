<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>I’ve Loved You For...</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />

  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
    }

    body {
      min-height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      background: radial-gradient(circle at top, #ffe5ec, #ffc2d1, #ff8fab);
      color: #2b1b27;
    }

    .card {
      background: rgba(255, 255, 255, 0.95);
      border-radius: 24px;
      padding: 24px 28px;
      max-width: 420px;
      width: 90%;
      box-shadow: 0 12px 30px rgba(0, 0, 0, 0.13);
      text-align: center;
      position: relative;
      overflow: hidden;
    }

    .heart {
      position: absolute;
      font-size: 80px;
      color: #ff4d6d;
      opacity: 0.08;
      pointer-events: none;
    }

    .heart.left {
      top: -10px;
      left: -10px;
    }

    .heart.right {
      bottom: -10px;
      right: -10px;
      transform: rotate(-20deg);
    }

    h1 {
      font-size: 1.7rem;
      margin-bottom: 4px;
    }

    .subtitle {
      font-size: 0.95rem;
      color: #7f6a7c;
      margin-bottom: 16px;
    }

    .timer {
      margin: 18px 0;
      font-size: 1rem;
      font-weight: 600;
      line-height: 1.3;
    }

    .timer span {
      display: inline-block;
      margin: 2px 4px;
      padding: 6px 10px;
      border-radius: 999px;
      background: #ffe5ec;
      font-size: 0.9rem;
    }

    .quote-box {
      margin-top: 18px;
      padding: 14px 12px;
      border-radius: 16px;
      background: #fff5f8;
      font-size: 0.95rem;
      font-style: italic;
      color: #4b2d3c;
    }

    .quote-author {
      margin-top: 6px;
      font-size: 0.8rem;
      font-style: normal;
      color: #9a7f92;
    }

    button {
      margin-top: 18px;
      border: none;
      border-radius: 999px;
      padding: 10px 18px;
      font-size: 0.9rem;
      font-weight: 600;
      cursor: pointer;
      background: #ff4d6d;
      color: white;
      transition: transform 0.08s ease, box-shadow 0.08s ease, background 0.15s ease;
      box-shadow: 0 6px 14px rgba(255, 77, 109, 0.4);
    }

    button:hover {
      background: #ff3359;
      transform: translateY(-1px);
      box-shadow: 0 8px 18px rgba(255, 77, 109, 0.5);
    }

    button:active {
      transform: translateY(0);
      box-shadow: 0 4px 10px rgba(255, 77, 109, 0.35);
    }

    .footer-note {
      margin-top: 12px;
      font-size: 0.75rem;
      color: #b093a5;
    }
  </style>
</head>
<body>
  <div class="card">
    <div class="heart left">♥</div>
    <div class="heart right">♥</div>

    <h1>I’ve loved you for</h1>
    <p class="subtitle">…every one of these moments & many more to come 💕</p>

    <div class="timer" id="timer">
      <!-- Filled by JavaScript -->
    </div>

    <div class="quote-box">
      <div id="quote-text">Loading quote…</div>
      <div class="quote-author" id="quote-author"></div>
    </div>

    <button id="new-quote-btn">New little reminder ✨</button>

    <p class="footer-note">
      (Made with lots of love and a little bit of code.)
    </p>
  </div>

  <script>
    // === 1. SET YOUR ANNIVERSARY DATE HERE ===
    // Format: new Date("YYYY-MM-DDTHH:MM:SS")
    // Example: June 1, 2023 at midnight
    const anniversary = new Date("2023-06-01T00:00:00");

    // === 2. TIMER LOGIC ===
    function updateTimer() {
      const now = new Date();
      const diffMs = now - anniversary;

      if (diffMs < 0) {
        document.getElementById("timer").textContent =
          "Our anniversary date is in the future! 😅";
        return;
      }

      const msPerSecond = 1000;
      const msPerMinute = msPerSecond * 60;
      const msPerHour = msPerMinute * 60;
      const msPerDay = msPerHour * 24;

      const days = Math.floor(diffMs / msPerDay);
      const daysRemainder = diffMs % msPerDay;

      const hours = Math.floor(daysRemainder / msPerHour);
      const hoursRemainder = daysRemainder % msPerHour;

      const minutes = Math.floor(hoursRemainder / msPerMinute);
      const minutesRemainder = hoursRemainder % msPerMinute;

      const seconds = Math.floor(minutesRemainder / msPerSecond);

      const timerEl = document.getElementById("timer");
      timerEl.innerHTML = `
        <span>${days} days</span>
        <span>${hours} hours</span>
        <span>${minutes} minutes</span>
        <span>${seconds} seconds</span>
      `;
    }

    // Update right away, then every second
    updateTimer();
    setInterval(updateTimer, 1000);

    // === 3. QUOTES ===
    const quotes = [
      {
        text: "I love you not only for what you are, but for what I am when I am with you.",
        author: "– Roy Croft"
      },
      {
        text: "In case you forgot today: you are capable, you are important, and you are so loved.",
        author: "– From me, always"
      },
      {
        text: "You are my favorite notification, my best decision, and my safest home.",
        author: "– Me, being honest"
      },
      {
        text: "I’ll choose you. Over and over. Without pause, without a doubt, in a heartbeat.",
        author: "– Every single day"
      },
      {
        text: "You have already survived 100% of your worst days. You can handle whatever comes next.",
        author: "– Your #1 fan"
      },
      {
        text: "Love is not about grand gestures; it’s the million tiny moments that say, ‘I’ve got you.’",
        author: "– Us"
      },
      {
        text: "No matter how today went, I am proud of you just for being you.",
        author: "– Me, always"
      },
      {
        text: "You are more than enough, exactly as you are right now.",
        author: "– A gentle reminder"
      }
    ];

    function showRandomQuote() {
      const { text, author } = quotes[Math.floor(Math.random() * quotes.length)];
      document.getElementById("quote-text").textContent = text;
      document.getElementById("quote-author").textContent = author;
    }

    // Show a quote on load
    showRandomQuote();

    // Button for new quote
    document.getElementById("new-quote-btn").addEventListener("click", showRandomQuote);
  </script>
</body>
</html>
