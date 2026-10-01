📍 Openingstijden Webapp — Jongerenwerk

Een lichte, mobielvriendelijke webapplicatie waarmee jongerenwerkers eenvoudig hun openingstijden, locaties en activiteiten kunnen beheren via Google Forms en Google Sheets, met automatische weergave via GitHub Pages.

✨ Functionaliteiten

Real-time synchronisatie: Gegevens worden direct ingeladen via een openbare Google Sheets CSV-export.

Automatische "Overige" verwerking: Handmatige toelichtingen bij Locatie, Type Avond of Activiteit worden automatisch netjes samengevoegd (bijv. Overige - Kookworkshop).

Geannuleerde activiteiten: Status-check op het woord "Geannuleerd" kleurt het betreffende kaartje automatisch rood, streept de tijden door en verwijdert de agendaknop.

Automatische datumfiltering: Verlopen openingstijden verdwijnen automatisch van het overzicht.

📅 Toevoegen aan agenda: Bezoekers kunnen met één klik een .ics-bestand downloaden om de bijeenkomst in hun eigen agenda (Google Calendar, Apple Agenda, Outlook) op te slaan.

Cache-buster: Voorkomt het tonen van verouderde gegevens door altijd direct een nieuwe versie bij Google op te vragen.

🛠️ Architectuur & Koppeling

[ Google Form ] ──> [ Google Sheet ] ──(CSV Export)──> [ Webapp op GitHub Pages ]


Kolomvolgorde Google Sheet

Om te zorgen dat de webapp de gegevens correct uitleest, dienen de kolommen in de gekoppelde Google Sheet op de volgende volgorde te staan:

A: Timestamp

B: Locatie (Dropdown)

C: Locatie - Overige (Optionele toelichting)

D: Type Avond (Dropdown)

E: Type Avond - Overige (Optionele toelichting)

F: Datum (DD-MM-YYYY)

G: Starttijd (HH:MM)

H: Sluitingstijd (HH:MM)

I: Activiteit (Dropdown)

J: Activiteit - Overige (Optionele toelichting)

K: Aanwezige begeleiders (Tekst)

L: Status (Optioneel: vul 'Geannuleerd' in om een bijeenkomst af te zeggen)

🚀 Installatie & Publicatie

Repository uploaden: Plaats index.html in de root van je GitHub repository.

GitHub Pages inschakelen:

Ga naar Settings > Pages in je GitHub repository.

Kies bij Source voor Deploy from a branch.

Selecteer de main (of master) branch en klik op Save.

Google Sheet Publiceren:

Open de Google Sheet met de antwoorden.

Ga naar Bestand > Delen > Publiceren op internet.

Selecteer het juiste blad en kies voor indeling CSV (.csv).

Plak de gegenereerde CSV-link op regel 178 in index.html bij CSV_BASE_URL.

📄 Licentie & Versie

Versie: v1.3.0

Licentie: MIT — Vrij te gebruiken en aan te passen voor jongerenwerkorganisaties.
