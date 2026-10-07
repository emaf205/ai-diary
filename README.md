# AI Diary

![AI Diary — interfaccia](assets/screenshot.jpg)

**Una cronaca pubblica e minimale di ciò che costruisco, testo, scopro e metto in discussione lavorando con l'intelligenza artificiale.**

### ▶ [APRI AI DIARY ONLINE](https://emaf205.com/ideas/ai-diary/)

**Micro-post · ricerca · hashtag · filtri · PWA · privacy by design**

---

## Il progetto

AI Diary nasce da un problema semplice: esperimenti, scoperte, idee e decisioni importanti finivano per perdersi dentro conversazioni molto lunghe con l'AI.

Invece di trasformare ogni piccola scoperta in un articolo, ho costruito una **cronaca cronologica del lavoro quotidiano con l'intelligenza artificiale**.

Ogni voce è scritta in prima persona, resta entro 140 caratteri e può includere hashtag, link pubblici, screenshot reali e, quando serve, dubbi o domande aperte.

Non è un archivio di trascrizioni. È una **memoria pubblica e compressa del processo**.

## Cosa entra nel diario

- progetti che costruisco;
- esperimenti con l'AI;
- scoperte e intuizioni;
- prompt e workflow;
- lezioni ed esperimenti didattici;
- prototipi e piccoli strumenti;
- progetti pubblicati;
- errori e risultati inattesi;
- idee che vale la pena conservare;
- domande e dilemmi ancora aperti.

I giorni vuoti restano vuoti. Nessun contenuto viene aggiunto solo per riempire la timeline.

## Privacy by design

Prima della pubblicazione:

- aziende e clienti vengono anonimizzati;
- i nomi personali vengono rimossi quando non necessari;
- indirizzi email e dati identificativi vengono esclusi;
- materiale sensibile o riservato non viene pubblicato;
- date, link e affermazioni non vengono inventati.

La repository non contiene intenzionalmente un archivio Markdown separato con tutti i post storici.

## Funzionalità

AI Diary è una web app statica e responsive con:

- blocchi settimanali;
- ricerca full-text;
- hashtag cliccabili;
- filtri temporali e intervallo date personalizzato;
- modalità chiara / scura;
- link pubblici ai progetti;
- screenshot reali opzionali;
- layout mobile-first a colonna singola;
- installazione come PWA.

Nessun framework, database o backend richiesto.

## PWA

AI Diary può essere installato come una piccola app.

Su browser compatibili Android e desktop compare l'azione **Installa**. Su iPhone/iPad:

**Safari → Condividi → Aggiungi alla schermata Home**

La PWA include:

- icona dedicata in PNG e SVG;
- modalità standalone;
- installazione sulla Home;
- cache locale dell'interfaccia;
- fallback offline per pagine e asset già memorizzati;
- salvataggio della preferenza chiaro/scuro.

## Aggiornamento

AI Diary non viene aggiornato soltanto a mano.

Un'attività programmata di ChatGPT, ogni **3 giorni**, analizza il lavoro recente disponibile nelle mie conversazioni e:

1. individua attività, esperimenti, scoperte, idee e dubbi rilevanti;
2. elimina duplicati e contenuti di scarso valore;
3. riscrive gli eventi utili come micro-post in prima persona entro 140 caratteri;
4. mantiene lunghezze naturali e variabili;
5. aggiunge da uno a tre hashtag pertinenti;
6. inserisce link pubblici verificati quando disponibili;
7. anonimizza aziende, clienti, persone e dati sensibili;
8. usa screenshot reali solo quando disponibili, pertinenti e sicuri;
9. preserva struttura settimanale, ricerca, filtri, PWA e tema;
10. aggiorna la versione di progetto di `index.html`;
11. prepara una nuova versione HTML pronta per la pubblicazione.

La pubblicazione online resta manuale via FTP: l'automazione prepara l'aggiornamento, il passaggio finale resta sotto il mio controllo.

## Perché

Volevo qualcosa a metà tra **changelog, taccuino di laboratorio, timeline di ricerca e memoria pubblica** del lavoro con l'AI.

La parte interessante non è soltanto ciò che arriva alla fine. Sono anche le piccole scoperte, gli errori e i dubbi che normalmente sparirebbero dentro una chat.

### [Apri AI Diary →](https://emaf205.com/ideas/ai-diary/)

## Struttura

```text
.
├── index.html
├── manifest.webmanifest
├── sw.js
├── assets/
│   ├── icon.svg
│   ├── icon-180.png
│   ├── icon-192.png
│   └── screenshot.jpg
├── LICENSE
└── README.md
```

## Avvio locale

Per una semplice anteprima puoi aprire `index.html`.

Per testare correttamente PWA e service worker, servi la cartella tramite HTTP/HTTPS.

**Versione online:**  
https://emaf205.com/ideas/ai-diary/

## Autore

**Emanuele BDC**

[Homepage](https://emaf205.com/) · [Blog](https://emaf205.com/blog/) · [Ideas](https://emaf205.com/ideas/) · [GitHub](https://github.com/emaf205)

*Made with ♥ in Milan by Emanuele BDC.*
