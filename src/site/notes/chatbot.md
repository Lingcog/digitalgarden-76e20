---
{"dg-publish":true,"permalink":"/chatbot/","created":"2025-04-28T08:45:41.000+02:00","updated":"2025-04-28T10:02:01.213+02:00"}
---


<!DOCTYPE html>
<html lang="da">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Chat med Uglebot</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f9f9f9;
      margin: 0;
      padding: 20px;
      display: flex;
      flex-direction: column;
      align-items: center;
      height: 100vh;
    }

    #chatbox {
      width: 90%;
      max-width: 600px;
      height: 70vh;
      background: #ffffff;
      border: 1px solid #ccc;
      border-radius: 10px;
      padding: 15px;
      overflow-y: auto;
      display: flex;
      flex-direction: column;
    }

    .message-row {
      display: flex;
      margin-bottom: 10px;
      align-items: flex-end;
    }

    .message {
      padding: 10px 15px;
      border-radius: 20px;
      max-width: 60%;
      font-size: 1rem;
      line-height: 1.4;
    }

    .user-message {
      background-color: #d2e5f1;
      align-self: flex-start;
    }

    .bot-message {
      background-color: #e0e0e0;
      align-self: flex-end;
      display: flex;
      align-items: center;
    }

    #userInput {
      width: 90%;
      max-width: 600px;
      display: flex;
      margin-top: 15px;
    }

    #userInput input {
      flex: 1;
      padding: 10px;
      font-size: 1rem;
      border: 1px solid #ccc;
      border-radius: 5px 0 0 5px;
    }

    #userInput button {
      padding: 10px;
      font-size: 1rem;
      background-color: #4CAF50;
      color: white;
      border: none;
      cursor: pointer;
      border-radius: 0 5px 5px 0;
    }

    #userInput button:hover {
      background-color: #45a049;
    }

    .owl-avatar {
      width: 40px;
      height: 40px;
      margin-left: 10px;
      animation: blink 5s infinite;
    }

    @keyframes blink {
      0%, 97%, 100% { transform: scaleY(1); }
      98%, 99% { transform: scaleY(0.1); }
    }

    h1 {
      margin-bottom: 10px;
    }
  </style>
</head>

<body>

  <h1>Chat med Uglebot 🦉</h1>

  <div id="chatbox"></div>

  <div id="userInput">
    <input type="text" id="textInput" placeholder="Skriv din besked her...">
    <button onclick="sendMessage()">Send</button>
  </div>

  <script>
    function sendMessage() {
      const inputField = document.getElementById("textInput");
      const userText = inputField.value.trim();
      if (userText === "") return;

      const chatbox = document.getElementById("chatbox");

      // Brugerens besked
      const userRow = document.createElement("div");
      userRow.className = "message-row";
      const userMessage = document.createElement("div");
      userMessage.className = "message user-message";
      userMessage.textContent = userText;
      userRow.appendChild(userMessage);
      chatbox.appendChild(userRow);

      chatbox.scrollTop = chatbox.scrollHeight;
      inputField.value = "";

      // Vis "Uglebot skriver..."
      const botRow = document.createElement("div");
      botRow.className = "message-row";
      const botMessage = document.createElement("div");
      botMessage.className = "message bot-message";
      botMessage.textContent = "Uglebot skriver...";
      const owlAvatar = document.createElement("img");
      owlAvatar.src = "https://upload.wikimedia.org/wikipedia/commons/thumb/3/3f/Owl_in_moonlight.jpg/220px-Owl_in_moonlight.jpg";
      owlAvatar.className = "owl-avatar";
      botMessage.appendChild(owlAvatar);
      botRow.appendChild(botMessage);
      chatbox.appendChild(botRow);

      chatbox.scrollTop = chatbox.scrollHeight;

      // Efter en kort pause ændres "Uglebot skriver..." til rigtig svar
      setTimeout(() => {
        botMessage.childNodes[0].textContent = generateBotResponse(userText);
      }, 1000);
    }

    function generateBotResponse(userInput) {
      userInput = userInput.toLowerCase();
      if (userInput.includes("hej")) {
        return "Hej med dig! 🦉 Hvordan kan jeg hjælpe?";
      } else if (userInput.includes("hvem er du")) {
        return "Jeg er din hjælpsomme uglebot!";
      } else if (userInput.includes("farvel")) {
        return "Farvel! På gensyn!";
      } else {
        return "Hmm, kan du sige det på en anden måde?";
      }
    }
  </script>

</body>
</html>
