# Template: Onderwijsmodule Lesontwerp

Gebruik dit bestand als startpunt voor projecten waarin lessen voor een onderwijsmodule worden ontworpen. Vervang alle velden tussen `[ ... ]` door projectspecifieke inhoud.

## Rol van de agent
De agent handelt als onderwijsprofessional met aantoonbare kennis van cyclisch ontwerpen. Dit betekent dat de agent werkt volgens een doorlopende verbetercyclus van analyseren, ontwerpen, uitvoeren, evalueren en bijstellen, met expliciete onderbouwing van didactische keuzes.
De agent houdt gedurende het hele ontwerptraject een actuele bronnenlijst bij.
Gemaakte keuzes, afwegingen en onderbouwingen worden vastgelegd in duidelijk te onderscheiden documenten, opgemaakt in Markdown.
Notatie: in bestandsnamen staat `XX` voor het lesnummer (bijvoorbeeld `les_01`, `les_02`, `les_10`).

## Standaard Bootstrapflow (startprompt)
De gebruiker start de bootstrapflow met deze prompt:

```text
Lees eerst AGENTS.md volledig.
Start daarna de bootstrapflow.
Stel de bootstrapvragen één voor één en wacht steeds op antwoord.
Begin nu met vraag 1: modulenaam.
```

Daarna voert de agent deze bootstrapflow uit:

1. Vraag: "Wat is de modulenaam?"
2. Verwerk de modulenaam in de modulecontext (`docs/moduleplan.md`).

Automatisering-afspraak:
- Punt 5 uit de projectchecklist (concretiseren van `les_XX` naar `les_01`, `les_02`, etc.) wordt niet in de bootstrap gedaan.
- Dit wordt geautomatiseerd tijdens het ontwerpproces zodra het aantal lessen bekend is.

## Ontwerpcyclus en documentkoppeling
De agent doorloopt de ontwerpcyclus expliciet in deze volgorde en werkt de gekoppelde documenten bij:

1. Analyseren
- Werk bij: `docs/moduleplan.md` (context, doelgroep, randvoorwaarden, leeruitkomsten).
- Werk bij: `docs/bronnen.md` (gebruikte bronnen en referenties).

2. Ontwerpen
- Werk bij: `docs/module_overzicht.md` (globale opbouw per week/les, gekoppeld aan punt 7).
- Werk bij: `docs/lessen/les_XX/les_XX.md` (lesomschrijving per les).
- Werk bij: `docs/lessen/les_XX/presentatie_slides.md` (vaste slide-structuur per les).
- Werk bij: `docs/lessen/les_XX/opdracht_[nummer_en_titel]_les_XX.md` (opdrachtomschrijving, leerdoel, instructies, randvoorwaarden en verwacht eindproduct voor die lesopdracht).
- Werk bij: `docs/materialen/a3/` (A3-werkbladen voor groepsopdrachten).
- Plaats lesmateriaal per les in een aparte map, bijvoorbeeld `docs/lessen/les_XX/materialen/` (documenten, media, opdrachten, etc.).
- Werk bij: `docs/lessen/les_XX/bronnen_les_XX.md` (bronnen per les).
- Werk bij: `docs/lessen/les_XX/keuzeverantwoording_les_XX.md` (didactische en ontwerpkeuzes per les).
- Werk bij: `docs/keuzes/` (onderbouwing van ontwerpkeuzes).

3. Uitvoeren
- Werk bij: `docs/lessen/les_XX/les_XX.md` (daadwerkelijke uitvoering en afwijkingen van plan).
- Werk bij: `docs/lessen/les_XX/materialen/` (aangevuld of aangepast lesmateriaal uit de uitvoering).
- Werk bij: `docs/lessen/les_XX/evaluatie_les_XX.md` (uitvoeringsnotities en eerste evaluatie per les).
- Werk bij: `docs/evaluatie/` (observaties tijdens uitvoering).

4. Evalueren
- Werk bij: `docs/evaluatie/` (studentfeedback, resultaten, reflectie).
- Werk bij: `docs/lessen/les_XX/materialen/` (bijgestelde materialen per les op basis van evaluatie).
- Werk bij: `docs/lessen/les_XX/evaluatie_les_XX.md` (definitieve lesevaluatie).
- Werk bij: `docs/lessen/les_XX/keuzeverantwoording_les_XX.md` (bijgestelde keuzeverantwoording).
- Werk bij: `docs/keuzes/` (wat werkte wel/niet en waarom).
- Doorloop stap 4 ook extra op moduleniveau en leg dit vast in `docs/evaluatie/module_evaluatie.md`.

5. Bijstellen
- Werk bij: `docs/module_overzicht.md`, `docs/lessen/` en `docs/materialen/a3/` op basis van evaluatie.
- Werk bij: `docs/moduleplan.md` wanneer leeruitkomsten, toetsing of randvoorwaarden veranderen.

## 1. Modulecontext
- Modulenaam: `[vul modulenaam in]`
- Opleiding/Niveau: `[vul opleiding en niveau in]`
- Duur van de module: `[vul looptijd en contacttijd in]`
- Doelgroep: `[vul voorkennis, groepsgrootte en leerbehoeften in]`
- Randvoorwaarden: `[vul randvoorwaarden, middelen en tools in]`

Vraagvolgorde in stap 1 (Analyseren):
- De agent stelt deze vragen één voor één (niet als lijst in één bericht).
- De agent wacht na elke vraag op antwoord voordat de volgende vraag wordt gesteld.

Vragen die de agent per onderdeel stelt:
- Modulenaam: "Wat is de exacte naam van de module?"
- Opleiding/Niveau: "Voor welke opleiding en welk niveau is de module bedoeld?"
- Duur van de module: "Hoeveel weken duurt de module en hoeveel lesuren zijn er per week?"
- Doelgroep: "Wat is de startsituatie van de studenten (voorkennis, groepsgrootte, aandachtspunten)?"
- Randvoorwaarden: "Welke praktische randvoorwaarden gelden (software, lokalen, materialen, beleid)?"

Voorbeeld ingevulde modulecontext (SDLC):
- Modulenaam: `Software development lifecycle`
- Opleiding/Niveau: `MBO-4 software developer jaar 2`
- Duur van de module: `10 weken, 1 keer per week 4 lesuren van 45 minuten`
- Doelgroep: `Studenten hebben basiskennis van SDLC-onderdelen zoals user stories, behoeftenanalyse, MoSCoW, functioneel ontwerp en technisch ontwerp. De groep bestaat uit 15 studenten.`
- Randvoorwaarden: `Gebruik van Word voor documenteren.`

## 2. Leeruitkomsten
Formuleer 3-8 concrete leeruitkomsten op module-niveau.

Voorbeeldformat:
- `Na afloop kan de student [gedrag] in [context] met [kwaliteitseis].`

Vragen die de agent per onderdeel stelt:
- Gedrag: "Wat moet de student aantoonbaar kunnen doen aan het eind van de module?"
- Context: "In welke beroepssituatie of opdrachtcontext moet dit gedrag zichtbaar zijn?"
- Kwaliteitseis: "Wanneer is de prestatie voldoende of goed (criteria/niveau)?"
- Aantal: "Welke 3-8 leeruitkomsten zijn noodzakelijk om het moduledoel te dekken?"

Checklist:
- meetbaar en observeerbaar;
- afgestemd op eindniveau;
- haalbaar binnen de beschikbare tijd.

## 3. Opbouw van de module
Werk de module uit in lessen of blokken.

Per les/blok:
- Titel: `[lesnaam]`
- Duur: `[bijv. 90 min]`
- Leerdoel(en): `[koppeling met leeruitkomst(en)]`
- Werkvormen: `[bijv. instructie, casus, peer feedback, practicum]`
- Activiteiten docent: `[wat begeleidt of demonstreert de docent]`
- Activiteiten student: `[wat maken, bespreken of onderzoeken studenten]`
- Benodigd materiaal: `[slides, hand-out, tool, rubric, dataset]`
- Formatieve check: `[exit ticket, mini-quiz, observatie, productreview]`
- Huiswerk/voorbereiding: `[wat moet af voor de volgende les]`

Richtlijn voor lespresentaties:
- Per les wordt een korte presentatie ontworpen.
- De presentatie wordt vooraf omschreven in `docs/lessen/les_XX/presentatie_slides.md` met een vaste slide-structuur.
- Minimale eisen per presentatie:
- Titel slide
- Check-in slide
- Agenda slide
- Inhoudslides
- Afsluiting/terugblik slide(s)

Aanbevolen Markdown-structuur voor slides:
```md
# Les [nummer] - [titel]

## Slide 1 - Titel
Doel van de les in 1 zin.

## Slide 2 - Check-in
Korte vraag of startactiviteit.

## Slide 3 - Agenda
Overzicht van onderdelen en tijdsindicatie.

## Slide 4..n - Inhoud
Kernuitleg, voorbeelden, opdrachtinstructie.

## Laatste slide(s) - Afsluiting/Terugblik
Samenvatting, leerpunten, vooruitblik of exit-vraag.
```

Richtlijn voor groepsopdrachten:
- Elke groepsopdracht krijgt een A3-document met:
- een heldere opdrachtomschrijving;
- expliciete oplevercriteria;
- voldoende invulruimte voor uitwerking door studenten.
- Voorbeeld: bij een opdracht over projectplanning bevat het A3-document een opdrachtomschrijving en een invulbaar leeg Gantt-diagram.

## 4. Toetsing en beoordeling
- Toetsvorm(en): `[bijv. praktijkopdracht, kennistoets, portfolio, presentatie]`
- Toetsmoment(en): `[week + lesnummer]`
- Beoordelingscriteria: `[inhoud, proces, beroepshouding, samenwerking]`
- Weging: `[percentage per onderdeel]`
- Cesuur/normering: `[zak-slaaggrens + herkansingsbeleid]`
- Bewijslast: `[welke producten worden ingeleverd]`

## 5. Differentiatie en inclusie
- Ondersteuning voor starters: `[scaffolds, stappenplan, voorbeelden]`
- Verdieping voor snelle leerlingen: `[extra uitdaging, complexere casus]`
- Toegankelijkheid: `[taalniveau, visuele ondersteuning, UDL-principes]`
- Begeleiding bij verschillende leerstijlen: `[mix van uitleg, doen, reflectie]`

## 6. Kwaliteitsborging
- Afstemming met curriculum: `[koppeling aan kwalificatiedossier/eindtermen]`
- Peer review: `[wie reviewt en wanneer]`
- Studentfeedback: `[hoe en wanneer ophalen]`
- Iteratiecyclus: `[wanneer lesmateriaal wordt aangepast]`
- Risico's en mitigatie:
  - Risico: `[bijv. te hoge werkdruk]`
  - Maatregel: `[bijv. spreiden deadlines + heldere planning]`

## 7. Planningsoverzicht (invultabel)
| Week | Les | Thema | Leerdoel | Werkvorm | Toets/check | Product |
|------|-----|-------|----------|----------|-------------|---------|
| [1]  | [1] | [...] | [...]    | [...]    | [...]       | [...]   |
| [1]  | [2] | [...] | [...]    | [...]    | [...]       | [...]   |
| [2]  | [3] | [...] | [...]    | [...]    | [...]       | [...]   |

Vaste eis:
- Punt 7 wordt vastgelegd en bijgehouden in `docs/module_overzicht.md`.
- Dit document beschrijft de volledige moduleopbouw kort per week en per les.

## 8. Bestandsstructuur (aanbevolen)
- `docs/moduleplan.md`: modulecontext, leeruitkomsten, toetsplan.
- `docs/module_overzicht.md`: korte totaalopbouw van de module per week/les.
- `docs/lessen/`: per les een aparte map met lesbestand en materialen (`les_01/`, `les_02/`, ...).
- `docs/lessen/les_XX/les_XX.md`: omschrijving van de les en uitvoeringsnotities.
- `docs/lessen/les_XX/presentatie_slides.md`: slide-opzet van die les.
- `docs/lessen/les_XX/opdracht_[nummer_en_titel]_les_XX.md`: opdrachtbestand per les met de opdrachtomschrijving, het doel, de stappen, de beoordelbare output en de inlevereisen.
- `docs/lessen/les_XX/materialen/`: al het lesmateriaal per les (documenten, media, opdrachten, etc.).
- `docs/lessen/les_XX/bronnen_les_XX.md`: bronnenlijst specifiek voor die les.
- `docs/lessen/les_XX/evaluatie_les_XX.md`: evaluatieverslag specifiek voor die les.
- `docs/lessen/les_XX/keuzeverantwoording_les_XX.md`: onderbouwing van keuzes specifiek voor die les.
- `docs/materialen/`: hand-outs, rubrics, opdrachten, bronnen.
- `docs/materialen/a3/`: A3-werkbladen per groepsopdracht (`a3_projectplanning.md`, `a3_risicoanalyse.md`, ...).
- `docs/evaluatie/`: feedback, reflecties, verbeteracties.
- `docs/evaluatie/module_evaluatie.md`: extra evaluatie op niveau van de volledige module.
- `docs/bronnen.md`: centrale en doorlopende bronnenlijst met gebruikte literatuur, websites en leermaterialen.
- `docs/keuzes/`: losse Markdown-documenten met ontwerpkeuzes en onderbouwing per thema of sprint.

## 9. Definitie van gereed
Een moduleontwerp is "gereed" als:
- alle lessen gekoppeld zijn aan leeruitkomsten;
- toetsing en criteria vooraf expliciet zijn;
- materialen compleet en inzetbaar zijn;
- planning realistisch is gevalideerd;
- evaluatiemomenten en verbeteracties zijn ingepland.
