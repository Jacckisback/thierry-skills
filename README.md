# Thierry Skills

Un skill pour Claude qui tient le rôle de directeur artistique : il conçoit des sites web sur mesure, avec une personnalité propre à chaque sujet, puis vérifie le résultat à l'écran avant de dire que c'est fini.

Les agents savent écrire du code d'interface correct. Ils savent beaucoup moins bien **avoir une idée** : la plupart des sites générés se ressemblent, parce qu'ils sont la moyenne de tous les sites. Ce skill part du métier, du lieu et de la matière du client pour trouver un concept, en déduit un système (typographie, couleur, espace, forme, image, voix, mouvement), l'exécute, puis capture le rendu et le note.

## Installer

```bash
npx skills@latest add Jacckisback/thierry-skills
```

Ou à la main : copie le dossier `skills/thierry-skill` dans le dossier `.claude/skills/` de ton projet (ou dans `~/.claude/skills/` pour l'avoir partout).

Dans Claude (claude.ai) : compresse le dossier `skills/thierry-skill` en `.zip` et importe-le dans les réglages des skills.

Les deux scripts de vérification demandent Node 18 ou plus. `regard.mjs` demande aussi Playwright avec Chromium :

```bash
npm i -D playwright
```

```bash
npx playwright install chromium
```

## Utiliser

Une phrase suffit :

> Utilise thierry-skill : crée la page d'accueil d'un caviste de vins nature à Madrid.

| Tu dis | Le skill fait |
| --- | --- |
| « Crée un site pour… » | une fiche de direction artistique, le code, puis la revue sur captures |
| « Refais ce site » | le diagnostic, ce qu'on garde, la nouvelle direction, un avant/après |
| « Qu'en penses-tu ? » | une note sur 100 et des corrections classées, sans rien modifier |
| « Peaufine » | les finitions, sans toucher au concept |
| « Ça fait générique », « ça fait IA » | la liste des tics repérés et leur remplacement |
| « Propose des pistes » | trois directions réellement différentes |
| « Prompt Lovable » | un prompt prêt à coller dans Lovable ou un autre générateur |

## Comment il travaille

Sept temps, dans cet ordre :

1. **Comprendre** : qui vient, pour quoi, et quelles matières appartiennent à ce monde (objets, documents, gestes, mots du métier).
2. **Trouver l'idée** : une phrase de la forme « Le site est [une métaphore tirée du sujet], pour que le visiteur ressente [un sentiment] », et une signature visuelle unique.
3. **Régler la personnalité** : sept curseurs (température, densité, énergie, ornement, époque, registre, contraste) convertis en valeurs précises.
4. **Construire le système** : polices, couleurs en OKLCH, grille, forme, image, voix, mouvement.
5. **Composer** : le déroulé de la page, section par section.
6. **Exécuter** : tous les états, le vrai texte, le mobile conçu en même temps que le bureau.
7. **Regarder, noter, reprendre** : captures à trois largeurs, cinq tests visuels, note sur 100.

Test central : si on remplace le logo par celui d'un concurrent et que le site fonctionne encore, il n'y a pas d'idée.

## Contenu

```
skills/thierry-skill/
├── SKILL.md                         le processus, les lois, les formats de sortie
├── references/
│   ├── 01-direction-artistique.md   concept, signature, conversion des curseurs
│   ├── 02-univers-par-secteur.md    vingt et un secteurs : attentes, clichés, deux directions
│   ├── 03-typographie.md            choix, associations, échelle, réglages, chargement
│   ├── 04-couleur.md                palette en OKLCH, contrastes, mode sombre
│   ├── 05-composition.md            espace, grille, premier écran, image, mobile
│   ├── 06-mouvement.md              quand animer, courbes, durées, chorégraphie, défilement
│   ├── 07-finitions.md              états, formulaires, accessibilité, performance, SEO
│   ├── 08-anti-generique.md         les tics « fait IA » et leur remplacement
│   ├── 09-ecriture.md               titres, boutons, typographie FR, ES, DE, EN, IT, PT
│   ├── 10-revue.md                  grille de notation sur 100, format de critique
│   └── 11-brief-lovable.md          gabarit de prompt et exemple rempli
├── assets/tokens.css                socle de variables, neutre, à adapter
└── scripts/
    ├── regard.mjs                   captures et mesures du rendu
    └── audit.mjs                    audit statique du code
```

## Les scripts

**`regard.mjs`** ouvre une URL ou un fichier HTML, le capture à plusieurs largeurs (premier écran, page entière, tranches lisibles, version en niveaux de gris, version floutée) et mesure ce que l'œil rate : contrastes insuffisants, débordement horizontal, cibles tactiles trop petites, lignes trop longues, polices non chargées, images sans dimensions, structure des titres, ce qui reste animé en mouvement réduit.

```bash
node skills/thierry-skill/scripts/regard.mjs http://localhost:3000 --out revue
```

Options : `--largeurs 360,768,1440`, `--hauteur 640`, `--attente 2000`, `--sombre`, `--dpr 2`.

**`audit.mjs`** parcourt le code et signale les tics et les fautes d'exécution : `transition: all`, entrées depuis `scale(0)`, focus supprimé, dégradés violets, texte de remplissage, typographie française fautive, et une trentaine d'autres.

```bash
node skills/thierry-skill/scripts/audit.mjs ./src
```

Les deux scripts donnent des indices, pas des verdicts. Ils ne testent ni le clavier, ni les états de formulaire, ni les lecteurs d'écran.

## Limites

- Le skill est écrit en français. Il produit des sites dans n'importe quelle langue.
- Il ne remplace pas le contenu du client : sans vraies photos, vrais prix et vraies preuves, il marque les emplacements « à fournir » au lieu d'inventer, et la note plafonne.
- Les directions par secteur sont des points de départ. Le sur-mesure vient de ce que le client a de particulier.

## Origine

Ce skill est né de l'étude des [skills d'Emil Kowalski](https://github.com/emilkowalski/skills), qui couvrent avec une grande précision l'animation et le détail d'interface. Celui-ci élargit le champ à la direction artistique complète et ajoute la vérification du rendu. Le texte et le code sont originaux.

## Licence

[MIT](LICENSE)
