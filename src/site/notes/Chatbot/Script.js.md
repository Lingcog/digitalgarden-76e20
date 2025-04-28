---
{"dg-publish":true,"permalink":"/chatbot/script-js/","created":"2025-04-28T08:39:52.675+02:00","updated":"2025-04-28T08:53:50.497+02:00"}
---



let step = 0;
let userSentence = "";

const botMessages = [
    "Lad os læse din sætning sammen. Hører du noget, der måske lyder forkert?",
    "Okay! Lad os fokusere på et bestemt sted i sætningen.",
    "Hint: Det handler om verbets tid. Hvilken tid bruger du her?",
    "Fejlen er i verbets bøjning. Prøv at rette det.",
    "Super indsats! Nu hjælper jeg dig lidt mere.",
    "Her er en ledetråd: Tænk på, om handlingen sker nu eller skete før.",
    "Det korrekte svar ville være: (indsæt rettelse). Godt gået!"
];

function sendMessage() {
    const inputField = document.getElementById("userInput");
    const chatbox = document.getElementById("chatbox");
    const mode = document.getElementById("mode").value;

    if (step === 0) {
        userSentence = inputField.value;
    }

    addMessage("Dig", inputField.value, "user", mode);

    if (step < botMessages.length) {
        addMessage("Uglebot", botMessages[step], "bot", mode);
        step++;
    } else {
        addMessage("Uglebot", "Vil du prøve med en ny sætning?", "bot", mode);
        step = 0;
    }

    chatbox.scrollTop = chatbox.scrollHeight;
    inputField.value = "";
}

function addMessage(sender, message, senderType, mode) {
    const chatbox = document.getElementById("chatbox");
    let messageClass = "";

    if (mode === "left") {
        messageClass = senderType === "user" ? "user-left" : "bot-right";
    } else {
        messageClass = senderType === "user" ? "user-classic" : "bot-classic";
    }

    const messageElement = `<div class="${messageClass}"><strong>${sender}:</strong> ${message}</div>`;
    chatbox.innerHTML += messageElement;
}
