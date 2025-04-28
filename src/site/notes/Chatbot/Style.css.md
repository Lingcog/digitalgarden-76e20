---
{"dg-publish":true,"permalink":"/chatbot/style-css/","created":"2025-04-28T08:38:46.605+02:00","updated":"2025-04-28T08:53:48.061+02:00"}
---



body {
    font-family: Arial, sans-serif;
    background-color: #eef2f3;
    margin: 0;
    padding: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
}

.chat-container {
    background: #fff;
    border-radius: 10px;
    box-shadow: 0 0 20px rgba(0,0,0,0.1);
    width: 90%;
    max-width: 400px;
    padding: 20px;
    display: flex;
    flex-direction: column;
}

.avatar-container {
    text-align: center;
    margin-bottom: 10px;
}

#owlAvatar {
    width: 100px;
    animation: float 3s ease-in-out infinite;
}

@keyframes float {
    0%, 100% { transform: translateY(0); }
    50% { transform: translateY(-10px); }
}

#chatbox {
    flex-grow: 1;
    overflow-y: auto;
    margin-bottom: 10px;
    border: 1px solid #ccc;
    padding: 10px;
    height: 300px;
    background-color: #fafafa;
}

.input-section {
    display: flex;
    gap: 10px;
    margin-bottom: 10px;
}

#userInput {
    flex-grow: 1;
    padding: 10px;
    font-size: 16px;
}

button {
    padding: 10px;
    font-size: 16px;
    background-color: #6699cc;
    color: white;
    border: none;
    cursor: pointer;
    border-radius: 5px;
}

button:hover {
    background-color: #557799;
}

.mode-selector {
    margin-top: 10px;
}
