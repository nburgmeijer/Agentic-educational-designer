# Agentic Educational Designer

> Disclaimer: output van agents kan onvolledig of onjuist zijn. De gebruiker blijft verantwoordelijk voor inhoudelijke controle, bronverificatie, didactische kwaliteit en de validiteit van alle gebruikte data.

Dit project is een basis om met een agent een onderwijsmodule te ontwikkelen.

## Doel
Deze repository bevat een template-structuur en werkafspraken voor het ontwerpen van lessen binnen een module, inclusief documentatie van bronnen, evaluaties en keuzeverantwoording.

Een voorbeeld van een prompt-uitwisseling tussen gebruiker en agent staat in `voorbeeld_prompts_python_module.md`.

## Voorwaarden
- Git is geïnstalleerd.
- Je werkt in de juiste lokale directory.
- Je gebruikt een Codex-sessie in deze repository.
- Je kunt ook een andere agent gebruiken; geef dan expliciet aan hoe de context is opgebouwd (o.a. structuur, documenten en werkwijze uit `AGENTS.md`).

## Snelstart
1. Clone deze repository.
2. Open deze repository lokaal in je editor.
3. Start een agent-sessie in deze map (bijvoorbeeld Codex).
4. Start de bootstrap met de prompt: `init`.
5. Beantwoord de vragen van de agent (modulenaam en nieuwe remote).
6. De agent stelt de remote in en controleert de uitkomst.
7. Gebruiker en agent doorlopen samen de ontwerpstappen uit `AGENTS.md`.

## Stap-voor-stap
1. Clone repository
```bash
git clone <bron-repository-url>
cd <repo-map>
```

2. Start een agent in deze map (Codex of alternatief)
```bash
codex
```

Gebruik je geen Codex, geef dan aan de agent minimaal:
- dat `AGENTS.md` leidend is;
- hoe de ontwerpcyclus is opgebouwd;
- welke map- en bestandsstructuur gebruikt moet worden.

3. Start bootstrap
Voorbeeld prompt:
```text
init
```

4. Beantwoord de vragen van de agent
Voorbeeld antwoorden:
```text
Modulenaam: <jouw modulenaam>
Remote: <nieuwe-remote-url>
```

5. Agent stelt remote in
Voorbeeld commando dat de agent uitvoert:
```bash
git remote set-url origin <nieuwe-remote-url>
```

6. Controleer remote
```bash
git remote -v
```

## Bootstrapflow (`init`)
Gebruik voor projectstart altijd de prompt:

```text
init
```

Daarna voert de agent deze flow uit:
1. Vraagt de modulenaam.
2. Vraagt de nieuwe remote URL.
3. Verwerkt de modulenaam in de modulecontext.
4. Zet `origin` naar de opgegeven remote.
5. Controleert de ingestelde remote.

Let op:
- Punt 5 uit de projectchecklist (lesnummering concretiseren van `les_XX` naar `les_01`, `les_02`, etc.) wordt geautomatiseerd tijdens het ontwerpproces, niet tijdens bootstrap.

## Verantwoordelijkheden
- Gebruiker:
  - Is verantwoordelijk voor clonen in de juiste directory.
  - Is verantwoordelijk voor het aanleveren van de juiste remote URL.
  - Controleert de uiteindelijke Git-configuratie.
- Agent:
  - Richt de projectdocumenten in volgens `AGENTS.md`.
  - Werkt de module uit via de ontwerpcyclus.
  - Documenteert keuzes, bronnen en evaluaties in de juiste bestanden.

## Ontwerpworkflow
De gebruiker en agent doorlopen de stappen uit `AGENTS.md`:
1. Analyseren
2. Ontwerpen
3. Uitvoeren
4. Evalueren (per les en extra op moduleniveau)
5. Bijstellen

## Belangrijke bestanden
- `AGENTS.md`: afspraken, structuur en werkwijze van de agent.
- `docs/moduleplan.md`: modulecontext en leeruitkomsten.
- `docs/module_overzicht.md`: planningsoverzicht per week/les.
- `docs/lessen/les_XX/`: lesgebonden documenten en materialen.

## Project Aanmaken Checklist
Gebruik deze checklist bij het opzetten van een nieuw project op basis van deze repository.

1. Gebruik de meegeleverde `LICENSE`
- De meegeleverde MIT-licentie geldt voor dit project en voor toekomstige afgeleide projecten, mits de licentietekst wordt meegeleverd.

2. Maak een eerste bootstrap-commit
- Commit minimaal `AGENTS.md`, `README.MD` en de `docs/`-basisstructuur.

3. Controleer Definition of Ready voor de start
- Modulenaam is bekend.
- Doelgroep is bekend.
- Duur van de module is bekend.
- Randvoorwaarden zijn bekend.

4. Concretiseer lesnummering
- Vervang placeholders zoals `les_XX` door echte lesmappen zoals `les_01`, `les_02`, `les_03`.

5. Leg overdracht vast
- Voeg kort toe hoe een andere gebruiker of agent het proces overneemt.
- Verwijs hierbij naar `AGENTS.md`, `README.MD`, `docs/moduleplan.md` en `docs/module_overzicht.md`.
