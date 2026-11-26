# Posta — lettore personale per Substack

Posta è una piccola web app installabile per raccogliere in una schermata gli ultimi articoli delle pubblicazioni Substack che segui.

## Pubblicazione su GitHub Pages

1. Crea un repository GitHub pubblico.
2. Carica **il contenuto di questa cartella** nella radice del repository, inclusa la cartella nascosta `.github`.
3. In **Settings → Pages**, scegli **GitHub Actions** come sorgente di pubblicazione.
4. Attendi il completamento del workflow `Pubblica Posta su GitHub Pages`; il link del sito comparirà nel job e nella sezione Pages.
5. Apri il link sul telefono. Su Android scegli **Installa app** o **Aggiungi a schermata Home** dal menu del browser. Su iPhone apri il link in Safari e usa **Condividi → Aggiungi alla schermata Home**.

Per installarla e aprirla offline serve HTTPS; GitHub Pages lo fornisce.

## Uso e limiti attuali

- Aggiungi una pubblicazione incollando il suo indirizzo, per esempio `https://nome.substack.com`; Posta aggiunge `/feed` automaticamente. Puoi anche incollare direttamente un URL RSS.
- Feed, articoli e stato di lettura sono salvati nel browser sul dispositivo. Non vengono sincronizzati tra telefono e computer e cancellando i dati del browser si perdono.
- I feed sono richiesti dal browser tramite il servizio pubblico RSS2JSON. È un servizio esterno: disponibilità e limiti dipendono da RSS2JSON. Non inserire credenziali o dati privati.
- Il testo mostrato come riassunto è l'estratto fornito dal feed, abbreviato quando è lungo. Non è un riassunto generato da un modello AI.
- La modalità offline mantiene disponibile la pagina, ma per aggiornare i feed serve una connessione Internet.
- Gli articoli riservati agli abbonati possono comparire solo nella misura in cui il feed ne espone i contenuti.

## Per i collaboratori

Tutta la logica è in `index.html`; il progetto non richiede build o installazione di dipendenze. `manifest.webmanifest` descrive l'app installabile e `sw.js` memorizza la pagina per l'apertura offline.
