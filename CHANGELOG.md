# Journal des versions

## 1.0.0 — 2026-10-24

Première version.

* Lecture TDMS (segments, entrelacé, gros-boutiste, index réutilisés, DAQmx brut avec échelles, horodatages, fichiers tronqués), MDF 4.0–4.2 (triés et non triés, DT/DL/HL/DZ, conversions, invalidation, champs de bits) et CSV (formats français et anglo-saxons, dates, unités).
* Courbes sur 8 fenêtres synchronisées, décimation min/max sans perte de pics, curseurs C1/C2, heure d'horloge, superposition d'essais.
* Mesures sur la vue ou entre curseurs, copie vers Excel, export CSV, export PNG.
* Pro : voies calculées rejouées sur tous les fichiers, seuils avec hystérésis et durée minimale, spectre FFT, rapport d'essai PDF, lot avec page de synthèse, modèles de rapport.
* Sessions enregistrables et réapplicables à l'essai suivant, thèmes clair et sombre, aucune connexion réseau.

Avant publication, une revue critique indépendante a conduit à corriger et compléter :

* DAQmx réel (en-têtes 0x1269 / 0x126A, codes de type DAQmx, plusieurs tampons bruts) et échelles NI table, thermocouples (NIST ITS-90), Pt100, thermistances, jauges, somme et différence ;
* écart-type exact malgré un fort décalage (Welford), mesures par agrégats de blocs (instantanées sur 50 millions de points) ;
* zoom borné à la précision des nombres, rapport recalculé seulement quand c'est nécessaire, plages de rapport figées, bloc de visa, logo, PDF sans en-têtes du navigateur ;
* voies calculées : jamais de remplacement d'une voie mesurée, voies d'autres groupes rééchantillonnées ;
* CSV : temps en ms, métadonnées sur deux colonnes, colonnes texte, séparateur de milliers, passage de minuit et d'heure d'hiver ;
* deux fichiers de même nom ouverts côte à côte, recalage à l'heure d'horloge entre fichiers ;
* surcouche de survol, échelles Y par unité, zoom vertical, tracé XY, panneaux redimensionnables, fenêtres en défilement ;
* spectre : moyennage de Welch, retrait de tendance, tableau des pics limité à la bande affichée, sans raies voisines ni bruit de fond ;
* seuils : le choix d'une voie juste après l'ouverture de l'onglet n'est plus écrasé ;
* rapport : axe de droite pour une seconde unité dans une même section de courbes ;
* nombreuses finitions (unités d'axe, arrondis d'export, légende dans le PNG, messages d'erreur mémoire en français).
