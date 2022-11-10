# Smarte Krankmeldung


## Konfiguration - Home Assistant
Füge deiner `configuration.yaml` folgende Zeilen hinzu um auch mit der Apple Watch auf die Actionable Notification reagieren zu können. 
```YAML 
ios:
  push:
    categories:
      - name: "Gesundheit" 
        identifier: 'illness_notification' 
        actions: 
          - identifier: 'illness.yes'
            title: 'Ja'
            icon: "sfsymbols:bed.double"
          - identifier: 'illness.no'
            title: 'Nein, Danke'
            icon: "sfsymbols:bag"
```
Starte anschließend dein HA neu, damit HA die Änderungen übernehmen kann.


## Konfiguration - Node-RED

Impotiere `smartekrankmeldung.json` in dein Node-RED um den Flow nutzen zu können.

