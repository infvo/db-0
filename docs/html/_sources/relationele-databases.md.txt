## Relationele databases

Tabellen zijn altijd belangrijk geweest voor het weergeven van *gestructureerde gegevens*.
In een tabel kun je gelijksoortige gegevens op een overzichtelijke manier weergeven.
Een voorbeeld hiervan is een spreadsheet-tabel.
Een ander voorbeeld is het gebruik van tabellen in een traditionele boekhouding.

> Ook in de oudste voorbeelden van het schrift ("spijkerschrift") komen we tabellen tegen.

Relationele databases zijn gebaseerd op tabellen van *gelijkvormige gegevens*:

* een relationele database bestaat uit tabellen;
* een tabel bestaat uit benoemde kolommen van gelijksoortige gegevens,
* en uit rijen die geïdentificeerd worden met een sleutel (key).

Elke kolom in een tabel heeft een (unieke) naam.
Een kolom van een tabel bevat gegevens van eenzelfde (data)type,
bijvoorbeeld tekst, geheel getal, of datum.

Een rij in een tabel identificeer je met een (unieke) *key*, bijvoorbeeld het mobiel nummer van een persoon.

Dit betekent dat je elk elementair gegeven in een tabel kunt vinden met de combinatie van rij-*key*
en kolom-naam.

Enkele voorbeelden van tabellen

### Rekenen met relaties

Een relationele database wordt zo genoemd omdat een tabel (zoals hierboven beschreven) wiskundig gezien een relatie voorstelt.
Het rekenen met tabellen kun je dan uitdrukken met relationele operaties.
Enkele voorbeelden van dit soort operaties:

* *selectie* in een tabel A, op basis van een voorwaarde: het resultaat is een tabel die alleen de rijen van A bevat die aan de voorwaaarde voldoen;
* *projectie* van een tabel A, op basis van een reeks kolomnamen: het resultaat is een tabel die alleen de kolommen van A bevat met de genoemde namen;
* *cartesisch* product van tabellen A en B: een tabel met alle combinaties van de rijen van A en B.
* *aggregatie* (samenvatten) van de waarden in een kolom van een tabel, bijvoorbeeld het optellen van de waarden in een kolom.
    * (is het resultaat hiervan weer een tabel? met een enkele rij? wat zijn de kolomnamen?)

Deze operaties leveren een tabel op, waarmee je weer verder kunt rekenen.
Dit betekent dat je formules kunt maken die je samenstelt uit tabellen en deze operatoren.
Het rekenen met relaties is hierdoor een krachtig middel voor het werken met database-gegevens.

Enkele voorbeelden van selectie, projectie en cartesisch product:
