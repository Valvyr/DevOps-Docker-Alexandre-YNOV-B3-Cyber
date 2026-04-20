2.1 J'ai ouvert Visual studio code pour créer un fichier
nommé "index.html" avec comme titre "Ma première image Docker" Avec mon prénom entre les balises <h1>

2.2 Le contenu du fichier Dockerfile :
FROM nginx:alpine

COPY index.html /usr/share/nginx/html/index.html

EXPOSE 80

2.3 Commande "docker build -t mon-site:v1 ."
2.4 docker run -d --name mon-site --rm -p 9090:80 mon-site:v1
2.5 Commande pour lister toutes les images Docker créées sur la machine: docker images
