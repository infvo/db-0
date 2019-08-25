# Inleiding Databases

Mensen en organisaties gebruiken gegevens (data) bij het nemen van beslissingen en voor het uitvoeren van acties.

> Je gebruikt een lijst met contacten bij het sturen van een mail, om iemand op te bellen, of om een kaartje te sturen. Je gebruikt een agenda om te bepalen wat je vandaag of morgen moet doen. Je school gebruikt de cijferadministratie om te bepalen of je overgaat naar het volgende leerjaar - enz.

Deze gegevens hebben een bestaansrecht onafhankelijk van de toepassingen die er nu gebruik van maken.
Veel gegevens hebben betrekking op de wereld "buiten de computer" - en zijn van belang voor beslissingen in die wereld.
Bovendien hebben deze gegevens vaak een erg lange levensduur:
voor een organisatie misschien 10 jaar,
voor personen enkele decennia,
en voor historisch inzicht milennia.

Databases zijn al zo oud als het schrift: ook voor de komst van de computer zijn er veel gegevens in databases georganiseerd.
Het gebruik van computers maakt dat je anders met dit soort gegevens om kunnen gaan. Je kunt:

* gegevens gemakkelijk delen met anderen, waarbij iedereen steeds de juiste gegevens heeft;
* werken met grote verzamelingen gegevens;
* werken met complexe gegevens ;
* snel beslissingen nemen - op basis van actuele gegevens.

Bij het bovenstaande speelt *database-technologie* een belangrijke rol.
Deze biedt onder andere de volgende mogelijkheden:

* meerdere gebruikers tegelijk;
* gebruik op afstand (via het internet);
* zoeken in en samenvatten van (zeer) grote verzamelingen gegevens;
* werken met complexe gegevens;
* snel en consistent verwerken van aanpassingen van gegevens ("transacties").

Database-technologie staat niet op zichzelf, maar wordt steeds meer in combinatie met andere technologiëen gebruikt:

* het internet is essentieel voor het gebruik van databases op afstand;
* het internet of things vormt een belangrijke bron van actuele gegevens over de "wereld";
  dit levert zulke grote hoeveelheden gegevens dat database-technologie daarvoor essentieel is;
* data analytics en artificial intelligence zijn in staat om in zeer grote hoeveelheden gegevens ("big data") patronen, structuren en betekenis te ontdekken - waarmee betere besluiten genomen kunnen worden;
* het web is een belangrijke bron van gegevens (bijvoorbeeld "click data");
* voor het web zijn databases essentieel: van de grote databases voor zoekmachines en andere algoritmen van Google en Facebook, via de databaes van Wikipedia, tot de databases die gebruikt worden door webwinkels, bloggers, en andere websites.

Databases zijn in het begin vooral gebruikt voor de administratie van organisaties.
Tegenwoordig spelen databases op veel meer gebieden een grote rol.
In bijna alle wetenschapsgebeiden vormen data en *data science* een belangrijk middel;
databases vormen daarvoor een essentiële bouwsteen.

**Consistentie en integriteit.** Zoals gezegd hebben de gegevens in een database betrekking op een bepaalde "wereld" - bijvoorbeeld een organisatie in relatie tot zijn omgeving.
Het is dan belangrijk dat de gegevens in de database overeenkomen met de toestand van die wereld.
We spreken dan over *integriteit* van de data.
Anders gezegd: bij *integriteit* gaat het erom of de data "waar" zijn.

Een basisvoorwaarde daarvoor is dat de data in de database elkaar niet tegenspreken. De data moet *consistent* zijn.
Als je een bepaald basisgegeven op meerdere plekken in de database opslaat, en je moet een verandering van dit gegeven verwerken, dan kan het lastig zijn om deze consistentie op elk moment te garanderen.
Het is voor de consistentie dan handiger om basisgegevens op één plek op te slaan.
Bij het database-ontwerp proberen we daarom een *genormaliseerd* (niet-redundant) model te maken.
Ook het gebruik van *afgeleide gegevens* die gebaseerd zijn op veranderlijke basisgegevens is een vorm van redundantie die consistente veranderingen lastig maakt.

Bij het ontwerpen van een fysieke database offeren we soms consistentie tijdelijk op, om sneller toegang tot de data te kunnen krijgen.

## Voorbeeldtoepassing

Als voorbeeld gebruiken we een (web)toepassing waarmee gebruikers zich kunnen inschrijven voor verschillende events - zoals bijvoorbeeld schaakwedstrijden.
Een deelnemer moet zich eerst als lid aanmelden, met voornaam, achternaam en email.
Een aangemeld lid kan zich bij verschillende events (op verschillende data) inschrijven.
Bij inschrijving maakt een lid een keuze uit de verschillende maaltijden bij deze event.
Een lid kan zijn/haar inschrijvingen achteraf aanpassen.
Een event-organisator kan een overzicht krijgen van de inschrijvingen voor een event.

De verschillende events zijn met hun gegevens (datum, maaltijdkeuze) "hard gecodeerd" in de toepassing.
(Deze hoeven niet in de database opgenomen te worden.)

### Web-applicatie

Een uitwerking van dit voorbeeld is te vinden op glitch.com:

* [project](https://glitch.com/~succulent-colon) en
* [live toepassing](https://succulent-colon.glitch.me).

Je kunt daar de database-operaties vinden als onderdeel van een Python-Flask web-applicatie.
Je kunt op glitch.com een eigen "remix" maken van deze toepassing, met eigen uitbreidingen en variaties.

## Opdrachten

**Opdracht INL-1**

Geef tenminste 3 voorbeelden van databases uit je eigen omgeving.
(Dit mogen ook niet-gecomputeriseerde databases zijn.)
Geef tenminste 3 voorbeelden van toepassingen waarin waarin mogelijk een database gebruikt wordt/zinvol is.
Motiveer je antwoord.
