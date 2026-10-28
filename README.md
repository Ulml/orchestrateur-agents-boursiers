# Orchestrateur d'agents distribués — Bourse

Prompt d'orchestrateur pour un système multi-agents d'analyse boursière, généré par le méta-orchestrateur à partir du modèle du dépôt immobilier.

## Principe

- **Un agent par ticker** : chaque sous-agent reçoit un harness standard (fiche du titre, contexte de stratégie, outils, données contextuelles, tendances)
- **Période de tendance ajustable** : scalping (heures), day trading (jours), swing (semaines), position (mois) — calibrée sur l'horizon de l'utilisateur
- **Auto-réparation** : si un élément du harness manque, un agent dédié le génère selon le SOTA ; si c'est impossible, signalement explicite, jamais d'invention
- **Synthèse transversale** : l'orchestrateur fusionne les rapports et ne remonte que les patterns (secteurs surévalués, facteurs dominants, signaux récurrents)
- **Interface** : carte sectorielle, graphiques de momentum, matrice de risque, graphe de synthèse

## Fichiers

- `PROMPT_ORCHESTRATEUR.md` : le prompt complet, prêt à coller
- `UI_SPEC.md` : spécification de l'interface visuelle

## Inspiration

Modèle issu du preprint *Distributed AI agents enable comprehensive discovery of biological insights at scale* (Sun et al., 2026) : https://doi.org/10.64898/2026.10.15.759436

Généré via `AGENT_META_ORCHESTRATEUR.md` du dépôt https://github.com/Ulml/orchestrateur-agents-immobiliers

## Avertissement

Les sorties de ce système sont des analyses, pas des conseils financiers. Toute décision d'investissement reste de la responsabilité de l'utilisateur.
