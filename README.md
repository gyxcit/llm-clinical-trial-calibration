# PFE LaTeX Skeleton — Régis Likassi

Squelette LaTeX complet pour ton mémoire de fin d'études, conforme aux normes
Aivancity (PGE5 — AI & Data Science, 2025-2026).

## Structure des fichiers

```
pfe_skeleton/
├── main.tex                           ← Fichier principal, à compiler
├── README.md                          ← Ce fichier
├── chapters/
│   ├── 00_coverpage.tex               ← Page de couverture
│   ├── 01_acknowledgements.tex        ← Remerciements (1 p max)
│   ├── 02_abstract.tex                ← Abstract EN + keywords
│   ├── 03_resume_fr.tex               ← Résumé FR + mots-clés
│   ├── 04_abbreviations.tex           ← Liste des acronymes
│   ├── 05_introduction.tex            ← Chap 1 — Introduction (3-5 p)
│   ├── 06_state_of_the_art.tex        ← Chap 2 — SOTA (10-15 p)
│   ├── 07_project_context.tex         ← Chap 3 — Context (5-8 p)
│   ├── 08_methodology.tex             ← Chap 4 — Méthodologie (15-20 p)
│   ├── 09_results.tex                 ← Chap 5 — Résultats (10-15 p)
│   └── 10_conclusion.tex              ← Chap 6 — Conclusion (3-5 p)
├── appendices/
│   ├── A_detailed_tables.tex          ← Tableaux détaillés
│   ├── B_prompts.tex                  ← Prompts intégraux
│   ├── C_reliability_diagrams.tex     ← Reliability diagrams individuels
│   ├── D_code_availability.tex        ← Reproductibilité
│   └── E_ai_declaration.tex           ← Déclaration IA (obligatoire)
├── bibliography/
│   └── references.bib                 ← Bibliographie (BibTeX, IEEE style)
└── figures/                           ← Images (PNG/PDF) à ajouter
```

## Compilation

### Option A : Overleaf (recommandé, aucune installation)

1. Va sur https://www.overleaf.com
2. Créer un nouveau projet → Upload Project
3. Zippe le dossier `pfe_skeleton/` et upload
4. Overleaf compile automatiquement avec `main.tex`

### Option B : Installation locale (TeX Live ou MiKTeX)

```bash
cd pfe_skeleton
pdflatex main.tex
biber main
pdflatex main.tex
pdflatex main.tex
```

Ou avec `latexmk` (plus simple) :

```bash
latexmk -pdf main.tex
```

## Normes Aivancity respectées

- ✓ Latin Modern 12pt
- ✓ Line spacing 1.5
- ✓ Margins 2.5/3cm
- ✓ Justified body text
- ✓ Structure imposée (Cover → Ack → Abstract → TOC → LOF → LOT →
     Abbreviations → Intro → SOTA → Context → Methodology → Results →
     Conclusion → Bibliography → Appendices)
- ✓ Style IEEE pour la bibliographie
- ✓ Déclaration IA générative en annexe E
- ✓ Booktabs pour les tableaux professionnels
- ✓ Hyperref pour PDF navigable

## Ordre de rédaction recommandé

1. **Methodology** (chap 4) — le plus facile, tout est documenté
2. **Results** (chap 5) — tu as les données
3. **State of the Art** (chap 2) — synthèse des lectures
4. **Discussion** (dans chap 6) — interprétation des résultats
5. **Introduction** (chap 1) — écrite en connaissant tout
6. **Conclusion** (chap 6) — synthèse finale

## Personnalisation à faire

Chaque fichier `.tex` contient des `% [TODO — X pages]` qui indiquent :
- La longueur cible pour chaque section
- Le contenu attendu (structure et éléments à inclure)

Il te suffit de remplacer les TODO par ton contenu au fur et à mesure.

## Commandes personnalisées disponibles

- `\ece` → produit "ECE" en formatage cohérent
- `\rlhf` → produit "RLHF"
- `\model{Mistral-7B}` → nom de modèle en small caps
- `\begin{hypothesis}[H1] ... \end{hypothesis}` → hypothèses formelles
- `\begin{finding}[F1: Titre] ... \end{finding}` → findings originaux

## Nombres de pages ciblés

| Chapitre                | Pages cible | Aivancity |
|-------------------------|-------------|-----------|
| Introduction            | 3-5         | 3-5       |
| State of the Art        | 10-15       | 10-15     |
| Project Context         | 5-8         | 5-8       |
| Methodology             | 15-20       | 15-20     |
| Results                 | 10-15       | 10-15     |
| Conclusion              | 3-5         | 3-5       |
| **TOTAL**               | **46-68**   | **60-90** |
| Bibliography + Annexes  | libre       | libre     |

## Contact

Pour toute question sur le squelette, réfère-toi au notebook Kaggle et aux
rapports d'avancement mensuels transmis à ta directrice de recherche.

Bonne rédaction !
