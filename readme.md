# 🚨 ANPR (Automatic Number Plate Recognition) Script voor FiveM 🚗

Het **ANPR (Automatic Number Plate Recognition)** script voor **FiveM** biedt een geavanceerde manier om kentekens van voertuigen te scannen en meldingen te sturen naar politieagenten wanneer een geregistreerd kenteken wordt gedetecteerd. Dit systeem maakt gebruik van zowel server- als client-side logica om een robuuste en effectieve manier van kentekenherkenning te bieden voor roleplay servers.

## 📋 Inhoud

1. [Overzicht van de Functies](#overzicht-van-de-functies)
2. [Event Flow en Gebruiksaanwijzing](#event-flow-en-gebruiksaanwijzing)
3. [Politie Meldingen](#politie-meldingen)
4. [Waypoint Functionaliteit](#waypoint-functionaliteit)
5. [Blips en Locatie Markering](#blips-en-locatie-markering)
6. [Commando's](#commando's)

---

## 🧠 Overzicht van de Functies

Dit ANPR script biedt de volgende kernfunctionaliteiten voor politieagenten op een FiveM-server:

- **Kentekenherkenning**: Het script detecteert wanneer een voertuig een kenteken heeft dat overeenkomt met een geregistreerd kenteken in de database.
- **Politie meldingen**: Wanneer een kenteken wordt gedetecteerd, wordt er een melding gestuurd naar politieagenten die de gebeurtenis kunnen bevestigen of negeren.
- **Waypoint functionaliteit**: Politiemedewerkers kunnen een waypoint naar het voertuig plaatsen, zodat ze snel naar de locatie van het voertuig kunnen navigeren.
- **Blips**: Verdachte voertuigen krijgen een visuele markering (blip) op de kaart, zodat politieagenten ze eenvoudig kunnen volgen.

---

## 🛠️ Event Flow en Gebruiksaanwijzing

Het ANPR script werkt met **server-side events** die worden getriggerd wanneer een voertuig met een geregistreerd kenteken passeert. Dit is hoe het werkt:

1. **Kentekenherkenning**: 
   - De server ontvangt het kenteken en de coördinaten van het voertuig en controleert dit tegen een vooraf ingestelde lijst van verdachte kentekens in de database.
   - Als er een overeenkomst wordt gevonden, wordt er een melding gestuurd naar de politieagenten die het kenteken kunnen bekijken en de gebeurtenis verder kunnen afhandelen.

2. **Melding naar de politie**:
   - Politieagenten ontvangen een melding die hen op de hoogte stelt van de match en de reden voor de match (bijvoorbeeld "gestolen voertuig").
   - De melding bevat de optie om een waypoint naar het voertuig te plaatsen of de gebeurtenis te negeren.

---

## 🧑‍✈️ Politie Meldingen

De politie ontvangt een **melding** die gedetailleerde informatie bevat over de hit. Dit zijn de belangrijkste onderdelen van de melding:

- **Titel**: Bijvoorbeeld: `🚨 ANPR Hit!`.
- **Beschrijving**: Gedetailleerde informatie over het voertuig, inclusief het kenteken en de reden voor de registratie (zoals "gestolen voertuig").
- **Opties**: Politieagenten krijgen de mogelijkheid om een waypoint naar de locatie van het voertuig in te stellen door op 'Y' te drukken of de melding te negeren door op 'N' te drukken.
- **Type**: De melding wordt gepresenteerd als een "error" om de urgentie te benadrukken.

---

## 🗺️ Waypoint Functionaliteit

Wanneer een politieagent een melding ontvangt, krijgt hij de mogelijkheid om een **waypoint** naar het voertuig in te stellen:

- **Y (Ja)**: Een waypoint wordt geplaatst op de locatie van het voertuig, zodat de politieagent snel kan navigeren.
- **N (Nee)**: De melding wordt gesloten zonder actie, en er wordt geen waypoint ingesteld.

Deze functionaliteit stelt politieagenten in staat snel actie te ondernemen en het voertuig te volgen, zelfs als ze de locatie niet fysiek kunnen zien.

---

## 📍 Blips en Locatie Markering

Een **blip** wordt toegevoegd op de kaart om de locatie van het verdachte voertuig te markeren. Dit stelt politieagenten in staat om het voertuig eenvoudig te volgen, zelfs als ze de locatie niet direct kunnen bereiken. De blip blijft op de kaart totdat de politieagent het zelf verwijdert of de situatie opgelost is.

---

## 🖥️ Commando's

Er zijn verschillende **commando's** die kunnen worden gebruikt om het ANPR-systeem te beheren en interactie te hebben met de server. Hier is een overzicht van de belangrijkste commando's:

1. **/check_plate [kenteken]**
   - **Beschrijving**: Controleert of het opgegeven kenteken aanwezig is in de database van verdachte voertuigen.
   - **Gebruik**: Dit commando wordt door admins of specifieke gebruikers gebruikt om handmatig een kenteken te controleren tegen de database.
   
2. **/add_suspect_plate [kenteken]** ^1(ADMIN ONLY)
   - **Beschrijving**: Voeg een kenteken toe aan de lijst van verdachte voertuigen.
   - **Gebruik**: Dit commando wordt gebruikt door admins om nieuwe verdachte kentekens in de database op te nemen. Wanneer een voertuig met dit kenteken passeert, zal het systeem een melding sturen naar de politie.

3. **/remove_suspect_plate [kenteken]** ^1(ADMIN ONLY)
   - **Beschrijving**: Verwijdert een kenteken uit de verdachte lijst.
   - **Gebruik**: Dit commando wordt gebruikt door admins om een kenteken uit de lijst van verdachte voertuigen te verwijderen. Verdachte kentekens worden niet meer gemeld als ze voorbijrijden.

4. **/clear_all_suspect_plates** ^1(ADMIN ONLY)
   - **Beschrijving**: Verwijdert alle kentekens uit de verdachte lijst.
   - **Gebruik**: Dit commando wordt gebruikt door admins om de volledige verdachte kentekenlijst te wissen.

---

## 🤝 Licentie

Dit script wordt aangeboden onder een **MIT**-licentie, wat betekent dat je het vrij kunt gebruiken en aanpassen zolang je de oorspronkelijke auteur en de licentie vermeldt.

---

Met deze gedetailleerde **README.md** heb je alle nodige informatie om het ANPR-systeem te begrijpen, inclusief de werking van de meldingen, waypoint-functionaliteit, blips en de beschikbare configuraties en commando's.

