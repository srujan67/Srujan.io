<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Nickname Generator</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    body {
      background: #f2f7fa;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      height: 100vh;
      margin: 0;
    }
    .container {
      background: #fff;
      padding: 2rem 3rem;
      border-radius: 12px;
      box-shadow: 0 4px 16px rgba(0,0,0,0.08);
      text-align: center;
    }
    input[type="text"] {
      padding: 0.7rem;
      width: 250px;
      border-radius: 6px;
      border: 1px solid #bbb;
      font-size: 1rem;
      margin-bottom: 1rem;
    }
    button {
      background: #0077ff;
      color: #fff;
      border: none;
      padding: 0.7rem 1.4rem;
      border-radius: 6px;
      font-size: 1rem;
      cursor: pointer;
      transition: background 0.2s;
    }
    button:hover {
      background: #005ecc;
    }
    .nickname {
      margin-top: 1.5rem;
      font-size: 1.2rem;
      color: #2d7a5f;
      font-weight: bold;
    }
  </style>
</head>
<body>
  <div class="container">
    <h2>Nickname Generator</h2>
    <form id="nicknameForm">
      <input type="text" id="nameInput" placeholder="Enter your name" required />
      <br>
      <button type="submit">Get Nickname</button>
    </form>
    <div class="nickname" id="nicknameResult"></div>
  </div>
  <script>
    const nicknames = [
      "the Brave", "the Swift", "the Wise", "the Bold", "the Great", "the Coder",
      "the Cool", "the Lionheart", "the Ninja", "the Wizard", "the Genius", "the Rockstar",
      "the Explorer", "the Maverick", "the Champion", "the Spark", "the Ace", "the Prodigy"
    ];

    document.getElementById('nicknameForm').addEventListener('submit', function(e) {
      e.preventDefault();
      const name = document.getElementById('nameInput').value.trim();
      if (name.length === 0) {
        document.getElementById('nicknameResult').textContent = "Please enter your name.";
        return;
      }
      // Pick a random nickname
      const randomNick = nicknames[Math.floor(Math.random() * nicknames.length)];
      document.getElementById('nicknameResult').textContent = `Your nickname: ${name} ${randomNick}`;
    });
  </script>
</body>
</html>

