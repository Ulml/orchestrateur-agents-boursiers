# Spécification interface — Visualisation de l'analyse boursière

## Vue carte (localisation sectorielle)

- Carte du monde ou de la zone d'étude (US, Europe, Asie selon l'univers)
- Un marqueur par ticker analysé, positionné sur son siège social ou son marché de cotation principal
- Couleur du marqueur = note finale (vert = 8-10, orange = 5-7, rouge = 1-4)
- Taille du marqueur = écart entre note et score sectoriel médian
- Au clic : panneau avec la fiche du titre, le rapport de l'agent, stop loss et cible suggérés
- Filtres : par note, par secteur GICS, par tendance (hausse / range / baisse sur la fenêtre de l'horizon), par capitalisation
- Couche optionnelle : heatmap sectorielle superposée (intensité de la note moyenne par secteur)

## Vue graphiques

- **Évolution des prix** : chandeliers OHLCV sur la fenêtre de l'horizon, avec bandes de Bollinger et projection
- **Volume** : histogramme aligné sous le prix, pour détecter les pics d'intérêt
- **Momentum** : RSI et MACD par ticker, petits multiples groupés par secteur
- **Distribution des notes** : histogramme des notes finales de l'univers entier
- **Tendances par paramètre** : petits multiples — un mini-graphique par paramètre du harness (PER, ROE, volume, sentiment...) sur la fenêtre ajustée
- **Matrice de corrélation** : note finale vs chaque paramètre, pour voir ce qui pèse dans le score
- **Graphe de synthèse** : réseau reliant secteurs, facteurs et signaux récurrents (reasoning atlas adapté)
- **Matrice de risque** : volatilité annualisée vs rendement attendu, type frontière efficiente

## Contraintes techniques

- Mise à jour en temps réel au fur et à mesure que les agents terminent
- Chaque graphique exportable en PNG ou SVG
- Mode sombre et mode clair
- Responsive desktop et tablette
- Alerte visuelle si un agent signale une donnée manquante au lieu de l'avoir réparée

## Lien avec le preprint

Le graphe de synthèse reprend l'idée du reasoning atlas de Sun et al. : entités (secteurs, facteurs, tickers) reliées par des preuves (rapports d'agents), au lieu d'une table triée.
