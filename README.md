# Audit de Qualité de Données : Impact de l'IA sur le Marché de l'Emploi (2030)

## 📌 Contexte & Problématique Métier
Ce projet avait pour objectif initial d'analyser comment le niveau d'études et les compétences allaient influencer le risque de remplacement des métiers par l'IA d'ici 2030. 

Cependant, une analyse exploratoire approfondie (EDA) a permis de lever une alerte majeure sur la structure même des données. Ce projet s'est donc transformé en un **Audit de Qualité des Données** afin de démontrer l'importance de l'esprit critique avant toute phase de modélisation.

## 🔍 Méthodologie & Constats Clés

### 1. Le Paradoxe du Niveau d'Études
En analysant la distribution du risque de remplacement par l'IA (`AI_Replacement_Risk`) selon le niveau d'études (`Education_Level`), les résultats montrent une uniformité parfaite (médianes toutes alignées à ~50%). Visuellement, les distributions se chevauchent entièrement, indiquant qu'un PhD n'est statistiquement ni plus ni moins protégé qu'un diplômé du secondaire.

### 2. Le Signal Alerte : L'Analyse des Compétences
La désimbrication de la variable `Required_Skills` a révélé le même phénomène : qu'il s'agisse de compétences purement humaines (*Leadership*, *Communication*) ou de compétences hautement techniques (*TensorFlow*, *AWS*), le score de risque moyen reste bloqué artificiellement autour de 0.50.

### 3. Preuve Mathématique (Matrice de Corrélation)
La Heatmap des variables numériques montre des coefficients de corrélation quasi-nuls (proches de `0.00`) entre l'expérience, le salaire et le risque IA. Dans un marché réel, ces variables sont interdépendantes. 

## 💡 Conclusion de l'Audit
**Verdict :** Ce dataset est identifié comme **100% synthétique (généré artificiellement)** de manière aléatoire. 
* **Impact Business :** Ce jeu de données est parfait pour s'exercer à manipuler des pipelines de données (Pandas, Seaborn), mais il est **inexploitable pour piloter une stratégie RH** ou prendre des décisions d'entreprise, car il ne reflète aucune réalité économique.

## 🛠️ Technologies Utilisées
* Python (Pandas, NumPy)
* Matplotlib & Seaborn (Data Visualization)
