# BCF Reader

> Lecteur et générateur de rapports BCF — 100% navigateur, aucune donnée transmise.
>
> <img width="1917" height="1060" alt="image" src="https://github.com/user-attachments/assets/9d139e72-c16d-4430-86f4-72e6cc0394af" />


![BCF Reader](https://img.shields.io/badge/BCF-2.1-f97316?style=flat-square)
![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-ready-22c55e?style=flat-square)
![No backend](https://img.shields.io/badge/backend-none-3b82f6?style=flat-square)
![License](https://img.shields.io/badge/license-MIT-64748b?style=flat-square)

---

## 🔒 Confidentialité garantie

**Vos fichiers BCF ne quittent jamais votre ordinateur.**

- Tout le traitement s'effectue **localement dans votre navigateur**
- Aucune donnée n'est transmise, stockée ou analysée sur un serveur
- Aucun cookie, aucun `localStorage`, aucune base de données
- Dès que vous fermez l'onglet, tout disparaît définitivement
- Le code source est entièrement **auditable** sur ce dépôt

GitHub Pages sert uniquement les fichiers statiques (HTML/CSS/JS). Il n'existe aucun backend capable de recevoir vos données.

---

## ✨ Fonctionnalités

- 📂 Chargement BCF par glisser-déposer ou sélecteur de fichier (.bcf, .bcfzip)
- 🔍 Recherche full-text sur titres, auteurs et commentaires
- 🎛️ Filtres par statut — Error / Warning / Info / Unknown — avec compteurs
- ↕️ Tri par titre, nombre de commentaires ou date
- 🖼️ Snapshots affichées dans le panneau de détail (réduit à 25% pour la lisibilité)
- ☑️ Sélection multi-topics via Ctrl+clic — barre flottante avec compteur et accès rapide à l'export
- 📄 Export rapport HTML autonome téléchargeable, comprenant :
- Page de garde (projet, émetteur, n°, indice, date, objet)
- Tableau récapitulatif avec donut SVG des statuts et liens d'ancrage vers chaque topic
- Détail des topics — layout image + commentaires côte à côte
- 3 topics par page, sauts de page automatiques pour impression / PDF
- 3 scopes au choix : tous les topics / topics filtrés actifs / sélection manuelle

---

## 🚀 Utilisation

### Via GitHub Pages

Accéder directement à l'URL de votre déploiement GitHub Pages — aucune installation requise.

### En local

```bash
# Cloner le dépôt
git clone https://github.com/votre-compte/bcf-reader.git
cd bcf-reader

# Ouvrir directement dans le navigateur
open index.html
# ou
start index.html   # Windows
```

Aucune dépendance Node/npm — le fichier s'ouvre tel quel.

---

## 📦 Déploiement GitHub Pages

1. Aller dans **Settings → Pages** du dépôt
2. Source : `Deploy from a branch`
3. Branch : `main` / `root`
4. Sauvegarder — l'URL est disponible en quelques secondes

---

## 🛠️ Stack technique

| Composant | Technologie |
|-----------|-------------|
| Interface | HTML5 / CSS3 / JavaScript ES6+ |
| Lecture ZIP | [JSZip 3.10](https://stuk.github.io/jszip/) via CDN |
| Parsing XML | `DOMParser` natif du navigateur |
| Graphique donut | SVG généré dynamiquement |
| Polices | [IBM Plex Sans](https://fonts.google.com/specimen/IBM+Plex+Sans) + [JetBrains Mono](https://fonts.google.com/specimen/JetBrains+Mono) via Google Fonts |
| Hébergement | GitHub Pages (statique) |

**Aucun framework JavaScript. Aucun bundler. Aucun backend.**

---

## 📋 Format BCF supporté

BCF (BIM Collaboration Format) version 2.1 — structure ZIP contenant :

```
<guid-topic>/
  markup.bcf     ← XML avec topic, commentaires, fichiers liés
  snapshot.png   ← Capture d'écran optionnelle
```

---

## 🏗️ Développé par

**BMS Project** — Développement et management BIM

## A tester 
https://msbim2025.github.io/WEB_BCF_Reader/

---

## 📄 Licence

MIT — libre d'utilisation, de modification et de redistribution.
