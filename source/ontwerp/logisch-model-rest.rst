
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
