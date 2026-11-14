# Déployer Le-J traduit sur Vercel

Ce dossier est un **site statique** prêt pour Vercel. Aucune étape de build :
`index.html` est servi à la racine, et `le-j-traduit-pro.zip` est téléchargeable.

## Option A — Vercel CLI (le plus simple)
1. Installez la CLI : `npm i -g vercel`
2. Dans CE dossier, lancez : `vercel`
   - Connectez-vous, acceptez les valeurs par défaut.
   - Framework Preset : **Other** · Build Command : *(vide)* · Output Directory : `./`
3. Mise en production : `vercel --prod`
4. Vercel vous donne l'URL (ex. `https://le-j-traduit.vercel.app`).

## Option B — via GitHub (déploiement automatique)
1. Créez un dépôt GitHub et poussez le contenu de ce dossier
   (`index.html`, `vercel.json`, `le-j-traduit-pro.zip`).
2. Sur https://vercel.com → **Add New… → Project → Import** votre dépôt.
3. Framework Preset : **Other**, pas de build. Cliquez **Deploy**.
4. Chaque `git push` redéploie automatiquement.

## Notes
- `vercel.json` force le **téléchargement** du `.zip` (en-tête Content-Disposition).
- Le fichier `.zip` fait ~18 Mo : c'est accepté par Vercel. Si vous préférez l'alléger,
  hébergez l'extension dans une **GitHub Release** et remplacez le lien du bouton
  « Télécharger le .zip » dans `index.html` par l'URL de la release.
- Le site est 100 % statique : il fonctionne aussi en ouvrant simplement `index.html`
  en local (les jeux et l'audio marchent ; le bouton de téléchargement marche si le
  `.zip` est à côté du fichier).

Le-J traduit · Comprendre aujourd'hui. Maîtriser demain.
