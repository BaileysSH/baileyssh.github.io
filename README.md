# DebtFree PWA

## Come installare su iPhone

1. Apri `index.html` in **Safari** su iPhone
   - Puoi aprirlo da un server locale, oppure caricarlo su qualsiasi hosting statico (GitHub Pages, Netlify, ecc.)

2. Tocca l'icona **Condividi** (il quadrato con la freccia verso l'alto) in basso al centro

3. Scorri verso il basso e tocca **"Aggiungi alla schermata Home"**

4. Dai il nome "DebtFree" e tocca **Aggiungi**

5. L'app apparirà sulla Home Screen come un'app normale, senza la barra di Safari.

---

## Struttura file

```
debtfree/
├── index.html      # App completa (single file)
├── sw.js           # Service Worker per funzionamento offline
├── manifest.json   # Configurazione PWA
└── README.md
```

---

## Dati e backup

I dati sono salvati in **localStorage** sul dispositivo.

Per backup su iCloud Drive:
1. Vai in **Impostazioni** → **Dati** → **Esporta JSON**
2. Il file viene scaricato — aprilo nell'app **File**
3. Spostalo nella cartella **iCloud Drive** di tua scelta

Per ripristinare: **Importa JSON** dallo stesso menu.

---

## Funzionalità

- **Inserimento rapido**: tastierino numerico + categoria in un tap
- **Dashboard**: KPI, data di libertà finanziaria, piano Avalanche
- **Movimenti**: storico spese filtrabili per categoria
- **Impostazioni**: gestione finanziamenti, entrate mensili, export/import

---

## Strategia Avalanche

Il sistema ordina i debiti per tasso di interesse (dal più alto al più basso).
Il surplus mensile (entrate − spese − rate minime) viene allocato interamente
sul debito con tasso più alto. Quando quel debito si estingue, la sua rata
viene aggiunta al surplus disponibile per il debito successivo ("debt rollover").
