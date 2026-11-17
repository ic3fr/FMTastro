Club Astro – Ciel de Chemillé

Page web d’aide à l’observation du ciel pour **Chemillé-en-Anjou (Maine-et-Loire, France)**. Elle réunit sur une seule page tout ce qui compte avant une soirée d’observation. Elle fonctionne dans un navigateur, sans installation.

**Page en ligne :** `https://VOTRE-PSEUDO.github.io/club-astro/ciel-chemille.html`
(remplacez `VOTRE-PSEUDO` par votre nom d’utilisateur GitHub)

## Ce que contient la page

| Module | Contenu |
|---|---|
| Observation cette nuit | Indice sur 100, durée de la nuit astronomique, créneau de « nuit noire » (sans Soleil ni Lune) |
| Soleil | Lever, coucher, midi solaire, durée du jour, crépuscules civil, nautique et astronomique |
| Lune | Lever, coucher, phase, éclairement, âge, distance, prochaines phases |
| Météo | Conditions du moment, résumé de la journée, tableau heure par heure de la nuit (nuages bas, moyens, hauts, vent, visibilité) |
| Point de rosée | Écart température / point de rosée et risque de buée ou de givre sur les optiques |
| Rayonnement solaire | Rayonnement heure par heure (W/m²), indice UV, activité géomagnétique (Kp) |
| Planètes | Magnitude, élongation et créneau d’observation de chaque planète |
| Étoiles filantes | Prochaines pluies de météores et gêne due à la Lune |

Un sélecteur de date permet de préparer une autre soirée. Le bouton **Mode rouge** préserve la vision nocturne.

## Mise en ligne avec GitHub Pages

1. Créer un dépôt public (par exemple `club-astro`).
2. Y déposer le fichier `ciel-chemille.html` (« Add file » puis « Upload files »).
3. Dans **Settings → Pages**, choisir « Deploy from a branch », la branche `main` et le dossier `/ (root)`.
4. Attendre une à deux minutes : l’adresse du site s’affiche en haut de la page Pages.

Si vous renommez le fichier `index.html`, il s’ouvrira directement à l’adresse `https://VOTRE-PSEUDO.github.io/club-astro/`.

## Changer de lieu

Au début du script de `ciel-chemille.html`, modifier les constantes :

```js
const LAT=47.2167, LON=-0.7333, TZ="Europe/Paris";
```

Latitude et longitude en degrés décimaux (longitude négative à l’ouest de Greenwich). Penser aussi à mettre à jour le titre et le sous-titre de la page.

## Sources de données

- **Météo, point de rosée, rayonnement :** [Open-Meteo](https://open-meteo.com) (prévisions sur 8 jours).
- **Activité géomagnétique (Kp) :** [NOAA SWPC](https://www.swpc.noaa.gov).
- **Soleil, Lune, planètes, phases :** calculés directement dans la page avec des formules astronomiques simplifiées.

## Précision et limites

- Soleil et Lune : environ 1 à 2 minutes sur les heures de lever et de coucher.
- Planètes : environ 0,5° en position. Les magnitudes sont approximatives (anneaux de Saturne non pris en compte).
- L’indice d’observation est une estimation indicative (nuages, vent, buée, Lune), pas une prévision officielle.
- Les heures sont affichées à l’heure de Paris.
- La météo et le Kp nécessitent une connexion Internet. Sans connexion, les autres modules continuent de fonctionner.
- Une page ouverte comme simple fichier sur un téléphone peut rester vide : certains navigateurs et aperçus de fichiers bloquent les scripts. Passer par l’adresse GitHub Pages règle le problème.