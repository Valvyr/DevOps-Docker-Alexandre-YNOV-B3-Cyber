# Exercice 2 - Première image Docker

## 2.1 Création du fichier index.html
J'ai ouvert Visual Studio Code pour créer un fichier nommé `index.html` avec comme titre "Ma première image Docker" avec mon prénom entre les balises `<h1>`.

## 2.2 Contenu du Dockerfile
```dockerfile
FROM nginx:alpine
COPY index.html /usr/share/nginx/html/index.html
EXPOSE 80
```

## 2.3 Construction de l'image
```bash
docker build -t mon-site:v1 .
```

## 2.4 Lancement du conteneur
```bash
docker run -d --name mon-site --rm -p 9090:80 mon-site:v1
```

## 2.5 Lister toutes les images Docker
```bash
docker images
```

## 2.6 Historique de l'image
```bash
docker history mon-site:v1
```
Deux layers ont été ajoutés (changement de port et ajout de index.html) mais en réalité seul le layer `index.html` "pèse".

## 2.7 Explication des étapes
Les étapes "CREATED" il y a 4 jours sont des étapes liées au cache, celles qui datent d'il y a 58 secondes sont des étapes ré-exécutées.

## 2.8 Suppression de l'image
```bash
docker rmi mon-site:v1
```
