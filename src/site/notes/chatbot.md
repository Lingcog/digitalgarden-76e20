---
{"dg-publish":true,"permalink":"/chatbot/","created":"2025-04-28T08:45:41.000+02:00","updated":"2025-04-28T09:28:31.000+02:00"}
---

[[Den digitale have\|Den digitale have]]

<!DOCTYPE html>
<html lang="da">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Chatbot</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f2f2f2;
      display: flex;
      flex-direction: column;
      align-items: center;
      padding: 2rem;
    }
    h1 {
      color: #333;
    }
    #chatbox {
      width: 90%;
      max-width: 600px;
      height: 400px;
      border: 1px solid #ccc;
      border-radius: 10px;
      padding: 1rem;
      background: white;
      overflow-y: auto;
      margin-bottom: 1rem;
    }
    #userInput {
      width: 90%;
      max-width: 600px;
      display: flex;
    }
    #userInput input {
      flex: 1;
      padding: 0.5rem;
      font-size: 1rem;
      border: 1px solid #ccc;
      border-radius: 5px 0 0 5px;
    }
    #userInput button {
      padding: 0.5rem 1rem;
      font-size: 1rem;
      border: none;
      background-color: #4CAF50;
      color: white;
      cursor: pointer;
      border-radius: 0 5px 5px 0;
    }
    #userInput button:hover {
      background-color: #45a049;
    }
    .message {
      margin: 0.5rem 0;
    }
    .user {
      text-align: right;
      color: blue;
    }
    .bot {
      text-align: left;
      color: green;
    }
  </style>
</head>
<body>

  <h1>Velkommen til Chatbotten</h1>
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

      // Vis brugerens besked
      const userMessage = document.createElement("div");
      userMessage.className = "message user";
      userMessage.textContent = userText;
      chatbox.appendChild(userMessage);

      // Simpel botsvar
      const botMessage = document.createElement("div");
      botMessage.className = "message bot";
      botMessage.textContent = generateBotResponse(userText);
      chatbox.appendChild(botMessage);

      // Scroll ned til bunden
      chatbox.scrollTop = chatbox.scrollHeight;

      // Ryd inputfeltet
      inputField.value = "";
    }

    function generateBotResponse(userInput) {
      // MEGET simpel logik
      userInput = userInput.toLowerCase();
      if (userInput.includes("hej")) {
        return "Hej med dig! Hvordan kan jeg hjælpe?";
      } else if (userInput.includes("hvem er du")) {
        return "Jeg er din hjælpsomme chatbot!";
      } else if (userInput.includes("farvel")) {
        return "Farvel! På gensyn!";
      } else {
        return "Det forstår jeg ikke helt. Kan du omformulere?";
      }
    }
  </script>

</body>
</html>
