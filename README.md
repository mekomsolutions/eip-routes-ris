------

# EIP Routes Radiology Information System

Camel routes used by the OpenMRS EIP Client to integrate OpenMRS with FHIR compatible Radiology Information System

## 1. Run OpenMRS on port 8080 and MySQL on port 3306

Follow instructions here: https://github.com/openmrs/openmrs-distro-referenceapplication/tree/3.x

#### Enable mysql bin log
If using Docker Compose, expose the `port` and override the `command` parameters in **docker-compose.yml**. For example:

```
    ports:
      - 3306:3306
    command: "mysqld --character-set-server=utf8 --collation-server=utf8_general_ci --log-bin --binlog-format=ROW"
    
```

## 2. How to use the routes

Follow the instructions here: https://github.com/mekomsolutions/eip-client

#### Note
Remember to provide an `application.properties` file defining the required runtime properties needed by the routes. Use this [template file](src/test/resources/application.properties). Uncomment the properties prefixed with `##` and set them appropriately.