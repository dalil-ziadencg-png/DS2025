# Rapport sur la base de données “Car Evaluation”

## 1. Introduction
La base de données **Car Evaluation** est un ensemble de données dérivé d’un **modèle de décision hiérarchique simple** conçu pour évaluer l’acceptabilité d’une voiture selon plusieurs critères.  
Elle est fréquemment utilisée dans le domaine de l’**apprentissage automatique** pour tester des méthodes de **classification**, de **construction de structure hiérarchique** et d’**induction constructive**.  

Cette base de données a été créée à partir du modèle de décision **DEX (Decision Expert)**, développé par **Marko Bohanec** et **Vladislav Rajkovič** afin de démontrer la méthodologie d’évaluation multicritère.

---

## 2. Contexte et origine
Le modèle initial, construit à l’aide de l’outil **DEX**, avait pour but d’aider à la **prise de décision** dans le choix d’un véhicule.  
Il reposait sur une structure hiérarchique claire :

- **CAR** (acceptabilité globale de la voiture)  
  - **PRICE** (prix global)  
    - buying (prix d’achat)  
    - maint (coût d’entretien)  
  - **TECH** (caractéristiques techniques)  
  - **COMFORT** (confort)  
    - doors (nombre de portes)  
    - persons (capacité de passagers)  
    - lug_boot (taille du coffre)  
  - **SAFETY** (sécurité estimée)  

Dans la version publique (UCI Machine Learning Repository), les niveaux intermédiaires ont été supprimés, ne conservant que les **6 attributs de base** directement liés à la **classe finale** (acceptabilité).

---

## 3. Description de la base de données

### 3.1 Caractéristiques générales
| Élément | Détail |
|----------|--------|
| **Nombre d’instances** | 1 728 |
| **Nombre d’attributs** | 6 attributs d’entrée + 1 attribut cible |
| **Type de données** | Catégorielles |
| **Valeurs manquantes** | Aucune |
| **Utilisation principale** | Classification, apprentissage hiérarchique, évaluation multicritère |

### 3.2 Attributs
| Attribut | Description | Valeurs possibles |
|-----------|--------------|------------------|
| **buying** | Prix d’achat | vhigh, high, med, low |
| **maint** | Coût d’entretien | vhigh, high, med, low |
| **doors** | Nombre de portes | 2, 3, 4, 5more |
| **persons** | Nombre de passagers | 2, 4, more |
| **lug_boot** | Taille du coffre | small, med, big |
| **safety** | Niveau de sécurité | low, med, high |
| **class (cible)** | Acceptabilité globale de la voiture | unacc, acc, good, vgood |

---

## 4. Objectifs et utilisation
Cette base de données est largement utilisée dans la **recherche en intelligence artificielle** et **data science** pour :

- Tester des algorithmes de **classification supervisée** (arbres de décision, SVM, réseaux de neurones, etc.)  
- Évaluer des méthodes de **constructive induction** (création de nouveaux attributs significatifs)  
- Expérimenter des techniques de **découverte de structure hiérarchique**  
- Enseigner la **décision multicritère** et la **modélisation hiérarchique** dans des contextes pédagogiques  

---

## 5. Intérêt pédagogique et scientifique
L’intérêt principal de la base **Car Evaluation** réside dans sa **simplicité apparente** et sa **structure cachée**.  
Bien que les données soient entièrement catégorielles, la logique hiérarchique sous-jacente permet d’aborder des sujets complexes tels que :

- La modélisation des préférences dans la décision  
- L’agrégation hiérarchique des critères  
- L’explicabilité des modèles de classification  
- L’évaluation qualitative d’options à partir de critères multiples  

Ainsi, cette base est à la fois un **outil d’expérimentation pratique** et un **support théorique** pour la compréhension des modèles décisionnels.

---

## 6. Conclusion
La base de données **Car Evaluation**, développée à partir du modèle **DEX** de Bohanec et Rajkovič, représente un excellent exemple de **modélisation décisionnelle hiérarchique** simplifiée.  
Grâce à ses données catégorielles structurées et à l’absence de valeurs manquantes, elle est idéale pour :
- l’expérimentation en apprentissage supervisé,  
- la recherche en induction de structure,  
- et l’enseignement de la décision multicritère.  

Sa popularité dans les études de machine learning s’explique par son équilibre entre **simplicité**, **interprétabilité** et **profondeur conceptuelle**.

---

## 7. QCM — Évaluation de compréhension

1. **Combien d’instances contient la base Car Evaluation ?**  
   - [ ] 1 000  
   - [ ] 1 500  
   - [x] 1 728  
   - [ ] 2 000  

2. **Combien d’attributs d’entrée comporte-t-elle (hors classe) ?**  
   - [ ] 4  
   - [ ] 5  
   - [x] 6  
   - [ ] 7  

3. **Quelle est la variable cible (classe) ?**  
   - [ ] low, medium, high  
   - [x] unacc, acc, good, vgood  
   - [ ] bad, average, good  
   - [ ] unacceptable, acceptable, excellent  

4. **Quel critère n’appartient pas à la hiérarchie d’origine ?**  
   - [ ] PRICE  
   - [ ] COMFORT  
   - [ ] SAFETY  
   - [x] TECH  

5. **Quel outil ou méthode a inspiré la création du modèle ?**  
   - [ ] AHP  
   - [x] DEX  
   - [ ] CART  
   - [ ] SVM  

6. **Quel attribut correspond à la taille du coffre ?**  
   - [ ] doors  
   - [ ] persons  
   - [x] lug_boot  
   - [ ] buying  

7. **De quel type sont les attributs de la base ?**  
   - [ ] Numériques continues  
   - [ ] Numériques discrètes  
   - [x] Catégorielles  
   - [ ] Mélange de types  

8. **Pour quel type de méthode cette base est-elle utile ?**  
   - [ ] Régression linéaire simple  
   - [ ] Clustering k-means uniquement  
   - [x] Découverte de structure / Induction constructive  
   - [ ] Séries temporelles  

9. **Y a-t-il des valeurs manquantes ?**  
   - [ ] Vrai  
   - [x] Faux  

10. **Quelles sont les valeurs possibles de l’attribut buying ?**  
   - [ ] low, med, high  
   - [x] vhigh, high, med, low  
   - [ ] cheap, moderate, expensive  
   - [ ] 0–100, 101–200, 201–300  
