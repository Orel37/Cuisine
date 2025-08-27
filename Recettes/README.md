# Recettes - Format A5 Paysage

Ce dossier contient des modèles HTML/CSS pour imprimer des recettes sur du papier A5 en orientation paysage.

## Fichiers disponibles

### Templates HTML
- `recette-courte.html` - **Template pour recettes courtes** (design confortable, texte lisible)
- `recette-longue.html` - **Template pour recettes longues** (design compact, maximum d'espace)

### CSS Modulaire
- `css/fonts.css` - **Google Fonts** (polices optionnelles)
- `css/variables.css` - **Variables CSS** (couleurs, tailles, espacements)
- `css/base.css` - **Styles communs** (structure de base, impression)
- `css/recette-courte.css` - **Styles spécifiques** aux recettes courtes
- `css/recette-longue.css` - **Styles spécifiques** aux recettes longues

> **Note** : La structure CSS est modulaire avec des variables centralisées. Les fichiers CSS sont organisés dans le dossier `css/` pour une meilleure organisation.

## Quel template choisir ?

### 📝 **Recette Courte** (`recette-courte.html`)
**Utilisez ce template quand :**
- Moins de 8-9 étapes d'instructions
- Recettes simples (cookies, crêpes, vinaigrettes...)
- Vous privilégiez la lisibilité

**Caractéristiques :**
- Police 12px (confortable à lire)
- Numéros avec cercles colorés
- Espacement généreux
- Ratio 30% ingrédients / 70% instructions

### 📚 **Recette Longue** (`recette-longue.html`)
**Utilisez ce template quand :**
- Plus de 9 étapes d'instructions
- Recettes complexes (plats mijotés, pâtisseries...)
- Vous avez besoin de place maximum

**Caractéristiques :**
- Police 11px (compact mais lisible)
- Numérotation simple (sans cercles)
- Espacement minimal
- Ratio 25% ingrédients / 75% instructions
- Abréviations culinaires (c.à.s., min, etc.)

## Comment utiliser les templates

### 1. **Choisir le bon template**
- Comptez le nombre d'étapes de votre recette
- Moins de 9 étapes → `recette-courte.html`
- Plus de 9 étapes → `recette-longue.html`

### 2. **Modifier le contenu**
1. Ouvrez le fichier HTML dans un éditeur de texte
2. Remplacez `[Nom de la recette]` par le titre de votre recette
3. Remplacez chaque `[Quantité] [ingrédient X]` par vos ingrédients réels
4. Remplacez chaque `[X étape de préparation]` par vos instructions
5. Ajoutez ou supprimez des lignes `<li>` selon vos besoins

### 3. **Exemples de remplacement**
```html
<!-- Au lieu de : -->
<li>[Quantité] [ingrédient 1]</li>

<!-- Écrivez : -->
<li>250g de farine</li>
```

```html
<!-- Au lieu de : -->
<li>[Première étape de préparation]</li>

<!-- Écrivez : -->
<li>Préchauffez le four à 180°C</li>
```

### 4. **Abréviations intégrées**
Les templates incluent des commentaires avec des abréviations courantes à copier-coller :

**Pour les ingrédients :**
- `<span class="abbr">c. à c.</span>` = cuillère à café
- `<span class="abbr">c. à s.</span>` = cuillère à soupe  
- `<span class="abbr">g</span>`, `<span class="abbr">ml</span>`, `<span class="abbr">cl</span>`, `<span class="abbr">l</span>`, `<span class="abbr">kg</span>` = unités de mesure
- `<span class="abbr">env.</span>` = environ

**Pour les instructions :**
- `<span class="abbr">min</span>` = minutes
- `<span class="abbr">h</span>` = heures
- `<span class="abbr">°C</span>` = degrés Celsius

**Exemples d'utilisation :**
```html
<li>250<span class="abbr">g</span> de farine</li>
<li>Cuire 20 <span class="abbr">min</span> à 180<span class="abbr">°C</span></li>
```

> **Note** : La classe `abbr` affiche les abréviations en police plus petite et grise pour une meilleure lisibilité. Les abréviations sont dans les commentaires HTML (invisibles à l'impression) pour un copier-coller rapide.

## Personnalisation facile

### 🎨 **Modifier les couleurs**
Éditez le fichier `css/variables.css` pour changer :
- `--color-primary-blue` : couleur du titre et séparateurs
- `--color-secondary-blue` : couleur des numéros et titres de sections
- `--color-text-dark` : couleur du texte principal

### 📏 **Ajuster les tailles**
Dans `css/variables.css`, modifiez :
- `--font-size-*` : tailles de police
- `--spacing-*` : espacements
- `--ingredients-width-*` : largeur de la colonne ingrédients

### 🔧 **Architecture modulaire**
- **css/variables.css** : Toutes les variables centralisées
- **css/base.css** : Structure commune (ne pas modifier)
- **css/recette-*.css** : Styles spécifiques (safe à modifier)

> Un seul changement dans `css/variables.css` affecte tous les templates !

### 🎨 **Changer les polices**
5 propositions de combinaisons sont disponibles :

**Proposition 1 - Élégant et lisible**
- Titre : Playfair Display (serif élégant)
- Texte : Source Sans Pro (sans-serif moderne)

**Proposition 2 - Moderne et clean**
- Titre : Montserrat (sans-serif géométrique)
- Texte : Open Sans (très lisible)

**Proposition 3 - Traditionnel français**
- Titre : Crimson Text (serif classique)
- Texte : Lato (humaniste)

**Proposition 4 - Rustique et chaleureux**
- Titre : Merriweather (serif pour écran)
- Texte : PT Sans (équilibré)

**Pour activer une proposition :**
1. Dans `css/fonts.css` : décommentez l'import souhaité
2. Dans `css/variables.css` : décommentez la proposition correspondante
3. Rechargez la page pour voir le changement

## Instructions d'impression

### Préparation
1. Ouvrez le fichier HTML de votre choix dans votre navigateur web
2. Modifiez le contenu de la recette selon vos besoins :
   - Changez le titre dans la section `<header class="title">`
   - Ajoutez/modifiez les ingrédients dans la liste `<ul>`
   - Ajoutez/modifiez les instructions dans la liste `<ol>`

### Paramètres d'impression dans Chrome
1. Appuyez sur `Ctrl + P` (ou `Cmd + P` sur Mac) pour ouvrir le dialogue d'impression
2. Cliquez sur "Plus de paramètres" pour afficher toutes les options
3. **Destination** : Sélectionnez votre imprimante
4. **Format de papier** : 
   - Si A5 n'est pas disponible, sélectionnez "Personnalisé" 
   - Entrez : Largeur 210mm, Hauteur 148mm
5. **Mise en page** : Paysage
6. **Marges** : Aucune
7. **Échelle** : Personnalisé 100%
8. **Options** :
   - Décochez "En-têtes et pieds de page"
   - **IMPORTANT** : Cochez "Graphiques d'arrière-plan" pour que le fond bleu du titre s'imprime

### Si le fond bleu ne s'imprime toujours pas
1. Vérifiez que "Graphiques d'arrière-plan" est bien coché
2. Dans les paramètres avancés de votre imprimante, activez l'impression couleur
3. Certaines imprimantes ont une option "Économie d'encre" à désactiver

### Si A5 n'est pas disponible
- Utilisez du papier A4 et découpez ensuite aux dimensions A5 (148 × 210 mm)
- Ou imprimez en format "Personnalisé" avec les dimensions exactes

### Navigateurs recommandés
- **Chrome** : Excellent support des CSS d'impression
- **Firefox** : Bon support, vérifiez l'aperçu avant impression
- **Edge** : Support correct

### Conseils d'impression
- **Papier recommandé** : Papier blanc standard 80-90g/m²
- **Qualité** : Mode "Normal" ou "Élevé" pour des couleurs vives
- **Test** : Imprimez d'abord une page de test pour vérifier l'alignement
- **Découpe** : Si vous utilisez du papier A4, découpez selon les dimensions A5
- **Perforation** : Une marge de 25mm est prévue de chaque côté pour la perforation
- **Recto-verso** : Les marges identiques permettent l'impression recto-verso
- **Centrage** : Le contenu est automatiquement centré et optimisé pour l'espace

### Personnalisation
Pour modifier les couleurs ou la mise en page :
1. Ouvrez le fichier HTML dans un éditeur de texte
2. Modifiez les styles CSS dans la section `<style>`
3. Principales couleurs utilisées :
   - Bleu clair : `#87CEEB`
   - Bleu foncé : `#4682B4`
   - Arrière-plan : `white` ou `#f8fcff`

### Résolution des problèmes
- **La page ne tient pas** : Vérifiez que l'orientation est bien en paysage
- **Couleurs manquantes** : Activez l'impression des graphiques d'arrière-plan
- **Texte coupé** : Réduisez les marges du navigateur
- **Mauvaise taille** : Vérifiez que l'échelle est à 100%

## Support
Pour toute question ou personnalisation supplémentaire, modifiez directement le code HTML/CSS selon vos besoins.
