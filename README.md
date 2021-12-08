# dispositif-9-sorties

* Système de diffusion mozaique 9 écrans (9x 720p) 
* à partir d'un flux réseau NDI, sépare un 4k en 9 flux indépendant

## 
* La syncronisation pourrait être plus raffiné et l

## Fonctionnement 

* À partir d'un vidéo 4k (3840x2160), 9 sorties NDI indépendantes, 9 lecteurs indépendant. 
* La source est chargé dans un logiciel de lecture libre (Open Broadcast studio)
* Utilise un système de micro ordinateur (raspberry pi) pour afficher les signal sur de moniteur vidéo
* Utilise le POE pour alimenter les micro ordinateurs ainsi que les écrans 
* L'ensemble du matériel est monté sur des rails dins afin de permettre une reconfiguration aisé 

### Installation 

* [installation](docs/install.md)

### Flux de signaux

![flux de signaux](docs/flux_de_signaux.png)

## image de référence (Calibration) 

### Calibration 9 écrans

![calibration 9 écrans ](calibration/mosaique.png)

### Calibration 1 écran

![calibration 1 signal ](calibration/720p_1280x720.png)

### Format de lecture 

#### H.264 
via ffmpeg 
```
ffmpeg -i input.mov -c:v libx264 -preset slow -pix_fmt yuv420p -crf 22 -c:a copy output.mp4
```

## Assemblage 

### Integration

![integration](docs/integration.drawio.png)

### Branchement 
![branchement](docs/branchements.drawio.png)

### Composantes 

| qte       |  objet                    | ref       |
|---        |---                        |---        |
|  9        | Moniteur vidéo            | 1080p          |
|  9        | Kit Raspberry pi POE DIN  |           |
|  1        | Ordinateur central        | OBS       | 
|  5        | Rails Din                 |           |
|  2        | Commutateurs eternet POE  |           |
|           |                           |           |


## Configuration 

### Raspberry

#### à partir de raspberry pi OS [Debian] [Buster] ou [Bulleyes]

suivre ces instructions : https://dicaffeine.com/raspbian

### Open Broadcast studio

#### OBS NDI

https://github.com/Palakis/obs-ndi



### Documentation visuelle

#### Kit Pi POE

![Kit Pi POE](./docs/pi_kit_poe.jpeg)

#### Flotte de PI POE en cours d'assemblage

![raspberry pi en cours d'assemblage](./docs/raspberrypi_assemblage.jpeg)
