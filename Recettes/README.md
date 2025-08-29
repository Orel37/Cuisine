# Recettes - Format A5 Paysage

Ce dossier contient des modèles HTML/CSS pour imprimer des recettes sur du papier A5 en orientation paysage.

## 📁 Organisation des dossiers

Les recettes sont organisées selon une structure à deux niveaux :

```
Recettes/
├── css/                    # Styles CSS communs
├── templates/              # Templates de base
├── francais/              # Cuisine française
│   ├── entrees/
│   ├── plats/
│   ├── desserts/
│   └── sauces/
├── italien/               # Cuisine italienne
│   ├── entrees/
│   ├── plats/
│   ├── desserts/
│   └── sauces/
├── asiatique/             # Cuisine asiatique
│   ├── entrees/
│   ├── plats/
│   ├── desserts/
│   └── sauces/
└── lorraine/              # Cuisine lorraine/familiale
    ├── entrees/
    ├── plats/
    ├── desserts/
    └── sauces/
```

### Principes d'organisation

**Premier niveau** - Style culinaire :
- `francais/` : Cuisine française traditionnelle
- `italien/` : Cuisine italienne
- `asiatique/` : Cuisine asiatique (chinoise, japonaise, thaï, etc.)
- `lorraine/` : Cuisine lorraine et spécialités familiales.

**Deuxième niveau** - Type de plat :
- `entrees/` : Entrées, amuse-bouches, hors-d'œuvre
- `plats/` : Plats principaux, résistance
- `desserts/` : Desserts, pâtisseries, sucreries
- `sauces/` : Sauces, vinaigrettes, accompagnements

## Templates disponibles

### Templates HTML dans `/templates/`
- `courte.html` - Template pour recettes courtes (design confortable)
- `longue.html` - Template pour recettes longues (design compact)

### CSS Modulaire dans `/css/`
- `fonts.css` - Google Fonts (polices optionnelles)
- `variables.css` - Variables CSS (couleurs, tailles, espacements)
- `base.css` - Styles communs (structure de base, impression)
- `recette-courte.css` - Styles spécifiques aux recettes courtes
- `recette-longue.css` - Styles spécifiques aux recettes longues

> **Note** : La structure CSS est modulaire avec des variables centralisées.

## Quel template choisir ?

### 📝 Recette Courte
**Utilisez `template/recette/courte.html` quand :**
- Moins de 8-9 étapes d'instructions
- Recettes simples (cookies, crêpes, vinaigrettes...)
- Vous privilégiez la lisibilité

**Caractéristiques :**
- Police 12px (confortable à lire)
- Numéros avec cercles colorés
- Espacement généreux
- Ratio 30% ingrédients / 70% instructions

### 📚 Recette Longue
**Utilisez `template/recette/longue.html` quand :**
- Plus de 9 étapes d'instructions
- Recettes complexes (plats mijotés, pâtisseries...)
- Vous avez besoin de place maximum

**Caractéristiques :**
- Police 11px (compact mais lisible)
- Numérotation simple (sans cercles)
- Espacement minimal
- Ratio 25% ingrédients / 75% instructions
- Abréviations culinaires intégrées

## Guide de création d'une recette

### 1. Choisir le template
Copiez un template depuis `/templates/` selon vos besoins (voir section précédente).

### 2. Choisir l'emplacement
Placez votre nouvelle recette dans le bon dossier :
```
[style-culinaire]/[type-de-plat]/nom-de-la-recette.html
```

**Exemples :**
- `francais/plats/coq-au-vin.html`
- `asiatique/entrees/gyozas.html`
- `italien/desserts/tiramisu.html`
- `lorraine/sauces/bechamel.html`

### 3. Modifier le contenu
1. Changez le titre de la recette
2. Modifiez les ingrédients et quantités
3. Adaptez les instructions
4. Ajoutez ou supprimez des éléments `<li>` selon vos besoins

> **Note** : Les chemins CSS (`../../css/recette-courte.css`) sont automatiquement corrects !

## Fonctionnalités avancées

### Classes CSS spéciales

#### Classe `.note` pour les remarques importantes
```html
<div class="note">
  <strong>Note :</strong> Information importante sur la recette.
</div>
```

#### Sous-listes à puces dans les instructions
```html
<ol>
  <li>Première étape principale
    <ul>
      <li>Option A : méthode manuelle</li>
      <li>Option B : méthode mécanique</li>
    </ul>
  </li>
</ol>
```

### Abréviations intégrées
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

## Personnalisation

### Modifier les couleurs
Éditez le fichier `css/variables.css` pour changer :
- `--color-primary-blue` : couleur du titre et séparateurs
- `--color-secondary-blue` : couleur des numéros et titres de sections
- `--color-text-dark` : couleur du texte principal

### Ajuster les tailles
Dans `css/variables.css`, modifiez :
- `--font-size-*` : tailles de police
- `--spacing-*` : espacements
- `--ingredients-width-*` : largeur de la colonne ingrédients

### Architecture modulaire
- `css/variables.css` : Toutes les variables centralisées
- `css/base.css` : Structure commune (ne pas modifier)
- `css/recette-*.css` : Styles spécifiques (safe à modifier)

> Un seul changement dans `css/variables.css` affecte tous les templates !

## Instructions d'impression

### Paramètres recommandés
1. **Format** : A5 paysage (210mm × 148mm)
2. **Marges** : Aucune
3. **Échelle** : 100%
4. **Graphiques d'arrière-plan** : ✅ Activé (important pour le fond bleu du titre)

### Étapes détaillées dans Chrome
1. Ouvrez votre recette HTML dans Chrome
2. Appuyez sur `Ctrl + P` (ou `Cmd + P` sur Mac)
3. Cliquez sur "Plus de paramètres"
4. Configurez :
   - **Format de papier** : A5 ou Personnalisé (210mm × 148mm)
   - **Mise en page** : Paysage
   - **Marges** : Aucune
   - **Échelle** : 100%
   - **Options** : Cochez "Graphiques d'arrière-plan"

### Conseils et résolution de problèmes

#### Conseils d'impression
- **Papier** : Standard 80-90g/m² blanc
- **Qualité** : Mode "Normal" ou "Élevé" pour des couleurs vives
- **Test** : Imprimez d'abord une page test
- **Marges** : 25mm prévues de chaque côté pour perforation/reliure

#### Problèmes courants
- **Fond bleu manquant** → Activez "Graphiques d'arrière-plan"
- **Page trop grande** → Vérifiez l'orientation paysage et l'échelle 100%
- **A5 indisponible** → Utilisez "Personnalisé" (210mm × 148mm)
- **Texte coupé** → Réduisez les marges du navigateur

#### Navigateurs supportés
- **Chrome** : Support excellent (recommandé)
- **Firefox** : Support bon
- **Edge** : Support correct

---

## Support et contributions

Ce système de recettes est prévu pour être modifié selon vos besoins. N'hésitez pas à adapter les templates et styles CSS pour personnaliser vos recettes.
