# 15 - CI/CD
CI/CD er forkortelser for "Continious Integration" og "Continious Deployment". I dag skal vi arbejde med begge dele hvilket overordnet vil sige at vi skal flytte vores mocroservice fra vores egen lokale maskine, gennem github, til en webserver der er hosted hos Microsoft Azure. Dette giver os den store fordel at vi kan dele vores microservice med resten af verden.

## Læringsmål
* Hvad er Github Actions
* Kunne forstå og skrive yaml filer til brug af Github Actions
* Oprette og opsætte en Virtuel linux instans hos Azure
* Oprette en konto på Dockerhub og pushe locale images til denne hub 
* Opsætte miljøvariabler til brug i forbindelse med deploymentprocessen
* 

## Forberedelse

## Dagen i dag


## Hjemmearbejde

## Materialer
* [Continuous integration](https://en.wikipedia.org/wiki/Continuous_integration)
* [YAML | In One Video](https://www.youtube.com/watch?v=cdLNKUoMc6c)
* [Understanding GitHub Actions](https://docs.github.com/en/actions/learn-github-actions/understanding-github-actions)
* [Video Lars - github actions](https://www.youtube.com/watch?v=qa5gI_u80zs)

## Øvelser

### Øv 1: Login fra github actions til Dockerhub
Se denne demo [Tip 10: Logging in to Docker Hub from a GitHub Actions workflow](https://www.youtube.com/watch?v=CDWLWjnYSGg).    
Lav din egen service og få den demonstreret login funktionallitet til at virke for dit eget projekt. 
Yaml filen som han bruger i videoen ser sådan ud:

```
name: ci

on:
  push:
    branches: main

jobs:
  login:
    runs-on: ubuntu-latest
    steps:
      -
        name: Login to Docker Hub
        uses: docker/login-action@v3
        with:
          username: ${{ secrets.DOCKERHUB_USERNAME }}
          password: ${{ secrets.DOCKERHUB_TOKEN }}
```

### Øv 2: Hello CI/CD
Følg denne tutorial video [xxx]()

I videoen bruger vi dette [repository](https://github.com/ITAKEA/flask-deploy-test)

I skal have en Dockerhub konto, en github konto og en Azure for Students konto for at kunne gennemføre øvelsen.


[Inspiration ChatGpt](https://chat.openai.com/share/c0d327c7-06a4-4de0-bf10-52e3350ccf10)
