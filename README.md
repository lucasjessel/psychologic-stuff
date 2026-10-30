# À portée de pensée — mémo et journal des distorsions

Petit outil personnel en français pour repérer des distorsions cognitives, tenir un journal de pensées et noter trois accomplissements par jour ainsi qu’un pourcentage ressenti. Les pages sont autonomes et fonctionnent dans le navigateur, sans serveur applicatif.

## Structure

- `index.html` : mémo des distorsions et journal.
- `semaine.html` : tableau hebdomadaire, du jeudi au mercredi, avec export PDF et import/export JSON.
- `.nojekyll` : désactive le traitement Jekyll de GitHub Pages.

## Mise en ligne avec GitHub Pages

1. Créez un dépôt GitHub (par exemple `memo-distorsions`). Pour la méthode ci-dessous, créez-le vide, sans README ni autre fichier initial.
2. Dans un terminal, placez-vous dans le dossier contenant ces fichiers, puis lancez :

   ```sh
   git init
   git branch -M main
   git add .
   git commit -m "Publication initiale"
   git remote add origin https://github.com/<user>/<repo>.git
   git push -u origin main
   ```

   Remplacez `<user>` et `<repo>` par votre nom d’utilisateur GitHub et le nom exact du dépôt. Si le dépôt a déjà été initialisé localement, ne relancez pas `git init` ; ajoutez plutôt le dépôt distant approprié.
3. Dans GitHub, ouvrez **Settings > Pages**. Sous **Build and deployment**, choisissez **Deploy from a branch**, puis la branche **main** et le dossier **/ (root)**, et cliquez sur **Save**.
4. Après le déploiement, le site sera normalement disponible à l’adresse `https://<user>.github.io/<repo>/` (le premier déploiement peut prendre quelques minutes).

Les liens entre les deux pages sont relatifs (`index.html` et `semaine.html`) et conviennent à ce chemin de projet GitHub Pages.

## Important : sauvegarde de vos données

Les entrées sont conservées dans le `localStorage` du navigateur et de l’appareil utilisés ; elles ne sont pas publiées avec le site et ne se synchronisent pas automatiquement entre appareils ou navigateurs. **Exportez régulièrement vos données en JSON** depuis chaque page et gardez les fichiers exportés dans un endroit sûr.
