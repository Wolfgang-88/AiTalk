# AiTalk – OpenRouter Anleitung / Guide

*API-Key und Modell einrichten · Setting up your API key and model · Deutsch & English*

## Deutsch

### 1. API-Key bei OpenRouter erstellen

1. Öffne https://openrouter.ai und melde dich an. Hast du noch kein Konto, lege zuerst eins an.
2. Öffne die Seite für API-Keys: https://openrouter.ai/settings/keys (alternativ https://openrouter.ai/keys).
3. Klicke auf **Create Key** (je nach Ansicht auch **Create API Key**).
4. Gib dem Key einen Namen, zum Beispiel „AiTalk“. Optional kannst du ein Guthaben-Limit (Credit limit) und ein Ablaufdatum festlegen. Das schützt dich vor unerwartet hohen Kosten.
5. Klicke auf **Create**. Der neue Key beginnt mit `sk-or-`.
6. **Kopiere den Key sofort** und speichere ihn sicher. Er wird nur einmal vollständig angezeigt. Geht er verloren, erstellst du einfach einen neuen.

**Guthaben:** Kostenpflichtige Modelle brauchen Guthaben auf deinem OpenRouter-Konto (Bereich „Credits“). Kostenlose Modelle, erkennbar an `:free` am Ende der Modell-ID, funktionieren ohne Guthaben, haben aber strengere Limits und sind oft überlastet (Fehler HTTP 429).

### 2. API-Key in AiTalk eintragen

1. Starte AiTalk und klicke oben links auf **Optionen**.
2. Füge den Key mit Strg+V in das Feld **OpenRouter API-Key** ein. Mit **Key anzeigen** kannst du prüfen, ob er vollständig und ohne Leerzeichen eingefügt wurde.
3. Klicke auf **Speichern**. Der Key wird in der Datei `AiTalk.json` im Installationsordner gespeichert.

### 3. Ein Modell auswählen und eintragen

1. Öffne die Modellliste: https://openrouter.ai/models
2. Suche ein Modell oder stöbere in der Liste. Trage "free" in das Suchfenster ein.
3. Klicke das gewünschte Modell an und kopiere seine **Modell-ID**. Sie hat das Format `anbieter/modellname`.
4. Öffne in AiTalk wieder **Optionen** und füge die ID in das Feld **KI-Modell** ein.
5. Klicke auf **Speichern**. Ab der nächsten Nachricht nutzt AiTalk das neue Modell.

Wichtig: Schreibe die Modell-ID **genau** so, wie sie auf OpenRouter steht, auch mit Zusätzen wie `:free`.

Beispiele für Modell-IDs:

- `openrouter/auto` – OpenRouter wählt automatisch ein passendes Modell
- `cohere/north-mini-code:free` – günstiges, schnelles Modell
- `anthropic/claude-sonnet-4.5` – leistungsstarkes Modell

Modelle und Preise ändern sich. Prüfe deshalb auf https://openrouter.ai/models, welche Modelle aktuell verfügbar sind.

### 4. Häufige Fehler

- **HTTP 401 / Invalid API key:** Der Key ist falsch kopiert, enthält Leerzeichen oder wurde bei OpenRouter gelöscht. Erstelle bei Bedarf einen neuen Key.
- **HTTP 402:** Das Guthaben ist aufgebraucht. Lade Credits in deinem OpenRouter-Konto auf oder wähle ein `:free`-Modell.
- **HTTP 404 / Modell nicht gefunden:** Die Modell-ID ist falsch geschrieben oder das Modell gibt es nicht mehr. Kopiere die ID erneut von https://openrouter.ai/models.
- **HTTP 429:** Das Modell ist überlastet oder dein Limit ist erreicht. Warte kurz oder wähle ein anderes Modell.

### 5. Sicherheit

Dein API-Key gehört nur dir. Er steht in `AiTalk.json` im Klartext. Gib diese Datei nicht weiter und veröffentliche sie nicht. Wurde der Key doch einmal weitergegeben, lösche ihn auf OpenRouter und erstelle einen neuen.

## English

### 1. Create an API key on OpenRouter

1. Go to https://openrouter.ai and sign in. If you do not have an account yet, create one first.
2. Open the API keys page: https://openrouter.ai/settings/keys (or https://openrouter.ai/keys).
3. Click **Create Key** (depending on the view it may read **Create API Key**).
4. Give the key a name, for example “AiTalk”. Optionally set a credit limit and an expiration date. This protects you from unexpectedly high costs.
5. Click **Create**. The new key starts with `sk-or-`.
6. **Copy the key immediately** and store it safely. It is shown in full only once. If you lose it, simply create a new one.

**Credits:** Paid models need credits on your OpenRouter account (the “Credits” section). Free models, recognizable by `:free` at the end of the model ID, work without credits but have stricter limits and are often overloaded (error HTTP 429).

### 2. Enter the API key in AiTalk

1. Start AiTalk and click **Options** at the top left.
2. Paste the key with Ctrl+V into the **OpenRouter API key** field. Use **Show key** to check that it was pasted completely and without spaces.
3. Click **Save**. The key is stored in the file `AiTalk.json` in the installation folder.

### 3. Choose and enter a model

1. Open the model list: https://openrouter.ai/models
2. Search for a model or browse the list. Enter "free" into the search box.
3. Click the model you want and copy its **model ID**. It has the format `provider/modelname`.
4. Open **Options** in AiTalk again and paste the ID into the **AI model** field.
5. Click **Save**. From the next message on, AiTalk uses the new model.

Important: Write the model ID **exactly** as it appears on OpenRouter, including suffixes such as `:free`.

Examples of model IDs:

- `openrouter/auto` – OpenRouter automatically picks a suitable model
- `cohere/north-mini-code:free` – inexpensive, fast model
- `anthropic/claude-sonnet-4.5` – powerful model

Models and prices change. Check https://openrouter.ai/models to see which models are currently available.

### 4. Common errors

- **HTTP 401 / Invalid API key:** The key was copied incorrectly, contains spaces, or was deleted on OpenRouter. Create a new key if needed.
- **HTTP 402:** Your credits have run out. Add credits to your OpenRouter account or choose a `:free` model.
- **HTTP 404 / model not found:** The model ID is misspelled or the model no longer exists. Copy the ID again from https://openrouter.ai/models.
- **HTTP 429:** The model is overloaded or you reached a limit. Wait a moment or choose a different model.

### 5. Security

Your API key belongs to you alone. It is stored in plain text in `AiTalk.json`. Do not share or publish this file. If the key was ever shared by accident, delete it on OpenRouter and create a new one.
