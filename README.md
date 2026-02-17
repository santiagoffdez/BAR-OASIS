# Cafe-Bar OASIS
>Une carte numérique interactive et responsive pour la présentation

Ce projet est une interface web vitrine pour le Cafe-Bar OASIS situé à Adra (Almería). Il permet aux clients de consulter les spécialités et le menu complet via une navigation fluide en accordéon. Le design est conçu avec Bootstrap pour assurer une compatibilité mobile optimale.

## Fonctionnalités principales
L'application propose les fonctionnalités d'affichage suivantes :
- **Carousel d'images** pour mettre en avant les spécialités visuelles.
- **Menu en accordéon** pour organiser les catégories (Petit-déjeuner, Tapas, Viandes, etc.) sans encombrer la page.
- **Design responsive** adapté aux smartphones et tablettes.
- **Traductions intégrées** (Espagnol / Anglais) pour les plats principaux.
- **Section contact** avec adresse et téléphone en pied de page.

## Aperçu du code
### Structure de l'accordéon (Menu)
Le menu utilise le composant "Panel" de Bootstrap pour créer des sections rétractables. Chaque catégorie est liée par un identifiant unique, comme par exemple `#collapseOne_1`.

```HTML
<div class="panel panel-primary">
    <div class="panel-heading" role="tab">
        <h4 class="panel-title">
            <a role="button" data-toggle="collapse" data-parent="#accordion_1"
                href="#collapseOne_1" aria-expanded="true">
                Desayuno
            </a>
        </h4>
    </div>
    <div id="collapseOne_1" class="panel-collapse collapse" role="tabpanel">
        <div class="panel-body">
            <ul>
                <li>Huevos Revueltos</li>
                <li>Fruta</li>
            </ul>
        </div>
    </div>
</div>
```

### Gestion des prix et traductions
Le code HTML structure l'information pour distinguer clairement le nom du plat, sa traduction et son prix grâce à des classes CSS spécifiques (`.tit-li`, `.precio`, `.traduccion`).

```HTML
<div class="m-b-0 col-xs-12 col-sm-6">
    <span class="tit-li">Desayuno Oasis (<span class="precio">3.50€</span>)</span>
    <ul>
        <li>Tomate con Melva (<span class="traduccion">tomato with melva</span>)</li>
        </ul>
</div>
```

## Installation et utilisation
**1. Structure des fichiers**
Assurez-vous que les dossiers `css`, `images` et `plugins` sont au même niveau que votre fichier HTML.

**Structure finale**
```
/Projet-Oasis
 ├── index.html
 ├── css/
 │   ├── style.css
 │   ├── custom.css
 │   ├── materialize.css
 │   └── themes/
 ├── fonts/
     └── Poppins-Medium.ttf
 ├── images/
 │   ├── logo.png
 │   └── foto_1.jpg...
 └── plugins/
     ├── jquery/
     └── bootstrap/
```

**2. Lancement** : Aucunt serveur n'est nécssaire. Ouvrez simplement le fichier `index.html` dans votre navigateur web préféré.

## Références
- Framework CSS : [Bootstrap 3](https://getbootstrap.com/)
- Bibliothèque JS : [jQuery](https://jquery.com/)