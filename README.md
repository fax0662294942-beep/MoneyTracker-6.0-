# 💰 MoneyTracker 6.0

Applicazione web per la gestione delle spese personali e familiari, installabile come app sul telefono (PWA).

## ✨ Funzionalità

- **Account multipli** — gestisci spese di famiglia, personali e altri account separati
- **Import backup 1Money** — importa il backup SQLite completo di 1Money (conti, categorie, transazioni)
- **Import CSV 1Money** — importa anche i file CSV esportati da 1Money
- **Categorie dinamiche** — crea, modifica ed elimina categorie di spesa e entrata
- **Conti dinamici** — gestisci i tuoi conti (Carta, Contanti, Banca, ecc.)
- **Grafici e statistiche** — visualizza le spese per categoria con grafico a ciambella e trend mensile
- **Budget mensili** — imposta budget per categoria e monitora le spese
- **Filtri periodo** — visualizza dati per settimana, mese, anno o intervallo personalizzato
- **Trasferimenti tra account** — registra i movimenti di denaro tra i tuoi account
- **Tasto indietro Android** — navigazione naturale tra le schermate, doppia pressione per uscire
- **Reset dati** — reset solo transazioni oppure reset completo all'origine
- **Funziona offline** — grazie al Service Worker le pagine già visitate funzionano senza internet
- **Installabile** — si installa come app sul telefono Android e iOS

## 🚀 Come usare

### Online
Apri direttamente: **[https://TUO-USERNAME.github.io/MoneyTracker-6.0/](https://TUO-USERNAME.github.io/MoneyTracker-6.0/)**

### Installare come app (Android)
1. Apri il link nel browser Chrome
2. Tocca i tre puntini in alto a destra
3. Seleziona **"Aggiungi a schermata Home"**
4. L'app appare come icona sul telefono

### Installare come app (iOS)
1. Apri il link in Safari
2. Tocca il tasto **Condividi** (quadrato con freccia)
3. Seleziona **"Aggiungi a schermata Home"**

## 📥 Import da 1Money

### Backup SQLite (consigliato — importa tutto)
1. In 1Money: Menu → Impostazioni → Backup → Crea backup
2. In MoneyTracker: ⚙️ Impostazioni → **"Apri Import SQLite"**
3. Seleziona il file backup (es. `1Money_BACKUP_20_02_26`)
4. Vengono importati automaticamente: conti, categorie e tutte le transazioni

### CSV (alternativo)
1. In 1Money: esporta in formato CSV
2. In MoneyTracker: ⚙️ Impostazioni → **"Importa da 1Money"** → seleziona il file `.csv`

## 🗂️ Struttura file

```
MoneyTracker-6.0/
├── index.html        ← App completa (tutto in un file)
├── manifest.json     ← Configurazione PWA
├── sw.js             ← Service Worker (offline support)
├── icons/            ← Icone app (da aggiungere)
│   ├── icon-192.png
│   └── icon-512.png
└── README.md         ← Questo file
```

## 🔧 Deploy su GitHub Pages

1. Crea un nuovo repository su GitHub chiamato `MoneyTracker-6.0`
2. Carica tutti i file
3. Vai su **Settings → Pages**
4. In **Source** seleziona `main` branch, cartella `/root`
5. Clicca **Save**
6. Dopo 1-2 minuti l'app è online all'indirizzo mostrato

## 💾 Dati

I dati sono salvati nel **localStorage** del browser del dispositivo. Non vengono inviati a nessun server. Se cambi dispositivo o browser, i dati non si trasferiscono automaticamente (usa l'export Excel per fare un backup).

## 📋 Versioni

| Versione | Note |
|----------|------|
| 6.0 | Import SQLite 1Money, categorie/conti dinamici, tasto indietro Android, reset dati |
| 2.0 | Account multipli, trasferimenti, import CSV 1Money |
| 1.0 | Versione base |
