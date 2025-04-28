---
{"dg-publish":true,"permalink":"/chatbot/index-html/","created":"2025-04-27T11:35:11.000+02:00","updated":"2025-04-28T09:05:02.376+02:00"}
---

<link rel="stylesheet" href="Style.css">
<script src="Script.js"></script>


<!DOCTYPE html>
<html lang="da">
<head>
    <meta charset="UTF-8">
    <title>Ugle Chatbot</title>
    <link rel="stylesheet" href="Style.css">
</head>
<body>
    <div class="chat-container">
        <div class="avatar-container">
            <img src="https://i.imgur.com/YO2lFmg.png" alt="Uglebot" id="owlAvatar">
        </div>
        <div id="chatbox"></div>
        <div class="input-section">
            <input type="text" id="userInput" placeholder="Skriv din sætning her..." autocomplete="off">
            <button onclick="sendMessage()">Send</button>
        </div>
        <div class="mode-selector">
            <label for="mode">Vælg chatstil:</label>
            <select id="mode">
                <option value="left">Skiftende sider (venstre-højre)</option>
                <option value="classic">Klassisk (alt samme side)</option>
            </select>
        </div>
    </div>

    <script src="Script.js"></script>
</body>
</html>
