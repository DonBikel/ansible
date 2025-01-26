# Mini-Projet Ansible: Déploiement d'une Application

Ce projet consiste en deux étapes pour déployer une application à l'aide d'Ansible : une première étape de déploiement classique et une seconde étape de déploiement en conteneur utilisant Docker, avec le support d'un proxy Nginx en tant que rôle Ansible.

## Prérequis

- **Ansible** installé sur votre machine
- **Docker** installé pour la seconde partie du projet
- Accès à un environnement cible (serveur ou machine virtuelle) où l'application sera déployée

## Partie 1 : Déploiement de l'Application avec un Playbook Simple

### Étapes à suivre

1. **Naviguer dans le répertoire `app-init` du dépôt.** :
   - cd ./app-init

2. Utiliser le playbook pour déployer l'application du client :
   - ansible-playbook -i hosts.yml --ask-vault-pass nginx_playbook.yaml
   - tapez le mot de passe d'accès à la clé crypté (vagrant)
     Vous devriez abtenir un resultat similaire à celui-ci :
     ![image](https://github.com/user-attachments/assets/a183982b-9b72-431c-9553-3939b51ccd36)

3. Vérifier que l'application est disponible :
   - Utilisez un navigateur web ou une commande curl pour vérifier que l'application est accessible à l'adresse spécifiée.

## Partie 2 : Déploiement de l'Application en Conteneur avec Docker et Nginx en utilisant les rôles ansible

### Étapes à suivre

1. Naviguer dans le répertoire app-template du dépôt :
  - cd ./app-template

2. Utiliser le playbook pour déployer l'application :
  - ansible-playbook -i hosts.yml --ask-vault-pass nginx_webapp_playbook.yaml 
    Vous devriez abtenir un resultat similaire à celui-ci :
    ![image](https://github.com/user-attachments/assets/69b2852d-c55a-4bc5-9cb1-028512e2dc44)

3. Vérifier que l'application est disponible :
   - Utilisez un navigateur web ou une commande curl pour vérifier que l'application est accessible à l'adresse spécifiée.
  
