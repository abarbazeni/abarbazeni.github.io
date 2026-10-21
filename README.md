# Alessandro Barbazeni — sito personale

Sito accademico statico (HTML + CSS, nessuna dipendenza, nessun build) pronto per GitHub Pages.
Contenuti migrati da https://sites.google.com/view/abarbazeni.

## Struttura

```
index.html          Home: presentazione, interessi di ricerca, contatti
research.html       Working papers e work in progress (abstract espandibili)
teaching.html       Esperienza didattica in ordine cronologico
404.html            Pagina "non trovata" servita da GitHub Pages
assets/
  css/style.css     Unico foglio di stile (tema chiaro/scuro automatico, stampa)
  favicon.svg       Icona con le iniziali
  img/              Qui va la foto profilo
.nojekyll           Dice a GitHub Pages di servire i file così come sono
```

## Pubblicazione su GitHub Pages

1. Crea un repository pubblico chiamato **`<tuo-username>.github.io`**
   (così il sito sarà su `https://<tuo-username>.github.io`).
2. Carica tutti i file di questa cartella nella radice del repository
   (dal sito: *Add file → Upload files*, trascina il contenuto della cartella, poi *Commit*).
3. Vai su **Settings → Pages**, alla voce *Build and deployment* scegli
   *Deploy from a branch*, branch **`main`**, cartella **`/ (root)`**, e salva.
4. Dopo uno o due minuti il sito è online.

Se usi un repository con un altro nome (es. `website`), il sito sarà su
`https://<tuo-username>.github.io/website/`: tutto funziona, il link "home" (e la favicon)
della pagina 404 vanno aggiornati con il nome del repo (qui: `/abarbazeni/`).

## Personalizzazione

- **Foto profilo**: salva la foto come `assets/img/profile.jpg` (formato verticale 4:5,
  circa 480×600 px). Finché il file non c'è, al suo posto compaiono le iniziali "AB".
- **CV**: il sorgente LaTeX è in `CV/CV.tex` (con `CV/resume.cls`). Compilando con latexmk
  (LaTeX Workshop), `CV/latexmkrc` copia da solo il PDF in `assets/cv.pdf`, dove puntano i link della home.
- **Nuovo paper**: in `research.html` duplica un blocco `<article class="paper">`.
  Per aggiungere un link al draft, inserisci ad esempio
  `<p><a href="URL">Draft (PDF)</a></p>` sotto il titolo.
- **Nuovo corso**: in `teaching.html` aggiungi un blocco `<li class="term">` in cima alla lista.
- **Colori e font**: sono definiti come variabili all'inizio di `assets/css/style.css`.
- **Dominio personalizzato**: aggiungi un file `CNAME` con il dominio
  e configuralo in *Settings → Pages → Custom domain*.
