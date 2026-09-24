Schéma du Projet : Intégration Git (UiPath) & Automation Ops

Voici une représentation visuelle de la timeline du projet sous forme de diagramme de Gantt.
```mermaid
%%{init: {
  "theme":"base",
  "themeVariables": {
    "fontFamily":"Inter, Arial, sans-serif",
    "primaryColor":"#0d6efd",
    "primaryBorderColor":"#0b5ed7",
    "primaryTextColor":"#ffffff",
    "lineColor":"#6c757d",
    "ganttSectionBkgColor":"#eef4ff",
    "ganttSectionBkgColor2":"#e9f7ef",
    "ganttCriticalTaskColor":"#dc3545",
    "ganttCriticalTaskTextColor":"#ffffff"
  }
}}%%
gantt
title Timeline Projet : Intégration Git (UiPath) – 8 Semaines
dateFormat  YYYY-MM-DD
axisFormat  S%W
excludes    weekends

section Phase 1 – Préparation (S1–S2)
Ticket Déblocage Flux (T1)      :crit, t1, 2025-10-28, 14d
Atelier Règles Draft (T2)       :t2,  after t1, 7d
Définir Périmètre POC (T3)      :t3,  after t2, 7d

section Phase 2 – Exécution POC (S3–S5)
POC P1 – Tests Initiaux (T4_1)  :t4_1, after t3, 7d
Analyse Pipelines (T3_1)        :t3_1, after t4_1, 7d
POC P2 – Tests Workflow (T4_2)  :t4_2, after t3_1, 7d
Analyse Déploiement (T3_2)      :t3_2, after t4_2, 7d
POC P3 – Validation (T4_3)      :t4_3, after t3_2, 7d
Rédaction Compte-rendu          :cr,   after t4_3, 7d

section Phase 3 – Finalisation (S6–S8)
Atelier Règles Final (T2_F)     :t2f,   after cr, 7d
Guide Bonnes Pratiques          :guide, after t2f, 7d
Préparation Démo (T5_1)         :t5_1,  after guide, 7d
Exécution Démo (T5_2)           :t5_2,  after t5_1, 7d
Bilan & Plan Déploiement        :bilan, after t5_2, 7d
Clôture POC                     :clot,  after bilan, 7d

```

Explication de la lecture :

Le diagramme est basé sur une durée en jours (7 jours = 1 semaine).

L'axe horizontal représente le nombre de jours depuis le début du projet (0, 7, 14... jusqu'à 56).

Phase 1 couvre les 2 premières semaines (jours 0-14).

Phase 2 couvre les 3 semaines suivantes (jours 14-35).

Phase 3 couvre les 3 dernières semaines (jours 35-56).

Le "Ticket Déblocage Flux" est marqué comme "critique" (crit) car beaucoup d'autres tâches en dépendent.