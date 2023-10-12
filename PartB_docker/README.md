# Container Registry + Web App
---

## Para crear la imagen
```
docker build -t edvai_proyecto_final:1.0 .
```

**-t:** tags

## Para crear el container
```
docker run -p 80:80 -e ID_USER=Nicolas123 edvai_proyecto_final:1.0
```

**-p:** publish

**-e:** env -> Variable de entorno 

## Para taggear la versión de la imagen
```
docker tag edvai_proyecto_final:1.0 <NOMBRE DEL CONTAINER REGISTRY>.azurecr.io/edvai_proyecto_final:1.0

docker tag edvai_proyecto_final:1.0 proyectoFinalEdvai.azurecr.io/edvai_proyecto_final:1.0
```


## Para registrarse en Azure
```
docker login <NOMBRE DEL CONTAINER REGISTRY>.azurecr.io

docker login proyectoFinalEdvai.azurecr.io
```

## Luego de registrarse, pushear la imagen
```
docker push proyectoFinalEdvai.azurecr.io/edvai_proyecto_final:1.0


