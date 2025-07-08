# 🌐 Guide CSS – Concepts Fondamentaux

Ce document couvre les bases essentielles du **CSS** pour structurer et styliser vos pages web de manière professionnelle.

---

## 🎯 Sélecteurs, Propriétés et Valeurs

- **Sélecteurs** : ciblent des éléments HTML (ex: `p`, `.classe`, `#id`)
- **Propriétés** : définissent ce qui est stylisé (ex: `color`, `font-size`, `margin`)
- **Valeurs** : précisent comment styliser (ex: `red`, `16px`, `auto`)

```css
p {
  color: blue;
  font-size: 16px;
}

🧱 Différence entre bloc et inline

Bloc (display: block) : occupe toute la largeur disponible (<div>, <p>)
Inline (display: inline) : s'aligne sur la même ligne, pas de largeur/hauteur personnalisable (<span>, <a>)
Inline-block : comme inline, mais permet width/height
🌍 Assurer la cohérence entre navigateurs (CSS Reset)

Les navigateurs ont des styles par défaut différents. Un CSS reset (ex: normalize.css) permet de :

Supprimer les marges/paddings de base
Uniformiser le rendu

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

🎚️ Définir des variables CSS
:root {
  --main-color: #3498db;
  --padding: 1rem;
}

body {
  background-color: var(--main-color);
  padding: var(--padding);
}

✅ Permet la réutilisation, simplifie la maintenance.

📎 CSS Inline, Embedded et Externe
| Type     | Emplacement         | Avantages                   | Inconvénients             |
| -------- | ------------------- | --------------------------- | ------------------------- |
| Inline   | Attribut `style=""` | Spécifique, rapide à tester | Difficile à maintenir     |
| Embedded | Dans `<style>`      | Centralisé par page         | Non réutilisable          |
| Externe  | Fichier `.css`      | Réutilisable, clair         | Requiert un lien `<link>` |

🧱 Système de grille avec les floats

Avant flex/grid, on utilisait float :
.col {
  float: left;
  width: 33.33%;
}
.row::after {
  content: "";
  display: table;
  clear: both;
}

🛑 Obsolète, mais encore vu dans des projets anciens.

🧩 Icônes : Webfonts vs SVG
| Webfonts (ex: FontAwesome)        | SVG                               |
| --------------------------------- | --------------------------------- |
| Faciles à styliser                | Résolution parfaite (vectorielle) |
| Moins accessibles                 | Plus accessibles                  |
| Dépend d'une police               | Fichier indépendant               |
| Plus léger pour beaucoup d’icônes | Plus flexible et personnalisable  |

🎯 Pseudo-classes vs Pseudo-éléments

Pseudo-classe → sélectionne un état

a:hover {
  color: red;
}

Pseudo-élément → sélectionne une partie virtuelle
p::first-line {
  font-weight: bold;
}

🎨 Créer des dégradés en arrière-plan

background: linear-gradient(to right, #ff7e5f, #feb47b);

linear-gradient, radial-gradient, conic-gradient

🌀 Animer des éléments en CSS

@keyframes fadeIn {
  from { opacity: 0; }
  to   { opacity: 1; }
}

.box {
  animation: fadeIn 2s ease-in-out;
}

Utilise @keyframes et la propriété animation

🧊 Transformer des éléments (2D / 3D)

.transform2d {
  transform: rotate(45deg) scale(1.2);
}

.transform3d {
  transform: rotateY(180deg) translateZ(50px);
  transform-style: preserve-3d;
  perspective: 1000px;
}

transform permet des effets 2D (rotate, scale, translate) et 3D (rotateY, perspective)

⚙️ Préfixes fournisseurs (Vendor Prefixes)

Certains navigateurs ont besoin de préfixes spécifiques :

.example {
  -webkit-transform: rotate(30deg);
     -moz-transform: rotate(30deg);
      -ms-transform: rotate(30deg);
          transform: rotate(30deg);
}

Utiles pour compatibilité avec anciens navigateurs
Utilisez autoprefixer (via PostCSS) pour automatiser

