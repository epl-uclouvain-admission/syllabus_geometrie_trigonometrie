# AGENTS.md — Guide pour les Agents IA (Syllabus de Trigonométrie et de Géométrie UCLouvain)

Ce dépôt contient les sources $\LaTeX$ du **Syllabus de Trigonométrie et de Géométrie** destiné à la préparation de l'examen spécial d'admission aux études d'ingénieur civil à l'**UCLouvain** (École Polytechnique de Louvain — EPL).

## 1. Architecture du projet

- `main.tex` : Fichier maître $\LaTeX$ (classe `book`, `11pt`, `a4paper`, `oneside`, marges de `2.5cm`). Définit les couleurs institutionnelles UCLouvain (`uclblue`, `ucllightblue`, `uclaccent`, etc.), les environnements `tcolorbox` (`theoreme`, `definition`, `exemple`, `attention`, `astuce`) et inclut tous les chapitres.
- `chap1_fondements.tex` : Chapitre 1 — Fondements et cercle trigonométrique.
- `chap2_formules.tex` : Chapitre 2 — Les grandes formules trigonométriques.
- `chap3_equations.tex` : Chapitre 3 — Équations et inéquations trigonométriques.
- `chap4_triangles.tex` : Chapitre 4 — Résolution des triangles.
- `chap5_geo_synthetique.tex` : Chapitre 5 — Géométrie synthétique plane et spatiale.
- `chap6_geo_plane.tex` : Chapitre 6 — Géométrie analytique dans le plan et coniques.
- `chap7_geo_espace.tex` : Chapitre 7 — Géométrie analytique et vectorielle dans l'espace $\mathbb{R}^3$.
- `chap5_formulaire.tex` : Chapitre 8 — Formulaire synthétique imprimable en 4 pages (marges réduites à `1.4cm`, 2 colonnes).
- `annexe_logique.tex` : Annexe — Raisonnement logique, conditions nécessaires et suffisantes.
- `chap6_correctifs.tex` : Chapitre 9 — Corrigés détaillés de tous les exercices de fin de chapitre.
- `.github/workflows/build-pdf.yml` : Workflow GitHub Actions compilant `main.tex` à chaque push/PR sur `main`, publiant l'artefact PDF et mettant à jour la release `latest` (`main.pdf` et `syllabus_geometrie_trigonometrie_uclouvain.pdf`).

## 2. Règles d'édition et de mise en page ($\LaTeX$)

1. **Zéro débordement (`Overfull \hbox`)** :
   - Après toute modification d'un fichier `.tex`, compilez avec `pdflatex -interaction=nonstopmode main.tex` (ou `latexmk -pdf main.tex`) et vérifiez dans `main.log` qu'aucun avertissement `Overfull \hbox` n'apparaît (`grep "Overfull" main.log`).
   - Si une équation hors texte (`\[ ... \]`) est trop longue ou comporte un `\boxed{...}` large, découpez-la sur plusieurs lignes avec `\begin{align*} ... \end{align*}` ou réduisez les espacements (`\quad` au lieu de `\qquad`).
   - Dans les listes d'exercices de fin de chapitre, utilisez systématiquement `\begin{enumerate}[label=\textbf{Exercice X.\arabic* --}, align=left, leftmargin=*]` afin que les numéros à deux chiffres (ex. `Exercice X.10`) ne débordent jamais dans la marge gauche.
2. **Figures TikZ / PGFPlots** :
   - Toutes les figures sont dessinées directement en TikZ/PGFPlots (aucune image externe requise).
   - Veillez à ce que la largeur totale d'une figure (ou de sous-figures placées côte à côte avec `\begin{scope}[shift={(...)}]`) ne dépasse jamais `\textwidth` ($16\text{ cm}$ dans les chapitres standards).
3. **Conventions mathématiques UCLouvain** :
   - Les fonctions réciproques se notent exclusivement `\arcsin`, `\arccos`, `\arctan` (jamais `\sin^{-1}`).
   - L'épreuve se déroule sans calculatrice : privilégiez toujours les valeurs exactes, le raisonnement géométrique et la vérification explicite des conditions d'existence (CE).
   - Chaque nouvel exercice ajouté à la fin d'un chapitre (`chap1` à `chap7`) doit avoir son corrigé complet correspondant dans `chap6_correctifs.tex`.
4. **Fichiers suivis par Git** :
   - Seuls les fichiers sources (`.tex`, `README.md`, `AGENTS.md`, `.gitignore`, `.github/workflows/build-pdf.yml`) doivent être suivis par Git. Ne commitez pas les fichiers auxiliaires (`.aux`, `.log`, `.out`, `.toc`) ni les `.pdf` générés localement.
