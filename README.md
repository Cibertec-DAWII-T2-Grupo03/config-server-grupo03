# config-server-grupo03

Servidor centralizado de configuración para FintechLoan, Grupo 03.

## Configuración

El servidor escucha en el puerto `8888` y se registra en Eureka en:

```text
http://localhost:8761/eureka/
```

La configuración se obtiene desde repositorios GitHub exclusivos mediante patrones:

- `solicitud-*` → repositorio `config-comercial-grupo03`
- `evaluacion-*` → repositorio `config-riesgos-grupo03`

El repositorio `config-default-grupo03` funciona como repositorio de respaldo.

## Ejecución

Requiere Java 25 y Maven:

```bash
mvn spring-boot:run
```

Para consultar la configuración de un cliente:

```text
http://localhost:8888/solicitud-service/dev
http://localhost:8888/evaluacion-service/dev
```

La autenticación de GitHub se gestiona mediante Git Credential Manager del equipo.
