# Literary Editing Skills for LLMs

> Repository di **System Prompts**, **Skills modulari** e **Workflow** progettati per trasformare modelli LLM in editor letterari professionali.

Questa repository fornisce un framework completo e versionabile per la revisione di romanzi, racconti e saggistica narrativa. Ogni skill è un prompt auto-contenuto, strutturato secondo standard rigorosi di Prompt Engineering, pensato per essere utilizzato in isolamento o all’interno di pipeline multi-pass.

---

## Struttura della Repository

```
literary-editing-skills/
├── 01-structural-editing/          # Trama, ritmo, archi personaggi, worldbuilding, buchi di trama
├── 02-line-editing/                # Prosa, show vs tell, voce narrante, dialoghi, ritmo frasale
├── 03-copy-and-proofreading/       # Sintassi, coerenza terminologica, registro, micro-errori
│   └── correttore-di-bozze-revisione-grammaticale.md
├── 04-beta-reader-personas/        # Agenti virtuali (lettore di genere, critico spietato, ecc.)
├── 05-workflows-and-pipelines/     # Pipeline multi-pass e sequenze di revisione
├── templates/                      # Template standard per nuove skills
└── README.md
```

---

## Skills disponibili

### 03-copy-and-proofreading

| Skill | Versione | Descrizione breve |
|-------|----------|-------------------|
| [Correttore di Bozze e Revisione Grammaticale Narrativa](03-copy-and-proofreading/correttore-di-bozze-revisione-grammaticale.md) | 2.0 | Revisione conservativa: ortografia, refusi, punteggiatura, concordanze inequivocabili + standardizzazione dialoghi ai caporali. Richiede approvazione dell’autore prima della restituzione del testo definitivo. |

---

## Formato Standard di ogni Skill

Ogni file `.md` rispetta rigorosamente questa struttura:

1. **Frontmatter YAML**  
   `title`, `category`, `target_llm`, `description`, `version`, `inputs_required`

2. **System Prompt Core**  
   Ruolo, vincoli d’azione, framework analitico di riferimento

3. **Step-by-Step Instructions**  
   Passaggi esecutivi precisi e non ambigui

4. **Input Data Template**  
   Sezione `[TESTO DA REVISIONARE]` + parametri contestuali

5. **Output Schema & Format**  
   Formato obbligatorio del feedback (tabelle, citazioni prima/dopo, prioritizzazione)

6. **Few-Shot Examples**  
   Almeno un esempio completo Input → Output

---

## Comandi Operativi (per interazione con l’assistente)

| Comando | Descrizione |
|---------|-------------|
| `/NEW_SKILL [nome/categoria]` | Genera un nuovo file `.md` completo e pronto per il commit |
| `/AUDIT_SKILL [incolla prompt]` | Analizza e ottimizza un prompt esistente |
| `/BUILD_PIPE [obiettivo]` | Crea una pipeline sequenziale multi-skill |
| `/REPO_STRUCT` | Aggiorna struttura directory e README |
| `/TEST_SAMPLE [nome_skill]` | Testa una skill su un estratto narrativo di prova |

---

## Principi di Design

- **Misurabilità**: nessun feedback generico. Ogni criticità deve essere categorizzata (Critico / Primario / Stilistico) e accompagnata da citazione testuale.
- **Tracciabilità**: ogni skill dichiara esplicitamente i suoi input obbligatori e lo schema di output.
- **Modularità**: le skills possono essere combinate in pipeline senza sovrapposizioni di responsabilità.
- **Riduzione allucinazioni**: istruzioni step-by-step + few-shot + vincoli di output vincolanti.
- **Conservazione della voce autoriale**: specialmente nelle skill di copy-editing (vedi protocollo anti-allucinazione e blocco applicazione automatica).

---

## Primi file essenziali ancora da creare

1. `01-structural-editing/plot-structure-analysis.md`  
   Analisi della struttura narrativa (atto, plot points, arco di trasformazione)

2. `01-structural-editing/character-arc-audit.md`  
   Valutazione della coerenza e profondità degli archi personaggio

3. `02-line-editing/show-vs-tell-detector.md`  
   Identificazione e riscrittura di passaggi “tell” eccessivi

4. `02-line-editing/dialogue-voice-consistency.md`  
   Controllo di voce, subtext e distintività dei dialoghi

5. `05-workflows-and-pipelines/four-pass-revision-pipeline.md`  
   Pipeline completa: Struttura → Scene → Prosa → Micro-editing

---

## Come contribuire / estendere

1. Usa il template in `templates/skill-template.md`
2. Rispetta il frontmatter e lo schema di output
3. Includi sempre almeno un few-shot example realistico
4. Testa la skill con `/TEST_SAMPLE` prima del commit

---

**Versione repository**: 0.2.0  
**Ultimo aggiornamento**: 2026-09-23  
**Manutentore**: Senior Narrative Designer & Prompt Engineer
