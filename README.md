# Concevoir un hit Roblox — De l'analyse au Game Design Document complet

> Document de direction créative. Objectif : concevoir un jeu original, addictif, respectueux du joueur, réalisable par une seule personne assistée par IA, avec un potentiel Top 100 Roblox.

---

# PARTIE 1 — Pourquoi les plus gros jeux Roblox fonctionnent

Avant de créer, il faut disséquer. Voici ce qui se cache réellement sous le capot des mastodontes.

## 1.1 Lecture rapide des références

| Jeu | Genre réel | Moteur psychologique dominant |
|---|---|---|
| **Grow a Garden** | Idle / incrémental | Croissance hors-ligne (« ça a poussé pendant mon absence ») + mutations RNG + économie |
| **Pet Simulator** | Collecteur gacha | Rareté + multiplicateurs + rebirth + trading |
| **Fisch** | Collecteur zen | Boucle apaisante + bestiaire + prises rares (RNG) |
| **Blox Fruits** | RPG anime | Progression longue + fantasme de puissance + collection de fruits |
| **Dead Rails** | Roguelite coop | Sessions rejouables + tension sociale + déblocages |
| **Brookhaven** | Bac à sable social | Liberté + roleplay + contenu gratuit fréquent |
| **Blade Ball** | PvP réflexe | Compétition + rounds courts + rangs + cosmétiques |
| **Steal a Brainrot** | Collecteur social | Personnages meme + vol entre joueurs (tension) + revenu passif |

**La leçon transversale la plus importante :** le mécanisme compte, mais **le thème « meme-able » et screenshotable** fait souvent autant pour la virale que la mécanique. « Grow a Garden » gagne parce que c'est instantanément compréhensible ; « Steal a Brainrot » gagne parce que les personnages sont hilarants et que le vol crée une histoire à raconter.

## 1.2 Les 15 leviers psychologiques, décortiqués

**Progression** — Principe : *goal-gradient effect* (on accélère quand la cible approche). Chaque action doit faire monter *quelque chose*. La règle d'or : **jamais une session sans gain visible.**

**Récompenses** — Principe : *renforcement à ratio variable* (la boîte de Skinner). Le cerveau s'accroche non pas à la récompense, mais à son **imprévisibilité**. Recette gagnante : beaucoup de petites récompenses garanties **+** de rares gros jackpots **+** des *near-miss* (« presque légendaire ! ») qui relancent l'envie.

**Collection** — Principe : *effet Zeigarnik* (une tâche inachevée démange). Un index avec des cases vides crée une tension irrésistible de complétion. C'est le moteur le plus rentable et le plus facile à étendre.

**Rareté** — Principe : *aspiration + statut*. Des paliers lisibles (Commun → Secret) avec des couleurs/lueurs instantanément reconnaissables transforment un objet en trophée social. La rareté n'a de valeur que si elle est **visible par les autres**.

**Hasard (RNG)** — Principe : *anticipation dopaminergique*. Le pic de dopamine arrive **avant** le résultat, pendant l'attente. D'où l'importance des animations d'ouverture, du suspense, du « one more pull ».

**Économie** — Principe : *robinets et éviers* (faucets & sinks). Une monnaie doit entrer facilement et sortir constamment. Le trading joueur-à-joueur crée une **valeur sociale réelle** et un marché vivant qui retient énormément.

**Prestige / Rebirth** — Principe : *nouvelle partie +*. Réinitialiser contre un multiplicateur permanent donne du sens rétroactif à tout le grind précédent et multiplie la durée de vie sans créer de contenu.

**Personnalisation** — Principe : *effet de dotation + expression identitaire*. Ce que le joueur possède et façonne, il ne veut plus le quitter. Excellente source de monétisation non-P2W.

**Coopération** — Principe : *lien social + objectifs partagés*. Jouer ensemble multiplie la rétention car on ne revient pas pour le jeu, on revient pour **les gens**.

**Compétition** — Principe : *comparaison sociale*. Classements et rangs donnent un statut. Attention : la compétition mal dosée frustre — il faut des ligues/segments pour que chacun gagne « à son niveau ».

**Événements** — Principe : *FOMO + fraîcheur*. Le contenu limité dans le temps crée une raison impérieuse de revenir maintenant. C'est le carburant de la rétention à long terme.

**Récompenses quotidiennes** — Principe : *aversion à la perte + formation d'habitude*. Une série (streak) qu'on ne veut pas casser est plus puissante qu'une grosse récompense unique.

**Objectifs courts et longs** — Principe : *objectifs imbriqués*. Le court terme (30 s) donne la dopamine immédiate ; le long terme (semaines) donne la rétention. Il en faut toujours des deux, empilés.

**Sentiment de puissance** — Principe : *fantasme de croissance rendue tangible*. Écraser en un clic ce qui était un défi il y a une heure procure une satisfaction viscérale. La puissance doit se **voir et s'entendre** (effets, sons, chiffres qui explosent).

**Surprises** — Principe : *delight inattendu*. Un secret caché, une mutation jamais vue, un événement surprise : ça génère du bouche-à-oreille (« regarde ce que j'ai eu ! »), le meilleur marketing gratuit qui existe.

## 1.3 Synthèse : l'ADN d'un hit solo-dev

Le point idéal pour **un développeur solo assisté par IA** :

- **Un collecteur idle** avec rareté, RNG, revenu passif et un index. C'est le genre le plus viral ET le plus faisable, parce qu'il est **piloté par les données** : ajouter du contenu = ajouter des lignes de config, pas coder de nouveaux systèmes.
- **Un hub social partagé** léger (visiter, montrer, échanger) pour la rétention sociale, sans netcode de combat complexe.
- **Un thème charismatique et extensible** à l'infini.

C'est la colonne vertébrale du concept gagnant. Passons aux idées.

---

# PARTIE 2 — 10 concepts 100 % originaux

Chaque concept respecte : compréhension < 30 s, boucle addictive, progression permanente, objectif toujours visible, faible temps mort, jouable 5 min ou 5 h, extensible, faisable en solo + IA.

> **Barème « Potentiel »** : /100, combinant viralité estimée, faisabilité solo, facilité de mise à jour et rétention.

---

### Concept 1 — **Wispbound** *(collecteur idle de créatures lumineuses)*
- **Résumé** : Tu peuples ton sanctuaire flottant de petites créatures d'énergie (« Wisps ») qui rôdent, brillent et te génèrent de l'Éclat pendant que tu joues — et même hors-ligne.
- **Pourquoi viral** : les Wisps sont mignons, ultra-screenshotables, et leur monnaie de statut s'appelle « **Aura** » (le slang que les ados adorent) → memes intégrés. Vol/visite social + rareté flashy.
- **Boucle** : invoquer (RNG) → la créature rôde et produit → dépenser pour invoquer/améliorer → compléter le Codex → débloquer un biome → **Ascension** (prestige) → recommencer plus fort.
- **Progression** : niveau du sanctuaire, liens avec chaque Wisp, complétion du Codex, biomes, Ascension (Aura), multiplicateurs de chance.
- **Social** : hub partagé où l'on visite les sanctuaires, trading sécurisé, événements coop, classements de collection, « Nuées » (guildes).
- **Monétisation** : cosmétiques (auras, thèmes de sanctuaire), auto-collecte, slots, potions de chance, passe saisonnier — **jamais de puissance exclusive**.
- **Difficulté dev** : moyenne-faible (data-driven).
- **Temps 1re version** : 4–6 semaines pour une vertical slice jouable.
- **Potentiel** : **93/100**.

---

### Concept 2 — **Static** *(chasseur d'anomalies inter-dimensionnelles)*
- **Résumé** : Tu gères une tour-antenne qui capte des « signaux » de mondes parallèles ; tu règles des fréquences pour matérialiser des anomalies rares à cataloguer.
- **Pourquoi viral** : esthétique unique (grésillement, VHS, glitch) qui tranche dans le paysage Roblox coloré ; le mystère fait parler.
- **Boucle** : régler la fréquence (RNG) → capturer une anomalie → la stocker (elle génère des « ondes ») → améliorer la tour → cataloguer → percer des mystères.
- **Progression** : puissance d'antenne, bande de fréquences débloquées, index d'anomalies, paliers de « corruption ».
- **Social** : co-signal coop (capturer ensemble une méga-anomalie), classements, partage de coordonnées de fréquences rares.
- **Monétisation** : cosmétiques de tour, boosts de signal, filtres visuels premium, passe.
- **Difficulté dev** : moyenne (le rendu « glitch » demande du soin).
- **Temps 1re version** : 6–8 semaines.
- **Potentiel** : **82/100** (thème plus abstrait = compréhension un peu plus lente).

---

### Concept 3 — **Pocket Realm** *(royaume miniature vivant)*
- **Résumé** : Un minuscule royaume grandit sous tes yeux sur une « table » flottante ; tu assignes des citoyens-lilliputiens, gères des événements et il continue de croître hors-ligne.
- **Pourquoi viral** : le facteur « adorable » et le diorama miniature sont extrêmement partageables ; visiter le royaume des autres est irrésistible.
- **Boucle** : placer un bâtiment → assigner citoyens → produire → événement RNG → agrandir → prestige « nouvelle ère ».
- **Progression** : niveau du royaume, technologies, population, ères (prestige), décor.
- **Social** : visites, dons entre royaumes, guerres amicales cosmétiques, classements de prospérité.
- **Monétisation** : parcelles, thèmes architecturaux, citoyens cosmétiques, passe.
- **Difficulté dev** : moyenne-élevée (gestion + IA de citoyens).
- **Temps 1re version** : 8–10 semaines.
- **Potentiel** : **85/100**.

---

### Concept 4 — **Deep Prism** *(plongée dans un abysse de lumière)*
- **Résumé** : Tu descends dans un abysse infini pour récolter des éclats vivants de plus en plus rares — plus tu plonges profond, plus c'est précieux et risqué.
- **Pourquoi viral** : la tension « jusqu'où oses-tu descendre ? » crée des histoires ; palette néon sur fond noir très esthétique.
- **Boucle** : plonger → récolter des éclats (rareté selon profondeur) → remonter avant la pression → vendre/collectionner → améliorer le submersible → plonger plus profond.
- **Progression** : profondeur max, coque/oxygène/lumière, bestiaire, prestige « effondrement ».
- **Social** : plongées coop, classement de profondeur, trading d'éclats.
- **Monétisation** : submersibles cosmétiques, boosts d'oxygène, sondes auto, passe.
- **Difficulté dev** : moyenne (génération verticale, gestion de risque).
- **Temps 1re version** : 6–8 semaines.
- **Potentiel** : **84/100** (proche de Fisch dans l'esprit — attention à bien différencier).

---

### Concept 5 — **Bloom Beasts** *(élevage génétique de créatures-plantes)*
- **Résumé** : Tu fais pousser des créatures mi-plante mi-animal à partir de graines et tu les croises pour obtenir des rarétés génétiques inédites.
- **Pourquoi viral** : le croisement génétique = surprises infinies (« regarde le monstre que j'ai fait ! ») + collection.
- **Boucle** : planter → faire éclore → croiser deux créatures (RNG génétique) → obtenir une variante → collectionner → prestige « saison ».
- **Progression** : serre, arbre génétique débloqué, Codex de traits, prestige.
- **Social** : partage de spécimens, trading génétique, concours de rareté.
- **Monétisation** : serres, engrais de chance, motifs cosmétiques, passe.
- **Difficulté dev** : moyenne (le système de traits combinables demande de la rigueur).
- **Temps 1re version** : 7–9 semaines.
- **Potentiel** : **86/100**.

---

### Concept 6 — **Orbit** *(bâtisseur de systèmes solaires)*
- **Résumé** : Tu lâches des planètes qui orbitent, entrent en collision et fusionnent (mécanique de merge en orbite) pour créer des corps célestes rares et récolter de la matière cosmique.
- **Pourquoi viral** : le merge est hypnotique et satisfaisant ; les fusions spectaculaires sont très partageables.
- **Boucle** : lâcher un corps → il orbite et fusionne → récolter de la matière → acheter de meilleurs corps → débloquer galaxies → prestige « big bang ».
- **Progression** : niveau de galaxie, index de corps célestes, matière, prestige.
- **Social** : galaxies visitables, classement de masse, dons de matière.
- **Monétisation** : skins de planètes, gravité auto, boosts, passe.
- **Difficulté dev** : moyenne (physique orbitale simplifiée).
- **Temps 1re version** : 6–8 semaines.
- **Potentiel** : **83/100**.

---

### Concept 7 — **Dream Diver** *(roguelite oniriques)*
- **Résumé** : Tu entres dans des rêves générés procéduralement pour récolter des fragments oniriques lors de courtes runs, en débloquant des pouvoirs permanents.
- **Pourquoi viral** : sessions courtes rejouables + esthétique surréaliste + coop de rêve.
- **Boucle** : entrer dans un rêve → run courte (récolter/éviter) → sortir avec du butin → dépenser en méta-progression → rêve plus profond.
- **Progression** : méta-upgrades permanents, index de rêves, personnages, difficulté.
- **Social** : rêves coop, classements de run, partage de « graines » de rêve.
- **Monétisation** : personnages cosmétiques, thèmes de rêve, boosts, passe.
- **Difficulté dev** : élevée (génération procédurale + gameplay actif = plus de netcode).
- **Temps 1re version** : 10–12 semaines.
- **Potentiel** : **80/100** (excellent mais plus lourd pour un solo).

---

### Concept 8 — **Deep Delve** *(minage vers le centre du monde)*
- **Résumé** : Tu creuses toujours plus profond pour extraire minerais, fossiles et reliques rares, en améliorant ta foreuse et en exposant tes trouvailles dans ta base.
- **Pourquoi viral** : boucle « creuser » ultra-satisfaisante et lisible ; le musée personnel donne envie de tout collectionner.
- **Boucle** : creuser → trouver (RNG de veines) → remonter et vendre/exposer → améliorer foreuse → couche plus profonde → prestige « effondrement de la mine ».
- **Progression** : profondeur, foreuse/sac/lampe, musée/Codex, prestige.
- **Social** : musées visitables, trading de reliques, classement de profondeur.
- **Monétisation** : foreuses cosmétiques, aimants auto, boosts, passe.
- **Difficulté dev** : **faible** (très data-driven, idéal solo).
- **Temps 1re version** : 4–6 semaines.
- **Potentiel** : **88/100**.

---

### Concept 9 — **Idol Keepers** *(panthéon à collectionner)*
- **Résumé** : Tu entretiens un sanctuaire où tes offrandes génèrent de la Faveur, que tu dépenses pour invoquer des divinités, chacune accordant un pouvoir et un multiplicateur.
- **Pourquoi viral** : le panthéon mythologique offre un Codex épique et un fantasme de puissance ; les invocations sont spectaculaires.
- **Boucle** : offrande → Faveur → invoquer un dieu (RNG) → il buff ton sanctuaire → compléter le panthéon → prestige « Ascension divine ».
- **Progression** : niveau de sanctuaire, panthéon, bénédictions, prestige.
- **Social** : sanctuaires visitables, trading de dieux, classements de dévotion.
- **Monétisation** : autels cosmétiques, encens de chance, skins de dieux, passe.
- **Difficulté dev** : faible-moyenne (data-driven).
- **Temps 1re version** : 5–7 semaines.
- **Potentiel** : **87/100**.

---

### Concept 10 — **Sugar Rush** *(fabrique de confiseries magiques)*
- **Résumé** : Tu diriges une usine à bonbons où tu découvres de nouvelles confiseries en combinant des ingrédients au hasard, tandis que tes machines produisent en continu.
- **Pourquoi viral** : univers gourmand irrésistible, très coloré et « cosy » ; les bonbons légendaires font rêver.
- **Boucle** : combiner ingrédients (RNG) → découvrir une recette → produire en idle → vendre → agrandir l'usine → prestige « nouvelle marque ».
- **Progression** : niveau d'usine, livre de recettes (Codex), machines, prestige.
- **Social** : boutiques visitables, trading de recettes rares, classements de vente.
- **Monétisation** : décors de boutique, machines cosmétiques, boosts, passe.
- **Difficulté dev** : faible-moyenne.
- **Temps 1re version** : 5–7 semaines.
- **Potentiel** : **84/100**.

---

## Tableau de décision

| # | Concept | Viralité | Faisabilité solo | Mise à jour | Rétention | **Total** |
|---|---|:-:|:-:|:-:|:-:|:-:|
| 1 | **Wispbound** | 9.5 | 9 | 10 | 9 | **93** |
| 8 | Deep Delve | 8.5 | 9.5 | 9 | 8.5 | 88 |
| 9 | Idol Keepers | 8.5 | 8.5 | 9.5 | 8.5 | 87 |
| 5 | Bloom Beasts | 8.5 | 8 | 9 | 8.5 | 86 |
| 3 | Pocket Realm | 8.5 | 7 | 8.5 | 9 | 85 |
| 4 | Deep Prism | 8 | 8 | 8.5 | 8 | 84 |
| 10 | Sugar Rush | 8 | 8 | 8.5 | 8 | 84 |
| 6 | Orbit | 8 | 8 | 8 | 8 | 83 |
| 2 | Static | 8.5 | 7 | 8 | 8 | 82 |
| 7 | Dream Diver | 8.5 | 6 | 7.5 | 8.5 | 80 |

**Concept retenu : #1 — Wispbound.**
Il maximise les quatre axes à la fois : thème viral et meme-able (« farmer de l'aura »), collecteur idle data-driven (mises à jour = fichiers de config), hub social léger sans netcode lourd, et une rétention triple (idle hors-ligne + Codex + événements). C'est le meilleur ratio *ambition virale / faisabilité solo*.

---

# PARTIE 3 — Amélioration du concept gagnant jusqu'au niveau « Top 100 »

Le concept brut est bon. Voici les ajouts qui le font passer de « joli jeu idle » à **candidat Top 100**.

**Améliorations clés apportées :**

1. **Le crochet culturel « Aura ».** La monnaie de prestige s'appelle *Aura* et sert de score de statut public affiché au-dessus de la tête (« Aura : 4 200 »). C'est un mot que la cible utilise déjà tous les jours → memes et TikToks gratuits. Le nom du jeu et sa boucle deviennent un running gag (« je farme mon aura »).

2. **Le hub partagé « vivant ».** Au lieu d'un menu, on invoque et on regarde ses Wisps rôder dans un vrai sanctuaire flottant que les autres visitent en temps réel. On *voit* la richesse et la rareté des autres → moteur d'aspiration permanent (le levier « rareté = statut visible »).

3. **Les Mutations comme couche de RNG secondaire.** Chaque Wisp peut apparaître avec une mutation (Chromatique, Givré, Prismatique, Corrompu, Doré…) qui multiplie son revenu ET son aura, avec des effets visuels distincts. Cela démultiplie la collection sans créer de nouvelles créatures → contenu quasi-gratuit + jackpots RNG.

4. **La « Tempête d'Aura » (événement systémique récurrent).** Toutes les ~30 min, une tempête traverse le serveur : pendant 3 min, les taux de mutation explosent. Tout le monde invoque en même temps → pic d'activité social, cris dans le chat, screenshots. C'est le « moment fort » récurrent qui crée du temps fort communautaire.

5. **Le vol social *consenti et non-punitif*.** Inspiration de la tension sociale des hits récents, mais **sans frustration** : on ne peut « emprunter l'aura » d'un joueur que via un mini-défi opt-in, et la victime **ne perd jamais** ses Wisps ni son Éclat — seulement un petit bonus temporaire est transféré, et elle est notifiée pour riposter. On garde le sel social, on retire le poison.

6. **Le Codex à triple complétion.** Compléter une espèce, puis toutes ses mutations, puis sa version « Céleste » donne trois vagues de récompenses → l'effet Zeigarnik est exploité trois fois par créature.

7. **L'Ascension généreuse.** Le prestige ne « détruit » pas la collection : les Wisps ascendés rejoignent une **Galerie éternelle** permanente (on garde le trophée), et on gagne de l'Aura + des bonus permanents. Prestige = fierté, jamais deuil.

8. **Boucle courte de 30 s garantie.** Toutes les 20–40 s, il y a *soit* un Wisp à collecter, *soit* un palier de Codex, *soit* une quête, *soit* une invocation abordable. Zéro temps mort.

Avec ces huit ajouts, Wispbound coche les 15 leviers psychologiques, reste 100 % jouable gratuitement, n'a aucune mécanique punitive, et se met à jour avec de simples fichiers de configuration.

---

# PARTIE 4 — GAME DESIGN DOCUMENT COMPLET : **WISPBOUND**

> *Titre de travail. Slogan : « Collectionne la lumière. Farme ton aura. »*

## 4.0 Vision & pitch

**Wispbound** est un collecteur idle social où tu peuples un sanctuaire flottant de créatures d'énergie (les **Wisps**). Elles rôdent, brillent, se multiplient en rareté et te génèrent des ressources en continu — même hors-ligne. Tu invoques, tu collectionnes, tu complètes ton Codex, tu décores, tu visites les autres, et tu ascends pour recommencer, toujours plus puissant.

**Test des 30 secondes** : *« Tu invoques une petite créature lumineuse. Elle se balade et te donne de l'argent. Tu réinvoques pour en avoir de plus rares. Tu remplis ton album. Voilà, tu as compris. »*

**Piliers de design :**
- **Satisfaction immédiate** (première invocation < 15 s après le spawn).
- **Progression permanente** (rien ne se perd, tout s'accumule).
- **Respect du joueur** (aucun P2W, aucune frustration, aucun timer bloquant).
- **Extensibilité totale** (tout le contenu est data-driven).

## 4.1 Boucle de gameplay (détaillée)

**Micro-boucle (20–40 s) :**
`Collecter l'Éclat au sol → Invoquer un Wisp (RNG) → Réaction (rareté/mutation) → Placer/regarder → répéter`

**Boucle de session (5–30 min) :**
`Compléter des quêtes du jour → progresser dans le Codex → améliorer le sanctuaire → participer à une Tempête d'Aura → visiter un ami / trader`

**Méta-boucle (jours/semaines) :**
`Débloquer un nouveau biome → compléter des lignées du Codex → atteindre un seuil d'Ascension → Ascender (Aura + bonus permanents) → viser le palier suivant → événement mensuel`

## 4.2 Les Wisps (le cœur du contenu)

Chaque Wisp est défini par un fichier de configuration (voir §5.3). Attributs :

- **Espèce** (nom, modèle, biome d'origine, cri/son).
- **Rareté** : Commun · Rare · Épique · Légendaire · Mythique · **Céleste** (secret).
- **Revenu de base** (Éclat/seconde) et **valeur d'Aura**.
- **Mutations possibles** (couche RNG secondaire).
- **Comportement de balade** (flotte, sautille, tournoie…) — purement cosmétique.

**Table de rareté (taux d'invocation de base) :**

| Rareté | Taux | Couleur/lueur | Rôle |
|---|---|---|---|
| Commun | 60 % | Blanc | Volume, sensation de gain constant |
| Rare | 25 % | Bleu | Premier « oh » |
| Épique | 10 % | Violet | Objectif de session |
| Légendaire | 4 % | Or | Jackpot, screenshot |
| Mythique | 0,9 % | Rouge/prisme | Trophée de fierté |
| Céleste (secret) | 0,1 % | Arc-en-ciel animé | Statut ultime, viral |

**Mutations (multiplicateurs cumulables, RNG indépendant) :**

| Mutation | Chance | Effet | Visuel |
|---|---|---|---|
| Chromatique | 1/20 | ×2 revenu & aura | teinte cyclique |
| Givré | 1/40 | ×3 | particules de glace |
| Enflammé | 1/40 | ×3 | flammes |
| Doré | 1/100 | ×5 | reflets or |
| Prismatique | 1/500 | ×10 | arc-en-ciel |
| Corrompu | 1/1000 | ×15 + effet de faille | glitch violet |

Un même Wisp peut être « Légendaire Prismatique » → chaque espèce a des dizaines de variantes collectionnables : **contenu quasi-infini sans nouveaux assets.**

## 4.3 Les monnaies

| Monnaie | Type | Source | Usage | Note anti-P2W |
|---|---|---|---|---|
| **Éclat** | Douce | Wisps (actif + hors-ligne), quêtes | Invocations, améliorations, décor | Cœur de la boucle, 100 % gratuite |
| **Aura** | Prestige/statut | Ascension | Bonus permanents, Wisps exclusifs, statut public | Uniquement via le jeu, jamais achetable |
| **Gemmes** | Premium | Robux **ou** gagnées lentement (quêtes, streak, événements) | Cosmétiques, potions de chance, slots, confort | Tout est aussi atteignable gratuitement |
| **Jetons d'Événement** | Limitée | Événements en cours | Boutique d'événement (cosmétiques + Wisps limités) | Se gagnent en jouant à l'événement |

**Règle d'or de l'économie** : les Gemmes n'achètent **jamais** de puissance exclusive ni ne débloquent de contenu inaccessible autrement. Elles achètent du **temps** (confort) et du **style** (cosmétiques). La chance premium (potions) reste plafonnée et la chance gratuite existe aussi.

## 4.4 Systèmes de progression (empilés)

1. **Niveau de Sanctuaire** — augmente le nombre de Wisps actifs, le revenu passif, débloque des fonctions.
2. **Lien de Wisp** — chaque Wisp gagne des niveaux de lien en restant chez toi ; augmente son revenu et débloque des poses cosmétiques.
3. **Codex (triple complétion)** — Espèce → toutes ses mutations → version Céleste. Chaque palier donne Éclat + Gemmes + bonus permanent.
4. **Biomes** — Prairie de Brume → Forêt Luminescente → Cité Céleste → Abysse → Faille (etc.). Chaque biome = un set d'espèces + une esthétique + de nouvelles quêtes.
5. **Ascension (prestige)** — au-delà d'un seuil de valeur de collection, ascends : la collection courante rejoint la **Galerie éternelle** (permanente), tu gagnes de l'Aura, un multiplicateur global permanent, et l'accès à des Wisps « Ascendants » exclusifs.
6. **Chance (Luck)** — améliorable via Codex, Aura, événements et (optionnellement) potions ; augmente les taux de rareté/mutation.

**Toujours un objectif visible** : l'UI affiche en permanence le prochain palier de Codex, la prochaine quête, le prochain seuil d'Ascension et le temps avant la prochaine Tempête d'Aura.

## 4.5 Systèmes de hasard & « moments forts »

- **Invocation** — animation de suspense (l'œuf/orbe de lumière pulse, la couleur se révèle) ; near-miss volontaire (« presque Mythique ! ») pour relancer.
- **Tempête d'Aura** — événement serveur toutes les ~30 min, 3 min de taux de mutation ×5. Alerte globale, ciel qui change, musique qui monte. **Le moment communautaire récurrent.**
- **Faille rare** — 1 fois/heure environ, une faille apparaît dans un biome et propose une invocation garantie Épique+ pour un coût. Surprise + décision.

## 4.6 Mécaniques sociales

- **Hub partagé** : les sanctuaires sont visitables en temps réel ; on voit les Wisps et l'Aura des autres (aspiration + statut).
- **Trading sécurisé** : échange Wisp contre Wisp, double confirmation, fenêtre anti-arnaque, cooldown, historique. Jamais de trade de monnaie premium.
- **« Emprunt d'Aura » (vol non-punitif)** : mini-défi opt-in ; le gagnant reçoit un **bonus temporaire d'aura** ; **personne ne perd de collection** ; la cible est notifiée et peut riposter. Tension sociale, zéro frustration.
- **Nuées (guildes)** : objectifs coop hebdomadaires, chat, bonus de nuée, classement de nuées.
- **Classements** : Aura totale, complétion de Codex, Wisp le plus rare. Segmentés par ligue pour que chacun gagne à son échelle.

## 4.7 Personnalisation

Thèmes de sanctuaire (îles, ciels, ambiances), socles et décors, **auras cosmétiques** appliquées à un Wisp, plaques de nom, **titres** (« Chasseur de Célestes »), effets d'invocation, animations de balade. Tout est cosmétique et n'affecte jamais la puissance.

## 4.8 Systèmes quotidiens & rétention

- **Série de connexion (streak)** : récompenses croissantes (Éclat → Gemmes → potion de chance → Wisp exclusif au jour 7/14/30). Casser la série ne pénalise pas au-delà de la remise à zéro (aversion à la perte, sans punition réelle).
- **Quêtes quotidiennes** (3) : « invoque 20 fois », « collecte X Éclat », « obtiens une mutation ». Rapides, garanties, dopamine sûre.
- **Boutique quotidienne** : rotation de cosmétiques et d'un Wisp acheté en Éclat (jamais premium-only).
- **Défi hebdomadaire** : objectif long récompensé par un cosmétique exclusif.

## 4.9 Objectifs courts & longs

| Horizon | Exemples | Récompense |
|---|---|---|
| 30 s | collecter, invoquer | Éclat, dopamine |
| 5 min | quête du jour, palier Codex | Gemmes, bonus |
| 1 session | débloquer un biome, ligne de Codex | multiplicateur |
| Semaine | défi hebdo, montée de nuée | cosmétique exclusif |
| Long terme | Ascensions, Codex 100 %, Célestes | statut, titres, Galerie |

## 4.10 Interfaces (toutes les UI)

1. **HUD principal** : Éclat, Gemmes, Aura, bouton Invoquer, prochain objectif, timer Tempête, mini-carte du sanctuaire.
2. **Écran d'Invocation** : bouton d'invocation (x1 / x10), animation, historique récent, taux affichés (transparence).
3. **Codex** : grille par biome, cases vides/remplies, filtres (rareté, mutation), barre de complétion, récompenses de palier.
4. **Sanctuaire** : vue de placement, déplacement des Wisps, infos au survol (revenu, lien, mutation).
5. **Inventaire de Wisps** : liste, tri, favoris, verrouillage (anti-vente accidentelle), fusion de doublons en Éclat.
6. **Boutique** : onglets Cosmétiques / Confort / Gemmes / Passe / Événement. Prix clairs, aucun « dark pattern ».
7. **Ascension** : jauge vers le seuil, aperçu du gain d'Aura et des bonus, Galerie éternelle, Wisps ascendants.
8. **Quêtes** : quotidiennes, hebdo, chaînes de biome, suivi de progression.
9. **Social / Hub** : liste d'amis, visite, trading, Nuées, classements.
10. **Passe Saisonnier** : piste gratuite + premium, paliers, temps restant.
11. **Événement** : hub d'événement, jetons, boutique limitée, compte à rebours.
12. **Paramètres** : audio, graphismes (perf mobile), confidentialité, options d'accessibilité, désactivation d'effets (confort).

## 4.11 Monétisation (respectueuse, non-P2W)

**Gamepasses (achats uniques) :**
- Auto-Collecte de l'Éclat au sol · Slots de sanctuaire supplémentaires · Voyage rapide entre biomes · VIP (tag de chat, zone de hub cosmétique, gemmes quotidiennes) · Chance+ (améliore les taux, mais la chance gratuite existe et rien n'est verrouillé) · ×2 Éclat (confort idle — le jeu étant essentiellement PvE, cela n'entrave personne).

**Passe Saisonnier :** piste **gratuite généreuse** + piste premium (cosmétiques, Wisps cosmétiquement exclusifs, gemmes). Se complète en jouant normalement.

**Consommables :** Potions de Chance (durée limitée), Boosts d'Éclat, Rerolls de mutation. Plafonnés, jamais obligatoires.

**Cosmétiques :** auras, thèmes, titres, effets d'invocation, plaques de nom.

**Gemmes :** packs Robux, mais aussi gagnées gratuitement (streak, quêtes, événements, classements).

**Garde-fous éthiques :** taux affichés en clair ; pas de lootbox trompeuse (l'invocation utilise l'Éclat gratuit) ; pas de timer bloquant ; pas de puissance exclusive payante ; trading protégé ; classements de complétion basés sur le temps/la chance, pas sur la dépense.

## 4.12 Roadmap de contenu — 1 an (12 mois)

> Cadence : **1 événement thématique majeur/mois** + 1 mise à jour d'équilibrage/quality-of-life toutes les 2 semaines. Chaque événement ajoute un mini-biome limité, 4–8 Wisps limités, une monnaie d'événement, une boutique et des cosmétiques.

| Mois | Mise à jour majeure | Contenu |
|---|---|---|
| **M1 — Lancement** | *Prairie de Brume* | Boucle complète, 30 Wisps, Codex, Ascension, hub, trading, passe S1 |
| **M2** | *Forêt Luminescente* | Nouveau biome, +20 Wisps, Nuées (guildes) |
| **M3** | Événement *Floraison* | Wisps floraux limités, tempête spéciale |
| **M4** | *Cité Céleste* | Biome vertical, +25 Wisps, classements de ligue |
| **M5** | Événement *Éclipse* | Wisps « Ombre », mutation événementielle |
| **M6 — Anniversaire mi-parcours** | *Abysse* | Biome sous-marin, +25 Wisps, refonte Codex 2.0 |
| **M7** | Événement *Été / Marée* | plage cosmétique, mini-jeu de pêche à Wisps |
| **M8** | *La Faille* | biome « corrompu », Wisps Corrompus, difficulté opt-in |
| **M9** | Événement *Récolte* | thème automne, Wisps citrouilles |
| **M10** | *Panthéon* (Wisps mythiques) | méga-Célestes, chaîne de quêtes épique |
| **M11** | Événement *Givre / Fêtes* | biome hivernal, Wisps de glace, cadeaux quotidiens |
| **M12 — Anniversaire an 1** | *Cosmos* | méga-biome, Ascension 2.0 (prestige de prestige), rétrospective |

Chaque événement recycle le **framework d'événement** (§5.4) : coder une fois, remplir des configs ensuite.

## 4.13 Principes anti-frustration (charte)

- Jamais de perte nette de progression (Ascension = gain, pas deuil).
- Jamais de timer qui **bloque** le jeu (les timers ne font qu'accélérer).
- Le vol social ne retire jamais de collection.
- Taux RNG transparents et pitié douce (near-miss, seuils de garantie sur certaines invocations).
- Pas de dark pattern d'achat ; annulation facile ; confirmations claires.
- Accessibilité : réduction d'effets, options daltonisme, perf mobile prioritaire.


---

# PARTIE 5 — Plan de développement (solo + IA), étape par étape

## 5.1 Stack technique (Roblox / Luau)

- **Moteur** : Roblox Studio, langage **Luau**.
- **Architecture** : single-place, **data-driven** (chaque Wisp = un `ModuleScript` de config). C'est LA clé de l'extensibilité solo.
- **Sauvegarde** : `ProfileService` (ou DataStore2) pour des données robustes anti-perte + session locking.
- **Communication client/serveur** : RemoteEvents/RemoteFunctions avec **validation serveur systématique** (l'invocation, l'économie et le trading se calculent côté serveur — anti-triche).
- **Performance mobile** : `StreamingEnabled`, LOD sur les Wisps, pool d'objets, limite du nombre de particules. **80 % des joueurs Roblox sont sur mobile** → mobile-first non négociable.
- **Économie de requêtes** : batching des sauvegardes, throttling des Remotes.

## 5.2 Où l'IA t'assiste concrètement

- Génération de **boilerplate Luau** (services, ProfileService setup, systèmes de quêtes, UI Roact/Fusion).
- **Schémas de données** et générateurs de config de Wisps.
- **Équilibrage** : tableurs de courbes de coût/revenu, simulations de progression.
- **Assets 3D/2D** via outils génératifs (concepts de Wisps, icônes, thèmes) → puis nettoyage manuel.
- **SFX/musique** via banques et outils IA.
- **Textes** : noms de Wisps, descriptions de Codex, quêtes, dialogues d'événement.
- **QA** : génération de cas de test, revue de logique anti-exploit.

## 5.3 Modèle de données d'un Wisp (exemple de config)

```lua
-- ModuleScript : Wisps/PrairieDeBrume/Lumibulle.lua
return {
  id = "lumibulle",
  nom = "Lumibulle",
  biome = "prairie_de_brume",
  rarete = "Commun",          -- Commun..Celeste
  revenuBase = 2,             -- Éclat / seconde
  auraBase = 1,
  mutationsAutorisees = {"Chromatique","Givre","Enflamme","Dore","Prismatique","Corrompu"},
  comportement = "flotte",    -- purement cosmétique
  modele = "rbxassetid://...",
  son = "rbxassetid://...",
}
```

> **Ajouter du contenu = ajouter un fichier.** Aucun nouveau système à coder pour un nouveau Wisp, une nouvelle mutation ou un nouvel événement.

## 5.4 Découpage en phases (feuille de route de production)

| Phase | Objectif | Livrable | Durée solo+IA |
|---|---|---|---|
| **P0 — Pré-prod** | Direction artistique, schéma de données, courbes d'éco | doc + prototypes gris | 1 sem |
| **P1 — Vertical slice** | Boucle cœur jouable | invoquer → Wisp rôde → génère Éclat → sauvegarde | 1,5–2 sem |
| **P2 — Économie & Codex** | Rareté, mutations, Codex, améliorations, 1er biome (30 Wisps) | progression complète solo | 1,5 sem |
| **P3 — Social & hub** | Hub partagé, visites, trading sécurisé, classements | multijoueur | 1,5 sem |
| **P4 — Prestige & profondeur** | Ascension, Galerie, Chance, quêtes/streak | rétention long terme | 1 sem |
| **P5 — Monétisation** | Gamepasses, passe S1, boutique, Gemmes | modèle éco vivant | 1 sem |
| **P6 — Framework d'événement** | Tempête d'Aura + moteur d'événement réutilisable | live-ops prêt | 1 sem |
| **P7 — Polish & juice** | Sons, particules, near-miss, optimisation mobile, onboarding | **build de soft-launch** | 1,5–2 sem |

**Total jusqu'au soft-launch : ~10–12 semaines** en solo assisté par IA (dont ~4–6 semaines pour une première *vertical slice* démontrable à P1–P2).

## 5.5 Stratégie de lancement (live-ops)

1. **Soft-launch discret** : petit trafic, mesurer rétention J1/J7, temps de session, taux de conversion, points de friction.
2. **Itération rapide** : corriger l'onboarding (les 60 premières secondes décident de tout) et les pics d'abandon.
3. **Boucle virale** : encourager le partage (screenshots de Wisps Célestes, statut d'Aura, invitations récompensées côté invitant **et** invité).
4. **Cadence live** : événement mensuel + QoL bihebdomadaire (§4.12). La régularité est ce qui construit le Top 100.
5. **Écoute communautaire** : Discord, sondages, correctifs d'équilibrage transparents — la confiance de la communauté est un actif.

## 5.6 KPIs à surveiller

- **Rétention J1 / J7 / J30** (le J1 doit viser > 30 % ; les hits dépassent 40 %).
- Durée de session moyenne, sessions/jour.
- Taux de complétion de l'onboarding (< 90 s).
- Taux de conversion payant (viser 2–5 %) **sans** dégrader l'expérience gratuite.
- Sentiment communautaire (ratio de likes, avis).

## 5.7 Risques & parades

| Risque | Parade |
|---|---|
| Onboarding trop lent | Première invocation garantie satisfaisante en < 15 s ; tutoriel invisible (guidé par les objectifs) |
| Économie qui s'effondre (inflation) | Sinks constants (Ascension, décor, rerolls) ; validation serveur ; monitoring |
| Triche/exploits | Toute logique sensible côté serveur ; anti-dupe sur trading |
| Contenu qui s'épuise | Cadence data-driven + mutations = contenu quasi-infini |
| Accusation de P2W | Charte §4.11 stricte ; communication transparente sur les taux |
| Perf mobile | Mobile-first dès P1 ; budget de particules ; LOD |

---

## Conclusion

**Wispbound** réunit tout ce qui fait un hit Roblox durable : compréhension immédiate, dopamine constante sans frustration, progression permanente, objectif toujours visible, dimension sociale légère mais forte, contenu extensible à l'infini via des fichiers de config — le tout réalisable par une personne seule assistée par une IA en ~10–12 semaines jusqu'au soft-launch.

Son atout viral décisif : il transforme un mot que la cible utilise déjà (« aura ») en système de jeu et en running gag communautaire, tout en restant **profondément respectueux du joueur** — gratuit-complet, sans pay-to-win, sans mécanique punitive.

*Prochaine étape recommandée : construire la vertical slice de la Partie 5 (P1–P2) pour valider la sensation de la boucle cœur avant d'investir dans le social et la monétisation.*
# Concept_Roblox_Wispbound
