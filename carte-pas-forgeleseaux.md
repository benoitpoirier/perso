Tu es un expert senior en développement front-end, cartographie web (Leaflet.js) et design UI/UX. Tu vas concevoir le code complet d'une carte interactive HTML/JS autonome de type "poster professionnel" pour un Pôle d'Accompagnement à la Scolarité (PAS).

### Objectif Principal
Générer un fichier HTML unique, propre et hautement professionnel affichant une carte géographique centrée sur le secteur géographique configuré (ex. Pays de Bray / Forges-les-Eaux et environs), avec des épingles (PIN) pour chaque établissement scolaire, reliées à des étiquettes latérales sans aucun croisement de lignes.

### Contraintes et Règles de Conception strictes :

1. **Agencement et Alignement (Layout "Boîte à Outils d'Ingénierie") :**
   - **Colonnes d'étiquettes latérales :** Les étiquettes portant le nom complet des établissements (avec leur commune entre parenthèses) ne doivent PAS flotter aléatoirement. Elles doivent être réparties et **alignées verticalement en deux colonnes strictes** de part et d'autre de la carte : une colonne à l'extrême **Gauche** et une colonne à l'extrême **Droite** (selon la position géographique ouest/est du PIN sur la carte).
   - **Pas de chevauchement d'étiquettes :** Chaque étiquette au sein d'une même colonne doit disposer d'un espacement vertical fixe et régulier (pas de superposition de texte).

2. **Routage des Lignes de Liaison (Leader Lines) :**
   - Chaque PIN géographique doit être relié à son étiquette correspondante par une **ligne de raccordement soignée et design**.
   - **Zéro croisement de lignes :** Les lignes ne doivent jamais se croiser de manière anarchique. Privilégiez des tracés orthogonaux (segments horizontaux et verticaux à 90°, style schématique ou diagramme technique) ou des courbes de Bézier douces et fluides.
   - Les lignes doivent utiliser la même couleur que le code thématique du type d'établissement (Maternelle, Élémentaire, Primaire, Collège, Lycée) avec une opacité maîtrisée pour rester discrètes et élégantes.

3. **Design et Ergonomie Générale :**
   - **Design de type "Poster" :** Un en-titre (titre et sous-titre) élégant et moderne flottant en haut au centre, et une légende claire et stylisée ancrée dans un coin.
   - **Fond de carte neutre :** Utilisation d'un fond OpenStreetMap propre, sans watermark publicitaire lourd, optimisé pour l'exportation PDF haute définition (`Ctrl + P`).
   - **Interactivité :** Au clic sur un PIN ou une étiquette, une pop-up élégante affiche les informations détaillées (Nom, Type, Commune, Code UAI).
   - **Dynamisme :** Les lignes SVG de raccordement doivent se recalculer et s'ajuster en temps réel si l'utilisateur zoome ou déplace la carte.
   - Les etiquettes sont repartie de manière logique, de chaque coté de l'ecran
   - Les etiquettes d'un meme coté sont equi distantes les une des autres
   - Le design et soigné.

### Données à intégrer :
UAI,Type,Établissement,Commune,"Coordonnées (Lat, Lon)"
0760306V,Maternelle,Ecole maternelle le Mont-Huleu,ARGUEIL,"49.5396, 1.5147"
0761270T,Élémentaire,Ecole élémentaire,AVESNES EN BRAY,"49.4608, 1.6749"
0761416B,Maternelle,Ecole maternelle,BEAUSSAULT,"49.6848, 1.5630"
0760307W,Élémentaire,Ecole élémentaire,BEAUVOIR EN LYONS,"49.5033, 1.5204"
0761271U,Élémentaire,Ecole élémentaire,BEZANCOURT,"49.4452, 1.6165"
0761273W,Élémentaire,Ecole élémentaire,BREMONTIER MERVAL,"49.5042, 1.6111"
0761767H,Lycée,Lycée pro. agricole du Pays de Bray,BREMONTIER MERVAL,"49.5050, 1.6150"
0763086S,Élémentaire,Ecole élémentaire,COMPAINVILLE,"49.6644, 1.5491"
0762593F,Maternelle,Ecole maternelle Maurice Prévert,CROISY SUR ANDELLE,"49.4632, 1.3934"
0761274X,Primaire,Ecole primaire Roger Cressent,CUY ST FIACRE,"49.5097, 1.6961"
0761275Y,Élémentaire,Ecole élémentaire,DAMPIERRE EN BRAY,"49.5375, 1.6514"
0760446X,Élémentaire,Ecole élémentaire,ELBEUF SUR ANDELLE,"49.4756, 1.3986"
0762446W,Primaire,Ecole primaire Charles Trenet,FERRIERES EN BRAY,"49.4827, 1.7483"
0761695E,Collège,Collège Saint-Exupéry,FORGES LES EAUX,"49.6166, 1.5375"
0761297X,Maternelle,Ecole maternelle Marguerite Couturier,FORGES LES EAUX,"49.6111, 1.5422"
0761412X,Élémentaire,Ecole élémentaire Eugène Anne,FORGES LES EAUX,"49.6120, 1.5410"
0762020H,Primaire,Ecole primaire privée Sacré-Coeur,FORGES LES EAUX,"49.6133, 1.5444"
0762600N,Lycée,Lycée Delamare-Deboutteville,FORGES LES EAUX,"49.6145, 1.5360"
0762503H,Primaire,Ecole primaire les Petit Mots Passants,GAILLEFONTAINE,"49.6542, 1.6175"
0761422H,Élémentaire,Ecole élémentaire Lazare Hoche,GAILLEFONTAINE,"49.6530, 1.6180"
0760046M,Collège,Collège Rollon,GOURNAY EN BRAY,"49.4800, 1.7250"
0761734X,Collège,Collège Saint-Hildevert,GOURNAY EN BRAY,"49.4805, 1.7234"
0762021J,Primaire,Ecole primaire privée Saint Hildevert,GOURNAY EN BRAY,"49.4810, 1.7240"
0762325P,Maternelle,Ecole maternelle Pierre et Marie Curie,GOURNAY EN BRAY,"49.4830, 1.7210"
0763100G,Élémentaire,Ecole élémentaire Georges Brassens,GOURNAY EN BRAY,"49.4845, 1.7260"
0761427N,Maternelle,Ecole maternelle,HAUSSEZ,"49.5694, 1.6961"
0762177D,Collège,Collège la Hêtraie,LA FEUILLIE,"49.4625, 1.5150"
0762527J,Élémentaire,Ecole élémentaire les Prunus,LA FEUILLIE,"49.4630, 1.5160"
0762748Z,Maternelle,Ecole maternelle les petits feuillois,LA FEUILLIE,"49.4635, 1.5155"
0760314D,Élémentaire,Ecole élémentaire,LA HALLOTIERE,"49.5186, 1.4647"
0763133T,Maternelle,Ecole maternelle,MAUQUENCHY,"49.5925, 1.4883"
0761429R,Élémentaire,Ecole élémentaire,MESNIL MAUGER,"49.6381, 1.5208"
0761282F,Maternelle,Ecole maternelle,MONTROTY,"49.4072, 1.6669"
0760319J,Élémentaire,Ecole élémentaire,MORVILLE LE HERON,"49.4667, 1.4239"
0760449A,Élémentaire,Ecole élémentaire,MORVILLE LE HERON,"49.4667, 1.4239"
0762435J,Primaire,Ecole primaire Jean Moulin,NEUF MARCHE,"49.4239, 1.7161"
0761430S,Élémentaire,Ecole élémentaire,RONCHEROLLES EN BRAY,"49.6267, 1.4697"
0762540Y,Primaire,Ecole primaire Jean Jaurès,SERQUEUX,"49.6319, 1.5433"
0760322M,Primaire,Ecole primaire,SIGY EN BRAY,"49.5447, 1.4800"
0762465S,Primaire,Ecole primaire,SOMMERY,"49.6264, 1.4553"

Crée un fichier HTML embarquant l'ensemble du code necessaire (HTML, CSS, JS et JSON).
Les bibliotheques JS peuvent etre référencées depuis des sources internet.

utilise un fond de carte  gratuit sans watermark comme openstreetmap ou mieux, plus design t soignée, si tu peux trouver.
centre la légende horizontalement et place là en bas de l'ecran afin qu'elle ne chevauche pas les etiquettes.

Adapte la taille de la font des etiquettes afin que les etiquettes occupe tout l'expace vertical de l'ecran