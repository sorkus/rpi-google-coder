# rpi-google-coder

Dit repository is een kloon van het orginele hypriot/rpi-google-coder Dockerfile. Dit project is gemaakt om eenvoudig het Google Coder project in een Docker container te draaien op de Raspberry Pi. Op een Raspberry Pi 2B kan je op deze manier met gemak meerdere Google Coder omgevingen draaien, waardoor je bijvoorbeeld in een klas of workshop in theorie maar 1 Raspberry Pi nodig hebt waarop individuele Coder omgevingen draaien. Daarnaast heb je wel een webbrowser nodig op een PC of tablet, waarmee je naar de Coder omgeving kan verbinden. De Coder omgevingen zelf zijn beveiligd met een wachtwoord nadat je de eerste keer verbinding hebt gemaakt.

## Docker image

[Google Coder](http://googlecreativelab.github.io/coder/) is een geweldig project dat voorziet in een simpele programmeer omgeving voor HTML, CSS en JavaScript in je web-browser. Het is opoit opgezet als educatief project voor de Raspberry Pi, ook om de GPIO poorten beschikbaar te stellen. Als je meerdere Coder omgevingen op 1 Pi draait, werkt dit niet meer zoals dit was opgezet. Voor projectenm met GPIO is nog steeds een individuele Pi per project nodig.


## Build the image
```
docker build -t hypriot/rpi-google-coder github.com/sorkus/rpi-google-coder
```

## Run Google Coder
```
docker run -d -p 8080:8080 -p 8081:8081 hypriot/rpi-google-coder
```

You can access Google Coder on your Raspberry Pi via a web browser: ```https://"%IP_of_your_Raspberry_Pi%":8080/```,
for example: ```https://192.168.2.108:8080/```
Do not forget to use ```https```!
