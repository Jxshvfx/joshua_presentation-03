# Instrumentum

## Idée

### Concept
Créer une sorte de concert personnel mais accessible au public. Celle-ci aurait des petites sculptures qui seront projeté par des projecteurs (3d Mapping) ainsi qu'un écran au centre. Ces projecteurs projecteront des visuels, l'écran projectera un visuel différent (peut être changer, différent options) et intéragiront avec l'audio. L'audio provient des instruments différents proposés (Guitare, Piano et Drum). Puis, un controlleur midi sera au centre pour mettre plus d'effets synth et de changer de visuelles, et des indicateurs lumières sur les côtés guideront et démontreront visuellement l'effet mis (s'il y a un effet qui marche, les lumières l'indiqueront).

## Références et inspirations

### Planche d'ambiance visuelles
![plancheVisuelle](assets/images/MoodBoard%20Visuel.png)

#### Pour les sculptures

https://www.temasarte.com/en/Angeles-Anglada-Sculpture-Allegory-to-the-music-aaanglada_alegoriaalamusica.html

### Planche d'ambiance sonores 

Pour l'ambiance générale, je cherche quelque chose qui va de normal (instruments normal) vers des effets synth, etc. Le choix d'un son "synth" ou "synthwave" serait car le son est plutot cinématique et me marque beaucoup.

https://youtu.be/iJjRTL1xcKI?t=212

https://youtu.be/iJjRTL1xcKI?t=138

https://youtu.be/-ZuS0p2qRYo?t=55

## Références artistique
Donc l’esthétique va de quelque chose plus réaliste/organique (sans effets) vers quelque chose de plus « synth ». Le visuel va renforcer cela, lorsqu’on va vers le synth, les visuels vont être plus abstrait. Les grosses références pour le projets sont les concerts. Certains de ces concerts on des visuels attrayant ce qui est une grosse qualité que je veux pour ceci.

https://youtu.be/VB7JBN37nlY?t=66

https://youtu.be/l1ZlwbHuhrU?t=58

https://youtu.be/lrJ2x7oOE5w?si=ycnQVbG8hp6aMAc-

## Scénario Interactif

### Interactif
```mermaid
graph TD;
    A{Utiliser Instruments}-->B{Guitare} & C{Piano} & D{Drum};
    B{Guitare} & C{Piano} & D{Drum}-->E{Interaction avec Projection};
    E{Interaction avec Projection}-->F{Plus D'interaction?};
    F{Besoin D'effets? De Changer le visuel?}--|Oui|-->G{Midi};
    F{Besoin D'effets? De Changer le visuel?}--|Non|-->I{Fin de l'intéraction?};
    G{Midi}-->H{Activation Lumiere};
    H{Activation Lumiere}-->I{Fin de l'intéraction?};
    I{Fin de l'intéraction?}--|Oui|-->J{Veille};
    I{Fin de l'intéraction?}--|Non|-->A{Utiliser Instruments};
    J{Veille}-->A{Utiliser Instruments};
```
### Narratif
```mermaid
graph TD;
    A{Point de départ}--|Choix d'instruments|-->B{Guitare} & C{Piano} & D{Drum};
    B{Guitare} & C{Piano} & D{Drum}-->E{Interaction avec Projection};
    E{Interaction avec Projection}-->F{La personne veut-elle plus?};
    F{La personne veut-elle plus? visuel ou effets}--|Oui|-->G{Utilise le clavier midi};
    F{La personne veut-elle plus? visuel ou effets}--|Non|-->I{la personne est satisfaite};
    G{Utilise le clavier midi}-->H{La personne ajoute des effets/change visuel};
    H{La personne ajoute des effets/change visuel}--> I{la personne est satisfaite} & J{la personne est impressionner} & K{La personne expérimente plus} & L{La personne quitte};
```

## Scénarimage / Simulation

### Simulation
![plancheVisuelle](assets/images/Simulation_02.jpg)

### Scénarimage
![plancheVisuelle](assets/images/scenarimage.jpg)

#### Organique
![plancheVisuelle](assets/images/examples_01_00009.jpg)

#### Organique Modifié (Synth)
![plancheVisuelle](assets/images/examples_02_00009.jpg)

#### Synth Complet
![plancheVisuelle](assets/images/examples_03_00009.jpg)

### Exemple Concret Dans Touch Designer (Merci à Victor)
https://youtu.be/ATLhkFcQZN0

## Synoptique

![plancheVisuelle](assets/images/Synoptique.jpg)

## Plantation
![plancheVisuelle](assets/images/Plantation.jpg)

## Technologies

### Support médiatique
Donc, il aurait quelques mp4 pour les bases des visuels, ensuite les instruments seront la source audio, et en midi il interagiront avec les autres logiciels (Touch Designer, reaper, Max, Qlc ou SoundSwitch) pour permettre une interaction visuelle et audiovisuelle.

### Matériel

#### Électronique
- 3 [Epsum Home Cinema 2150 Wireless 3CLD Projector](https://epson.ca/Remise-%C3%A0-neuf-certifi%C3%A9e/Divertissement-%C3%A0-domicile/Home-Cinema-2150-Wireless-1080p-3LCD-Projector---Remise-%C3%A0-neuf-certifi%C3%A9e/p/V11H852020-N)
  ![plancheVisuelle](assets/images/projecteur_epson.PNG)
  
- 2-6 5PX-HEX (Lumières)
  ![plancheVisuelle](assets/images/5PX-HEX.jpg)
  
- 2 Sculpture Mains
  
  ![plancheVisuelle](assets/images/main_sculptures.jpg)

- [Support pour les sculptures](https://youtu.be/exuQNdkZcog)
  
- Ordinateurs (1 ou 2)
  
- NanoKontrol 2
  ![plancheVisuelle](assets/images/nanokontrol2.jpg)
  
- Fils XLR, HDMI, USB-C, USB-A
- 2-6 Speakers Genelec
  
  ![plancheVisuelle](assets/images/genelec_speakers.jpg)

#### Instruments
- Akai MPK Mini Plus 37-key Keyboard
  ![plancheVisuelle](assets/images/akai_keyboard-37.png)
  
- EART Electric Guitar SSS Single Coil
  ![plancheVisuelle](assets/images/guitar_electrique.jpg)
  
- Donner Electric Drum Set
  ![plancheVisuelle](assets/images/drum_set.jpg)
  


### Logiciels
Différents Logiciels seront utilisé pour que les projections, les instruments et les lumières intéragissents entre elles.

- Touch Designer (Pour la projection et l'intéraction sur les visuels)
- MadMapper (Pour mapper les visuels sur les sculptures)
- After Effects (Pour les visuels de bases de l'écran)
- QLC+ ou SoundSwitch (Pour les lumières et l'intéractivité avec celle-ci)
- Reaper ou Max (Pour la détection d’audio des instruments, et les effets sur celle-ci)
- Blender / Maya (Pour les bases de visuels 3D, objets, etc.)

Le réseau de communication serait majoritairement midi car celle-ci est faite pour la détection d’audio d’instruments musicales.

## Réferences: 

https://village-numerique.mutek.org/fr/installations/isochrone-par-manuel-chantre
