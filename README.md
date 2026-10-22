# Loyoly Partner Kit

Site statique du kit média partenaires Loyoly, déployé automatiquement sur Vercel à chaque push sur `main` : https://loyoly-partner-kit.vercel.app

## Structure

- `index.html` : la page (contenu, textes, styles, script).
- `assets/logos/` : logos (SVG et PNG).
- `assets/badges/` : badges partenaires par tier, versions claire et sombre.
- `assets/visuals/` : visuels produit.
- `assets/docs/` : one-pager et descriptions (PDF, DOCX).

## Modifier le kit

1. Textes, liens, couleurs : éditer `index.html` directement.
2. Remplacer un visuel : écraser le fichier dans `assets/` en gardant le même nom.
3. Ajouter un fichier : le déposer dans le bon dossier `assets/`, puis l'ajouter dans `index.html`
   (une balise `<img data-file="...">` pour l'afficher, un bouton `data-file-dl="..."` pour le téléchargement)
   et dans l'index JSON `<script id="files">` avec son type MIME, pour qu'il soit inclus dans les zips.
4. Commit et push sur `main` : Vercel redéploie en moins d'une minute.

Charte : cream #EEEDE6, ink #2B251F, jaune #FFC700, pink #FA5A8C, bleu #2965FE. Lexend pour les titres, Inter pour le reste.
