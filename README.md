# Prompt de Validation E6 - BTS CIEL-IR

**Version : 0.2.0**

## Description

Ce prompt permet d'analyser et de valider automatiquement les fiches de présentation de projet pour l'épreuve E6 du BTS CIEL option Informatique et Réseaux. Il fournit une évaluation structurée en 6 étapes avec un système de validation progressif.

## Comment utiliser ce prompt

### 1. Préparation

Assurez-vous d'avoir :
- Le fichier `prompt_general_e6.md` (ce prompt)
- La fiche de présentation de projet à analyser (format .docx ou convertie en markdown)

### 2. Commande d'exécution

Pour lancer l'analyse, utilisez la commande suivante avec votre assistant IA :

```
Analyser la fiche de présentation projet E6 fournie en suivant le processus de validation en 6 étapes avec gates de validation à 75%.
```

### 3. Fournir le document à analyser

Après avoir lancé la commande, fournissez le document de la fiche de présentation du projet :
- Soit en copiant le contenu du fichier
- Soit en indiquant le chemin vers le fichier si l'outil de conversion est disponible

### 4. Conversion automatique (optionnel)

Si disponible, l'outil `/usr/local/bin/convert_pandoc` peut être utilisé pour convertir automatiquement un fichier .docx en markdown :

```bash
/usr/local/bin/convert_pandoc fichier_entree.docx fichier_sortie.md
```

## Processus de validation

Le prompt analyse le document selon **6 étapes séquentielles** :

1. **Conformité formelle** - Vérification de la structure et des sections obligatoires
2. **Complétude administrative** - Contrôle des informations administratives et du contexte entreprise
3. **Analyse du contenu projet** - Évaluation de la qualité de la description du projet
4. **Vérification technique** - Contrôle des aspects techniques et architecturaux
5. **Alignement compétences E6** - Vérification de la couverture des 4 compétences (C01, C03, C08, C10)
6. **Validation pédagogique finale** - Évaluation globale pour la commission du rectorat

## Système de notation

Chaque étape est notée sur une échelle de 0 à 4 :

- **0** : Non conforme / Absent
- **1** : Insuffisant (< 25%)
- **2** : Partiel (25-50%)
- **3** : Satisfaisant (50-75%) ✓
- **4** : Complet (> 75%) ✓✓

### Gate de validation

**Règle importante** : Une étape doit obtenir une note **≥ 3** pour être validée.

- Si note ≥ 3 : Passage à l'étape suivante
- Si note < 3 : ARRÊT du processus, le document doit être corrigé

## Résultats fournis

À la fin de l'analyse, vous recevrez :

1. **Notes détaillées** pour chaque étape validée
2. **Tableau récapitulatif** avec un score global sur 24
3. **Liste des points forts** du dossier
4. **Top 5 des améliorations prioritaires** avec actions concrètes
5. **Message personnalisé** pour l'étudiant
6. **Prochaines étapes** selon le résultat (validé ou à reprendre)
7. **Décision finale** : Validation pour le rectorat ou demande de corrections

## Compétences évaluées

Le prompt vérifie la couverture des 4 compétences obligatoires :

- **C01** : Communiquer en situation professionnelle
- **C03** : Gérer un projet
- **C08** : Coder
- **C10** : Exploiter un réseau informatique

## Support

Pour toute question sur l'utilisation du prompt ou l'interprétation des résultats, consultez :
- La documentation complète dans `prompt_general_e6.md`
- Le référentiel BTS CIEL
- Votre tuteur ou professeur responsable

---

*Dernière mise à jour : Version 0.2.0*
