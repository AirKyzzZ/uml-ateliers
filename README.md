# Atelier 2 UML - Recharger son véhicule

Ce dépôt contient les sources du diagramme d'activité de l'Atelier 2 : processus « Recharger son véhicule ».

## Contenu utile

- `Atelier2/recharger_vehicule.pu` : source PlantUML du diagramme d'activité.
- `Atelier2/recharger_vehicule.png` : export PNG du diagramme pour une lecture directe.
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
