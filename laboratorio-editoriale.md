# Il laboratorio editoriale

Uno stack di strumenti che gira interamente sui miei computer, senza servizi esterni. Nasce per automatizzare la produzione editoriale ricorrente — notiziari, comunicati, rassegne — e per garantire che le uscite a scadenza fissa non saltino. Sotto: cosa contiene e cosa permette di offrire.

---

## Come è fatto

### 1. Produzione editoriale quotidiana in automatico
Da mail grezza a documento pubblicato senza passaggi manuali.
* **Pipeline TESTI WORD** — lasci un .docx in una cartella, torna formattato allo standard editoriale che hai definito: font, stili, gerarchie di titoli, gestione delle righe di link, inserimento automatico dei permalink agli atti citati. Zero formattazione a mano.
* **Rialzo dei nomi propri** — nella conversione dal maiuscolo riconosce le sigle, una rubrica di nomi che aggiorni tu e i cognomi che seguono un ruolo ("il ministro X"). I casi incerti finiscono in un report da rileggere.
* **Controllo di fedeltà** — a fine lavorazione confronta parola per parola l'originale e il formattato: se manca qualcosa, lo segnala.
* **Prodotti ricorrenti** — la stessa impalcatura regge notiziari quotidiani e settimanali: raccolta, formattazione, arricchimento dei riferimenti, PDF, invio ai destinatari. Il documento pronto alimenta anche l'impaginato InDesign per i prodotti più curati.

### 2. Assistenti di scrittura e ricerca — Open WebUI
Chat in locale con 9 "skill" pronte, tarate sul tono di voce del committente, con glossario e linee guida di stile condivise.
* **Skill editoriali**: comunicato-stampa, verbale-riunione, newsletter, editor-redazionale, analisi-conferenze, grafica-editoriale, ricerca-web, photo, lettura-codice.
* **RAG sui documenti** — carichi Word/PDF/scansioni, il sistema li converte in testo (Docling), li indicizza (Qdrant) e ci ragiona sopra: una registrazione di conferenza stampa diventa una bozza di comunicato in pochi minuti.
* **Ricerca web offline (SearXNG) e generazione immagini (ComfyUI)**, senza uscire dai miei server.
* **Più modelli in locale**, scelti e calibrati di volta in volta sulle esigenze del cliente: testo istituzionale, codice, multimodale, RAG con tool use.

### 3. I guardiani — perché un guasto non resti invisibile per giorni
* **Spia del laboratorio** — un sorvegliante che sta fuori dai programmi che controlla (così parla anche quando loro si fermano): tiene d'occhio contenitori, workflow, credenziali scadute, il programma che sorveglia i Word in arrivo, la saturazione della memoria video, lo spazio sui dischi e il fatto che fisso e portatile non lavorino in doppio. Avvisa solo quando c'è un guaio.
* **Auto-healing** — prima di avvisarti, prova a rimettere in moto le cose da solo: mette in quarantena le elaborazioni andate storte, riavvia il watcher, controlla che i notiziari siano usciti.
* **Audit semestrale** — a febbraio e agosto confronta quello che gira davvero con la documentazione e elenca i disallineamenti.

### 4. Le fondamenta
* **Tutto in locale** — niente cloud dove è evitabile: ricerca, conversione documenti ed embedding sono self-hosted. Nessun contenuto passa da servizi terzi.
* **Replicabile** — ogni componente è bloccato a una versione precisa: se una macchina si rompe, la ricostruisci identica in poco tempo.
* **Due macchine allineate** — postazione fissa con lo stack completo e un portatile con profilo alleggerito per la trasferta: la produzione editoriale di base non si ferma nemmeno fuori sede.
* **Printing Press** — una libreria di strumenti a riga di comando già pronti, con scheduler, per le lavorazioni ricorrenti.

---

## Cosa offro con il laboratorio

### Sistema grafico e impaginazione
Definizione di uno standard editoriale — griglia tipografica, stili, gerarchie — e sua applicazione coerente su grandi volumi. Formattazione di circolari, bollettini, atti, rassegne; impaginazione InDesign per opuscoli, periodici e materiali per convegni.

### Notiziari e periodici ad alto volume
Gestione completa di prodotti a cadenza fissa: raccolta dei contenuti, formattazione allo stile della testata, arricchimento con link e riferimenti normativi, esportazione PDF, distribuzione. Sostenibile anche per redazioni di una sola persona.

### Redazione e revisione
Prime stesure di comunicati stampa, newsletter, verbali, sintesi di convegni e conferenze, con tono calibrato sul committente. Editing redazionale, sintesi di documenti lunghi (atti, rapporti, trascrizioni).

### Ricerca, rassegna e basi di conoscenza
Rassegna stampa e ricerca tematica. Estrazione e strutturazione di contenuti da PDF, scansioni e archivi. Costruzione di basi documentali consultabili sul corpus del committente.

### Immagini
Generazione e ritocco di immagini per editoriale e social, ottimizzate per stampa e web.

### Automazioni editoriali su misura
Progettazione di flussi per altre redazioni e uffici stampa: intake da posta e cartelle condivise, formattazione automatica, archiviazione strutturata, pubblicazione multicanale.

---

## Due garanzie trasversali

* **Riservatezza** — le lavorazioni restano sui miei sistemi: adatto a materiale sotto embargo, dati personali, bozze pre-pubblicazione.
* **Continuità** — la sorveglianza automatica assicura che le uscite periodiche rispettino la scadenza anche quando qualcosa si inceppa.