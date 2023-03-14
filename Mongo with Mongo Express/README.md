# Docker Compose With Mongo Express

## Explications à propos de cette image docker-compose mongodb mongo-express :

- [**version**](https://docs.docker.com/compose/compose-file/) : '3.8' -> Détermine la version du fichier compose, plus d’infos sur .

- [**services**](https://docs.docker.com/engine/swarm/how-swarm-mode-works/services/) : On définit 2 services *"mongodb"* et *"mongo-express"*

- **container_name** : est utilisé pour définir le nom d’un container. Dans notre exemple, ce sera *"mongodb"* et *"mongo-express"*

- [**depends_on**](https://docs.docker.com/compose/compose-file/#depends_on) : Permet d'attendre que le service *"mongodb"* soit démaré avant de créer le service *"mongo-express"*. 

- **restart** : *"always"* Permet au container d'être automatiquement redémarré quand le service Docker sera redémarré ou quand le container lui-même est redémarré.

- **ports** : Utilisé pour définir le mapping de port *[HOST_PORT] : [CONTAINER_PORT]* entre la machine hôte et le container.

- [**environment**](https://docs.docker.com/compose/environment-variables/set-environment-variables/) : Permet de définir des variables d’environnement pour un container donné.


- [**volumes**](https://docs.docker.com/storage/volumes/) : Utilisé pour monter un dossier de la machine hôte sur le container.
Par exemple, pour le service mongodb, on monte le volume data-volume dans le dossier /data du container afin de stocker la base de données et persister les données lorsque le container est éteint.