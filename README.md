# CV — LaTeX

My résumé/CV, written in LaTeX for full control over layout and typography. The content is split from the layout so I can tailor the CV to a specific job offer by editing a single small file.

🇫🇷 [Lire en français](#français) | 🇬🇧 [Read in English](#english)

---

## English

📄 **[Download the PDF](cv_lucas_vacquie.pdf)**

This repository contains the LaTeX source for my CV, along with the custom font and icon assets used in the design.

### Structure (English)

```text
cv-latex/
├── cv_lucas_vacquie.tex     ← layout (design, positioning) — rarely touched
├── cv_banque_contenus.tex   ← content bank: every experience/project/
│                               commitment I could put on the CV, as macros
├── selection_classique.tex       ← content SELECTION for a given application
│                               (which macros from the bank to show, and in
│                               which order) — this is the file to edit
├── cv_lucas_vacquie.pdf     ← compiled PDF (always up to date)
├── Photos/                  ← personal photos used for the CV
├── Oswald/                  ← custom font used in the design
└── Pictogramme/             ← icons used in the design
```

### Adapting the CV to a specific job offer

1. Duplicate `selection_classique.tex` into `selection_<company>.tex`.
2. Inside, edit:
   - `\Profil` — pick a variant from the bank (`\ProfilIngenierieSysteme`, `\ProfilEmbarqueLogiciel`, `\ProfilGeneraliste`) or write a custom paragraph.
   - `\Competences` and `\OutilsLangages` — lists of `\item`s; pick from the reserve at the end of `cv_banque_contenus.tex` or add your own.
   - `\SelectionExperience`, `\SelectionAssociatif`, `\SelectionProjets` — which items from `cv_banque_contenus.tex` to display, and in what order.
3. In `cv_lucas_vacquie.tex`, change the single line:

   ```latex
   \input{selection_classique.tex}
   ```

   to point to the new selection file.
4. Recompile and check the page still fits (the background height is fixed, so adding/removing items can under- or overflow the page).

The layout file itself should not need to change between applications — only the selection file does.

### Build it yourself

```bash
xelatex cv_lucas_vacquie.tex
```

(Requires a LaTeX distribution such as TeX Live or MacTeX.)

### Why LaTeX?

Full control over layout, consistent typography, and version-controlled updates — no fighting with a Word template every time I need to update a line, and no risk of breaking the design when I only want to swap out content for a new application.

---

## Français

📄 **[Télécharger le PDF](cv_lucas_vacquie.pdf)**

Ce dépôt contient le code source LaTeX de mon CV, avec la police et les icônes utilisées dans la mise en page. Le contenu est séparé de la mise en page pour pouvoir adapter le CV à une offre précise en éditant un seul petit fichier.

### Structure

```text
cv-latex/
├── cv_lucas_vacquie.tex     ← mise en page (design, positionnement) —
│                               rarement modifié
├── cv_banque_contenus.tex   ← banque de contenus : toutes les expériences/
│                               projets/engagements possibles, sous forme
│                               de macros
├── selection_classique.tex       ← SÉLECTION de contenus pour une candidature
│                               donnée (quelles macros de la banque afficher,
│                               dans quel ordre) — c'est le fichier à éditer
├── cv_lucas_vacquie.pdf     ← PDF compilé (toujours à jour)
├── Photos/                  ← photos personnelles utilisées pour le CV
├── Oswald/                  ← police personnalisée utilisée
└── Pictogramme/             ← icônes utilisées dans la mise en page
```

### Adapter le CV à une offre précise

1. Dupliquer `selection_classique.tex` en `selection_<entreprise>.tex`.
2. Éditer :
   - `\Profil` — choisir une variante de la banque (`\ProfilIngenierieSysteme`, `\ProfilEmbarqueLogiciel`, `\ProfilGeneraliste`) ou écrire un paragraphe sur mesure.
   - `\Competences` et `\OutilsLangages` — listes de `\item` ; piocher dans la réserve en fin de `cv_banque_contenus.tex` ou en ajouter.
   - `\SelectionExperience`, `\SelectionAssociatif`, `\SelectionProjets` — les éléments de `cv_banque_contenus.tex` à afficher, et dans quel ordre.
3. Dans `cv_lucas_vacquie.tex`, changer uniquement la ligne :

   ```latex
   \input{selection_classique.tex}
   ```

   pour pointer vers le nouveau fichier de sélection.
4. Recompiler et vérifier que tout tient sur la page (le fond a une hauteur fixe, donc ajouter/retirer des éléments peut créer du vide ou un débordement).

Le fichier de mise en page ne devrait pas avoir besoin de changer entre deux candidatures — seul le fichier de sélection change.

### Compiler soi-même

```bash
xelatex cv_lucas_vacquie.tex
```

(Nécessite une distribution LaTeX comme TeX Live ou MacTeX.)

### Pourquoi LaTeX ?

Un contrôle total sur la mise en page, une typographie cohérente, et un suivi de version propre — plus besoin de lutter avec un template Word à chaque mise à jour, et aucun risque de casser le design en voulant simplement changer de contenu pour une nouvelle candidature.
