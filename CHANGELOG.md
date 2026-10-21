# Versies

Het versienummer staat in `VERSION`. Bij elke nieuwe versie: nummer ophogen, hier een regel toevoegen, `python3 build.py` draaien.

## Versie 16 · 21-10-2026
- Regels maken en wijzigen in een eigen venster van de Office Assistent, geopend vanuit het paneel. Het venster toont meteen welke berichten in je postbus aan de regel voldoen en wat er per bericht verandert.
- Toepassen: een regel gaat ook over de berichten die er al zijn. Metagegevens alleen binnen de bedenktijd, mappen en markeringen in de hele postbus. Regels van de organisatie en het team kun je bekijken en op je eigen postbus toepassen, niet wijzigen.
- Techniek en Help beschrijven hoe het venster per mailprogramma werkt.

## Versie 15 · 21-10-2026
- Doorstroom: de animatie loopt trager, ongeveer een seconde per stap, met de melding dat het in werkelijkheid binnen een seconde gaat.
- Een envelop reist langs de negen stappen: dicht bij Exchange en in de wachtrij, opengevouwen bij de brug (met bijlagen), als bestand in Nextcloud, met eigen identificatie in het register, met metagegevens van de regel (zakelijk, classificatie, bron), en met kentekens voor objectopslag, zoekindex en een ongelezen-stip in Postvak IN. Een voortgangslijn en de actieve stap lichten op.

## Versie 14 · 21-10-2026
- Regels in het paneel van de Office Assistent, op drie niveaus: van de organisatie (informatiebeheerder), het team en de medewerker zelf. Een regel zet metagegevens zodra een bericht binnenkomt: zakelijk, classificatie, zaak, dossier, en voor de organisatie ook vertrouwelijkheid en Woo-categorie. Wat een regel zet, krijgt de regel als bron en valt onder dezelfde bedenktijd.
- Een nieuwe regel test je eerst op je berichten, en past hij desgewenst toe op berichten die nog binnen de bedenktijd vallen. Persoonlijk maken, weggooien en doorsturen naar buiten de gemeenten kan niet met een regel.
- Regels draaien bij het register, niet in de mailserver. Alleen wat bij aflevering moet gebeuren (map, markering, doorsturen binnen de gemeenten, afwezigheid) schrijft ELSA als Sieve-script; ManageSieve staat dicht voor mailprogramma's. De weergave Filters heet nu Regels en toont het beleid per niveau. Doorstroom, Architectuur, Techniek en Groeipad zijn bijgewerkt.

## Versie 13 · 19-10-2026
- Woo-categorie bij elk zakelijk bericht: zelf te kiezen, of overgenomen van de zaak of het dossier. Een zaak of dossier met een categorie gaat voor op de eigen keuze.
- Openbaar maken: met een categorie uiterlijk twee weken na ontvangst of verzending (Woo, artikel 3.3 lid 4), met het einde van de bedenktijd ervoor. Zonder categorie alleen openbaar op verzoek.

## Versie 12 · 19-10-2026
- Herzien binnen de bedenktijd: bovenaan Dit bericht staat de keuze, met de datum tot wanneer je haar kunt herzien en de knop om te wisselen. Persoonlijk kan nu ook terug naar zakelijk, ook na de bedenktijd. Verplaatsen uit de map Persoonlijk doet hetzelfde.
- Overzicht toont welke gekozen berichten je nog kunt herzien, met de resterende dagen.

## Versie 11 · 13-10-2026
- In lijn met de Office Assistent: het paneel is de Office Assistent in de mailomgeving, met de module E-mailarchivering. Architectuur toont de integratielaag tussen werkplek en ELSA; de assistent heeft geen token meer in het mailprogramma.
- Techniek: tabel met wat elke mailomgeving levert, ook Outlook met een Exchange-postbus ter vergelijking. Dezelfde tabel staat in de demo van de Office Assistent.

## Versie 10 · 13-10-2026
- Architectuur: productnamen veralgemeniseerd, zoals in MIRA. SharePoint of Teams heet nu Samenwerkomgeving (SharePoint, Teams, MijnBureau, LaSuite of een andere); het mailprogramma heet Mailomgeving.

## Versie 9 · 13-10-2026
- Architectuur: werkplek en aanvoer staan naast elkaar. De aanvoer loopt uitsluitend tussen backendsystemen; de werkplek komt alleen bij de ingangen voor het lezen en werken, en verzendt via SMTP.

## Versie 8 · 13-10-2026
- Een zakelijk bericht kan binnen de bedenktijd terug naar persoonlijk. De bewaarvergrendeling gaat pas in als de bedenktijd voorbij is.
- Niet als het bericht aan een zaak of dossier is gekoppeld (eerst ontkoppelen), en nooit als het onder een lopend Woo-verzoek valt.
- Na de bedenktijd alleen op verzoek, met reden. De informatiebeheerder beslist met een tweede beoordelaar; bij toekenning wordt de vergrendelde versie onleesbaar gemaakt en houdt het register vast dat het bericht bestond. Nieuwe rol Informatiebeheerder onder Sleutels.
- Afwezigheid: met het afwezigheidsbericht aan staat de bedenktijd stil. Nieuw voorbeeldbericht dat tijdens een vakantie automatisch zakelijk werd.

## Versie 7 · 13-10-2026
- Geen NiFi meer. Een kleine brug leest elk bericht uit Kafka en schrijft het in Nextcloud. Daarna loopt een bericht langs dezelfde weg als een bestand op een netwerkschijf: register, objectopslag, bewaartermijn en zoekindex via het register en de apps rond Nextcloud.
- Bijgewerkt in Doorstroom, Architectuur, Techniek en Groeipad. Techniek legt uit waarom dit afwijkt van XENA Deel I en wat het kost.

## Versie 6 · 12-10-2026
- Achter ELSA is opgesplitst in Architectuur, Techniek en Groeipad, zoals in de andere demo's.
- Architectuur: de lagen van werkplek tot Nextcloud-stack, en per handeling de stappen. Eén bericht in de objectopslag, met de IMAP-server en Nextcloud Files als twee ingangen.
- Techniek: drie manieren om IMAP naast WebDAV te laten draaien, een vergelijking van Apache James, Stalwart en Dovecot, wat er moet worden gebouwd en de open standaarden.
- Groeipad: vijf stappen, van archief en zoeken naast Exchange tot werken zonder Exchange.

## Versie 5 · 12-10-2026
- Een zakelijk bericht koppel je aan een zaak en aan een of meer dossiers. De zaak komt uit het zaaksysteem, dat leidend blijft; ELSA legt de koppeling vast als kenmerk. Een dossier verwijst naar het bericht, zonder kopie.
- Zaken en dossiers zoek je op met een invulveld dat al tijdens het typen voorstellen toont, met toetsenbordbediening. In de demo is het opzoeken nagebootst.
- Voorstellen voor een zaak of dossier op basis van het bericht.
- Colofon onder de titel, zoals in de andere demo's.

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
