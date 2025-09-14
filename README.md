# holbertonschool-softy-pinko-docker

## Description
Ce projet met en œuvre une architecture Docker pour une application web composée de trois services principaux :
- **Back-end** : Une API Flask qui fournit des données dynamiques.
- **Front-end** : Un serveur Nginx qui sert du contenu statique.
- **Proxy** : Un serveur Nginx qui agit comme un reverse proxy et un load balancer.

## Structure du projet
- `task5/` : Configuration de base avec un proxy, un front-end et un back-end.
- `task6/` : Extension de l'architecture pour inclure plusieurs instances du back-end avec un équilibrage de charge.

## Fonctionnalités
- **Task 5** : Mise en place d'un reverse proxy pour rediriger les requêtes vers le front-end ou le back-end.
- **Task 6** : Scalabilité horizontale avec plusieurs instances du back-end et un équilibrage de charge (round-robin).

## Prérequis
- Docker
- Docker Compose

## Instructions

### Lancer les services
1. Placez-vous dans le répertoire `task5` ou `task6` :
   ```bash
   cd task5
   ```
2. Construisez et lancez les conteneurs :
   ```bash
   docker-compose up --build
   ```

### Scalabilité (Task 6)
Pour lancer deux instances du back-end :
```bash
docker-compose up --scale back-end=2
```

### Accéder à l'application
- Ouvrez votre navigateur et accédez à [http://localhost](http://localhost).

## Vérification des logs
Pour voir les logs des conteneurs :
```bash
docker-compose logs -f
```

## Auteur
Lucas Boyadjian
