---
theme: the-unnamed
class: text-center
highlighter: shiki
lineNumbers: false
info: false
drawings:
  persist: false
transition: slide-left
css: unocss
title: Eco-Index - Le nutriscore du développement
fonts:
  sans: Lato
  serif: Roboto Slab
  mono: Fira Code
themeConfig:
  primary: green
layout: cover
---

# Eco-Index

## Le nutriscore du développement

<div class="absolute bottom-5 right-10" style="color: white">
  <span class="font-700">
    BreizhCamp 2023
  </span>
</div>

---
layout: about-me

helloMsg: Hello!
name: Cécilia Bossard
imageSrc: /profile.png
job: Développeuse / apicultrice
line1: 
line2: 
social1: Twitter /@CeciliaBossard/
social2: Masto /@cbossard@piaille.fr/
social3: 
---
<uim-rocket />
---
layout: center
---
# Etat des lieux

**4%** des gaz à effet de serre émis par notre consommation numérique (en 2018)

Accroissement de **9%** par an

---
layout: center
---

# Pollution numérique

La fabrication des terminaux a plus d'impact environnemental que leur utilisation

![Local Image](/fabrication.png)

---
layout: center
---

# « Alors on ne peut rien y faire nous ! »

---
layout: center
---

# Et pourtant ...

"Ça rame ! Je vais encore devoir changer mon téléphone !"


---
layout: section
---

# Ce serait chouette d'avoir un outil permettant de mesurer l'impact environnemental de nos applis


<!--
On aimerait bien pouvoir juger du score environnemental de notre application.

Pouvoir suivre sa valeur, un peu comme un nutriscore
-->
---
layout: center
---

# Eco-Index !

---
---
# Qu'est ce que c'est ?

- outil créé par le collectif GreenIT
- open source
- résultats sous licence CC-By-NC-ND

---
---
# Utilisable en ligne

[https://www.ecoindex.fr/](https://www.ecoindex.fr/)


---
---
# Eco-index

![Local Image](/eco-index1.png)

---
---
# Eco-index

![Local Image](/eco-index2.png)

---
---
# Eco-index

![Local Image](/eco-index3.png)


---
layout: section
---
# Qu'est ce que ça veut dire ces résultats ?

---
---
# La performance environnementale

- score sur 100
- représenté par une lettre (de A à G)
- plus le score est élevé, meilleure est la performance environnementale

![Local Image](/eco-index3Bis.png)

---
---
# L'empreinte environnementale

Calcul des émissions de gaz à effet de serre et consommation d'eau générés par l'affichage de la page

![Local Image](/eco-index4.png)


---
---
# L'empreinte environnementale

<img src="/quantiteCo2.png" class="mx-40 h-90" />

via https://impactco2.fr/

---
layout: section
---
# Comment c'est calculé ?

---
---
# Utilisation de 3 critères

- complexité de la page 
- poids des données transférées
- nombre de requêtes HTTP

---
---
![Local Image](/eco-index5.png)


---
---
# Calcul

Moyenne pondérée : 
- 3 pour le DOM
- 2 pour les requêtes HTTP
- 1 pour le poids des données transférées

Formule de calcul : $x = 100 - \frac{(3QtilDOM + 2QtilHttp + QtilKo)}{6}$

---
layout: section
---
# Utilisation au quotidien

Comment l'utiliser au cours des développements ?

---
layout: default
---
# Plugin dans le navigateur (Firefox ou Chrome)


<p class="mx-80">
  <img src="/greenITAnalysis.png" class="h-40" />
  GreenIT-Analysis
</p>
---
layout: default
---
# Plugin dans le navigateur (Firefox ou Chrome)

## Démo !

---
---
# GreenIT-Analysis

![Local Image](/plugin1.png)

---
---
# GreenIT-Analysis

![Local Image](/plugin2.png)

---
---
# GreenIT-Analysis

![Local Image](/plugin3.png)

---
layout: default
---
# Ligne de commande

https://github.com/cnumr/ecoindex_cli


---
layout: default
---
# Ligne de commande

## Démo !

---
---
# Ligne de commande

## Récupération de l'image docker

```bash
alias ecoindex-cli="docker run -it --rm -v /tmp/ecoindex-cli:/tmp/ecoindex-cli vvatelot/ecoindex-cli:latest ecoindex-cli"
```

---
---
# Ligne de commande

## Analyse

```bash
ecoindex-cli analyze --url https://www.breizhcamp.org
```

---
---
# Ligne de commande

## Analyse avec rapport HTML

```bash
ecoindex-cli analyze --url https://www.breizhcamp.org --html-report
```

---
layout: center
---

# A vous de jouer ! 

[https://www.ecoindex.fr](https://www.ecoindex.fr)


