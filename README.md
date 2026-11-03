# Feurcalc — calculateur de dégâts façon Showdex pour Cobblemon

Mod **100 % côté client** pour **Cobblemon 1.8.x** (Fabric, Minecraft 1.21.1) : il marche sur
n'importe quel serveur, même si personne d'autre ne l'a.

Les calculs sont faits par **le calculateur officiel de Pokémon Showdown** (`@smogon/calc`, le même
que l'extension Showdex), qui tourne dans le moteur JavaScript déjà présent dans Cobblemon.
Rien à télécharger en plus, pas besoin d'internet.

## En combat

- Un bouton **Feurcalc [J]** apparaît en haut au centre de l'écran de combat.
- Juste en dessous, un **résumé** : pour chacune de tes attaques, les % de dégâts sur l'adversaire
  en face et les chances de KO (`OHKO`, `2HKO`, `38% 2HKO`...), plus sa meilleure attaque contre toi (▼).
  Clic droit sur le bouton pour masquer / afficher ce résumé.
- **Clic** sur le bouton (ou touche **J**) : ouvre le calculateur complet.

Tout se remplit tout seul : ton Pokémon (vraies stats, IV, EV, nature, talent, objet, attaques),
l'adversaire (espèce, forme, niveau), ses **PV**, ses **boosts** et son **statut**.

## Le calculateur (touche J ou `/feurcalc [pokémon]`)

| Toi (A) — à gauche | Adversaire (B) — à droite |
|---|---|
| Pokémon, niveau, PV | Pokémon, niveau, PV |
| Talent, objet, nature, Téra, statut | Talent, objet, nature, Téra, statut |
| 4 attaques : **% min–max** et **KO** contre B | 4 attaques : **% min–max** et **KO** contre A |
| Base / **IV** / **EV** / stat finale / **boosts −/+** | Base / **IV** / **EV** / stat finale / **boosts −/+** |
| Protection, Mur Lumière, Voile Aurore, Piège de Roc, Picots, Vent Arrière | idem pour son côté |

En haut : **Météo**, **Champ**, **Gravité**, **Coup critique**, et **⇄** pour inverser les côtés.

- **Clic** sur un nom (Pokémon, talent, objet, nature, attaque, type Téra) : fenêtre de choix avec recherche.
- **Clic droit** : précédent / retirer / remettre à zéro.
- **Molette** sur une case IV / EV / Niv. / PV : IV ±1, EV ±4 (Maj : min / max).
- Survole une attaque pour voir le détail complet du calcul (format Showdown).
- La vitesse finale est comparée : ▲ plus rapide, ▼ plus lent.

**Les spreads que tu règles pour un adversaire sont retenus par espèce** (`config/feurcalc_sets.json`) :
la prochaine fois que tu le croises, il est déjà réglé. Clic droit sur le nom du Pokémon pour revenir
aux valeurs par défaut (IV 31, EV 0, nature neutre, 4 dernières attaques apprises par niveau).

## Télécharger le .jar

Dossier **`telechargement/`** du dépôt → clique sur le .jar → bouton **Download raw file**.

## Crédits

Calculs : [@smogon/calc](https://github.com/smogon/damage-calc) (licence MIT), regroupé dans
`src/main/resources/assets/feurcalc/js/feurcalc.js`. Icônes de types et traductions : Cobblemon.
