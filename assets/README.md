# Promemoria: CV e sito

Quando compili `CV.tex` con latexmk (LaTeX Workshop in VS Code), il file `latexmkrc`
nella cartella del CV copia da solo il PDF in:

```
/Volumes/Alessandro/University/Website/assets/cv.pdf
```

I link "CV" della home del sito puntano a quel file.

## Se sposti qualcosa

- **Cartella del CV**: puoi spostarla dove vuoi, ma tieni insieme `CV.tex`,
  `resume.cls` e `latexmkrc`.
- **Cartella `Website`** (o se la rinomini): apri `latexmkrc` e aggiorna il
  percorso nella riga `my $site_cv = '…/assets/cv.pdf';`.
- **Nome del file** (se `CV.tex` diventa un altro nome): aggiorna anche `CV.pdf`
  dentro `latexmkrc`.

## Da ricordare

- La copia avviene solo compilando con latexmk. Con Overleaf o altri comandi
  devi copiare il PDF a mano in `assets/cv.pdf`.
- Dopo la compilazione il PDF è aggiornato solo sul computer: per pubblicarlo
  ricarica `assets/cv.pdf` su GitHub.
