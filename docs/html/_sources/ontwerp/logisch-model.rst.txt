
Een logisch model
=================

We geven hier een voorbeeld een logisch model in de vorm van een Entity-Relationship Diagram.
We gebruiken weer hetzelfde voorbeeld als in het vorige hoofdstuk:
een webtoepassing waarmee leden zich kunnen inschrijven voor één of meer events.

.. figure:: Model-0.png
  :width: 450px
  :align: center

  Entity-Relationship diagram - eerste stap

Dit is een eerste, nog onvolledige stap naar het logische model.
De belangrijkste elementen in het model zijn:

* Lid: een entiteit
* Event: een entiteit
* Inschrijving: een relatie tussen Lid en Event.

Een **Entiteit** is een concreet of abstract "ding" dat betekenis heeft in de organisatie ("business").
Je geeft een entiteit aan met een zelfstandig naamwoord.
In een E-R diagram gebruiken we een rechthoek met daarin de naam van de entiteit.

Een **Relatie** geeft het verband tussen twee of meer entiteiten weer.
Je geeft een relatie aan met een werkwoord (bijvoorbeeld "inschrijven") of een werkwoordsvorm ("inschrijving").
In een E-R diagram gebruiken we een ruit met daarin de naam van de relatie.

Je kunt het bovenstaande lezen als: een Lid heeft zich ingeschreven voor een Event.

Multipliciteit
--------------

.. figure:: ERD-Multipliciteit.png
  :width: 300px
  :align: right

  Kraaienpootnotatie voor multipliciteit


In de figuur hierboven zie je ook wat de multipliciteit is van de relatie,
aan de hand de kraaienpoot-notatie.
Je ziet dan direct of er sprake is van een 1-1 relatie, een 1-N relatie, of een N-M relatie;
en of de relatie optioneel is (0 als ondergrens) of verplicht (1 als ondergrens).

Zo'n kraaienpoot kun je zien als een speciale pijl die je leest als "heeft".
Het onderwerp van de zin staat aan het begin van de pijl;
de relatie beschrijf je als een werkwoordsvorm;
het aantal staat aan de kant van de pijlpunt, bij het lijdend voorwerp in de zin.

Uit de ERD-figuur hierboven kunnen we dan aflezen:

* *elk* Lid heeft zich ingeschreven voor 0 of meer Events;
* *elk* Event heeft 0 of meer ingeschreven Leden.

Aan de hand van dergelijke "ERDish" zinnen kan een ontwerper nagaan bij een gebruiker of domein-expert of hij de organisatie of toepassing goed begrepen heeft.

  *Opmerking.* Soms kom je de term ''cardinaliteit'' tegen in plaats van ''multipliciteit''. We volgen hier de terminologie en de motivatie erachter van [https://martinfowler.com/bliki/MultiplicityNotCardinality.html Martin Fowler].

Attributen
----------

We hebben in het model meer details nodig over de entiteiten en de relaties,
in de vorm van attributen.

Een '''attribuut''' beschrijft een eigenschap van een entiteit of relatie.

.. figure:: Model-1.png
  :width: 700px
  :align: center

  E-R model met entiteiten, relatie en attributen

In de bovenstaande figuur zien we het volgende:

* de entiteit Lid heeft als attributen: *email*-adres, voornaam, achternaam;
* de entiteit Event heeft als attributen: *datum*, *beschrijving*;
* de relatie Inschrijving heeft als attribuut: maaltijd (-keuze).

Identificatie
-------------

De namen van enkele van de attributen zijn in de figuur onderstreept.
Hiermee geef je aan dat deze attributen de bijbehorende entiteit *identificeren*:

* het attribuut :code:`email` identificeert een Lid;
* de combinatie van `datum` en `beschrijving` identificeert een Event.

Dit is de **unieke identificatie (UID)** van de entiteiten zoals de ''business'' dit gebruikt.

Later gaan we in op de identificatie van een Inschrijving.

* `Wikipedia: Entity-Relationshipmodel <https://nl.wikipedia.org/wiki/Entity-relationshipmodel>`_

Instanties
----------

Een entiteit beschrijft alle mogelijke instanties van die "klasse".
Op dezelfde manier beschrijft het logische model alle mogelijke combinaties van instanties.
Dit zie je ook terug in de ERDish-zinnen: "Elk lid heeft een voornaam, een achternaam, een email-adres, en 0 of meer inschrijvingen."
Het is soms lastig om de gevolgen van zulke uitspraken te begrijpen.

In de communicatie met de opdrachtgever kan het handig zijn om voorbeelden (en tegenvoorbeelden) van instanties te geven,
om de randgevallen van deze uitspraken te controleren.

Constraints
-----------

(In dit voorbeeld hebben we geen andere constraints dan die voor de multipliciteit.)
NB: deze constraints zijn "business rules" die de data in de database bepalen/beperken.

Redundantie/normalisatie
------------------------

* '''Opmerking''': de rol van normalisatie in het logische model verschilt van die in het fysieke model! Uitleggen...

(In dit voorbeeld hebben we geen redundantie; het is in genormaliseerde vorm.)

* redundantie/normalisatie

De belangrijkste regel voor normalisatie is dat elk feit maar één keer in het model voorkomt.
Dit heet ook wel: het model bevat geen redundantie.

Voorbeelden van redundantie:
* afgeleide feiten, bijvoorbeeld leeftijd (kun je uitrekenen uit de geboortedatum en de huidige datum);
* herhaalde feiten, bijvoorbeeld: als je bij de naam van een leerling in een cijfertabel ook steeds het adres en het telefoonnummer noemt. Een leerling komt waarschijnlijk vaker dan één keer in de tabel voor: hetzelfde adres en telefoonnummer moet dan steeds herhaald worden.


De regel is dan dat elk attribuut van een entiteit alleen en volledig afhangt van de primaire sleutel (UID) van die entiteit.
Anders gezegd:
* een attribuut hangt niet af van andere attributen (dan de primary key);
*

Wat bedoelen we hier met "afhangen van"?
* A hangt af van B betekent: als je A verandert, moet je ook B aanpassen.
** bijvoorbeeld: als je de naam van een leerling verandert in de cijfertabel, bijvoorbeeld omdat je eerst een foute naam genoteerd had, moet je ook het adres en het telefoonnummer aanpassen.


"Afhangen van" is eigenschap van "de business": je kunt deze vraag alleen beantwoorden met kennis van de business (de "wereld").


Waarom normaliseren?
*

Het fysieke model kunnen we eventueel "de-normaliseren": we kunnen bepaalde afgeleide gegevens bewaren, of we kunnen gegevens op meerdere plekken in de database opslaan. Dat maakt het lastiger en minder efficiënt om veranderingen op een consistente manier door te voeren. Een belangrijke reden om dit toch te doen is om bepaalde gegevens sneller te kunnen opvragen.
