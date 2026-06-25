# Boîtier de contrôle — Convoyeur à bande Niryo

> Projet CAO | SolidWorks | Assemblage mécanique

---

## Contexte

Conception d'un boîtier de contrôle permettant de piloter un convoyeur à bande Niryo.  
Le projet consiste à intégrer l'ensemble des composants fournis dans un boîtier compact, ergonomique et adapté à une production en série de 500 à 1 000 exemplaires.

---

## Cahier des charges

| Contrainte | Valeur |
|---|---|
| Dimensions max (sans boutons) | 100 × 75 × 52 mm |
| Usage | Posé sur table (ergonomique) |
| Production | Série de 500 à 1 000 exemplaires |
| Environnement | Aucune contrainte particulière |
| Câblage | Non requis |
| Plan | Au moins un plan d'un élément du boîtier |

---

## Composants intégrés

| Référence | Description |
|---|---|
| 10001063-1 | Vis FHC M3×14 CL8.8 |
| 10001064-1 | Cache potentiomètre SIFAM3-03-TPN110 |
| 10001065-1 | Pied caoutchouc D20 EP3 |
| 10001066-1 | Écrou frein H M3 CL04 |
| 10001068-1 | Bouton arrêt d'urgence D40 HBAN-HBY5-02TS |
| 10001142-1 | Carte Interface Controller Conveyor PCB REV.E1 |
| 10001239-1 | Potentiomètre angulaire BOURNS PDB181-K220K-103B |
| 10001243-1 | Prise DC099 5,5 mm × 2,1 mm |

---

## Choix de conception

### Structure du boîtier

Inspiré d'un modèle existant de boîte d'arrêt d'urgence Niryo, le boîtier se compose d'une **coque principale** et d'un **couvercle** pour faciliter le montage et la maintenance. L'ensemble est assemblé par les vis M3×14 fournies (10001063-1).

> Note d'amélioration identifiée : des chanfreins auraient pu être ajoutés au niveau des trous de vis afin que les têtes ne débordent pas en surface. Un taraudage direct aurait également été envisageable pour une finition plus soignée, mais cela aurait dépassé les exigences du cahier des charges.

### Positionnement des composants

- **Prise d'alimentation DC + carte PCB** : montées sur la paroi latérale de la boîte pour optimiser l'espace intérieur et éviter tout chevauchement avec le bouton d'arrêt d'urgence. La prise DC se fixe par vissage de sa partie intérieure (sans fixation supplémentaire). La carte PCB est fixée par des trous dédiés avec les mêmes vis M3×14.

- **Bouton AU + potentiomètre** : positionnés sur le dessus du boîtier, conformément au schéma d'inspiration. La molette du potentiomètre est contrainte avec son cache, avec une liaison mécanique de rotation entre les deux composants.

- **Pieds caoutchouc** : une empreinte de quelques millimètres a été réalisée sur le bas de la boîte pour maintenir les pieds en position fixe.

> Point à corriger : une ouverture pour le passage de câbles n'a pas été prévue sur l'un des côtés — à intégrer dans une révision.

---

## Arborescence des fichiers

```
boitier-controle-niryo/
├── assemblage/
│   └── assemblage_boitier.SLDASM
├── pieces/
│   ├── coque.SLDPRT
│   ├── couvercle.SLDPRT
│   └── ...
├── exports/
│   ├── coque.step
│   ├── assemblage.step
│   └── renders/
│       ├── vue_iso.png
│       ├── vue_dessus.png
│       └── vue_interieure.png
├── plans/
│   └── plan_coque.PDF
└── README.md
```

---

## Aperçu

| Vue isométrique | Vue intérieure |
|---|---|
| *(renders/vue_iso.png)* | *(renders/vue_interieure.png)* |

---

## Outils utilisés

- **SolidWorks** — modélisation et assemblage
- **Format d'échange** — `.step` pour tous les composants

---

## Statut du projet

- [x] Modélisation de la coque et du couvercle
- [x] Intégration de tous les composants fournis
- [x] Fixation de la carte PCB
- [x] Liaison mécanique potentiomètre / cache
- [x] Empreintes pieds caoutchouc
- [ ] Ouverture passage de câbles *(à ajouter)*
- [ ] Chanfreins sur les trous de vis *(amélioration future)*
