# AI Business Assistant

Recueil de prompts construits et évalués progressivement pour un assistant IA polyvalent capable d'aider des collaborateurs à exploiter des documents, analyser des données, faire du machine learning et produire des résultats structurés.

Réalisé dans le cadre de l'**Atelier Prompt Engineering**.

## Contexte

Une entreprise souhaite mettre en place « AI Business Assistant », un assistant capable de traiter trois grands types d'entrées — **documents**, **données**, **questions** — et de produire une sortie structurée, vérifiée et évaluée.

```
AI BUSINESS ASSISTANT
        │
 ┌──────┼──────┐
 ↓      ↓      ↓
Documents Données Questions
 │      │      │
 ↓      ↓      ↓
Résumé  Analyse  LLM
Traduction ML/EDA │
Extraction Visualisation ↓
Classification    Réponse
 │              │
 └──────┬───────┘
        ↓
  Sortie structurée
        ↓
   Vérification
        ↓
Évaluation du prompt
```

## Structure du dépôt

```
ai-business_assistant/
│
├── README.md
├── partie1_anatomie.md              # Décomposition d'un prompt d'analyse d'avis clients
├── partie2_techniques_prompting.md  # Zero-shot / one-shot / few-shot / structuré
├── partie3_raisonnement.md          # Décomposition + auto-vérification
├── partie4_sorties_structurees.md   # JSON + règles de validation
├── partie5_applications_metier.md   # Résumé, traduction, ticket, facture, email
├── partie6_ml.md                    # Prompts ML sur le dataset de capteurs IoT
├── partie7_rag.md                   # Comparaison A/B/C avec et sans document (RAG)
├── partie8_evaluation.md            # Optimisation de prompt de résumé
├── partie9_bonus.md                 # Activité bonus proposée
└── documents/                       # Documents utilisés pour les tests
    ├── Contexte.pdf
    ├── Facture.pdf
    ├── Ticket.pdf
    ├── Doc_traduction.pdf
    ├── partie_5_prompt_1_doc_a_resume.pdf
    └── mesures_capteurs.csv
```

## Contenu par partie

| Partie | Sujet | Statut |
|---|---|---|
| 1 | Anatomie d'un prompt (analyse d'avis clients) | Traité |
| 2 | Comparaison zero-shot / one-shot / few-shot / structuré sur une classification de sentiment | Traité |
| 3 | Décomposition d'un prompt + auto-vérification (hallucinations, contradictions) | Traité |
| 4 | Sorties structurées JSON + règles de validation | Traité |
| 5 | Prompts métier : résumé, traduction, classification de ticket, extraction de facture, email client | Traité |
| 6 | Prompts ML sur le dataset de capteurs IoT (nettoyage, visualisations, modèles, métriques) | Traité |
| 7 | RAG : comparaison sans document / avec document / avec document + contraintes | Traité |
| 8 | Optimisation d'un prompt de résumé (3 versions) | En cours |
| 9 | Bonus | À faire |

## Documents utilisés pour les tests

- **`Contexte.pdf`** — fiche logistique interne (retard de livraison NovaTech) — utilisé pour la Partie 5 (email client)
- **`Facture.pdf`** — facture BureauPro Solutions — utilisée pour la Partie 5 (extraction de facture)
- **`Ticket.pdf`** — ticket support utilisateur (accès CRM) — utilisé pour la Partie 5 (classification de ticket)
- **`Doc_traduction.pdf`** — spécifications techniques d'infrastructure — utilisé pour la Partie 5 (traduction FR → EN)
- **`partie_5_prompt_1_doc_a_resume.pdf`** — rapport de fin de projet "ÉcoTri 2026" — utilisé pour les Parties 5 et 8 (résumé)
- **`mesures_capteurs.csv`** — relevés de capteurs IoT (température, humidité, pression, consommation, état) — utilisé pour la Partie 6 (ML)

## Méthodologie

Pour chaque partie :
1. Construire le(s) prompt(s) demandé(s), en explicitant les composantes (rôle, contexte, tâche, contraintes, format de sortie).
2. Tester le(s) prompt(s) avec un LLM.
3. Documenter la réponse obtenue.
4. Évaluer/comparer (pertinence, exactitude, respect des contraintes, absence d'hallucination).

## Enseignements clés

- Plus d'exemples (few-shot) améliore surtout le **format** de sortie, pas la **logique de décision** face à un cas ambigu.
- Une **règle de décision explicite** (prompt structuré) rend le comportement du modèle prévisible et justifiable.
- Sans document fourni, un modèle peut soit halluciner soit refuser de répondre — comportement non garanti. Avec document **et** contraintes de type RAG (contexte uniquement, signalement d'absence, citation de la source), la réponse devient fiable et vérifiable.
- Les contraintes de format (JSON, sections imposées) sont essentielles pour rendre une sortie exploitable automatiquement par une application.

## Livraison

- Dépôt GitHub public personnel, poussé d'abord vide.
- Mise à jour au fur et à mesure, avec un message de commit explicite après chaque tâche accomplie.

## Auteur

Rokhaya — P1 IA, Orange Digital Center
