<p align="center">
  <img src="https://media1.tenor.com/m/c0iM4FE94koAAAAC/brain-3d-image.gif" alt="Neurone" width="220">
</p>

<!-- Option B: ou, après avoir uploadé assets/neuron.png dans le dépôt, utilisez :
  <img src="assets/neuron.png" alt="Neurone" width="220">
  -->
</p>

<p align="center">
  <strong>Introduction rapide — TP1</strong><br>
  Une fiche de TD et des exemples R pour découvrir la manipulation de données, visualisation et analyses simples.
</p>

[![Licence](https://img.shields.io/badge/licence-MIT-blue.svg)](#license) <!-- remplacez la licence si nécessaire -->
[![R-CMD-check](https://img.shields.io/badge/R%20ready-yes-brightgreen.svg)](#)

## À propos
Ce dépôt contient une fiche de TD au format R Markdown (fiche-td.Rmd), un petit jeu de données d'exemple (data/petits_vehicules.csv) et des instructions pour les étudiants. Le contenu est conçu pour être copié/collé dans GitHub (ou cloné), ouvert dans RStudio et exécuté.

## Contenu
- fiche-td.Rmd — fiche de TD prête à knitter (HTML/PDF)
- data/petits_vehicules.csv — petit jeu de données d'exemple (format CSV)
- resultats/ — dossier suggéré pour sauvegarder les sorties (à créer)

## Démarrage rapide
1. Cloner le dépôt :
   git clone https://github.com/Meriemminette/TP1.git
2. Ouvrir RStudio et charger le fichier `fiche-td.Rmd`.
3. Installer les paquets nécessaires (si besoin) :
   install.packages(c("ggplot2","dplyr","knitr"))
4. Dans RStudio, cliquer sur "Knit" pour générer la version HTML du TD.

## Utilisation (copier-coller pour les étudiants)
- Lire les données :
```r
df <- read.csv("data/petits_vehicules.csv", stringsAsFactors = FALSE)
head(df)
```
- Calculer moyenne et écart-type :
```r
mean(df$mpg)
sd(df$mpg)
```
- Tracer un histogramme :
```r
library(ggplot2)
ggplot(df, aes(x = mpg)) + geom_histogram(binwidth = 2, fill = "steelblue")
```

## Personnaliser l'image du header
- Option 1 (préférée) : uploader votre image `neuron.png` dans `assets/` puis remplacer la balise image par `assets/neuron.png`.
- Option 2 : remplacer l'URL distante dans le header par celle d'une image publique que vous aimez.

Pour ajouter une image via l'interface GitHub :
1. Cliquez sur "Add file" → "Upload files" → sélectionnez `assets/neuron.png`.
2. Committez sur une nouvelle branche (ex : `add-readme-art`), puis proposez une Pull Request.

## Contribuer
- Pour proposer des modifications : créez une branche, faites vos changements (README, Rmd, données) puis ouvrez une Pull Request.
- Indiquez dans votre PR si vous ajoutez des données privées — évitez d'uploader des données sensibles.

## Licence
Ce dépôt est sous licence MIT — adaptez la licence si nécessaire.

---

Si vous voulez, je peux :
<p align="center">
  <img src="https://media1.tenor.com/m/c0iM4FE94koAAAAC/brain-3d-image.gif" alt="Neurone" width="220">
</p>

<p align="center">
  <strong>Introduction rapide — TP1</strong><br>
  Une fiche de TD et des exemples R pour découvrir la manipulation de données, visualisation et analyses simples.
</p>

[![Licence](https://img.shields.io/badge/licence-MIT-blue.svg)](#license)  
[![R-CMD-check](https://img.shields.io/badge/R%20ready-yes-brightgreen.svg)](#)

---

## Astuces visuelles (Notes, Tips, Important)

Voici plusieurs façons d'ajouter des encadrés lisibles et colorés dans votre README. Copiez‑collez ce qui vous plaît.

### 1) Badges colorés (rapide et propre)
Utilisez des badges shields.io :
```markdown
![Important](https://img.shields.io/badge/Important-important-red)
![Astuce](https://img.shields.io/badge/Astuce-tip-blue)
![Note](https://img.shields.io/badge/Note-info-yellow)
```

Exemple rendu :
![Important](https://img.shields.io/badge/Important-important-red) ![Astuce](https://img.shields.io/badge/Astuce-tip-blue) ![Note](https://img.shields.io/badge/Note-info-yellow)

---

### 2) Blockquote stylisé (compatible GitHub)
Simple, fonctionne partout :
```markdown
> 🔴 **Important :** Ne partagez pas de données sensibles dans ce dépôt.
>
> 💡 **Astuce :** Pour que les étudiants écrivent le code, mettez `eval=FALSE` sur certains chunks de `.Rmd`.
```

---

### 3) Encadré collapsible (utile pour solutions ou détails)
```markdown
<details>
<summary>💡 Astuce — cliquer pour ouvrir</summary>

- Installez les paquets nécessaires : `install.packages(c("ggplot2","dplyr","knitr"))`.
- Pour générer un HTML : ouvrez `fiche-td.Rmd` dans RStudio et cliquez sur *Knit*.

</details>
```

---

### 4) Encadrés "Important/Warning" avec emoji pour attirer l'œil
```markdown
> ⚠️ **Attention :** Vérifiez le chemin `data/petits_vehicules.csv` avant de lancer `read.csv()`.
```

---

### 5) Utiliser une petite image couleur (si vous upload `assets/warn.png`)
Après avoir uploadé `assets/warn.png` :
```markdown
<p>
  <img src="assets/warn.png" alt="warning" width="36" style="vertical-align:middle">
  <strong>Important :</strong> N'ajoutez pas de données confidentielles.
</p>
```
(Remarque : GitHub nettoie le style inline, mais l'image et le texte s'affichent correctement.)

---

## Exemple complet (section "Important" + "Astuce") — à coller tel quel
```markdown
![Important](https://img.shields.io/badge/Important-important-red)

> 🔴 **Important :** Ne partagez pas de données sensibles dans ce dépôt.
>
> ⚠️ **Avant de commencer :**
> - Créez un dossier `data/` et déposez-y les CSV.
> - Pour que les étudiants modifient le code, mettez `eval=FALSE` sur certains chunks `.Rmd`.

<details>
<summary>💡 Astuce — comment rendre un `.Rmd` en HTML</summary>

1. Ouvrez `fiche-td.Rmd` dans RStudio.  
2. Si besoin, installez les paquets : `install.packages(c("ggplot2","dplyr","knitr"))`.  
3. Cliquez sur *Knit* → choisissez HTML.  

</details>
```
---

## 1) Simple — blockquote + emoji (recommandé pour simplicité)
```markdown
> 💡 **Note :** Voici une information utile pour les étudiants.
```

Rendu :  
> 💡 **Note :** Voici une information utile pour les étudiants.

---

## 2) Badge coloré + blockquote (visuel fort)
```markdown
![Note](https://img.shields.io/badge/Note-info-blue)

> 💡 **Note :** Voici une information utile pour les étudiants.
```

Rendu :  
![Note](https://img.shields.io/badge/Note-info-blue)

> 💡 **Note :** Voici une information utile pour les étudiants.

---

## 3) Important / Warning (avec emoji pour attirer l'œil)
```markdown
> 🔴 **Important :** Ne partagez pas de données sensibles dans ce dépôt.
>
> ⚠️ **Warning :** Vérifiez le chemin `data/petits_vehicules.csv` avant de lancer `read.csv()`.
```

Rendu :  
> 🔴 **Important :** Ne partagez pas de données sensibles dans ce dépôt.
>
> ⚠️ **Warning :** Vérifiez le chemin `data/petits_vehicules.csv` avant de lancer `read.csv()`.

---

## 4) Encadré repliable (collapsible) — bon pour solutions ou détails
```markdown
<details>
<summary>💡 Astuce — cliquer pour ouvrir</summary>

- Installez les paquets nécessaires : `install.packages(c("ggplot2","dplyr","knitr"))`.
- Pour générer un HTML : ouvrez `fiche-td.Rmd` dans RStudio et cliquez sur *Knit*.

</details>
```

Rendu (clic pour ouvrir) :  
<details>
<summary>💡 Astuce — cliquer pour ouvrir</summary>

- Installez les paquets nécessaires : `install.packages(c("ggplot2","dplyr","knitr"))`.
- Pour générer un HTML : ouvrez `fiche-td.Rmd` dans RStudio et cliquez sur *Knit*.

</details>

---

## 5) Table avec icône (plus "encadré") — upload d'une icône recommandée
- Uploadez une petite icône (ex: assets/warn.png) dans le dépôt via "Add file → Upload files".
- Puis collez ce tableau :

```markdown
| | |
|---:|---|
| <img src="assets/warn.png" alt="warning" width="36"> | **⚠️ Important :** Ne mettez pas de données privées dans le dépôt. |
```

Exemple rendu (si assets/warn.png existe) :  
| | |
|---:|---|
| <img src="assets/warn.png" alt="warning" width="36"> | **⚠️ Important :** Ne mettez pas de données privées dans le dépôt. |

(Remarque : GitHub autorise l'image et le tableau, mais ne permet pas d'ajouter du style CSS personnalisé.)

---

## 6) Exemple complet d'une section "Important + Astuce" à coller
```markdown
![Important](https://img.shields.io/badge/Important-important-red)

> 🔴 **Important :** Ne partagez pas de données sensibles dans ce dépôt.
>
> ⚠️ **Avant de commencer :**
> - Créez un dossier `data/` et déposez-y les CSV.
> - Pour que les étudiants modifient le code, mettez `eval=FALSE` sur certains chunks `.Rmd`.

<details>
<summary>💡 Astuce — comment rendre un `.Rmd` en HTML</summary>

1. Ouvrez `fiche-td.Rmd` dans RStudio.  
2. Installez les paquets : `install.packages(c("ggplot2","dplyr","knitr"))`.  
3. Cliquez sur *Knit* → choisissez HTML.  

</details>
```

---

## Conseils / choix
- Pour compatibilité maximale : utilisez le modèle "blockquote + emoji".
- Pour un rendu plus coloré : combinez badge (shields.io) + blockquote.
- Si vous voulez un rendu très graphique, uploadez des icônes dans `assets/` et utilisez le tableau 2‑colonnes.
- Évitez CSS inline (GitHub le nettoie) — préférez les solutions ci‑dessous.

---

Si vous voulez, je peux :
- Mettre ces encadrés directement dans votre README sur @Meriemminette/TP1 (je peux créer une branche et y pousser le README modifié) — dites-moi le nom de la branche à créer (ex. `add-readme-notes`), ou
- Uploader quelques icônes libres dans `assets/` pour des encadrés graphiques (donnez-moi les URLs des images ou dites "choisis-toi des icônes libres" et je les ajouterai).

Ce que j'ai fait : je vous ai fourni plusieurs modèles prêts à copier-coller et expliqué les avantages de chacun.  
Prochaine étape : dites-moi si je dois appliquer ces changements directement au README de @Meriemminette/TP1 (et le nom de la branche) ou si vous voulez que je uploade des icônes d'abord.

---

Si vous voulez que je mette en place :
- le README corrigé directement dans @Meriemminette/TP1 (donnez le nom de la branche à créer), ou
- que j'uploade quelques icônes (assets/*.png) pour encadrés colorés (donnez-moi des URLs publiques des images ou dites que je choisis des icônes libres),

je le fais pour vous tout de suite.



- Coller ce README dans votre dépôt @Meriemminette/TP1 et créer la branche que vous souhaitez (donnez-moi le nom de la branche), ou
- Générer et pousser aussi le fichier `assets/neuron.png` si vous me donnez une URL d'image publique à utiliser.
