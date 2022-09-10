# Flow-4--NodeRed-MQTT
Este repositorio contiene el Flow 4 realizado en NodeRed del Diplomado de Ineternet de las Cosas.

## Introducción

Este flow consiste en un tablero que presente la información de temperatura y humedad locales. Este flow recibe la información por MQTT con un broker local.

## Material Necesario

Para realizar este flow necesitas lo siguiente

- [Ubuntu 20.04](https://releases.ubuntu.com/20.04/)
- [NodeJS](https://nodejs.org/es/)
    - [NPM](https://www.npmjs.com/)
    - [NodeRed](https://nodered.org/docs/getting-started/local)
    - [Nodos Dashboard](https://flows.nodered.org/node/node-red-dashboard)
- [Mosquitto](https://mosquitto.org/)

## Material de referencia

En los siguientes enlaces puedes encontrar cursos en la plataforma de edu.codigoiot.com que te permitirán realiar las configuraciones necesarias

- [Instalar VirtualBox y Ubuntu 20.4](https://www.youtube.com/watch?v=rYkKjmwuot0)
- [Instalacion de NodeRed en ubuntu 20.4](https://www.arubacloud.com/tutorial/how-to-install-node-red-on-ubuntu-20-04.aspx)
- [Introduccion a NodeRed](https://www.codigoiot.com/curso/introduccion-a-node-red/)
- [Introducción a Mosquitto](https://edu.codigoiot.com/course/view.php?id=851)

## Instrucciones
Hacer un flow que pueda obtener la informacion por mqtt y la grafique.

### Requisitos previos

Para que este flow funcione, debes cumplir con los siguientes requisitos previos
1. Instalación de NodeJS. Se recomienda tener instalado NodeJS en alguna versión LTS. Al momento de creación de este documento, se usó la versión 16.17.0LTS. Esta instalación debe incluir las Build-Tools para hacer uso de NPM
2. Instalación de NodeRed. La instalación se realiza por NPM. Al momento de la creación de este contenido, se usó la versión 3.0.2
3. Instalar los nodos node-red-dashboard. Para ello, dirigete a la opcion "Manage Palet" de NodeRed y en la pestaña Install busca node-red-dashboard. Finalmente haz clic en instalar.
4. Instalación de Broker local Mosquitto MQTT.

### Instrucciones de preparación del entorno

Para ejecutar este flow, es necesario lo siguiente
1. Arrancar NodeRed con el comando `node-red`
2. Importar el flow del repositorio
3. Hacer clic en el boton Deploy

### Instrucciones de operación

- Para observar el resutlado de este flow, abre un navegador y dirígete a localhost:1880/ui
-  Enviar por MQTT un mensaje que contenga un JSON con las variables ID, temp y hum

### Notas

- Este Flow se suscribe al tema codigoIoT/MQTT/flow4
- El mensaje mqtt usado para probar este flow es `mosquitto_pub -h localhost -t codigoIoT/MQTT/flow4 -m '{"ID":"David Sanchez","temp":21,"hum":60}'`
- El segundo mensaje mqtt utilizado para probar este flow es `mosquitto_pub -h localhost -t codigoIoT/MQTT/flow4 -m '{"ID":"David Sanchez","temp":20,"hum":53}'`
- Para que la gráfica historica muestre información, deben enviarse al menos 2 puntos

## Resultados
A continuación se muestran los nodos del flow.
![image](https://user-images.githubusercontent.com/111893490/189499229-79c2cf02-b141-46e6-b1eb-7c1c198dafd5.png)

A continuacion se muestran las grficas resultantes en el tablero (dashboard).
![image](https://user-images.githubusercontent.com/111893490/189499289-4b405f68-afa0-4b40-931e-6c6642300e3c.png)

## Evidencias


## Créditos

Desarrollado por David Sanchez Vazquez
- [GitHub](https://github.com/DavidSv00)
