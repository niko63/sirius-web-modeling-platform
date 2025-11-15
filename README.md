# sirius-web-modeling-platform

Welcome to the sirius-web platform modeling.  

## Overview

This tool allows you to make diferent enterprise models such as:  
* Grai Grid: model to represent the decisional aspect of an organisation. This model includes Grai network
* Grai network: a sub-model of a grid that describes precisely a decisional activity.
* Actigram: model to represent  a process according to specific modeling object

## Installation

1. Download and install https://www.docker.com/ 
2. Download the executable of the platform at [sirius-web platform](https://imtminesales-my.sharepoint.com/:u:/g/personal/nicolas_daclin_mines-ales_fr/EVRa3kjf3yBAuPDQO71BALcBMtqAZ3XDymT9C4tfSzXjdA?e=JJIHBZ)

## Run the platform  
  
1. Run docker and create a container using: 
```
docker run -p 5438:5432 --rm --name sirius-web-postgres -e POSTGRES_USER=USERNAME -e POSTGRES_PASSWORD=PASSWORD -e POSTGRES_DB=sirius-web-db -d postgres:15
```
|Note  | You can create container directly in the docker's terminal|
|---|---|

2. Run the platform using:
```
java -jar sirius-web-2025.10.0.jar --spring.datasource.url=jdbc:postgresql://localhost:5438/sirius-web-db --spring.datasource.username=USERNAME --spring.datasource.password=PASSWORD
```
3. Open a web browser and go to: http://localhost:8080/projects

You access the following page and you can start to create projects and models. Enjoy!  

![alt text](https://github.com/niko63/sirius-web-modeling-platform/blob/main/SiriusWebPlatform.png)
