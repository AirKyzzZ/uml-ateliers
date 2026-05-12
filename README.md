# Ateliers UML

Ce dépôt contient les sources PlantUML et les exports PNG des ateliers UML.

## Atelier 1

- `Atelier1/etape1.pu` et `Atelier1/etape1.png` : services client.
- `Atelier1/etape2.pu` et `Atelier1/etape2.png` : administration et maintenance.
- `Atelier1/etape3.pu` et les exports PNG associés : délestage.
- `Atelier1/rendu.tex` : wrapper LaTeX du rendu.

## Atelier 2

- `Atelier2/recharger_vehicule.pu` et `Atelier2/recharger_vehicule.png` : diagramme d'activité du processus « Recharger son véhicule ».
- `Atelier2/schema_final.tex` : wrapper LaTeX minimal pour générer le PDF du schéma final.
- `Atelier2/rendu.tex` : wrapper LaTeX avec une page de titre et le schéma.

Les fichiers PDF et logs LaTeX générés sont volontairement ignorés pour garder le dépôt propre.

## Génération locale

Depuis la racine du dépôt :

```sh
plantuml -tpng Atelier2/recharger_vehicule.pu
cd Atelier2
pdflatex -interaction=nonstopmode -halt-on-error -jobname=schema_final schema_final.tex
pdflatex -interaction=nonstopmode -halt-on-error rendu.tex
```
