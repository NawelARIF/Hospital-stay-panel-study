# Hospital-stay-panel-study
Analyse économétrique de l’impact des équipements médicaux sur la durée des séjours hospitaliers (données de panel).

# 🏥 Impact des investissements en équipements médicaux sur la durée des séjours hospitaliers

## 📖 Objectif de l'étude
L’objectif de ce projet est d’analyser si **les investissements en équipements médicaux** (IRM, scanners CT) et **l’expansion de la capacité hospitalière** (nombre de lits) contribuent à **réduire la durée moyenne des séjours hospitaliers**.  
Cette question est essentielle pour les politiques de santé publique, car elle touche directement :
- l’efficacité du système hospitalier,
- l’optimisation des coûts,
- la qualité des soins pour les patients.

---

## 🧠 Démarche méthodologique

### 1️⃣ Collecte des données
Les données proviennent de [Kaggle – Healthcare Investments and Length of Hospital Stay](https://www.kaggle.com/datasets/babyoda/healthcare-investments-and-length-of-hospital-stay).  
Elles couvrent :
- 32 pays,
- la période **1990 – 2018**,
- les variables suivantes : durée moyenne des séjours, nombre d’IRM, nombre de scanners CT, nombre de lits pour 1 000 habitants.

---

### 2️⃣ Statistiques descriptives
- La durée moyenne des séjours est de **7,14 jours** en moyenne.
- Les pays présentent une **forte hétérogénéité** dans leurs équipements (IRM et scanners CT).
- Première observation : une **corrélation négative** semble exister entre équipements et durée des séjours → mais il faut vérifier si elle est causale.

---

### 3️⃣ Modélisation économétrique
Pour isoler l’effet des équipements médicaux :
- Un **modèle de panel à effets fixes bidirectionnels** est utilisé.
- Les effets fixes permettent de **contrôler les spécificités propres à chaque pays et à chaque année**.
- Plusieurs modèles ont été testés :
  - **Pooled OLS** (non retenu, biaisé),
  - **Effets aléatoires (FGLS)** (rejeté par le test de Hausman),
  - **Effets fixes (WITHIN)** → retenu car le plus robuste.

---

### 4️⃣ Résultats clés
- **CT Scanners** : effet **négatif et significatif** → un nombre plus élevé réduit la durée des séjours.
- **Nombre de lits d’hôpital** : effet **négatif et significatif** → une plus grande capacité réduit la durée d’hospitalisation.
- **IRM** : effet non significatif.

---

### 5️⃣ Conclusion
L’étude confirme que les investissements dans les infrastructures hospitalières, en particulier les scanners CT et l’augmentation du nombre de lits, contribuent à réduire la durée des séjours hospitaliers.  
Des recherches futures pourraient inclure :
- de nouvelles variables (qualité des soins, réformes hospitalières),
- des modèles économétriques plus avancés (variables instrumentales) pour mieux traiter l’endogénéité.

---

## 📂 Contenu du dépôt
- **ARIF Nawel Panel.pdf** → Rapport complet détaillant l’analyse et les résultats.
- **README.md** → Résumé de la démarche.

---

## 👩‍💻 Auteur
**Nawel Arif**  
Master Data Science pour l’Économie et l’Entreprise – Université de Strasbourg
