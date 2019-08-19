Een fysiek model
================

Een volgende stap is het vertalen van het logische model in een fysiek model, passend bij het DBMS dat voor de database gebruikt wordt.
Het fysieke model voor een relationele database ziet er anders uit dan dat voor een NoSQL document-database.
We geven hier het fysieke model voor de relationele Leden-Inschrijvingen-Events database.

.. figure:: MySQL-inschrijvingen-3.png
  :width: 650px
  :align: center

  Fysiek model van het voorbeeld, voor een relationele database

Het logische ERD-model is omgezet naar het fysieke relationele model:

* *entiteiten* worden *tabellen*: leden en events
* de relatie *inschrijving'* wordt ook een *tabel*: inschrijvingen
* *attributen* worden *kolommen* van deze tabellen.
* voor elk attribuut is het datatype bepaald (bijvoorbeeld: ``INT``, of ``VARCHAR(30)``).


Een instantie van een Lid, bijvoorbeeld met als waarden :code:`{"email": "jklaassen@kpnmail.nl", "voornaam": "Jan", "achternaam": "Klaassen"}`, wordt een rij in de tabel ``leden``.

Voor de identificatie van de leden en van de events gebruiken we een uniek nummer: <code>lidnr</code> en <code>eventnr</code>.
Een inschrijving identificeren we met de combinatie :code:`(lidnr, eventnr)`.
In een relationele database heet de identificatie van een rij de **primary key**.
Deze key gebruik je ook om te verwijzen naar deze rij vanuit een andere tabel;
de verwijzing in die andere tabel heet een **foreign key**.

Enkele opmerkingen hierbij:

* in het E-R Diagram gebruiken we meestal een enkelvoud, voor een tabelnaam een meervoud;
* een relatie wordt niet altijd een tabel; dit kan ook een verwijzing tussen tabellen zijn.

Schema
------

Uiteindelijk moeten we dit model in SQL beschrijven.
Zo'n beschrijving van een database of van een tabel noemen we ook wel een schema van de database of van de tabel.

In een relationeel DBMS wordt het schema van elke database in een database van het DBMS opgeslagen.
Je kunt dit dan ook opvragen via SQL.

Constraints
-----------

Zoals je ziet bevat het schema ook enkele constraints:

* de (externe) identificatie van een Lid is het email-adres; dat moet daarom uniek zijn.
* de (externe) identificatie van een Event is de combinatie (datum, beschrijving); deze moet uniek zijn.

Het relationele DBMS zorgt ervoor dat bij operaties op de database deze constraints gehandhaafd blijven,
ook als een gebruiker of een toepassing opdrachten geeft die hiermee in strijd zijn.

Index
-----

Een relationele DBMS maakt voor elke key een index, om daarmee efficiënt te kunnen zoeken.
Als je ook op een andere kolomwaarden efficiënt wilt kunnen zoeken, dan kun je daarvoor in het fysieke model een index opnemen.
Zo'n index vraagt wel extra ruimte.

Oefeningen
----------

* oefening/opdracht: opvragen van schema
* oefening: effect van constraints
* oefening: index????
