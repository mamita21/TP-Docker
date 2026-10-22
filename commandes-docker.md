\# TP Docker – Getting Started



\## 1. Vérification de Docker

```bash

docker info

```



\## 2. Exécution de Hello World

```bash

docker run hello-world

```



\## 3. Recherche et téléchargement d'Ubuntu

```bash

docker search ubuntu

docker pull ubuntu

docker images

```



\## 4. Création d'un conteneur Ubuntu

```bash

docker run --name ubuntu-java-tp -it ubuntu bash

```



\## 5. Installation de Java

À l'intérieur du conteneur Ubuntu :



```bash

apt-get update

apt-get install -y default-jdk

java -version

exit

```



Version obtenue : OpenJDK 25.0.4.1.



\## 6. Création de l'image Docker

```bash

docker commit ubuntu-java-tp ubuntu-java:1

docker images

```



\## 7. Publication sur Docker Hub

```bash

docker login

docker tag ubuntu-java:1 mamita21/ubuntu-java:1

docker push mamita21/ubuntu-java:1

```



\## 8. Vérification de l'image publiée

```bash

docker pull mamita21/ubuntu-java:1

docker run -it mamita21/ubuntu-java:1 bash

java -version

```



Lien Docker Hub : https://hub.docker.com/r/mamita21/ubuntu-java



\## Conclusion



Ce TP m'a permis de découvrir les principales commandes Docker, de créer un conteneur Ubuntu, d'y installer Java, de créer une image avec `docker commit` et de publier cette image sur Docker Hub.

