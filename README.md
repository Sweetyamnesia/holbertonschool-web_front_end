# 🌐 Apprendre les bases de HTML5

Ce document présente les notions fondamentales à maîtriser pour structurer correctement une page HTML5 moderne. Il couvre les bonnes pratiques, les balises sémantiques, l'intégration de médias, et bien plus.

---

## ✅ Bonnes pratiques à suivre pour HTML

- Toujours utiliser la déclaration `<!DOCTYPE html>` en début de document.
- Respecter l’indentation et la hiérarchie des balises.
- Utiliser des balises **sémantiques** pour donner du sens au contenu.
- Séparer le contenu (HTML), la présentation (CSS) et le comportement (JavaScript).
- S’assurer que la page est **valide** (W3C Validator).
- Toujours définir l’encodage UTF-8 avec `<meta charset="UTF-8">`.

---

## 🧱 Structure de base d’une page HTML5

```html
<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Titre de la page</title>
</head>
<body>
  <!-- Contenu ici -->
</body>
</html>

🧩 Utiliser les balises sémantiques pour structurer une page

Balises principales :

<header> : en-tête du site ou d’une section.
<nav> : zone de navigation.
<main> : contenu principal de la page.
<section> : regroupe des contenus thématiquement liés.
<article> : contenu autonome, indépendant (ex : blog, actualité).
<aside> : contenu complémentaire ou contextuel.
<footer> : pied de page.

🟦 div vs span : quelles différences ?

Balise	Description	Type
<div>	Conteneur bloc sans signification sémantique.	block
<span>	Conteneur en ligne sans signification sémantique.	inline
Utiliser div pour organiser la structure globale (layouts), span pour appliquer du style à une portion de texte en ligne.

🔠 L’importance de la hiérarchie des titres (<h1> à <h6>)

<h1> est le titre principal de la page (à utiliser une seule fois).
Suivre un ordre logique : <h1> → <h2> → <h3>...
Cela améliore l’accessibilité et le référencement (SEO).

📋 Créer des listes en HTML

Liste non ordonnée :
<ul>
  <li>Élément 1</li>
  <li>Élément 2</li>
</ul>

Liste ordonnée :
<ol>
  <li>Étape 1</li>
  <li>Étape 2</li>
</ol>

🖼️ Différences entre les formats médias
| Format       | Caractéristiques                       | Usage recommandé                    |
| ------------ | -------------------------------------- | ----------------------------------- |
| **SVG**      | Vectoriel, redimensionnable sans perte | Icônes, logos                       |
| **GIF**      | Supporte l’animation, faible qualité   | Petites animations                  |
| **PNG**      | Transparence, sans perte               | Images nettes avec fond transparent |
| **JPG/JPEG** | Compression avec perte, léger          | Photos, images complexes            |

📊 Structurer des données dans un tableau
<table>
  <thead>
    <tr>
      <th>Nom</th>
      <th>Âge</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Alice</td>
      <td>25</td>
    </tr>
  </tbody>
</table>

🎥 Intégrer une vidéo dans une page
<video controls width="600">
  <source src="video.mp4" type="video/mp4">
  Votre navigateur ne supporte pas la vidéo.
</video>

🔊 Intégrer un fichier audio
<audio controls>
  <source src="audio.mp3" type="audio/mpeg">
  Votre navigateur ne supporte pas l’audio.
</audio>

🌍 Intégrer du contenu externe (embed)

Exemple avec une vidéo YouTube :
<iframe width="560" height="315"
  src="https://www.youtube.com/embed/ID_VIDEO"
  title="YouTube video player"
  frameborder="0"
  allowfullscreen>
</iframe>

🧭 Structuration correcte d’une page HTML

1. Utiliser les balises sémantiques (header, main, footer, etc.).
2. Respecter la hiérarchie des titres (h1 à h6).
3. Organiser le contenu avec section, article, aside, nav.
4. Inclure des attributs utiles (lang, alt, title, etc.).
5. Tester l’accessibilité (ex : lecteur d’écran) et la validité du code.

🏁 Conclusion

Maîtriser la structure HTML est essentiel pour créer des sites accessibles, bien référencés et maintenables. Ce guide vous offre les bases pour construire des pages claires et bien organisées.