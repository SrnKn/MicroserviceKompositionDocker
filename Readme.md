# Docker
Conductor:  
Unter /conductor-master-prototyp/docker ist ein docker-compose File zu finden, über welches alle benötigten Komponenten und Services gestartet werden können.
Der Conductor Server wurde angepasst, sodass die benötigten Tasks und der Prozess automatisch beim starten deployt werden.
Der Prozess selbst wird durch den Timeseries Service automatisch alle 5 Minuten gestartet.  

Eureka: http://localhost:8761/  
Conductor Ui: http://localhost:5000/  
Conductor Swagger Ui: http://localhost:8080/  

Camunda:  
Auch hier ist ein docker-compose File hinterlegt, über welches alle benötigten Komponenten und Services gestartet werden können.  
Die Prozesse werden standardmäßig automatisch deployt und der Prozess durch den Timeseries Service automatisch alle 5 Minuten gestartet.  

Eureka: http://localhost:8761/  
Camunda Cockpit TimeseriesService: http://localhost:7777/  
Camunda Cockpit ECPConnectService: http://localhost:7779/  
User: demo  
Passwort: demo  


Der Startvorgang kann in beiden Fällen einige Minuten in Anspruch nehmen, während dieser Zeit werfen die Microservices ggf. Exceptions, wenn noch nicht alle Komponenten verfügbar sind.

