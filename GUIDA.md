# Come modificare il sito da solo

## 1. Cosa serve (una volta sola)
- **VS Code** (editor): https://code.visualstudio.com
- **Live Sass Compiler** (estensione di VS Code, di Glenn Marks): compila lo SCSS in CSS da sola ogni volta che salvi.
- **Live Server** (estensione di VS Code): apre il sito nel browser e lo ricarica a ogni salvataggio.
- **GitHub Desktop**: https://desktop.github.com, per caricare le modifiche online senza usare il terminale. Al primo avvio accedi con l'account `masterx567`, poi *File → Add local repository* e scegli questa cartella.

## 2. Dove sta cosa
| Voglio cambiare... | File |
|---|---|
| Testi della home, progetti, numeri | `index.html` |
| Esperienze, formazione, lingue | `cv.html` |
| Form e card dei contatti | `contatti.html` |
| Colori, font | `scss/_variables.scss` |
| Stile (spazi, bordi, griglie) | `scss/main.scss` |
| Foto | `img/profile.jpg` (sostituiscila con lo stesso nome) |
| Presentazioni dei progetti | cartella `progetti/` |
| Presentazione PDF della consegna | `presentazione/slides.html` |

**Non modificare `css/main.css` a mano**: viene rigenerato dallo SCSS.

## 3. Fare una modifica
1. Apri la cartella in VS Code (*File → Apri cartella*).
2. Clicca **Watch Sass** in basso nella barra blu (serve solo se tocchi i file `.scss`).
3. Tasto destro su `index.html` → **Open with Live Server**.
4. Modifica e salva (Ctrl+S): il browser si aggiorna da solo.

Esempi:
- **Cambiare un colore**: in `scss/_variables.scss` cambia `$viola: #6c4cf0;` con un altro codice colore.
- **Aggiungere un progetto**: in `index.html` copia un blocco `<a class="card-progetto ...">...</a>` dentro la sezione `<!-- SEZIONE PROGETTI (grid) -->`, cambia titolo, testo e `href` (il file va messo in `progetti/`).
- **Aggiungere un'esperienza al CV**: in `cv.html` copia un `<li>...</li>` dentro `<ol class="timeline">`.

## 4. Pubblicare online
1. Apri GitHub Desktop: a sinistra vedi i file modificati.
2. In basso scrivi una frase (es. "Aggiunto progetto X") e clicca **Commit to main**.
3. Clicca **Push origin** in alto.
4. Dopo 1-2 minuti le modifiche sono su https://masterx567.github.io/sito-personale/ (se non le vedi: Ctrl+F5).

## 5. Rigenerare la presentazione PDF
1. Apri `presentazione/slides.html` con **Microsoft Edge** o Chrome.
2. Ctrl+P → Destinazione **Salva come PDF**.
3. In *Altre impostazioni*: margini **Nessuno**, spunta **Grafica di sfondo**, togli **Intestazioni e piè di pagina**.
4. Salva come `presentazione-sito-personale.pdf`.
