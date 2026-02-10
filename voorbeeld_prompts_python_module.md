# Voorbeeld Prompts: Python Module (Gebruiker ↔ Agent)

Dit bestand simuleert een volledige interactie tussen gebruiker en agent voor het ontwerpen van een Python-module volgens de afspraken in `AGENTS.md`.

## Simulatie

**Gebruiker:**
```text
Lees eerst AGENTS.md volledig.
Start daarna de bootstrapflow.
Stel de bootstrapvragen één voor één en wacht steeds op antwoord.
Begin nu met vraag 1: modulenaam.
```

**Agent:**
```text
Wat is de modulenaam?
```

**Gebruiker:**
```text
Python Fundamentals voor Software Developers
```

**Agent:**
```text
Ik verwerk de modulenaam in de modulecontext en start daarna stap 1 van de ontwerpcyclus.
```

**Gebruiker:**
```text
Start ontwerpcyclus stap 1 (Analyseren). Stel de vragen voor modulecontext en leeruitkomsten.
```

**Agent:**
```text
Wat is de exacte naam van de module?
```

**Gebruiker:**
```text
Python Fundamentals voor Software Developers
```

**Agent:**
```text
Voor welke opleiding en welk niveau is de module bedoeld?
```

**Gebruiker:**
```text
MBO-4 Software Developer, jaar 2
```

**Agent:**
```text
Hoeveel weken duurt de module en hoeveel lesuren zijn er per week?
```

**Gebruiker:**
```text
2 weken, 1 les per week van 4 x 45 minuten
```

**Agent:**
```text
Wat is de startsituatie van de studenten (voorkennis, groepsgrootte, aandachtspunten)?
```

**Gebruiker:**
```text
15 studenten, basis in algoritmisch denken, weinig programmeerervaring in Python
```

**Agent:**
```text
Welke praktische randvoorwaarden gelden (software, lokalen, materialen, beleid)?
```

**Gebruiker:**
```text
Laptop per student, VS Code, Python 3.12, internettoegang
```

**Agent:**
```text
Noem 3-8 leeruitkomsten in de vorm: Na afloop kan de student [gedrag] in [context] met [kwaliteitseis].
```

**Gebruiker:**
```text
- Na afloop kan de student variabelen, datatypen en basisoperatoren correct toepassen in kleine Python-scripts met maximaal 1 syntaxfout per script.
- Na afloop kan de student beslisstructuren en lussen gebruiken om een probleemstap uit te werken in een script dat functioneel correct draait.
- Na afloop kan de student functies definiëren en aanroepen in een praktische opdracht met duidelijke input/output-structuur.
```

**Gebruiker:**
```text
Ik lever extra bronnen aan voor de module:
- https://docs.python.org/3/tutorial/
- https://realpython.com/python-basics/
Verwerk deze in docs/bronnen.md en verwijs per les naar relevante bronnen.
```

**Agent:**
```text
Ik verwerk de bronnen in docs/bronnen.md en koppel ze aan les_01 en les_02 in bronnen_les_XX.md.
```

**Gebruiker:**
```text
Ga naar stap 2 (Ontwerpen). Ontwerp 2 lessen. Les 1 krijgt 1 opdracht. Les 2 krijgt 2 opdrachten. Maak en vul de lesdocumenten, presentatiebestanden en opdrachtbestanden aan.
```

**Agent:**
```text
Ik ontwerp nu:
- les_01 met 1 opdracht
- les_02 met 2 opdrachten
Ik werk per les bij:
- les_XX.md
- presentatie_slides.md
- opdracht_[nummer_en_titel]_les_XX.md
- bronnen_les_XX.md
- keuzeverantwoording_les_XX.md
```

**Gebruiker:**
```text
Werk les 1 uit met focus op variabelen, input/output en if-else. Maak 1 groepsopdracht met A3-werkblad.
```

**Agent:**
```text
Les 1 uitgewerkt.
Opdracht les 1:
- opdracht_01_python_basics_checker_les_01.md
A3-werkblad toegevoegd voor groepsopdracht met opdrachtomschrijving en invulruimte.
Presentatie bevat: titel, check-in, agenda, inhoud, afsluiting/terugblik.
```

**Gebruiker:**
```text
Ik lever 2 afbeeldingen aan voor les 1:
- assets/python_datatypes_overzicht.png
- assets/if_else_flowchart.png
Neem ze op in presentatie_slides.md en koppel ze aan de juiste inhoudslides.
```

**Agent:**
```text
Ik verwerk beide afbeeldingen in docs/lessen/les_01/presentatie_slides.md met slideverwijzingen en korte toelichting.
```

**Gebruiker:**
```text
Werk les 2 uit met focus op lussen en functies. Voeg 2 opdrachten toe: 1 individuele en 1 groepsopdracht.
```

**Agent:**
```text
Les 2 uitgewerkt.
Opdrachten les 2:
- opdracht_01_lussen_oefencasus_les_02.md (individueel)
- opdracht_02_functies_miniproject_les_02.md (groep)
Presentatie en bron-/keuzeverantwoording bijgewerkt.
```

**Gebruiker:**
```text
Maak de opdrachten niet alleen als markdown, maar ook als Word-documenten voor uitdeling in de klas.
```

**Agent:**
```text
Ik maak voor elke opdracht een Word-versie en sla die op in de lesmap onder materialen/opdrachten/:
- opdracht_01_python_basics_checker_les_01.docx
- opdracht_01_lussen_oefencasus_les_02.docx
- opdracht_02_functies_miniproject_les_02.docx
De markdownversies blijven leidend voor versiebeheer.
```

**Gebruiker:**
```text
Ik lever bestaand lesmateriaal aan:
- input/bestaand_materiaal/python_intro_slides_2024.pdf
- input/bestaand_materiaal/werkblad_debugging.docx
Hergebruik wat passend is en noteer wat je overneemt in keuzeverantwoording en bronnen.
```

**Agent:**
```text
Ik analyseer het bestaande materiaal, hergebruik relevante onderdelen voor les 1 en les 2, en leg dit vast in:
- bronnen_les_01.md en bronnen_les_02.md
- keuzeverantwoording_les_01.md en keuzeverantwoording_les_02.md
```

**Gebruiker:**
```text
Ik lever ook een rubric aan:
- input/rubrics/rubric_python_opdrachten_v1.xlsx
Koppel deze aan de opdrachten en neem beoordelingscriteria op in de opdrachtbestanden.
```

**Agent:**
```text
Ik verwerk de rubriccriteria in:
- opdracht_01_python_basics_checker_les_01.md
- opdracht_01_lussen_oefencasus_les_02.md
- opdracht_02_functies_miniproject_les_02.md
en verwijs naar de rubric in toetsing en bronvermelding.
```

**Gebruiker:**
```text
Ga naar stap 3 (Uitvoeren). Simuleer uitvoeringsnotities per les.
```

**Agent:**
```text
Ik vul nu per les uitvoeringsnotities aan in les_XX.md en start de eerste evaluatie in evaluatie_les_XX.md.
```

**Gebruiker:**
```text
Ik lever ingevulde lesevaluatieformulieren aan:
- input/evaluaties/les_01_formulier.csv
- input/evaluaties/les_02_formulier.csv
Verwerk de samenvatting in evaluatie_les_01.md, evaluatie_les_02.md en module_evaluatie.md.
```

**Agent:**
```text
Ik verwerk de evaluatiegegevens per les en voeg een modulebrede samenvatting toe in docs/evaluatie/module_evaluatie.md.
```

**Gebruiker:**
```text
Ga naar stap 4 (Evalueren). Verwerk feedback per les en voer ook module-evaluatie uit.
```

**Agent:**
```text
Ik werk bij:
- docs/lessen/les_01/evaluatie_les_01.md
- docs/lessen/les_02/evaluatie_les_02.md
- docs/evaluatie/module_evaluatie.md
Daarnaast actualiseer ik keuzeverantwoording en materialen op basis van de evaluatie.
```

**Gebruiker:**
```text
Ga naar stap 5 (Bijstellen). Verwerk verbeteringen in lesopbouw en planningsoverzicht.
```

**Agent:**
```text
Bijstelling uitgevoerd in:
- docs/module_overzicht.md
- docs/lessen/les_01/les_01.md
- docs/lessen/les_02/les_02.md
- docs/lessen/les_01/presentatie_slides.md
- docs/lessen/les_02/presentatie_slides.md
```

**Gebruiker:**
```text
Rond af met een korte status: wat is gereed en wat staat nog open?
```

**Agent:**
```text
Gereed:
- Modulecontext en leeruitkomsten
- 2 lessen ontworpen
- Les 1 met 1 opdracht
- Les 2 met 2 opdrachten
- Presentatiestructuren per les
- Lesbronnen, evaluaties en keuzeverantwoording per les
- Module-evaluatie en bijstelling verwerkt

Open:
- Eventuele fine-tuning van toetscriteria na eerste echte uitvoering
```

## Gebruik
Gebruik deze prompts als startpunt en vervang de inhoud met je eigen modulecontext.
