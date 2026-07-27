# CV — LaTeX

My résumé/CV, written in LaTeX for full control over layout and typography.

🇫🇷 [Lire en français](#français) | 🇬🇧 [Read in English](#english)

---

## English

📄 **[Download the PDF](CV_3.pdf)**

This repository contains the LaTeX source for my CV, along with the custom font and icon assets used in the design.

### Structure

```
cv-latex/
├── CV_3.tex        ← LaTeX source
├── CV_3.pdf        ← compiled PDF (always up to date)
├── Photos/         ← Personal photos used for the CV
├── Oswald/         ← custom font used in the design
└── Pictogramme/    ← icons used in the design
```

### Build it yourself

```bash
xelatex CV_3.tex
```

(Requires a LaTeX distribution such as TeX Live or MacTeX.)

### Why LaTeX?

Full control over layout, consistent typography, and version-controlled updates — no fighting with a Word template every time I need to update a line.

---

## Français

📄 **[Télécharger le PDF](CV_3.pdf)**

Ce dépôt contient le code source LaTeX de mon CV, avec la police et les icônes utilisées dans la mise en page.

### Structure

```
cv-latex/
├── CV_3.tex        ← code source LaTeX
├── CV_3.pdf        ← PDF compilé (toujours à jour)
├── Photos/         ← photos personnelles utilisées pour le CV
├── Oswald/         ← police personnalisée utilisée
└── Pictogramme/    ← icônes utilisées dans la mise en page
```

### Compiler soi-même

```bash
xelatex CV_3.tex
```

(Nécessite une distribution LaTeX comme TeX Live ou MacTeX.)

### Pourquoi LaTeX ?

Un contrôle total sur la mise en page, une typographie cohérente, et un suivi de version propre — plus besoin de lutter avec un template Word à chaque mise à jour.
