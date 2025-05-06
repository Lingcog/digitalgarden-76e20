---
{"dg-publish":true,"permalink":"/chatbot/","created":"2025-05-06T10:29:30.833+02:00","updated":"2025-05-06T10:32:05.097+02:00"}
---


[[Feedback\|feedback]]

### Chatbot med datalogging

Jeg har udviklet en webbaseret chatbot, der kombinerer kunstig intelligens med læringsanalyse. Chatbotten er bygget op omkring OpenAI’s GPT-model, som besvarer brugerens spørgsmål på dansk i en pædagogisk og dialogisk form. Den er designet til sprogundervisning, hvor fokus ligger på at støtte og udfordre kursisten gennem vejledende feedback.

Det unikke ved løsningen er, at hver interaktion automatisk logges i en Supabase-database. Hver gang en kursist stiller et spørgsmål og får svar, registreres data som emne, underemne, person, forsøg, input og feedback. Det giver mulighed for at analysere, hvordan brugerne udvikler deres spørgestrategier, og hvordan feedback fra AI’en påvirker deres progression. Denne datalogning foregår helt automatisk i baggrunden, uden at forstyrre brugeroplevelsen.

Løsningen er udviklet med tanke på transparens og enkelhed. Eksporterede data kan analyseres manuelt eller bruges til videreudvikling af pædagogiske værktøjer. Målet er at kombinere AI, sprogdidaktik og datainformeret praksis.


