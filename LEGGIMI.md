# AZZE LIST

App per liste, valigie e cose da comprare. Funziona offline, i dati restano sul telefono.

## File

- `index.html` — l'app (tutto qui dentro: struttura, stile, logica)
- `manifest.webmanifest` — nome, icona, colori, apertura a schermo intero
- `sw.js` — service worker: tiene i file in cache per l'uso offline
- `icon-192.png`, `icon-512.png`, `icon-maskable-512.png`, `apple-touch-icon.png` — icone

Vanno tenuti tutti nella stessa cartella, con questi nomi.

## Categorie

Dentro ogni lista puoi creare categorie (es. Medicine, Vestiti, Documenti). Quando aggiungi
un oggetto scegli la categoria dal menu. Nel viaggio le categorie diventano sezioni apribili
con la loro barra di completamento e i pulsanti per spuntare o escludere tutta la sezione.
Gli oggetti senza categoria finiscono in fondo sotto "Senza categoria".

## Categorie di base

Scheda Categorie: blocchi riutilizzabili (es. "cose da padel") con i loro oggetti.
Dalla scheda Liste li inserisci in qualsiasi lista con "Inserisci": entra una COPIA,
che poi modifichi liberamente senza toccare l'originale.
Il segnalibro sull'intestazione di una categoria dentro una lista fa il contrario:
la salva tra le categorie di base.

La spesa è passata in alto a destra, nell'icona del carrello con il contatore.

## Nel viaggio

- Filtro in tre posizioni: Tutto, Senza esclusi (nasconde le X), Da prendere (lascia solo cosa manca).
- "Azzera spunte" riporta il viaggio a zero senza toccare oggetti e categorie.
- "Salva come lista" trasforma il viaggio in un modello riutilizzabile.
- Campo di ricerca che filtra mentre scrivi.

Nella scheda Liste puoi creare una lista nuova copiandone una esistente.

## Pubblicare (GitHub Pages)

1. Su github.com: nuovo repository pubblico, nome `azze-list`.
2. "Add file" → "Upload files" → carica tutti i file di questa cartella → Commit.
3. Settings → Pages → Source: "Deploy from a branch", branch `main`, cartella `/root` → Save.
4. Dopo un paio di minuti l'indirizzo è `https://TUONOME.github.io/azze-list/`.

## Installare sul telefono

Apri l'indirizzo con Safari → Condividi → Aggiungi a Home.
Da lì in poi parte a schermo intero e non serve più internet.

## Aggiornare

Ricarica i file modificati nel repository. Alla prima apertura con rete l'app scarica
la versione nuova, che entra in funzione alla riapertura successiva.

## Impostazioni (ingranaggio in alto a destra)

- Backup completo .json: tutto, compresi viaggi e spesa. Da tenere da parte, non si modifica a mano.
- Foglio Excel .xlsx: liste e categorie di base, modificabile a mano o con l'aiuto di un'AI.
  Il foglio Legenda spiega tutte le regole. All'importazione premi prima Prova: controlla
  riga per riga e non importa niente finché non è tutto a posto.
  Gli ID nelle colonne servono a riconoscere cosa aggiornare: non vanno toccati, e una riga
  nuova senza ID diventa una cosa nuova.
  Il foglio ha tre pagine: Dati (liste e categorie di base), Spesa (il carrello) e Legenda.

## Backup

Scheda Liste → "Esporta backup": si apre il pannello di condivisione, scegli "Salva su File"
e la cartella che vuoi. Il nome è datato e progressivo: `azze-list-2026-09-08.json`, e se
nello stesso giorno ne fai un altro diventa `-2`, `-3` e così via.
"Importa backup" lo ricarica, anche su un altro telefono.

Dopo sette giorni senza backup, all'apertura compare un promemoria con il pulsante per farlo.
