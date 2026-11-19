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
3. Visuels produit : la section « Product visuals » est générée depuis `assets/manifest.json`
   (groupes, libellés, fichiers, formats). Pour en ajouter un : déposer le PNG dans `assets/visuals/`
   et ajouter une entrée dans le manifeste. `index.html` n'a pas à être modifié.
   Ces visuels sont alimentés automatiquement depuis Figma (fichier Product-visuals, sections `[HUB]`).
4. Logos, badges, docs : déposer le fichier dans le bon dossier `assets/`, puis l'ajouter dans `index.html`
   (une balise `<img data-file="...">`, un bouton `data-file-dl="..."`) et dans l'index JSON `<script id="files">`
   avec son type MIME, pour qu'il soit inclus dans les zips.
5. Commit et push sur `main` : Vercel redéploie en moins d'une minute.

Charte : cream #EEEDE6, ink #2B251F, jaune #FFC700, pink #FA5A8C, bleu #2965FE. Lexend pour les titres, Inter pour le reste.

Déployé automatiquement par Vercel depuis ce repo.
