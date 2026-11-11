<p align="center">
  <a href="../README.md">English</a> ·
  <strong>Français</strong> ·
  <a href="README.de.md">Deutsch</a> ·
  <a href="README.es.md">Español</a> ·
  <a href="README.it.md">Italiano</a> ·
  <a href="README.pt.md">Português</a>
</p>

<p align="center">
  <img src="images/hero.svg" alt="Thierry Skill : direction artistique web sur mesure" width="100%">
</p>

# Thierry Skill

**Un directeur artistique pour Claude.** Ce skill fait travailler Claude comme un bon studio : il trouve une idée dans le métier du client, en déduit un système visuel complet, construit le site, puis regarde le rendu et le note avant de dire que c'est fini.

[![Licence : MIT](https://img.shields.io/badge/licence-MIT-14161a.svg)](../LICENSE)
![Compatible Claude Code](https://img.shields.io/badge/Claude_Code-skill-e5412d.svg)
![Langue du skill : français](https://img.shields.io/badge/langue_du_skill-français-5c6370.svg)

```bash
npx skills@latest add Jacckisback/thierry-skills
```

## Le problème

Les agents écrivent du code d'interface correct. Il leur manque un point de vue. Demandez « un beau site moderne » et vous obtenez la moyenne de tous les sites : la même police, le même dégradé violet, les mêmes trois cartes à icônes. Rien n'est faux, et rien ne reste en mémoire.

Les skills de design existants polissent surtout la surface : courbes, durées, micro-interactions. Ce travail compte, mais il vient en dernier. Un site aux animations parfaites et sans idée reste un gabarit.

## Ce que ce skill change

Il oblige Claude à répondre à trois questions, dans l'ordre, avant d'ajouter le moindre effet :

1. **Quelle est l'idée ?** Une phrase qui dit quelque chose de précis sur ce client, que le site d'un concurrent ne pourrait pas dire.
2. **Quel est le système ?** Typographie, couleur, espace, forme, image, voix et mouvement, tous déduits de cette idée.
3. **Est-ce juste à l'écran ?** Des captures à trois largeurs, mesurées et notées.

Deux briefs d'une phrase, deux résultats sans rapport :

<table>
  <tr>
    <td width="50%"><img src="images/demo-luthier.png" alt="Page d'accueil d'un luthier, composée comme le carnet de commandes de l'atelier"></td>
    <td width="50%"><img src="images/demo-pour-contre.png" alt="Premier écran du site d'une avocate en droit du travail : POUR les salariés, CONTRE leur employeur"></td>
  </tr>
  <tr>
    <td><em>« Un site pour un luthier de guitares flamencas à Madrid, trois guitares par mois, sur commande. »</em><br>Idée : le carnet de commandes de l'atelier. Trois lignes par mois, l'une peut porter votre nom.</td>
    <td><em>« Un site pour une avocate en droit du travail à Lyon, qui défend uniquement les salariés. »</em><br>Idée : un jeu de conclusions. « Pour : les salariés. Contre : leur employeur. »</td>
  </tr>
</table>

Ces deux pages ont été produites par le skill pendant ses essais, à partir de briefs fictifs. Notées avec sa propre grille, elles ont obtenu 81 et 82 sur 100. C'est sous son seuil de 85, surtout parce qu'un brief d'une phrase ne contient ni vraies photos, ni prix, ni preuves, et que le skill marque ces emplacements « à fournir » au lieu d'inventer.

## La direction artistique, expliquée

Un site est beau quand trois choses sont vraies en même temps :

- **Une idée.** Il dit quelque chose de précis sur son sujet.
- **Un système.** Chaque choix visuel découle de cette idée, et les choix se répondent.
- **Une exécution.** Chaque détail invisible est juste : alignements, états, rythme, vitesse, accessibilité.

La plupart des sites ratent le premier point et compensent par des effets. Un effet n'est jamais une idée.

Le skill cherche l'idée dans ce dont le métier est fait : ses objets, ses documents, ses gestes, ses lieux, ses matières, ses mots, ses mesures. Un caviste a des étiquettes et des fiches de dégustation. Un architecte a des plans et des coupes. Un avocat a des conclusions. Ces formes appartiennent déjà au client : un site construit à partir d'elles ne peut pas être confondu avec celui d'un autre.

Le test central est celui du **logo échangé** : remplacez le logo par celui d'un concurrent direct. Si le site fonctionne encore, il n'y a pas d'idée, et le travail reprend.

<p align="center">
  <img src="images/process.svg" alt="Les sept temps du skill" width="100%">
</p>

*Les sept temps : comprendre, trouver l'idée, régler la personnalité, construire le système, composer, exécuter, regarder et noter.*

### La personnalité en chiffres

« Chaleureux », « sérieux » ou « audacieux » ne disent rien à une feuille de style. Le skill place sept curseurs de 0 à 10 (température, densité, énergie, ornement, époque, registre, contraste) et convertit chacun en paramètres concrets : rayons, graisses, interlettrage, durées, marges, saturation. Deux entreprises du même secteur reçoivent des réglages différents : c'est de là que vient le sur-mesure.

<p align="center">
  <img src="images/sliders.svg" alt="Sept curseurs de personnalité pour deux directions d'un même métier" width="100%">
</p>

## En chiffres

| | |
| --- | --- |
| **7** | temps, du brief à la revue |
| **9** | lois que le skill n'enfreint jamais sans qu'on le lui demande |
| **7** | curseurs de personnalité, chacun converti en valeurs exactes |
| **21** | secteurs, avec les attentes du visiteur, les clichés à écarter et deux directions opposées |
| **10** | architectures de premier écran au choix |
| **11** | fichiers de référence, environ 30 000 mots, chargés seulement au besoin |
| **6** | langues dont la typographie est réglée : français, espagnol, allemand, anglais, italien, portugais |
| **35** | contrôles statiques sur le code (`audit.mjs`) |
| **22** | contrôles sur la page rendue (`regard.mjs`) |
| **100** | points dans la grille de revue, sur 9 axes pondérés |

## Il vérifie son propre travail

Un design jugé seulement en lisant du code n'a pas été jugé. Le dernier temps est obligatoire : capturer, regarder, noter, corriger.

`regard.mjs` ouvre la page dans un vrai navigateur à trois largeurs. Il enregistre le premier écran, la page entière, des tranches lisibles, une version en niveaux de gris et une version floutée, puis mesure ce que l'œil rate.

<table>
  <tr>
    <td width="33%"><img src="images/regard-ecran.png" alt="Capture du premier écran"></td>
    <td width="33%"><img src="images/regard-gris.png" alt="Capture en niveaux de gris"></td>
    <td width="33%"><img src="images/regard-flou.png" alt="Capture floutée"></td>
  </tr>
  <tr>
    <td><strong>Premier écran.</strong> Le test des cinq secondes : que retient un inconnu ?</td>
    <td><strong>Niveaux de gris.</strong> La hiérarchie tient-elle sans la couleur ?</td>
    <td><strong>Flou.</strong> Le test des yeux plissés : une masse dominante, puis une deuxième, puis le reste.</td>
  </tr>
</table>

Mesuré à chaque passage : le contraste du texte selon les seuils WCAG, le débordement horizontal, les cibles tactiles sous 24 et 44 px, la longueur des lignes, les familles et tailles de polices réellement affichées, les polices non chargées, les images sans dimensions ou sans texte alternatif, la structure des titres, les champs sans étiquette, les décalages de mise en page, et ce qui bouge encore quand le visiteur a demandé moins de mouvement.

`audit.mjs` lit le code source et signale les tics de gabarit et les fautes d'exécution : `transition: all`, entrées depuis `scale(0)`, anneaux de focus supprimés, dégradés violets, texte de remplissage, libellés de boutons vagues, ponctuation française fautive.

Ensuite la page est notée. Sous 85, les trois faiblesses les plus lourdes sont corrigées et la page est capturée de nouveau.

<p align="center">
  <img src="images/score.svg" alt="La grille de revue sur 100 points" width="100%">
</p>

*La grille : idée et personnalité 20, typographie 15, composition 15, couleur et forme 10, contenu et voix 10, finitions 10, accessibilité et performance 10, image 5, mouvement 5.*

## Ce que vous pouvez demander

| Vous dites | Le skill livre |
| --- | --- |
| « Crée un site pour… » | une fiche de direction artistique, le code, puis la revue sur captures |
| « Refais ce site » | le diagnostic, ce qu'on garde, la nouvelle direction, un avant/après |
| « Qu'en penses-tu ? » | une note sur 100 et des corrections classées, sans rien modifier |
| « Peaufine » | les finitions, sans toucher au concept |
| « Ça fait générique », « ça fait IA » | la liste des tics repérés et ce qui remplace chacun |
| « Propose des pistes » | trois directions qui diffèrent par le concept, pas par la couleur |
| « Prompt Lovable » | un prompt prêt à coller dans Lovable ou un autre générateur |

## Installer

```bash
npx skills@latest add Jacckisback/thierry-skills
```

Ou à la main : copiez `skills/thierry-skill` dans le dossier `.claude/skills/` de votre projet, ou dans `~/.claude/skills/` pour l'avoir partout. Dans les applications Claude, compressez le dossier `skills/thierry-skill` en `.zip` et importez-le dans les réglages des skills.

Les deux scripts demandent Node 18 ou plus. `regard.mjs` demande aussi Playwright avec Chromium :

```bash
npm i -D playwright
```

```bash
npx playwright install chromium
```

## Utiliser

Une phrase suffit :

> Utilise thierry-skill : crée la page d'accueil d'un caviste de vins nature à Madrid.

Le skill est écrit en français et répond dans la langue où vous écrivez. Il construit des sites dans toutes les langues.

Les scripts se lancent aussi à la main :

```bash
node skills/thierry-skill/scripts/regard.mjs http://localhost:3000 --out revue
```

```bash
node skills/thierry-skill/scripts/audit.mjs ./src
```

## Contenu

```
skills/thierry-skill/
├── SKILL.md                         le processus, les lois, les formats de sortie
├── references/
│   ├── 01-direction-artistique.md   concept, signature, conversion des curseurs
│   ├── 02-univers-par-secteur.md    21 secteurs : attentes, clichés, deux directions
│   ├── 03-typographie.md            choix, associations, échelle, réglages, chargement
│   ├── 04-couleur.md                palettes en OKLCH, contrastes, mode sombre
│   ├── 05-composition.md            espace, grille, premier écran, image, mobile
│   ├── 06-mouvement.md              quand animer, courbes, durées, chorégraphie
│   ├── 07-finitions.md              états, formulaires, accessibilité, performance, SEO
│   ├── 08-anti-generique.md         les tics « fait IA » et leur remplacement
│   ├── 09-ecriture.md               titres, boutons, typographie en six langues
│   ├── 10-revue.md                  la grille sur 100 et le format de critique
│   └── 11-brief-lovable.md          gabarit de prompt avec un exemple rempli
├── assets/tokens.css                variables CSS neutres, à adapter
└── scripts/
    ├── regard.mjs                   captures et mesures
    └── audit.mjs                    audit statique du code
```

## L'objectif

Des sites qui ne peuvent appartenir qu'à leur propriétaire. Un visiteur doit pouvoir décrire le site de mémoire le lendemain, et le client doit y reconnaître son métier. Le skill traite la beauté comme le résultat d'une précision : une idée vraie, un système strict, une preuve à l'écran.

## Limites

- Il ne remplace pas le contenu du client. Sans vraies photos, vrais prix et vraies preuves, il marque les emplacements et la note plafonne.
- Les directions par secteur sont des points de départ. Reprises telles quelles, elles donneraient le même site à toutes les entreprises d'un secteur.
- Les scripts donnent des indices à vérifier à l'œil. Ils ne testent ni la navigation au clavier, ni les états de formulaire, ni les lecteurs d'écran.
- Les résultats dépendent du modèle qui exécute le skill, et n'ont été testés que sur deux briefs à ce jour.

## Origine

Ce skill est né de l'étude des [skills d'Emil Kowalski](https://github.com/emilkowalski/skills), qui couvrent l'animation et le détail d'interface avec une grande précision. Il élargit le champ à la direction artistique complète et ajoute la vérification du rendu. Le texte et le code sont originaux.

## Licence

[MIT](../LICENSE)
