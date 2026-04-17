# Portfolio — NEBIE Gaston Cyrille
## Ingénieur Hydrologue | Expert en Gestion des Risques Climatiques

Portfolio professionnel construit avec [Quarto](https://quarto.org) et déployé sur 
[GitHub Pages](https://pages.github.com).

🌐 **Site en ligne :** https://ngastoncyrille.github.io

---

## 🛠️ Stack technique

| Outil | Rôle |
|-------|------|
| [Quarto](https://quarto.org) | Générateur de site statique |
| [R](https://www.r-project.org) | Analyses, visualisations, cartes |
| [RStudio](https://posit.co) | Environnement de développement |
| [GitHub Pages](https://pages.github.com) | Hébergement |
| [GitHub Actions](https://github.com/features/actions) | CI/CD automatique |

---

## 🚀 Démarrage rapide (RStudio)

### 1. Pré-requis

Installez les logiciels suivants :
- [R ≥ 4.3.0](https://cloud.r-project.org/)
- [RStudio ≥ 2024.09](https://posit.co/download/rstudio-desktop/)
- [Quarto ≥ 1.5](https://quarto.org/docs/get-started/)
- [Git](https://git-scm.com)

### 2. Cloner le dépôt

```bash
git clone https://github.com/ngastoncyrille/ngastoncyrille.github.io.git
cd ngastoncyrille.github.io
```

### 3. Ouvrir dans RStudio

- Ouvrir RStudio → File → Open Project → sélectionner le dossier `portfolio-nebie`
- Ou double-cliquer sur le fichier `.Rproj` si vous en créez un

### 4. Installer les packages R nécessaires

Dans la console RStudio :

```r
install.packages(c(
  "quarto",
  "rmarkdown",
  "knitr",
  "ggplot2",
  "plotly",
  "leaflet",
  "dplyr",
  "tidyr",
  "sf",
  "terra",
  "evd",
  "cluster",
  "randomForest",
  "caret",
  "lubridate"
))
```

### 5. Prévisualiser le site en local

Dans le Terminal de RStudio :

```bash
quarto preview
```

Ou via le bouton **Render** sur n'importe quel fichier `.qmd`.

Le site s'ouvre dans votre navigateur à `http://localhost:XXXX`.

### 6. Compiler le site

```bash
quarto render
```

Les fichiers HTML sont générés dans le dossier `docs/`.

---

## 📁 Structure du projet

```
portfolio-nebie/
├── _quarto.yml              ← Configuration principale du site
├── styles.scss              ← Thème sombre (eau & risques)
├── index.qmd                ← Page d'accueil
├── about.qmd                ← À propos (bio + carte leaflet)
├── skills.qmd               ← Compétences (radar + barres)
├── publications.qmd         ← Publications & conférences
├── contact.qmd              ← Contact (formulaire Formspree)
│
├── projects/
│   ├── index.qmd            ← Galerie des projets
│   ├── teledetection.qmd    ← Projet télédétection R
│   ├── ml-aquifere.qmd      ← Projet IA cartographie
│   ├── modelisation-nakambe.qmd
│   └── gire-communautaire.qmd
│
├── blog/
│   ├── index.qmd            ← Listing automatique des articles
│   └── posts/
│       ├── idf-curves-r/index.qmd
│       ├── kmeans-landsat/index.qmd
│       └── biais-correction/index.qmd
│
├── assets/
│   ├── img/
│   │   └── photo.jpg        ← ⚠️ Ajouter votre photo ici
│   └── cv/
│       └── cv_nebie_2026.pdf  ← ⚠️ Ajouter votre CV ici
│
└── .github/
    └── workflows/
        └── deploy.yml       ← Déploiement automatique GitHub Actions
```

---

## ⚙️ Configuration GitHub Pages

### Étape 1 — Créer le dépôt GitHub

1. Créer un nouveau dépôt nommé **`ngastoncyrille.github.io`**
   (remplacer `ngastoncyrille` par votre nom d'utilisateur GitHub exact)
2. Le dépôt doit être **public**

### Étape 2 — Connecter RStudio à GitHub

Dans le Terminal RStudio :

```bash
git init
git remote add origin https://github.com/ngastoncyrille/ngastoncyrille.github.io.git
git add .
git commit -m "Initial commit — portfolio NEBIE Gaston Cyrille"
git push -u origin main
```

### Étape 3 — Activer GitHub Pages

Dans les paramètres du dépôt GitHub :
1. Aller dans **Settings → Pages**
2. Source : **GitHub Actions**

### Étape 4 — Déploiement automatique

À chaque `git push`, GitHub Actions :
1. Installe R et Quarto
2. Compile le site (`quarto render`)
3. Déploie les fichiers sur GitHub Pages

**URL finale :** `https://ngastoncyrille.github.io`

---

## 📸 Personnalisation

### Ajouter votre photo

Copier votre photo dans `assets/img/photo.jpg` (format JPG/PNG recommandé, 
résolution minimum 400×400 px).

### Ajouter votre CV

Copier votre CV PDF dans `assets/cv/cv_nebie_2026.pdf`.

### Formulaire de contact

1. Créer un compte sur [Formspree.io](https://formspree.io) (gratuit)
2. Créer un nouveau formulaire
3. Remplacer `VOTRE_ID_FORMSPREE` dans `contact.qmd` par votre identifiant Formspree

### Ajouter un nouveau projet

Créer un nouveau fichier `projects/mon-projet.qmd` avec le modèle :

```yaml
---
title: "Titre du projet"
subtitle: "Description courte"
author: "NEBIE Gaston Cyrille"
date: "2024"
categories: [R, Hydrologie, SIG]
format:
  html:
    toc: true
---
```

### Ajouter un article de blog

Créer un dossier `blog/posts/mon-article/` avec un fichier `index.qmd` :

```yaml
---
title: "Titre de l'article"
description: "Description pour le listing"
author: "NEBIE Gaston Cyrille"
date: "2024-06-01"
categories: [R, Hydrologie]
format:
  html:
    toc: true
---
```

---

## 🎨 Palette de couleurs

| Rôle | Couleur | Code |
|------|---------|------|
| Fond principal | Bleu nuit profond | `#0d1b2a` |
| Surface carte | Bleu marine | `#112240` |
| Primaire (eau) | Cyan océan | `#00b4d8` |
| Secondaire | Cyan clair | `#48cae4` |
| Texte principal | Bleu pâle | `#cdd6f4` |
| Danger/Risque | Rouge alerte | `#e63946` |
| Succès/Vert | Turquoise | `#06d6a0` |
| Avertissement | Ambre/Sable | `#f4a261` |

---

## 📞 Contact

**NEBIE Gaston Cyrille**  
📧 ngastoncyrille@gmail.com  
🌐 https://rpubs.com/nebiegc  
💼 https://www.linkedin.com/in/gaston-cyrille-nebie-a2a977222

---

*Portfolio développé avec l'assistance de Claude (Anthropic) — 2026*
