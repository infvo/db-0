# Inleiding Databases

Mensen en organisaties gebruiken gegevens (data) bij het nemen van beslissingen en voor het uitvoeren van acties.

> Je gebruikt een lijst met contacten bij het sturen van een mail, om iemand op te bellen, of om een kaartje te sturen. Je gebruikt een agenda om te bepalen wat je vandaag of morgen moet doen. Je school gebruikt de cijferadministratie om te bepalen of je overgaat naar het volgende leerjaar - enz.

Deze gegevens hebben een bestaansrecht onafhankelijk van de toepassingen die er nu gebruik van maken.
Veel gegevens hebben betrekking op de wereld "buiten de computer" - en zijn van belang voor beslissingen in die wereld.
Bovendien hebben deze gegevens vaak een erg lange levensduur:
voor een organisatie misschien 10 jaar,
voor personen enkele decennia,
en voor historisch inzicht milennia.

> Het schrift is ontstaan uit de behoefte om gegevens over zakelijke transacties vast te leggen (boekhouding).
Voor een hedendaags historicus zijn deze oude boekhoudingen van groot belang.

Het gebruik van computers maakt dat we anders met dit soort gegevens om kunnen gaan:

* we kunnen deze gegevens veel gemakkelijker delen met anderen, waardoor we ervoor kunnen zorgen dat iedereen op elk moment de juiste gegevens heeft;
* we kunnen veel gemakkelijker met grote verzamelingen gegevens werken;
* we kunnen met veel complexere gegevens werken;
* we kunnen veel sneller beslissingen nemen - op basis van actuele gegevens.

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

> Als voorbeeld van een database gebruiken we een eenvoudige website

Databases zijn in het begin vooral gebruikt voor de administratie van organisaties -
net als de eerste toepassingen van het schrift.
Tegenwoordig spelen databases op veel meer gebieden een grote rol.
In bijna alle wetenschapsgebeiden vormen data en *data science* een belangrijk middel;
databases vormen daarvoor een essentiële bouwsteen.

**Consistentie en integriteit** Zoals gezegd hebben de gegevens in een database betrekking op een bepaalde "wereld" - bijvoorbeeld een organisatie in relatie tot zijn omgeving.
Het is dan belangrijk dat de gegevens in de database overeenkomen met de toestand van die wereld.

**Verschillen tussen "normale" bestanden en databases**.

Zoals gezegd biedt een database-systeem (DBMS) de volgende mogelijkheden:

* meerdere gebruikers tegelijk;
* gebruik op afstand (via het internet);
* werkem met zeer grote hoeveelheden gegevens;
* werken met complexe gegegens;
* snel en consistent verwerken van aanpassingen (transacties)

De combinatie van deze mogelijkheden maakt het verschil ten opzichte van normale bestanden.

De grens tussen databases en bestanden is niet absoluut:
tegenwoordig kun je samenwerken aan een gemeenschappelijk spreadsheet-document.
Dat kun je zien als een eenvoudige database.
Maar een belangrijk verschil blijft dan de *schaalbaarheid*:
je kunt met een spreadsheet werken met 100 rijen, of misschien 1000,
maar de stap naar 1.000.000 rijen is niet werkbaar.
