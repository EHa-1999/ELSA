# ELSA

**Electronic Letters & Storage Archive.** Een demo van e-mailarchivering in XENA: elk bericht komt automatisch in het register en de objectopslag, en de medewerker leest het gewoon in zijn eigen mailprogramma via IMAP.

ELSA hoort bij XENA, naast de demo van de opslag, MIRA (de assistent in het kantoorpakket) en TINA (het zoekportaal voor de inwoner).

> Een demo, geen product. Personen, berichten, adressen en nummers zijn verzonnen.

## Wat de demo laat zien

| Weergave | Wat je ziet |
|---|---|
| **Postbus** | Een mailprogramma dat via IMAP uit ELSA leest. Per bericht de keuze zakelijk of persoonlijk, met tien dagen bedenktijd, metagegevens aanvullen en versleutelen. Verwijderen van een zakelijk bericht haalt het uit de map, maar het blijft bewaard. |
| **Doorstroom** | Hoe een bericht via Exchange Online, een transport rule, Kafka en Apache NiFi binnen een seconde in het register, de objectopslag en de zoekindex komt, zonder kopie in Exchange. |
| **Filters** | Sieve-filters die in ELSA zelf draaien, met de acties die niet zijn toegestaan omdat ze de scheiding zouden omzeilen. |
| **Adresboek** | Een gemeentelijk adresboek waarin iedereen zelf kiest of en met welke gegevens hij staat, gedeeld via CardDAV. |
| **Sleutels** | Persoonlijke berichten zijn versleuteld met een eigen sleutel. Alleen de gemeentesecretaris kan toegang geven of die bevoegdheid delegeren, en alles wordt gelogd. |
| **Achter ELSA** | De architectuur (optie 3, data volledig in eigen beheer) en de open punten. |

Met de knoppen bovenaan spring je vooruit in de tijd om te zien wat er na tien dagen gebeurt.

## Uitgangspunten

- Exchange Online verzendt en ontvangt; ELSA bewaart. Er blijft geen kopie in Exchange. Een andere mailprovider vervangt alleen de aanvoer.
- Een medewerker heeft tien dagen om zakelijk en persoonlijk te scheiden. Daarna geldt een bericht als zakelijk.
- Persoonlijk betekent: in de map Persoonlijk, versleuteld met een eigen sleutel en buiten het zoekbereik voor de Woo. De medewerker is daarvoor verantwoordelijk.
- Filters mogen niet weggooien, niet naar Persoonlijk verplaatsen en niet doorsturen buiten de aangesloten gemeenten.
- Opname in het adresboek is een persoonlijke keuze.

## Gebruik

Open `index.html` in een browser. Er is geen server nodig. Talen: Nederlands, Duits, Engels en Frans; `#de`, `#en` of `#fr` achter het adres kiest de taal voor die ene link.

## Bouwen

De bron staat in `src/demo.html`, de vertalingen in `i18n/<taal>.json` (sleutel is de Nederlandse tekst).

```
python3 build.py
```

schrijft `index.html` en `ELSA - v<N>.html`. Het versienummer staat in `VERSION`.

## Licentie

EUPL-1.2, zie `LICENSE`.
