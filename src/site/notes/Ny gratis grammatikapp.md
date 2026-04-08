---
{"dg-publish":true,"permalink":"/ny-gratis-grammatikapp/","created":"2026-04-07T07:59:27.895+02:00","updated":"2026-04-08T14:43:02.555+02:00"}
---

Velkommen til den nyeste udgave af min digitale assistent for undervisere og kursister i dansk som andetsprog! Min [tidligere app](https://lingcog.com/ny-dansk-grammatikapp/) lagde vægt på at en frase kan indgå i en sætning som til gengæld kan indgå i en helsætning med en konjunktion, altså et meget mekanisk og funktionelt sprogsyn. Denne nye app hviler på et funktionelt-kognitivt sprogsyn der lægger op til at kursister skal eksperimentere med sprogets bestanddele og forstå at betydning ændrer sig, når vi skifter nogle dele ud med andre. 

1. **Den er helt gratis i drift.**
2. **Den tilbyder en ny, visuel introduktion til grammatikforståelse.**

Her er en kort guide til, hvad appen kan, og hvordan den pædagogisk understøtter tilegnelsen af dansk.

---

## 💡 En ny introduktion til Grammatikforståelse

Mange kursister – særligt dem uden en stærk skolebaggrund – synes grammatik er abstrakt og uforståeligt. For at løse dette, bygger denne app på et helt centralt pædagogisk greb: **Grammatik som visuelle byggeklodser der kan interageres med**.

### Forankring i virkeligheden og byggeklodser

Appens helt store styrke er introduktionen til de danske ordklasser. I stedet for at starte med lange, abstrakte forklaringer, bliver kursisten præsenteret for grammatik gennem "byggeklodser", som de kan manipulere med.

- **Substantiver** (bla. i kombination med demonstrative pronominer)
- **Verber** (bla. modalverbers kognitive betydning)
- **Adjektiver** (bla. deres funktionelle betydning) ... og så videre.

Dette fjerner det fremmedgørende metasprog og lader kursisten "se" sætningens struktur. Den visuelle forankring fungerer som et solidt pædagogisk stillads, der forhåbentlig gør selv svagere kursister i stand til at bygge og forstå danske sætninger intuitivt. Det er ikke bare grammatik; det er leg med sprogets struktur.

### Funktionel-kognitiv grammatik: Fra abstrakte regler til meningsfuld forankring

Kernemodulet "Hvorfor bruger vi grammatik?" repræsenterer appens fundamentale tilgang til at bruge grammatik. Modulet trækker på et funktionelt-kognitivt lingvistisk perspektiv. I stedet for at kræve at kursisten skal lære indviklede regler, bliver grammatikken brudt op og forklaret uhyre simpelt som sprogets måde at fastgøre "ting" og "handlinger" i virkeligheden på.

I løbet af en række **enkle interaktive trin** og hele **7 konkrete valg/forankringer**, får kursisten demonstreret præcis, hvordan byggeklodserne skaber mening sammen. Kursisten skal bl.a. vælge:

- **Tingsforankring (pronominer der fungerer som ankre):** Valget mellem f.eks. "Et barn", "Mit barn", "Det barn" eller "Dette barn". Det viser, om en ting er ukendt, tilhører nogen, er langt væk eller nær.
- **Tidsforankring (verber der fungerer som ankre):** Valget mellem "spiser" (nu), "spiste" (fortid) eller "skal spise" (fremtid).

Gennem træk-og-slip øvelser skal kursisten sammensætte disse valg. Den samlede "Forankring"-øvelse illustrerer således de 7 fundamentale grammatiske dimensioner. Det abstrakte system gøres funktionelt – og meget, meget enkelt. Ved hvert niveau inviteres brugeren til at undersøge det grammatiske fænomen nærmere, og der er links til diverse øvelser.

### Interaktive øvelser med målrettet feedback

Appen indeholder specifikke træningsmoduler for de vigtigste byggeklodser:

- **Pronomen-træning:** Øvelser der hjælper kursisten med at navigere i "han/ham/hans" osv., samt det altid drilske _"der er" vs. "det er"_.
- **Verber:** Forskel på datid og førnutid. Desuden er der et modul træner i brugen af de 70 mest brugte verber på dansk.
- **Konjunktioner og adverbier:** Forståelsen af formålet med sætningsforbindere og ord der angiver tid og holdninger, bliver uddybet og guidet af umiddelbar feedback på brugerens valgte sprog.
- **Lær nye ord:** Integrerede ordforrådsøvelser baseret på semantiske netværk (overbegreber, underbegreber, antonymer, synonymer). 

Feedbacken fastholder kursistens opmærksomhed. Hver gang de vælger forkert, fortæller systemet dem _hvorfor_, ofte med referencer direkte til byggeklodserne eller den specifikke kontekst.

### Oversættelse af Feedback til 17 Sprog

Et af de allerstørste pædagogiske løft i den nye platform er den udvidede modersmålsstøtte. Appen er nu i stand til at levere præcis, metalingvistisk feedback oversat til hele **17 forskellige sprog**. Det vil sige, at der er indbygget "mekanisk" feedback, som hviler på forståelse af grundprincipper fremfor udenadslære. Eftersom feedbacken er indbygget i øvelserne, kræver det ikke API-opkald. Dette bygger videre på princippet om _modersmålet som ressource_. Frem for at kursisten skal afkode en kompliceret dansk forklaring på en fejl (og derved bruge dyrebar kognitiv kapacitet på at oversætte), får de forklaringen serveret på et sprog, de allerede forstår. Det minimerer misforståelser drastisk og sikrer, at selv kursister på niveau A1 kan få udbytte af komplekse, strukturelle forklaringer.

---

## 🛠 For de teknologisk interesserede: Hvorfor den er "gratis i drift"

I den [tidligere version af appen](https://lingcog.com/ny-dansk-grammatikapp/) løb jeg ind i et reelt problem med server-infrastrukturen: AI tager tid om at tænke. For ikke at få en "timeout" fejl og miste svaret efter 10 sekunder, måtte jeg betale for et avanceret Netlify-abonnement, alene for at forlænge svartiden op til 26 sekunder.

**Det problem er nu løst ved at lade brugerens eget system trække læsset.** Hovedårsagen til, at "Gratisapp" vitterligt er 100 % gratis at drive for mig, ligger i arkitekturen. I stedet for at kalde dyre API'er via en bagvedliggende server, bygger appen på skræddersyede _Gembots_ (specialiserede AI-tutorer) via Google Gemini.

Dette teknologiske skift betyder:

1. **Egne konti:** For at løse de interaktive chat-øvelser sendes kursisten over til en Gembot hos Gemini, hvor de blot bruger deres egen private internetkonto ved at logge ind. Det fjerner API-udgifterne helt.
2. **Ingen timeouts:** Dels er feedbacken i de fleste øvelser indbygget i appen, og dels hænger svartiden  direkte på Geminis chat-grænseflade, så kursisten undgår servernedbrud, bare fordi en sætningsanalyse tager 12 sekunder at udregne.
3. **Samtykke i højsædet:** På grund af denne omvej findes der naturligvis en integreret AI-advarsel (consent) ved hver eneste opgave, før linket til Gembot'en aktiveres. Brugeren skal eksplicit krydse af, at de har forstået rammerne, før de kan starte deres gratis AI-session. Hvis de har gratis konto hos google, skal de nemlig advares om at Google træner AI på deres interaktion med øvelsen. Heldigvis er de fleste af øvelserne i appen ikke afhængige af direkte AI-interaktion.

---

### Integration i undervisningen

Præcis ligesom den forrige app, prioriterer denne web-app processen frem for det fejlfrie slutprodukt. Når en kursist præsenteres for "byggeklodserne", tvinger det dem til at reflektere over ordklassen, før de gætter på en form.

**Brugertip:** Lad kursisterne arbejde med "Grounding"-modulet i de første uger af et nyt modul, for at give dem et fælles sprog om de farvekodede ordklasser, som du derefter kan bygge videre på i undervisningen på tavlen!

_(Feedback modtages naturligvis stadig med kyshånd, når jeres kursister tager appen i brug!)_