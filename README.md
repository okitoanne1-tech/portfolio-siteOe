# Portfolio · Chantier Sérénité (OE-Architecture)

Site web statique animé (HTML + CSS + JavaScript, **aucune installation ni build**).
Auteure : OKITO EHADI Anne · Projet de spécialisation marketing · Novembre 2026.

## Voir le site en local
Ouvrez un terminal dans ce dossier puis lancez :

    python3 -m http.server 8000

et visitez http://localhost:8000 (un double-clic sur `index.html` fonctionne aussi).

## Ce qu'il faut modifier (et où)

| Je veux changer…                                        | Fichier                                  |
|---------------------------------------------------------|------------------------------------------|
| Les chiffres du mois, les objectifs, le taux de change  | `assets/js/data.js` (`mois`, `objectifs`, `params`) |
| Le budget, les actions QQOQCCP, le Gantt, le Kanban, le planning du lancement | `assets/js/data.js` |
| Les textes (contexte, audit, brief, bilan…)             | `index.html`                             |
| Les couleurs, polices, tailles                          | `assets/css/style.css` (variables en haut) |
| Les photos                                              | `assets/img/` (gardez les mêmes noms de fichiers) |
| Les documents à télécharger                             | `assets/livrables/` (remplacez les .docx/.pdf/.xlsx en gardant les noms) |
| Les aperçus des documents                               | `assets/previews/` (une image par document) |
| Le nom du tuteur, les corrections du tuteur             | section « Bilan » de `index.html`        |

Les chiffres de novembre 2026 sont des **estimations de travail** : remplacez-les par les valeurs réelles dans `assets/js/data.js`.

## Mettre en ligne : GitHub puis Vercel
1. Sur github.com, créez un dépôt (par exemple `portfolio-chantier-serenite`), puis envoyez-y tout le contenu de ce dossier :
   - soit avec « Add file → Upload files » (glissez le dossier),
   - soit en ligne de commande : `git init && git add . && git commit -m "Portfolio" && git branch -M main && git remote add origin <URL du dépôt> && git push -u origin main`.
2. Sur vercel.com, connectez-vous avec GitHub, cliquez sur « Add New… → Project » et importez le dépôt.
3. Réglages : **Framework Preset : Other**, laissez **Build Command** et **Output Directory** vides, puis « Deploy ».
4. Chaque modification poussée sur GitHub (`git push` ou modification dans l'interface web de GitHub) redéploie automatiquement le site.

Astuce : dans GitHub, ouvrez un fichier et cliquez sur le crayon pour le modifier directement depuis le navigateur.

## Contenu
- `index.html` : la page unique (8 sections : contexte, analyse, planification, coordination, communication 360°, performance, livrables, bilan)
- `assets/js/main.js` : animations (apparition au défilement, compteurs, entonnoir, anneau du budget, Gantt, Kanban glisser-déposer, simulateur de tableau de bord, visionneuse d'images)
- `assets/js/data.js` : toutes les données modifiables
- `vercel.json` : réglages de déploiement (mise en cache)

## Droits d'image
Les rendus 3D, la brochure, le logo et les plans d'affaires appartiennent à OE-Architecture / à l'auteure : vérifiez l'autorisation avant publication publique.


## Thème « chantier » (version 2)
- Couleurs : modifiez les variables en haut de `assets/css/style.css` (`--y` jaune sécurité, `--o` orange, `--b` bleu).
- Filigrane animé (grue + bâtiment) : bloc `<div class="bg-build">` au début de `index.html`.
- Contact : section `#contact` et pied de page de `index.html` (e-mail, téléphone, ville).
- Images : toutes dans `assets/img/`, noms en minuscules, chemins relatifs. Si une image manque, un cadre « Image introuvable » s'affiche et le nom du fichier apparaît dans la console du navigateur (F12).
