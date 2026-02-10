# VS Code Handleiding (kort)

Deze korte handleiding helpt je om dit project in VS Code te gebruiken, inclusief het lezen van Markdown-bestanden en het werken met een agent.

## 1. Project openen in VS Code
1. Open VS Code.
2. Kies `File` -> `Open Folder...`.
3. Selecteer de projectmap.

## 2. Markdown-bestanden lezen
Belangrijke bestanden:
- `README.MD`
- `AGENTS.md`
- `voorbeeld_prompts_python_module.md`
- `docs/moduleplan.md`
- `docs/module_overzicht.md`

Handige functies in VS Code:
- Open preview: `Cmd+Shift+V` (macOS) of `Ctrl+Shift+V` (Windows/Linux).
- Open preview naast editor: `Cmd+K V` of `Ctrl+K V`.
- Zoek in project: `Cmd+Shift+F` of `Ctrl+Shift+F`.

## 3. Agent gebruiken in VS Code
Je kunt een agent gebruiken via:
- de terminal;
- een VS Code-extensie/plugin voor een specifieke agent.

Basisstappen:
1. Open de geïntegreerde terminal (`Terminal` -> `New Terminal`).
2. Start je agent in de projectmap.
3. Geef eerst de startprompt uit `README.MD`.
4. Laat de agent daarna de vragen één voor één stellen en beantwoord deze.

Alternatief via extensies:
1. Open `Extensions` in VS Code.
2. Installeer een extensie voor de agent die je gebruikt.
3. Open de agent-chat/paneel van die extensie in deze projectmap.
4. Geef dezelfde startprompt uit `README.MD` en volg daarna de bootstrapvragen.

## 4. Praktische werkwijze
1. Lees `README.MD`.
2. Start de bootstrapflow met de startprompt.
3. Werk vanuit `AGENTS.md` door de ontwerpcyclus.
4. Gebruik `voorbeeld_prompts_python_module.md` als referentie voor promptstijl.

## 5. Tip
Gebruik split view:
- links `AGENTS.md`
- rechts het document dat je invult (bijv. `docs/moduleplan.md`)

Zo kun je sneller controleren of de agent de juiste structuur volgt.
