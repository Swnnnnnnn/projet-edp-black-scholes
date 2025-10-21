# Estimation de la volatilité à partir d’un problème inverse de l’équation de Black–Scholes

Ce dépôt présente un projet d’analyse numérique et d’optimisation réalisé dans le cadre de la formation en ingénierie mathématique à l’École des Mines de Nancy.  
Le travail a été mené avec **thibaud Ader** et **Ismail Wahoub**.

## Objectif du projet
L’objectif est d’estimer la volatilité implicite d’un actif financier à partir des prix observés d’options européennes.  
Le problème est formulé comme un **problème inverse de l’équation de Black–Scholes**, résolu à l’aide de méthodes numériques et d’outils d’optimisation.

## Méthodologie
1. **Problème direct** : résolution de l’équation de Black–Scholes pour un call européen à l’aide de schémas numériques.  
2. **Problème inverse** : estimation de la volatilité σ à partir de l’écart entre la solution observée et la solution calculée.  
3. **Méthode variationnelle** : introduction d’un multiplicateur de Lagrange et dérivation de l’**équation adjointe** pour exprimer le gradient du critère d’erreur.  
4. **Résolution numérique** :
   - Schéma de **Crank–Nicholson** pour les EDP directes et adjointes.  
   - Comparaison avec la **méthode des éléments finis (FEM)**.  
   - Analyse d’erreur et validation par rapport à la solution analytique.  
5. **Optimisation** :
   - Descente de gradient pour la minimisation de la fonction de coût.  
   - Comparaison avec l’algorithme de **Newton–Raphson**.

## Résultats principaux
- Le schéma de Crank–Nicholson offre une précision d’ordre 2 en temps et de bonnes propriétés de stabilité.  
- La méthode de la descente de gradient permet une convergence robuste vers la volatilité réelle (σ ≈ 0.25).  
- L’algorithme de Newton–Raphson converge plus rapidement mais est plus sensible à l’initialisation.  
- La méthode des éléments finis, dans ce contexte 1D, est moins adaptée que les différences finies.

## Compétences mobilisées
- Équations aux dérivées partielles (EDP) et méthodes numériques  
- Problèmes inverses et équations adjointes  
- Optimisation numérique (descente de gradient, Newton–Raphson)  
- Programmation scientifique en **Python (NumPy, SciPy, Matplotlib)**  
- Analyse d’erreur et validation numérique  
- Rédaction scientifique sous **LaTeX**


Tous les codes Python associés à ce projet sont présentés en annexe du rapport.
