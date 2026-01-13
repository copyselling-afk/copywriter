# PROMPT ENGINEERING GUIDE FOR TRIAS EDGE
**Verzia:** 1.0
**Účel:** Knižnica pokročilých techník pre riadenie AI agentov v rámci systému TRIAS Edge.

---

## I. ZÁKLADNÁ ŠTRUKTÚRA PROMPTU (The Skeleton)

Dobrý prompt pre náš systém musí obsahovať týchto 5 zložiek. Ak jedna chýba, výstup bude priemerný.

1.  **ROLE (Kto si):** "Si TRIAS Edge Stratég..."
2.  **CONTEXT (Čo vieš):** "Vychádzaj zo súborov @trias_manifest.md a @klient_config.md..."
3.  **TASK (Čo máš robiť):** "Analyzuj riziko volatility pre oceľ..."
4.  **CONSTRAINTS (Čo nesmieš):** "Nepoužívaj marketingový jazyk, buď cynický realist..."
5.  **OUTPUT FORMAT (Ako to má vyzerať):** "Výstup daj do Markdown tabuľky..."

---

## II. KĽÚČOVÉ TECHNIKY (Power Moves)

### 1. Chain-of-Thought Prompting (Mysli nahlas)
Núti AI, aby pred finálnou odpoveďou ukázala svoj myšlienkový proces. Zvyšuje to logickú presnosť.
* **Príkaz:** *"Predtým, než napíšeš finálny text, urob si v odrážkach analýzu problému a krok za krokom si odôvodni, prečo je tento prístup správny."*

### 2. Few-Shot Prompting (Ukáž príklad)
AI najlepšie pochopí štýl, ak jej ukážeš vzor.
* **Príkaz:** *"Píš štýlom, ako je uvedené v tomto príklade:"*
    > *ZLE: Naše riešenie je kvalitné.*
    > *DOBRE: Naše riešenie eliminuje riziko prestoja vďaka 20% rezerve v materiáli.*

### 3. Persona Adoption (Hranie rolí)
Aby sme dosiahli špecifický "TRIAS tón", musíme AI prepnúť do role experta.
* **Príkaz:** *"Správaj sa ako cynický senior nákupca s 20-ročnou praxou, ktorý nenávidí, keď mu obchodníci klamú. Píš text tak, aby presvedčil práve teba."*

### 4. Negative Constraints (Zákazy)
Je dôležitejšie povedať AI, čo *nemá* robiť, než čo má robiť.
* **Príkaz:** *"V žiadnom prípade nepíš, že sme 'najlacnejší', 'najlepší' alebo 'flexibilní'. Ak nemáš dáta, priznaj neistotu. Nepoužívaj výkričníky."*

---

## III. ŠABLÓNY PROMPTOV PRE AGENTOV

### Pre Agenta: STRATÉG (Hľadanie tém)
```text
Si TRIAS Edge Stratég. Tvojou úlohou je nájsť "informačnú dieru" na trhu klienta [KLIENT].
Analyzuj jeho súbor @klient_config.md.
Nájdi jeden mýtus, ktorému trh verí (napr. že cena je všetko), a navrhni tému článku, ktorá tento mýtus logicky a matematicky rozbije.
Nechcem názov článku. Chcem "Argumentačnú osnovu".