# Exercice 1 - Premier contact avec Docker

## 1.1
```docker pull nginx:alpine
```

### 1.2
```docker run -d --name mon-nginx -p 8080:80 nginx:alpine
```

### 1.3
```docker ps
```

### 1.4
Dans le lien http://localhost:8080 on observe une page d'accueil par défaut du serveur web nginx

### 1.5
Afficher les logs du conteneur "mon-nginx" avec la commande 
```docker logs [ID]
```

### 1.6
```docker ps -a
```

La commande liste même ceux arrêté (avec "STATUS Exited")

### 1.7
```docker rm [ID]
```

### 1.8
```docker run -d --name mon-nginx -p 8080:80 --rm nginx:alpine
```
