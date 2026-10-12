# Versies

Het versienummer staat in `VERSION`. Bij elke nieuwe versie: nummer ophogen, hier een regel toevoegen, `python3 build.py` draaien.

## Versie 4 · 12-10-2026
- Het gemeentelijk adresboek staat in het paneel van de assistent: zoeken op naam, functie of afdeling, filteren op gemeente, de mensen bij het geopende bericht, favorieten (als verwijzing, geen kopie), een vermelding openen, een bericht beginnen of het adres kopiëren.
- Je eigen vermelding beheren in het paneel: opnemen of intrekken, kiezen wat je deelt, met een voorbeeld van hoe collega's je zien.
- Het adresboek is alleen zichtbaar binnen gemeenten die de Office Assistent gebruiken. Help legt uit hoe het werkt per mailprogramma (CardDAV in Thunderbird, alleen het paneel in Outlook).

## Versie 3 · 12-10-2026
- Drie mailprogramma's: Thunderbird (extensie), Outlook (klassiek) op Windows met een COM-invoegtoepassing die labels als lokale categorieën zet, en de nieuwe Outlook zonder assistent.
- Help legt uit waarom de nieuwe Outlook en Outlook op het web geen invoegtoepassing laden bij een IMAP-account.

## Versie 2 · 12-10-2026
- De assistent staat in een eigen paneel naast het bericht, zoals in MIRA, met de onderdelen Overzicht, Dit bericht en Help.
- In de berichtenlijst staan labels zoals een mailprogramma ze toont (IMAP-trefwoorden), in plaats van ingevoegde statusregels.
- Keuze tussen Thunderbird (assistent als extensie) en Outlook met een IMAP-account (geen assistent; scheiden via de map Persoonlijk, aanvullen in de webmail).

## Versie 1 · 12-10-2026
- Postbus: mailprogramma via IMAP, scheiden van zakelijk en persoonlijk met tien dagen bedenktijd, metagegevens, versleutelen, verwijderen met behoud van zakelijke berichten, zoeken, nieuw bericht met het adresboek.
- Doorstroom van Exchange Online via Kafka en NiFi naar register, objectopslag en zoekindex.
- Filters (Sieve) met de toegestane en verboden acties.
- Gemeentelijk adresboek met eigen keuze over opname, via CardDAV.
- Sleutels: toegang tot persoonlijke berichten alleen via de gemeentesecretaris, met logboek.
- Achter ELSA: architectuur en open punten.
- Talen: Nederlands, Duits, Engels en Frans.
