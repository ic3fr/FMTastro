# Club Astro

Site d’astronomie pour le club, centré sur **Chemillé-en-Anjou (Maine-et-Loire, France)**. Ouvrez `index.html` : c’est le menu qui mène à toutes les pages. Aucune installation n’est nécessaire.

**Site en ligne :** `https://ic3fr.github.io/
(remplacez `VOTRE-PSEUDO` par votre nom d’utilisateur GitHub)

## Les pages

| Fichier | Contenu |
|---|---|
| `index.html` | Menu du site |
| `ciel-chemille.html` | Soleil, Lune, météo heure par heure, point de rosée, rayonnement solaire, planètes observables, nuit noire, indice d’observation, étoiles filantes |
| `phases-lune-chemille.html` | Heure exacte de la prochaine pleine Lune, compte à rebours, phases des 14 prochains jours |
| `phases-lune.html` | Phases de la Lune en simulation (temps accéléré, passé et futur, hémisphère nord ou sud) |
| `systeme-solaire.html` | Position des planètes en temps réel |
| `jour-nuit.html` | Globe avec jour, nuit, saisons et heure solaire |
| `mission-mars.html` | Simulation d’un voyage Terre-Mars et de la mise en orbite |
| `voie-lactee.html` | Place du système solaire dans la galaxie |
| `echelle-univers.html` | Zoom de la longueur de Planck à l’univers observable |
| `moon.jpg` | Photo de la Lune utilisée dans les pages de phases |

Toutes les pages doivent rester **dans le même dossier** : elles se renvoient les unes aux autres, et les pages de la Lune chargent `moon.jpg`. Si la photo est absente, elles affichent une Lune stylisée à la place.

## Mise en ligne avec GitHub Pages

1. Créer un dépôt public (par exemple `club-astro`).
2. Y déposer tous les fichiers de ce dossier (« Add file » puis « Upload files »).
3. Dans **Settings → Pages**, choisir « Deploy from a branch », la branche `main` et le dossier `/ (root)`.
4. Attendre une à deux minutes : l’adresse du site s’affiche en haut de la page Pages. Comme le menu s’appelle `index.html`, il s’ouvre directement à cette adresse.

## Changer de lieu

Au début du script de `ciel-chemille.html` et de `phases-lune-chemille.html`, modifier les constantes :

```js
const LAT=47.2167, LON=-0.7333, TZ="Europe/Paris";
```

Latitude et longitude en degrés décimaux (longitude négative à l’ouest de Greenwich). Penser aussi à mettre à jour les titres des pages.

## Sources de données

- **Météo, point de rosée, rayonnement :** [Open-Meteo](https://open-meteo.com) (prévisions sur 8 jours).
- **Activité géomagnétique (Kp) :** [NOAA SWPC](https://www.swpc.noaa.gov).
- **Positions du Soleil, de la Lune et des planètes, phases :** calculées directement dans les pages avec des formules astronomiques.

## Précision et limites

- Pleine et nouvelle Lune : environ une minute. Quartiers : environ 30 minutes.
- Lever et coucher du Soleil et de la Lune : environ 1 à 2 minutes. Planètes : environ 0,5° en position, magnitudes approximatives.
- L’indice d’observation est une estimation indicative, pas une prévision officielle.
- Heures affichées à l’heure de Paris.
- Seule la météo (et l’indice Kp) demande une connexion Internet.
- Ouvertes comme simples fichiers sur un téléphone, les pages peuvent rester vides : certains navigateurs et aperçus de fichiers bloquent les scripts. Passer par l’adresse GitHub Pages règle le problème.
