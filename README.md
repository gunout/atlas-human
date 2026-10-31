<div align="center">

# 🧬 Atlas 3D — Moniteur Anatomique

**Moniteur 3D interactif du corps humain basé sur les données HuBMAP / Human Reference Atlas et Allen Brain Atlas**

<br>

[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Live-brightgreen?logo=github&style=for-the-badge)](https://gunout.github.io/atlas-human/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](LICENSE)
[![Three.js](https://img.shields.io/badge/Three.js-0.160-blue?logo=three.js&style=for-the-badge)](https://threejs.org/)
[![GLTF](https://img.shields.io/badge/GLTF-2.0-orange?style=for-the-badge)](https://www.khronos.org/gltf/)
[![Draco](https://img.shields.io/badge/Draco-Compressed-purple?style=for-the-badge)](https://google.github.io/draco/)

<br>

[![HuBMAP](https://img.shields.io/badge/Data-HuBMAP%20%2F%20HRA-red?style=for-the-badge)](https://humanatlas.io/)
[![Contributors](https://img.shields.io/github/contributors/gunout/atlas-human?style=for-the-badge)](https://github.com/gunout/atlas-human/graphs/contributors)
[![Last Commit](https://img.shields.io/github/last-commit/gunout/atlas-human?style=for-the-badge)](https://github.com/gunout/atlas-human)

<br>

[**🌐 Voir la démo en ligne**](https://gunout.github.io/atlas-human/) · [**📦 Cloner le projet**](https://github.com/gunout/atlas-human.git)

</div>

---

## ✨ Fonctionnalités

- 🧬 **Superposition anatomique** — peau, vasculature, cœur et cerveau dans un seul référentiel
- 🎯 **Recentrage animé** — clic sur une structure → la caméra vole vers elle en 700 ms
- 🔍 **Filtres par catégorie** — artères, veines, peau, organes, cœur, cerveau
- 📸 **Export PNG** — capture haute résolution de la vue courante
- 🖥️ **Plein écran** — mode immersif
- ⌨️ **Raccourcis clavier** — navigation rapide sans souris
- 📱 **Responsive** — fonctionne sur desktop et mobile
- ⚡ **Optimisé** — GLB compressés Draco (17 Mo au lieu de 374 Mo)

## 🎮 Contrôles

| Action | Souris | Clavier | Tactile |
|:---|:---|:---:|:---:|
| **Rotation 360°** | Clic gauche + glisser | — | 1 doigt |
| **Pan** | Clic droit + glisser | ↑↓←→ / ZQSD | 2 doigts |
| **Zoom** | Molette | — | Pincement |
| **Recentrer** | Bouton ↺ Reset | Home | — |
| **Isoler** | Bouton | I | — |
| **Labels** | Bouton | L | — |
| **Rotation auto** | Bouton | R | — |
| **Mode Pan** | Bouton ✥ Pan | P | — |
| **Désélectionner** | — | Échap | — |

## 🚀 Installation locale

Ouvrez un terminal et lancez :

    git clone https://github.com/gunout/atlas-human.git
    cd atlas-human
    python3 -m http.server 5013

Puis ouvrez **http://localhost:5013/** dans votre navigateur.

## 📦 Structure du projet

    atlas-human/
    ├── index.html
    ├── LICENSE
    ├── README.md
    ├── 3d-vh-f-blood-vasculature.glb
    ├── 3d-vh-m-blood-vasculature.glb
    ├── 3d-vh-f-heart.glb
    ├── 3d-vh-m-heart.glb
    ├── 3d-allen-f-brain.glb
    ├── 3d-allen-m-brain.glb
    ├── united-f-opt.glb
    ├── united-m-opt.glb
    ├── united.json
    ├── united1.json
    ├── graph.json
    ├── graph(1).json
    ├── heart.json
    ├── heart1.json
    ├── brain.json
    └── brain1.json

## 🛠️ Technologies

| Technologie | Usage |
|:---|:---|
| Three.js 0.160 | Moteur 3D WebGL |
| GLTFLoader | Chargement des modèles |
| DRACOLoader | Décompression Draco |
| OrbitControls | Navigation caméra |
| gltf-transform | Compression GLB |

## 📊 Source des données

- **HuBMAP Human Reference Atlas** — modèle anatomique (CC BY 4.0)
- **KG Explorer** — index des organes 3D
- **Allen Brain Atlas** — modèles cérébraux (CC BY-SA 4.0)

## 🔧 Compression des GLB

Les fichiers compressés avec Draco :

    npx --min-release-age=0 @gltf-transform/cli optimize 3d-vh-f-united.glb united-f-opt.glb --compress draco
    npx --min-release-age=0 @gltf-transform/cli optimize 3d-vh-m-united.glb united-m-opt.glb --compress draco

**Résultat** : 374 Mo → 17 Mo (réduction de 95 %).

## 📄 Licence

Ce projet est sous licence **MIT** — voir LICENSE.

## 🙏 Remerciements

- HuBMAP Consortium pour les modèles de référence
- Kristen Browne et Heidi Schlehlein pour la création des modèles 3D
- Three.js pour le moteur 3D

## 👥 Contributeurs

- [@gunout](https://github.com/gunout)
- [@Moonwalkeuse](https://github.com/Moonwalkeuse)

---

⭐ **Si ce projet vous est utile, n'hésitez pas à lui donner une étoile !**
