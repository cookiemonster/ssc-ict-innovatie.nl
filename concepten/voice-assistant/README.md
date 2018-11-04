# Voice assistent
Voice control is sterk in opkomst. Dat is op zich geen nieuws, want digitale assistenten als Siri bestaan al jaren. Toch begint het kantoorgebruik van stemtechnologie nu pas echt door te breken. Hier in Nederland is het nog even afwachten, maar er is absoluut geen reden om stil te zitten. Wat kunnen wij met deze voice assistants wanneer ze de [Nederlandse taal](https://www.smarthomemagazine.nl/2018/07/nederlandse-google-assistant-home/) gaan beheersen?

## Aanleiding
Algemene informatie over onze organisatie is voor een groot deel vervat in intranet en FAQ.
Dat heeft twee problemen:
 1. Het is soms best een zoektocht om de juiste info te vinden (ook met de zoekfunctie)
 2. Niet altijd heb je toegang tot intranet als je een vraag hebt.
Daarnaast worden vanuit veel invalshoeken voice assistenten gezien als volgende interactie met gebruikers. Goed om op een niet al te complexe manier hier mee te gaan experimenteren om ervaring op te doen bij het maken en de interactie met de gebruikers.

De opdrachtgever geeft deze [video](https://youtu.be/ViB3XhsTLuo) als voorbeeld voor een concept.

## Hypothese
Met het ontsluiten van de geisoleeerde informatie via een voice assistent bijdragen aan een nieuwe gebruikerservaring.

## Wat wil de opdrachtegever bereiken met het concept?
 1. Ervaring opdoen met
   a. Het ontsluiten van informatie uit bestaande bronnen (intranet) voor voice assistenten
   b. Gebruikers feedback ophalen op deze manier van informatie aanbieden en deze wijze van interactie
 2. Opdoen van ideeen voor meer usecases.

## Technologie verkenning.

### oktober 2018
Op het moment heeft aleen Google Home een ondersteuning voor de Nederlandse taal (in BETA). Daarom gaan we de eerste prototype bouwen boven op [DialogFlow](https://dialogflow.com) en met [Actions](https://developers.google.com/actions/) met dit Smart Home [voorbeeld in Node.js](https://github.com/vgevers/smart-home-nodejs). Het voorbeeld is hier [gebouwd](https://ssc-ict-innovatie.slack.com/messages/CDJA596DQ). 

### november 2018
Open source project [MyCroft](https://community.mycroft.ai/t/how-to-get-mycroft-to-speak-and-understand-dutch/4963) maakt gebruik van Google services voor een Nederlandse taal ondersteuning. De [On Premise](https://mycroft.ai/enterprise/) Enterprise oplossing heeft nog geen eige ondesteuning voor Nederlandse taal.
