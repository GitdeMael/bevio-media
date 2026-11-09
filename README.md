# bevio-media

Visuels publiés sur Instagram **@beviosite** (agence Bevio, sites internet, Angers).

Ce repo est **public** : chaque fichier ici est visible par tout le monde. On n'y met que ce qui finira de toute façon en ligne. Jamais de photo client sans accord écrit, jamais d'audit, de devis ou de document avec des tarifs ou des coordonnées personnelles.

## Contenu

| Dossier | Rôle |
|---|---|
| `charte/` | Identité graphique Bevio, version 4 (novembre 2026) : logos, kit Instagram, couleurs, police Inter, charte PDF. Source de vérité pour tout visuel. |
| `posts/` | Visuels prêts à publier, un dossier par mois : `posts/2026-11/2026-11-12_sujet.jpg`. Un carrousel = un dossier `2026-11-12_sujet/` avec `01.jpg`, `02.jpg`… |
| `tests/` | Fichiers de test techniques, jamais publiés. |

Adresse publique d'un fichier, à donner à Instagram :
`https://raw.githubusercontent.com/GitdeMael/bevio-media/main/<chemin du fichier>`

## Règles de fabrication des visuels

Elles reprennent `charte/charte-graphique-bevio.pdf` (page 2) et ajoutent les contraintes techniques de la publication automatique.

### Contraintes techniques (publication par l'API Instagram)

- **Format JPEG uniquement**, 8 Mo maximum, en sRGB. Les fonds de la charte sont en PNG : le visuel final est toujours exporté en JPEG (qualité 90).
- **Ratio accepté : de 4:5 à 1.91:1.** Le format 3:4 (1080 × 1440) recommandé par la charte est plus étroit que 4:5 : l'API le refuse. Pour les posts publiés automatiquement, on utilise **4:5 (1080 × 1350)**, sauf si un test prouve un jour que le 3:4 passe.
- Carrousel : 2 à 10 images, toutes au même format, photos uniquement (pas de vidéo dans un carrousel).
- Story : image JPEG ou vidéo MP4/MOV de 3 à 60 s, 1080 × 1920. Pas de légende possible.
- Reel : vidéo MP4/MOV, 3 s à 15 min, 9:16 conseillé.

### Fonds selon le type de post

- `sarcelle-trame` : annonces, réalisations, avant / après
- `lilas-pale-trame` : conseils, carrousels pédagogiques
- `creme-uni` : avis clients, citations, texte long

Utiliser la version `_signe` (logo déjà placé en bas au centre), sauf si le logo apparaît déjà ailleurs dans le visuel.

### Typographie

- Titres : Inter Display SemiBold ou Inter SemiBold, 64 à 96 px sur 1080 px de large.
- Texte : Inter Regular, 32 px minimum.
- Fichiers dans `charte/3-couleurs-et-police/police-Inter/`.

### Couleurs

| Nom | HEX | Usage |
|---|---|---|
| Sarcelle nuit | `#0A3438` | Texte et fonds forts |
| Lilas | `#8E70C9` | Accent sur fond clair (titres uniquement) |
| Lilas clair | `#B9A3E8` | Accent sur fond sarcelle |
| Lilas pâle | `#F1EDF8` | Fonds clairs |
| Crème | `#F2EFE9` | Texte et blocs sur sarcelle |
| Gris | `#4A5D5F` | Texte secondaire sur fond clair |
| Gris clair | `#A9C9C6` | Texte secondaire sur fond sarcelle |

### Mise en page

- 80 px de marge minimum autour des textes.
- Un seul mot en accent par visuel (lilas clair sur sarcelle, lilas sur fond clair), en titre seulement.
- Deux couleurs de texte maximum par visuel.
- Jamais de lilas en texte courant.
- Logo jamais recoloré, déformé, ni posé sur une photo chargée.
- Vérifier le placement avec `charte/2-instagram/gabarits-zones-de-securite/` : rien d'important dans les zones rognées par la grille du profil.

## Circuit de publication

1. Maël donne le sujet (et éventuellement le texte, des photos, un angle).
2. Claude crée le visuel selon les règles ci-dessus, l'exporte en JPEG et le range dans `posts/`.
3. Claude rédige la légende.
4. Maël valide le visuel **et** la légende. Aucune publication sans validation explicite du post précis.
5. Claude pousse le fichier sur le repo et publie sur @beviosite avec l'adresse publique.
