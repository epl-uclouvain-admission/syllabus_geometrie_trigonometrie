# Syllabus de Trigonométrie et de Géométrie — Examen d'admission UCLouvain (EPL)

[![Build LaTeX PDF](https://github.com/epl-uclouvain-admission/syllabus_geometrie_trigonometrie/actions/workflows/build-pdf.yml/badge.svg)](https://github.com/epl-uclouvain-admission/syllabus_geometrie_trigonometrie/actions/workflows/build-pdf.yml)

Bienvenue sur le dépôt officiel du **Syllabus de Trigonométrie et de Géométrie** destiné à la préparation de l'épreuve fusionnée de trigonométrie et de géométrie de l'**examen spécial d'admission aux études d'ingénieur civil** à l'[UCLouvain](https://uclouvain.be/fr/facultes/epl) (École Polytechnique de Louvain — EPL).

---

## 📥 Télécharger le syllabus (PDF)

Le document PDF est compilé automatiquement à chaque mise à jour du dépôt via GitHub Actions :

- 👉 **[Télécharger la dernière version du PDF (`syllabus_geometrie_trigonometrie_uclouvain.pdf`)](https://github.com/epl-uclouvain-admission/syllabus_geometrie_trigonometrie/releases/download/latest/syllabus_geometrie_trigonometrie_uclouvain.pdf)** *(lien direct issu de la dernière release)*
- 📄 Vous pouvez également consulter la page des **[Releases](https://github.com/epl-uclouvain-admission/syllabus_geometrie_trigonometrie/releases/tag/latest)** ou récupérer l'artefact généré dans l'onglet **[Actions](https://github.com/epl-uclouvain-admission/syllabus_geometrie_trigonometrie/actions)**.

---

## 📚 Contenu de l'ouvrage

Ce syllabus couvre l'ensemble de la matière de l'épreuve fusionnée de trigonométrie et de géométrie (qui se déroule **sans calculatrice**) ainsi que de nombreux exemples résolus et exercices issus des annales de l'examen d'entrée (2018–2026) :

1. **Chapitre 1 — Fondements et cercle trigonométrique** (`chap1_fondements.tex`) : angles, radians, cercle trigonométrique, valeurs remarquables, angles associés, fonctions trigonométriques et réciproques ($\arcsin$, $\arccos$, $\arctan$).
2. **Chapitre 2 — Les grandes formules trigonométriques** (`chap2_formules.tex`) : formules d'addition, de duplication, de Carnot, de Simpson, factorisation et linéarisation.
3. **Chapitre 3 — Équations et inéquations trigonométriques** (`chap3_equations.tex`) : équations fondamentales, méthodes de réduction, conditions d'existence et représentation des solutions sur le cercle.
4. **Chapitre 4 — Résolution des triangles** (`chap4_triangles.tex`) : triangles rectangles, loi des sinus, théorème d'Al-Kashi (loi des cosinus), aires et applications géométriques.
5. **Chapitre 5 — Géométrie synthétique plane et spatiale** (`chap5_geo_synthetique.tex`) : angles inscrits et au centre, puissance d'un point par rapport à un cercle, triangles semblables, théorème de Thalès, relations métriques, rapports d'aires et de volumes, sections planes de solides (sphères, cônes, cylindres).
6. **Chapitre 6 — Géométrie analytique dans le plan et coniques** (`chap6_geo_plane.tex`) : vecteurs et produit scalaire dans $\mathbb{R}^2$, droites, distances, cercles et étude complète des coniques (ellipse, hyperbole, parabole, tangentes).
7. **Chapitre 7 — Géométrie analytique et vectorielle dans l'espace $\mathbb{R}^3$** (`chap7_geo_espace.tex`) : produit scalaire, produit vectoriel, produit mixte, équations cartésiennes et paramétriques de droites et de plans, projections orthogonales, symétries, distances et sphères.
8. **Chapitre 8 — Formulaire récapitulatif** (`chap5_formulaire.tex`) : synthèse imprimable de toutes les formules essentielles de trigonométrie et de géométrie.
9. **Annexe — Raisonnement logique, conditions nécessaires et suffisantes** (`annexe_logique.tex`) : implication, équivalence, contraposée et pièges classiques lors de la résolution d'équations.
10. **Chapitre 9 — Corrigés détaillés des exercices** (`chap6_correctifs.tex`) : solutions complètes et commentées de tous les exercices de fin de chapitre.

---

## 🛠️ Compilation locale

Pour compiler le syllabus sur votre machine, vous devez disposer d'une distribution $\LaTeX$ complète (par exemple **TeX Live** ou **MacTeX**) incluant `pdflatex`, `latexmk` ainsi que les packages standards (`tikz`, `pgfplots`, `tcolorbox`, `amsmath`, `babel`, etc.).

Exécutez simplement la commande suivante à la racine du dépôt :

```bash
latexmk -pdf -interaction=nonstopmode main.tex
```

Ou avec `pdflatex` (deux passes sont nécessaires pour générer la table des matières et les références croisées) :

```bash
pdflatex main.tex
pdflatex main.tex
```

Le fichier généré s'intitule `main.pdf`.

---

## 👥 Auteurs, direction et sources

- **Direction artistique & *Prompt Engineering*** : **Hadrien Rattez**, **Jean-François Remacle** et **Pierre Schaus** (équipe trigonométrie & géométrie de l'examen d'admission à l'EPL — UCLouvain).
- **Rédaction et mise en forme $\LaTeX$ / TikZ** : assistée par Intelligence Artificielle sous la supervision des enseignants.
- **Sources** :
  - L'excellent syllabus *« Synthèse de trigonométrie »* rédigé par **Yvan Haine** et **Pierre Joris** (Août 2012, Université de Liège — ULiège), suite à une suggestion du Professeur E. Delhez, a servi de source principale pour structurer et inspirer la partie trigonométrique.
  - Les supports des cours préparatoires, formulaires et annales d'examens d'admission de l'**UCLouvain** (2018 à 2026).

---

## 🤝 Signaler une coquille ou contribuer

Si vous repérez une coquille dans un énoncé, une figure ou un corrigé, n'hésitez pas à ouvrir une **[Issue](https://github.com/epl-uclouvain-admission/syllabus_geometrie_trigonometrie/issues)** ou à proposer une **[Pull Request](https://github.com/epl-uclouvain-admission/syllabus_geometrie_trigonometrie/pulls)**.
