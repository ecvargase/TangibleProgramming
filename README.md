# TangibleProgramationOverCarWiFi

![Build Status](https://travis-ci.org/ecvargase/CarWiFi.svg?branch=master)
[![codecov](https://codecov.io/gh/ecvargase/CarWiFi/branch/master/graph/badge.svg)](https://codecov.io/gh/ecvargase/CarWiFi)

##Develop Board: ESP8266
### Documentacion: 
 - http://arduino-esp8266.readthedocs.io/en/latest/
 - https://github.com/esp8266/Arduino/tree/master/doc/esp8266wifi
 
## Sensores
-  Sensor de proximidad
## Actuadores
- Motor x2 (moto reductor)
- Led o bufffer de error en compilacion
- Led del sensor de proximidad

## Red 
 -  Modulo wifi, en hostpot mode
 
## Protocolos de comunicacion
 -  Web server HTTP, API REST port 80 ---> IP 192.168.4.1 normalmente
 
### REST Services contracts:

1. /api/v1/session

         Metodo : POST
         Body:
         {
         name: "",
         device: ""
         }
         Response on success : 200 , json
         { 
         session: "sessionID" 
         }

2. /api/v1//instructionsSet 
Recibe una lista de codigos de instrucciones

          Metodo : POST
          Body:
          {
          sessionID: "",
          intructions: [01,03,10,04]
          }
         Response on success : 200 
