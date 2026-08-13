# Gemini CLI Project Instructions: German Notes (Obsidian Vault)

Welcome! This repository (`German`) is a structured Obsidian vault containing Marco Di Fresco's personal notes for learning the German language (focused on studies at *Klubschule Migros* and *Sprachschule ILS-Zürich* in Switzerland).

All notes are written in Markdown and designed to be opened as an Obsidian vault. Future AI agents or contributors MUST strictly adhere to the guidelines, conventions, and structures outlined in this document.

---

## 1. Directory Structure & Organization

The repository is organized into distinct logical directories. Keep files sorted in their respective directories:

*   **Root Directory (`/`)**: High-level grammatical concepts, indices, and pronunciation files (e.g., `Adjektive.md`, `Verben.md`, `Vokabular.md`, `Pronomen.md`, `Kasus.md`).
*   **`Grammatik/`**: Notes detailing specific German grammar rules and constructions (e.g., `Bedingungssätze.md`, `Infinitiv mit zu.md`, `Passiv.md`).
*   **`Kasus/`**: Specific deep dives into German grammatical cases (`Akkusativ.md`, `Dativ.md`, `Genitiv.md`, `Nominativ.md`).
*   **`Verben/`**:
    *   `Konjugation/`: Subdirectory containing verb-specific notes. Each file is named after the infinitive capitalized form of the verb (e.g., `Abbrechen.md`, `Kaufen.md`).
    *   `Modi und Typen/`: Conceptual files about verb types and grammatical moods (e.g., `Typ - Regular verben.md`, `Modus - Indikativ.md`).
*   **`Vokabular/`**: Vocabulary notes grouped by thematic semantic domains (e.g., `Essen.md`, `Familie.md`, `Farben.md`, `Schweizer Varianten.md`).
*   **`zzz-Media/`**: Central storage for attachments, images, diagrams, homework files, and PDFs. Never put media files in the content directories.

---

## 2. Formatting & Markdown Conventions

To maintain a consistent presentation and fully leverage Obsidian's features, adhere to the following Markdown patterns:

### Metadata Block (Horizontal Rules)
Every note must start with a metadata block surrounded by triple underscores `___`. It must contain tags starting with `#Languages/German/` and relevant index links.

```markdown
___
Tags: #Languages/German/Grammar
Links: [[Vokabular]]
___
```

*   **Common Tags**:
    *   `#Languages/German/Grammar`
    *   `#Languages/German/Vocabulary`
    *   `#Languages/German/Cases`
    *   `#Languages/German/Grammar/Verbs`
    *   `#Languages/German/Other`

### Internal Obsidian Linking
*   Always use double-bracket Wikilinks for internal references (e.g., `[[Vokabular]]` or `[[Dativ]]`). Do **NOT** use standard Markdown links (`[Vokabular](Vokabular.md)`) for internal files.
*   Use custom link labels when needed by adding a pipe `|` (e.g., `[[Vokabular|Nouns]]`).
*   When renaming a file, you must search and replace all internal Wikilinks pointing to that file across the entire vault to prevent broken links.

### Block References & Transclusions
*   Obsidian block references (indicated by a caret and a unique ID, e.g., `^3ed54c` at the end of a block/paragraph) are used for transclusions (e.g., `![[Typ - Hilfs verben#^3ed54c]]`).
*   **CRITICAL**: Do not remove, edit, or modify any lines containing carets and block IDs (e.g., `^5ef5c7`) in source files, as this will break transclusions in index pages.

---

## 3. Swiss-German Spelling Conventions
Because the user studies in Switzerland, the notes follow **Swiss orthography (Swiss Standard German)**:
*   **No Eszett (`ß`)**: Always use **`ss`** instead of `ß` (e.g., use `Süss` instead of `Süß`, `Gross` instead of `Groß`, `schliessen` instead of `schließen`, and `weiss` instead of `weiß`).
*   Ensure that any new content or corrections follow this convention. Do not "correct" Swiss spelling to German Standard German spelling.

---

## 4. Specific Note Templates

### Vocabulary Notes (`Vokabular/*.md`)
Vocabulary lists should follow a two-column markdown table comparing English on the left and German on the right.

1.  **Nouns**: Always include the definite article (`Der`, `Die`, `Das`) and the plural form in parenthesis using abbreviated suffix rules.
    *   *Examples*: `Der Apfel (Ä-)`, `Das Bier (-e)`, `Die Gurke(-n)`, `Der Kuchen (-)` (no change).
2.  **Verbs**: List with a lowercase infinitive and, if relevant, reference their conjugation file.
3.  **Footnotes**: Use standard markdown footnotes (`[^1]`) at the end of the file for annotations or clarifications.

```markdown
___
Tags: #Languages/German/Vocabulary
Links: [[Vokabular]]
___

English | German
------------ | ------------
Apple | Der Apfel (Ä-)
Butter | Die Butter
To buy | [[Kaufen]]
```

### Verb Conjugation Notes (`Verben/Konjugation/*.md`)
Verb files must follow a strict, comprehensive sequence of headings representing different moods and tenses. The title must be the capitalized infinitive verb.

```markdown
___
Links: [[Verben]] [[Typ - Regular verben]]
Meaning: to buy
___

# [[Modus - Indikativ]] - Präsens
ich kaufe
du kaufst
...

# [[Modus - Indikativ]] - Präteritum
...

# [[Modus - Indikativ]] - Perfekt
[[Pronomen]] + [[Haben]] + gekauft
ich habe gekauft
...

# [[Modus - Indikativ]] - Plusquamperfekt
...

# [[Modus - Indikativ]] - Futur I
...

# [[Modus - Indikativ]] - Futur II
...

# [[Modus - Konjunktiv]] 1 - Präsens
...

# [[Modus - Konjunktiv]] 1 - Perfekt
...

# [[Modus - Konjunktiv]] 1 - Futur I
...

# [[Modus - Konjunktiv]] 1 - Futur II
...

# [[Modus - Konjunktiv]] 2 - Präteritum
...

# [[Modus - Konjunktiv]] 2 - Futur I
...

# [[Modus - Konjunktiv]] 2 - Futur II
...

# [[Modus - Konjunktiv]] 2 - Plusquamperfekt
...

# [[Modus - Imperativ]] - Präsens
...

# [[Modus - Partizips]] - Präsens
...

# [[Modus - Partizips]] - Perfekt
...
```

---

## 5. Guidelines for AI Agents

1.  **Do Not Invent Files**: If you need to link to a concept, make sure it exists, or create it if requested. Do not create orphaned red links in Obsidian unless intentionally adding missing vocabulary/concepts.
2.  **No Explanatory Markdown Comments**: Never leave hidden HTML/Markdown comments explaining your edits or communicating with the user inside the notes themselves. Communication must remain strictly within the CLI chat.
3.  **Preserve Table Layouts**: Use tidy, readable markdown tables with balanced columns using hyphens and pipe alignments.
4.  **Swiss Context**: Keep `Vokabular/Schweizer Varianten.md` updated if Swiss-specific vocabulary comes up during lessons.
