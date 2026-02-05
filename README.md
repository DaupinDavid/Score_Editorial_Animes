# 🎬 Projet Data Science : Score Éditorial Anime

Identifier rapidement des animés "à forte valeur éditoriale" à partir de données limitées pour une plateforme de streaming.


> **Problématique :**  
> Comment identifier les animés à **forte valeur de rétention** et éviter de promouvoir des séries irrégulières génératrices de churn ?

---

## 📉 Le Problème Métier

Une plateforme de streaming souhaite mettre en avant des animés de qualité.  
Cependant, la **Note Globale utilisateur** est souvent biaisée par la hype et ne reflète pas la **régularité réelle** d’une série.

- ⚠️ **Risque** : Mettre en avant un shonen de 300 épisodes inégal → frustration → désabonnement  
- 🎯 **Besoin** : Un **KPI éditorial fiable** pour automatiser la curation du catalogue

---

## 💡 La Solution : le *Score Éditorial*

J’ai développé un algorithme de scoring qui **pénalise l’instabilité narrative et technique** tout en respectant l’avis du public.

### 🧮 Formule du Score Éditorial

```python
Score_Editorial = (0.45 * Note_Globale + 0.40 * Regularite + 0.15 * Note_Meilleur_Episode)
````

### 🧩 Interprétation des composantes

* **Note Globale (45 %)** : perception générale du public
* **Régularité (40 %)** : stabilité de la qualité sur l’ensemble des épisodes
* **Pic de qualité (15 %)** : capacité à produire un moment culte (*Wow effect*)

---

## 📊 Résultats & Insights Clés

Analyse menée sur **59 animés majeurs**.

### 1️⃣ La “malédiction” des séries fleuves 📉

* Les séries de **plus de 100 épisodes** (ex. *Naruto*, *One Piece*) subissent une pénalité moyenne de **−0.70 point**
* Cause principale : filler, baisse de qualité, irrégularité de production

**Décision produit :**
👉 Ne pas utiliser les séries fleuves comme produit d’appel pour les nouveaux abonnés

---

### 2️⃣ Le *Safe Bet* : les Light Novels 📘

* Les adaptations de **Light Novels** affichent la **meilleure régularité moyenne (7.90/10)**

**Décision business :**
👉 Catégorie la plus fiable pour l’acquisition de licences et la mise en avant éditoriale

---

### 3️⃣ Le Grand Remplacement 👑

Le **Score Éditorial** a bouleversé le Top 10 :

* ❌ **Sortie** : *One Piece* (trop irrégulier)
* ✅ **Entrée** : *Your Lie in April*
  **Score Éditorial : 8.52 — Chef-d’œuvre stable**

👉 Le Score Éditorial corrige les biais de popularité.

---

### 💰 Impact Business

* La mise en place de ce score vise à réduire le taux de désabonnement (Churn) lié à la déception post-clic.

### ⚖️ Légal & Éthique
* **Données :** Publiques (Open Data), aucune donnée personnelle (RGPD Compliant).
* **Biais :** Le modèle dépend des notes historiques des utilisateurs, pouvant défavoriser les œuvres de niche.
* **AI Act :** Système de recommandation non critique (Risque Faible).

### 🚧 Limites du Modèle
1.  **Subjectivité :** La "Note Globale" reste une composante majeure (45%).
2.  **Volatilité :** Les séries en cours peuvent voir leur score changer chaque semaine.

## 📸 Aperçu Visuel

**Comparaison : Note Publique (gris) vs Score Éditorial (vert)**

![Comparaison Score](./img/Note%20Global%20vs%20Score%20Editorial.png)

---

## 📂 Structure du Projet

| Fichier / Dossier                 | Description                                  |
| --------------------------------- | -------------------------------------------- |
| `score_editorial_animes.ipynb`    | Nettoyage, EDA, Feature Engineering, Scoring |
| `data/processed/animes_final.csv` | Dataset final enrichi                        |
| `img/`                            | Graphiques exportés                          |

---

## 🚀 Installation & Utilisation

### 1️⃣ Cloner le dépôt

```bash
git clone https://github.com/DaupinDavid/Score_Editorial_Animes.git
```

### 2️⃣ Installer les dépendances

```bash
pip install pandas seaborn matplotlib wordcloud
```

### 3️⃣ Lancer l’analyse

Ouvrir le notebook `score_editorial_animes.ipynb` et exécuter toutes les cellules.

---

## 👤 Auteur

**[DAUPIN David]**
Data Analyst / Data Scientist

🔗 [LinkedIn](https://www.linkedin.com/in/david-daupin-691034212)
🌐 [Portfolio](https://https://daupindavid.github.io/Ma-Carte-de-Visite/)

---

