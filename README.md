# 📡 Eureka Server

Este proyecto es un **Eureka Server** para descubrimiento de servicios dentro de una arquitectura de microservicios basada en Spring Cloud.

## 🚀 Tecnologías

- Java 17+
- Spring Boot 3+
- Spring Cloud Netflix Eureka Server
- Maven

## 🛠️ Cómo ejecutar

### Prerrequisitos

- Java 17 instalado
- Maven instalado

### Ejecutar localmente

1. Clona el repositorio:

```bash
[git clone https://github.com/tu-usuario/eureka-server.git](https://github.com/AndresOnate/eureka-server.git)
cd eureka-server
```

2. Compila el proyecto:

```bash
mvn clean install
```

3. Ejecuta la aplicación:

```bash
mvn spring-boot:run
```

La consola estará disponible en:

```
http://localhost:8761
```

## ⚙️ Configuración (application.yml)

```yaml
server:
  port: 8761

spring:
  application:
    name: eureka-server

eureka:
  client:
    register-with-eureka: false
    fetch-registry: false
```

## 📦 Registrar otros servicios

Para registrar microservicios en este Eureka Server, los clientes deben tener la siguiente configuración:

```yaml
eureka:
  client:
    service-url:
      defaultZone: http://localhost:8761/eureka/
```

Y la anotación:

```java
@EnableEurekaClient
```

## 📸 Vista del panel

Una vez que los servicios se registran, puedes verlos en:

```
http://localhost:8761
```

## 🧑‍💻 Autor

Andrés Camilo Oñate Quimbayo
