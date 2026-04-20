2.1 J'ai ouvert Visual studio code pour créer un fichier
nommé "index.html" avec comme titre "Ma première image Docker" Avec mon prénom entre les balises <h1>
2.2 Le contenu du fichier Dockerfile :
FROM nginx:alpine
COPY index.html /usr/share/nginx/html/index.html
EXPOSE 80
2.3 Commande "docker build -t mon-site:v1 ."
2.4 docker run -d --name mon-site --rm -p 9090:80 mon-site:v1
2.5 Commande pour lister toutes les images Docker créées sur la machine: docker images
2.6 docker history mon-site:v1
Deux layers ajouté (changment de port et ajout index.html) mais en réalité seul le layer index.html "pèse"
2.7 Les étapes "CREATED” il y a 4 jours sont des étapes liées au cache, celles qui datent d’il y a 58 secondes sont des étapes ré exécutées
2.8 docker rmi mon-site:v1
