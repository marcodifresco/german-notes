# Agent Guide: German Notes (Obsidian Vault)

Welcome! This repository (`German`) is a structured personal Obsidian vault containing German language learning notes by Marco Di Fresco. The notes support his German studies (B1–B2 level) at *Klubschule Migros* and *Sprachschule ILS-Zürich* in Switzerland, using course materials such as *Schritte plus Neu 5 (Schweiz)* Kursbuch (kb) and Arbeitsbuch (AB).

All notes are written in Markdown and designed to be opened as an Obsidian vault. Any AI model or agent interacting with this repository MUST strictly follow the architecture, formatting conventions, linguistic standards, and operational recipes detailed below.

---

## 1. Vault Architecture & Directory Taxonomy

The repository follows a clean, modular structure. Every file has an exact home:

```
German/
├── Agents.md                                # This agent instruction manual
├── README.md                                # Public repository overview
├── LICENSE.md                               # Project license
├── AAA TEMPORARY NOTE.md                    # Live scratchpad used during classes
│
├── [Root Index & Reference Notes]
│   ├── Adjektive.md                         # Adjective declension tables and adjective vocab
│   ├── Adverbien und Präpositionen.md       # Prepositions, cases governed, adverbs, time/location rules
│   ├── Aussprache.md                        # Pronunciation guide (diphthongs, sounds)
│   ├── Kasus.md                             # High-level overview of the four German cases
│   ├── Pronomen.md                          # Personal, possessive, reflexive pronouns
│   ├── Umlaut.md                            # Umlaut reference & keyboard shortcuts
│   ├── Verben.md                            # Central verb index (transcludes verb type summaries)
│   └── Vokabular.md                         # Master vocabulary index and general word list
│
├── Grammatik/                               # Deep dives into specific grammatical constructions
│   ├── Bedingungssätze.md                   # Conditional clauses (wenn, falls, Konjunktiv II)
│   ├── Befehl.md                            # Imperatives and sentence position rules
│   ├── Direct - Indirect.md                 # Direct vs. indirect questions & speech
│   ├── Gegensatzklausel.md                  # Adversative clauses (aber, trotzdem, obwohl, nicht nur... sondern auch)
│   ├── Grammatischer Vokabular.md           # Grammatical terminology (Substantiv, Adverb, Satz, etc.)
│   ├── Infinitiv mit zu.md                  # Infinitive clauses with "zu" (rules, exceptions)
│   ├── Kausalsätze.md                       # Causal clauses (weil, da, denn, nämlich, zumal)
│   ├── Komparation.md                       # Comparative and superlative forms
│   ├── Passiv.md                            # Passive voice (Vorgangspassiv & Zustandspassiv)
│   ├── Relativsätzen.md                     # Relative clauses and relative pronouns
│   ├── Wann - Wenn - Als.md                 # Temporal conjunction rules (wann vs. wenn vs. als)
│   └── Wo.md                                # Direction vs. location prepositions (wo vs. wohin vs. woher)
│
├── Kasus/                                   # Dedicated deep-dives for each grammatical case
│   ├── Nominativ.md                         # Subject case, declensions, rules
│   ├── Akkusativ.md                         # Direct object case, motion prepositions, declensions
│   ├── Dativ.md                             # Indirect object case, static prepositions, declensions
│   └── Genitiv.md                           # Possession case, genitive prepositions, declensions
│
├── Verben/
│   ├── Konjugation/                         # Individual conjugation files (over 100+ verbs)
│   │   └── <Verb>.md                        # Capitalized infinitive name (e.g., Kaufen.md, Schliessen.md)
│   │
│   └── Modi und Typen/                      # Conceptual notes on grammatical moods & verb categories
│       ├── Modus - Indikativ.md             # Indicative mood tenses and usage
│       ├── Modus - Konjunktiv.md            # Subjunctive I and II usage, forms, and rules
│       ├── Modus - Imperativ.md             # Imperative forms and rules
│       ├── Modus - Partizips.md             # Partizip I and II forms and usage
│       ├── Typ - Hilfs verben.md            # Auxiliary verbs (sein, haben, werden) + block ref ^3ed54c
│       ├── Typ - Modal verben.md            # Modal verbs (können, müssen, etc.) + block ref ^530533
│       ├── Typ - Regular verben.md          # Regular verbs table + block ref ^5ef5c7
│       ├── Typ - Irregular verben.md        # Irregular verbs overview + block ref ^5057b3
│       ├── Typ - Reflexive Verben.md        # Reflexive verbs list and pronoun usage
│       └── Typ - Trennbare verben.md        # Separable verbs table + block ref ^ba9865
│
├── Vokabular/                               # Thematic semantic vocabulary files
│   ├── Arbeitsplatz.md                      # Workplace, professions, and career terms
│   ├── Essen.md                             # Food, beverages, groceries, cooking
│   ├── Familie.md                           # Family members, relationships
│   ├── Farben.md                            # Colors
│   ├── Gängige Redewendungen.md             # Common everyday idioms, expressions, and phrases
│   ├── Geographie.md                        # Countries, landscapes, travel geography
│   ├── Gesundheit.md                        # Health, body, medical visits, illnesses
│   ├── Haus.md                              # Home, apartment, furniture, rooms
│   ├── Menge.md                             # Quantities, portions, units
│   ├── Natur.md                             # Nature, animals, plants, outdoor environment
│   ├── Schweizer Varianten.md               # German vs. Swiss German vocabulary comparisons
│   ├── Synonyme.md                          # Synonyms and alternative expressions
│   ├── Wetter.md                            # Weather and climate
│   ├── Zahlen.md                            # Numbers, counting, ordinal numbers
│   └── Zeit.md                              # Time, days, months, frequency, duration
│
└── zzz-Media/                               # Central storage for all attachments, images, and documents
    ├── *.png, *.jpg, *.heic                 # Diagram images, whiteboard snapshots, lesson graphics
    ├── *.pdf                                # Grammar cheatsheets, solution manuals
    └── *.odt                                # Homework documents
```

---

## 2. Obsidian Syntax & Markdown Conventions

Adhere strictly to these formatting standards to ensure full compatibility with Obsidian's graph, search, and transclusion engines:

### 2.1 Metadata Block (Triple Underscores)
Every note in the vault starts with a metadata block delimited by triple underscores `___` (not standard YAML `---`):

**For General, Grammar, and Vocabulary Notes:**
```markdown
___
Tags: #Languages/German/<SubCategory>
Links: [[IndexNote]]
___
```

**For Verb Conjugation Notes (`Verben/Konjugation/<Verb>.md`):**
```markdown
___
Links: [[Verben]] [[Typ - Regular verben]] [[Akkusativ]]
Meaning: to buy
___
```

### 2.2 Tag Taxonomy
Always use the standardized tag hierarchy starting with `#Languages/German/`:
*   `#Languages/German/Grammar` (Grammar notes, syntax rules)
*   `#Languages/German/Grammar/Verbs` (Verb categories and mood notes)
*   `#Languages/German/Grammar/Verbs/Regular` (Regular verb index notes)
*   `#Languages/German/Grammar/Verbs/Irregular` (Irregular verb index notes)
*   `#Languages/German/Vocabulary` (Vocabulary files in `Vokabular/` and thematic lists)
*   `#Languages/German/Cases` (Case files in `Kasus/`)
*   `#Languages/German/Other` (Pronunciation, keyboard shortcuts, phonetics)

### 2.3 Internal Wikilinks
*   **Always use double brackets**: `[[NoteName]]` or aliased `[[NoteName|Custom Label]]`.
*   **Do NOT use standard markdown file links**: Never write `[Label](path/to/file.md)`.
*   **Use flat basenames**: Obsidian resolves note names across folders automatically. Use `[[Kaufen]]`, `[[Akkusativ]]`, `[[Infinitiv mit zu]]` (never `[[Verben/Konjugation/Kaufen]]`).
*   **No broken links**: Only link to files that already exist or that you are intentionally creating as part of your task.

### 2.4 Transclusions & Block Reference IDs (CRITICAL)
The central verb index `Verben.md` uses Obsidian block transclusions to embed summary tables from files in `Verben/Modi und Typen/`:
*   `![[Typ - Hilfs verben#^3ed54c]]`
*   `![[Typ - Modal verben#^530533]]`
*   `![[Typ - Regular verben#^5ef5c7]]`
*   `![[Typ - Irregular verben#^5057b3]]`
*   `![[Typ - Trennbare verben#^ba9865]]`

> ⚠️ **CRITICAL INSTRUCTION**:
> - **NEVER** edit, remove, or alter any line containing a block reference caret ID (e.g., `^5ef5c7`).
> - When appending new rows to tables in `Typ - Regular verben.md` or `Typ - Trennbare verben.md`, **ALWAYS insert the new table row ABOVE the block reference ID line**.

### 2.5 Media Attachments
*   All images, homework files, and PDFs belong strictly in `zzz-Media/`. Never place media files in content directories.
*   Reference images using Obsidian embed syntax: `![[image-name.png]]` without folder path prefixes.

### 2.6 Footnotes
Use standard Markdown footnotes for clarifying notes or exceptions:
```markdown
English | German
------------ | ------------
Relocate[^1] | [[Umziehen]] (I)

[^1]: Also used for changing clothes ("sich umziehen").
```

---

## 3. Swiss Standard German (Schweizer Hochdeutsch)

Because the user lives and studies in Switzerland (*Klubschule Migros* / *Sprachschule ILS-Zürich*), the entire vault follows **Swiss Standard German orthography**:

1.  **Strict Prohibition of Eszett (`ß`)**:
    *   **NEVER use the character `ß`**. Always use double `ss`.
    *   *Examples*:
        *   `schliessen` (NOT `schließen`)
        *   `gross` (NOT `groß`)
        *   `heissen` (NOT `heißen`)
        *   `Spass` (NOT `Spaß`)
        *   `weiss` (NOT `weiß`)
        *   `Fussball` (NOT `Fußball`)
        *   `regelmässig` (NOT `regelmäßig`)
    *   Do NOT "correct" Swiss spellings back to German standard `ß`. If user text contains `ß`, quietly convert it to `ss`.
2.  **Swiss Vocabulary Awareness**:
    *   Consult and maintain `Vokabular/Schweizer Varianten.md` when Swiss terms arise in coursework.
    *   Common Swiss terms to expect and respect:
        *   *Grüetzi* (Hallo / Guten Tag)
        *   *En Guete* (Guten Appetit)
        *   *Merci Vilmal* (Vielen Dank)
        *   *grillieren* (grillen)
        *   *Poulet* (Hühnchen)
        *   *der Camion* (der Lastwagen)
        *   *der Stock* (Kartoffelbrei / Püree)
        *   *umzügeln* (umziehen)
        *   *der Abfall* (der Müll)
        *   *das Kuvert* (der Briefumschlag)
        *   *das Velo* (das Fahrrad)
        *   *das Töff* (das Motorrad)
        *   *hässig* (verärgert / sauer)
        *   *das Znüni* (Vormittagssnack / 9-Uhr-Pause)
        *   *das Zvieri* (Nachmittagssnack / 4-Uhr-Pause)

---

## 4. Note Templates & Structural Standards

### 4.1 Verb Conjugation Note (`Verben/Konjugation/<Verb>.md`)
Filename must be the capitalized infinitive (e.g., `Stechen.md`, `Kaufen.md`). Every verb note MUST include all 17 canonical sections shown below.

```markdown
___
Links: [[Verben]] [[Typ - Regular verben]] [[Akkusativ]]
Meaning: to buy
___

# [[Modus - Indikativ]] - Präsens
ich kaufe
du kaufst
er/sie/es kauft
wir kaufen
ihr kauft
Sie kaufen

# [[Modus - Indikativ]] - Präteritum
ich kaufte
du kauftest
er/sie/es kaufte
wir kauften
ihr kauftet
Sie kauften

# [[Modus - Indikativ]] - Perfekt
ich habe gekauft
du hast gekauft
er/sie/es hat gekauft
wir haben gekauft
ihr habt gekauft
Sie haben gekauft

# [[Modus - Indikativ]] - Plusquamperfekt
ich hatte gekauft
du hattest gekauft
er/sie/es hatte gekauft
wir hatten gekauft
ihr hattet gekauft
Sie hatten gekauft

# [[Modus - Indikativ]] - Futur I
ich werde kaufen
du wirst kaufen
er/sie/es wird kaufen
wir werden kaufen
ihr werdet kaufen
Sie werden kaufen

# [[Modus - Indikativ]] - Futur II
ich werde gekauft haben
du wirst gekauft haben
er/sie/es wird gekauft haben
wir werden gekauft haben
ihr werdet gekauft haben
Sie werden gekauft haben

# [[Modus - Konjunktiv]] 1 - Present
ich kaufe
du kaufest
er/sie/es kaufe
wir kaufen
ihr kaufet
Sie kaufen

# [[Modus - Konjunktiv]] 1 - Perfekt
ich habe gekauft
du habest gekauft
er/sie/es habe gekauft
wir haben gekauft
ihr habet gekauft
Sie haben gekauft

# [[Modus - Konjunktiv]] 1 - Futur I
ich werde kaufen
du werdest kaufen
er/sie/es werde kaufen
wir werden kaufen
ihr werdet kaufen
Sie werden kaufen

# [[Modus - Konjunktiv]] 1 - Futur II
ich werde gekauft haben
du werdest gekauft haben
er/sie/es werde gekauft haben
wir werden gekauft haben
ihr werdet gekauft haben
Sie werden gekauft haben

# [[Modus - Konjunktiv]] 2 - Präteritum
ich kaufte
du kauftest
er/sie/es kaufte
wir kauften
ihr kauftet
Sie kauften

# [[Modus - Konjunktiv]] 2 - Futur I
ich würde kaufen
du würdest kaufen
er/sie/es würde kaufen
wir würden kaufen
ihr würdet kaufen
Sie würden kaufen

# [[Modus - Konjunktiv]] 2 - Futur II
ich würde gekauft haben
du würdest gekauft haben
er/sie/es würde gekauft haben
wir würden gekauft haben
ihr würdet gekauft haben
Sie würden gekauft haben

# [[Modus - Konjunktiv]] 2 - Plusquamperfekt
ich hätte gekauft
du hättest gekauft
er/sie/es hätte gekauft
wir hätten gekauft
ihr hättet gekauft
Sie hätten gekauft

# [[Modus - Imperativ]] - Präsens
kaufe (du)
kaufen wir
kauft (ihr)
kaufen Sie

# [[Modus - Partizips]] - Präsens
kaufend

# [[Modus - Partizips]] - Perfekt
gekauft
```

**Key verb conjugation rules:**
*   **Auxiliary verb selection**: Choose `haben` or `sein` based on verb semantics. Motion and change of state verbs (e.g. `Gehen`, `Kommen`, `Fahren`, `Aufwachen`) take `sein` (e.g., `ich bin gegangen`, `ich war gegangen`, `ich sei gegangen`, `ich wäre gegangen`).
*   **Irregular verbs**: Set header link to `[[Typ - Irregular verben]]`.
*   **Separable verbs**: Set header link to `[[Typ - Trennbare verben]]`. In Präsens and Präteritum, split prefixes correctly (e.g. `ich kaufe ein`).

### 4.2 Vocabulary Note (`Vokabular/<Category>.md` and `Vokabular.md`)
Vocabulary notes use a two-column markdown table (`English | German`).

```markdown
___
Tags: #Languages/German/Vocabulary 
Links: [[Vokabular]]
___

# <Optional Category Heading>
| English | German |
| ------- | ------ |
| Apple   | Der Apfel (Ä-) |
| Beer    | Das Bier (-e) |
| Bag     | Die Tasche (-n) |
| Key     | Der Schlüssel (-) |
| Book    | Das Buch (-ü-er) |
| To buy  | [[Kaufen]] |
```

**Noun formatting standards (CRITICAL):**
*   **Always include the definite article capitalized**: `Der`, `Die`, or `Das`.
*   **Always include plural suffix notation in parentheses**:
    *   `(-)` = No change in plural (e.g., `Der Kugelschreiber (-)`, `Der Schalter (-)`)
    *   `(-e)` = Suffix -e (e.g., `Der Ingenieur (-e)`, `Der Trickfilm (-e)`)
    *   `(-n)` or `(-en)` = Suffix -n or -en (e.g., `Die Tasche (-n)`, `Die Rechnung (-en)`)
    *   `(-s)` = Suffix -s (e.g., `Das Blinddate (-s)`, `Der Event (-s)`)
    *   `(Ä-)`, `(Ö-)`, `(Ü-)` = Umlaut only (e.g., `Der Apfel (Ä-)`)
    *   `(-ü-er)`, `(-öfe)` = Umlaut + suffix (e.g., `Das Buch (-ü-er)`, `Der Bauernhof (-öfe)`)
    *   `(always plural)` = No singular form (e.g., `Die Wahlen (always plural)`)
*   **Verbs in vocabulary lists**: Written as infinitive, linked to `[[Verb]]` if a conjugation file exists.

### 4.3 Grammar Note (`Grammatik/<Topic>.md`)
Grammar notes describe specific syntactical structures, clause patterns, and connective words:

```markdown
___
Tags: #Languages/German/Grammar 
Links: [[Vokabular]]
___

[Concise introductory definition explaining when and why this grammatical construction is used.]

# Rules
- [Word order explanation: Hauptsatz vs. Nebensatz, verb position 0, 1, 2, or end]
- [Connector / conjunction list: e.g., weil, denn, da, obwohl, etc.]

| Conjunction / Form | Function / Meaning | Example |
| ------------------ | ------------------ | ------- |
| **weil**           | Reason (Verb at end) | Ich bleibe zu Hause, **weil** es regnet. |
| **denn**           | Reason (Position 0)  | Ich bleibe zu Hause, **denn** es regnet. |

# Examples
- [Authentic, clear German example sentences with bolded structural elements]
- [Contextual notes or common student errors to avoid]
```

### 4.4 Case Note (`Kasus/<Case>.md`)
Case notes detail the German cases (Nominativ, Akkusativ, Dativ, Genitiv):

```markdown
___
Tags: #Languages/German/Cases 
___

[Explanation of syntactic role: Subject, Direct Object, Indirect Object, Possession.]

# Artikel
[Definite, indefinite, and negative article declension tables comparing Nominativ with this case]

# Pronomen
[Personal, possessive, and reflexive pronoun declension tables]

# Prepositions
[List of two-way (Wechselpräpositionen) or fixed prepositions governing this case, with question words: Wer? Wen? Wem? Wessen? Wo? Wohin?]

# Examples
[Contrastive example sentences illustrating case usage]
```

---

## 5. Agent Operational Recipes (Step-by-Step)

### Recipe A: Adding a New Verb
When requested to conjugate or add a new verb:
1.  **Check if file already exists**: Look in `Verben/Konjugation/<Verb>.md`.
2.  **Determine verb category**:
    *   Regular, Irregular, Modal, Auxiliary, Reflexive, or Separable?
    *   Auxiliary verb for Perfekt: `haben` or `sein`?
    *   Case governed: does it typically take `[[Akkusativ]]` or `[[Dativ]]`?
3.  **Create conjugation note**: Write `Verben/Konjugation/<Verb>.md` with all 17 sections using Swiss orthography (no `ß`).
4.  **Register verb in verb index tables**:
    *   If **regular**: Add row to table in `Verben/Modi und Typen/Typ - Regular verben.md` **ABOVE** the line containing `^5ef5c7`.
    *   If **separable**: Add row to table in `Verben/Modi und Typen/Typ - Trennbare verben.md` **ABOVE** the line containing `^ba9865`.
    *   If **irregular**: Ensure `[[Typ - Irregular verben]]` is in the `Links:` line of the verb's header.

### Recipe B: Processing `AAA TEMPORARY NOTE.md`
The file `AAA TEMPORARY NOTE.md` is Marco's in-class scratchpad. It often contains rough vocabulary, book references (e.g. `kb p 11-28` for Kursbuch, `AB` for Arbeitsbuch), grammar snippets, or homework reminders.

When instructed to process or clean up temporary notes:
1.  **Read and parse**: Extract all vocabulary terms, grammar rules, phrases, and verbs.
2.  **Dispatch to destination files**:
    *   **Vocabulary** -> Append to appropriate `Vokabular/<Category>.md` or `Vokabular.md` using the strict noun format (`Der/Die/Das Noun (plural)`).
    *   **Grammar rules** -> Append to relevant `Grammatik/<Rule>.md` or create a new note if it covers a distinct grammar topic.
    *   **Verbs** -> Create full conjugation file in `Verben/Konjugation/` if requested.
3.  **Preserve scratchpad header & shortcuts**:
    *   Do **NOT** delete the keyboard shortcuts memo at the top (`AltGr + q = ä`, etc.).
    *   Update the `Created:` timestamp if resetting.
    *   Remove only the processed lesson notes.

### Recipe C: Adding New Vocabulary
When adding vocabulary from lessons, reading, or homework:
1.  **Select the best category file**: Check `Vokabular/` for an existing thematic note (`Arbeitsplatz.md`, `Essen.md`, `Haus.md`, etc.). If no category fits, use `Vokabular.md` general list.
2.  **Verify uniqueness**: Avoid duplicate entries in the same file.
3.  **Apply standard notation**:
    *   Noun: `Der/Die/Das <Word> (<Plural>)`
    *   Verb: Lowercase infinitive or `[[Verb]]` Wikilink
    *   Adjective: Lowercase
    *   Swiss spelling: Always `ss`, never `ß`
4.  **Keep tables tidy**: Maintain markdown table pipe formatting.

---

## 6. Golden Rules for AI Agents

1.  **Never Hallucinate or Break Wikilinks**:
    *   Only link to files that exist or that you are actively creating.
    *   Use flat basename links: `[[Kaufen]]`, not folder paths.
2.  **Never Touch Transclusion Block IDs**:
    *   Lines ending in carets like `^5ef5c7`, `^ba9865`, `^3ed54c`, `^530533` are vital Obsidian anchors. Never remove or alter them.
3.  **Swiss German Only (Zero `ß` Policy)**:
    *   Never emit `ß`. Always convert to `ss`.
4.  **No Meta-Commentary Inside Notes**:
    *   Never leave comments like `<!-- Added by AI -->` or explanatory chat remarks inside the markdown notes. All communication with the user must stay inside the CLI conversation.
5.  **Preserve Existing Vault Structure**:
    *   Do not reorganize existing directory structures, rename folders, or alter root files unless explicitly directed by the user.
