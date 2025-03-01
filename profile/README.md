# Space-Station X 🎮👾

Este proyecto consiste en un sistema de ventas de videojuegos desarrollado con una arquitectura de microservicios en **Spring Boot** para el backend y **Angular** para el frontend. El objetivo principal es ofrecer un sistema modular, escalable y sencillo para la administración de videojuegos, clientes, ventas y usuarios.

## Tabla de Contenidos
1. [Descripción General](#descripción-general)
2. [Arquitectura del Sistema](#arquitectura-del-sistema)
3. [Tecnologías Utilizadas](#tecnologías-utilizadas)
4. [Microservicios](#microservicios)
5. [Frontend](#frontend)
6. [Configuración e Instalación](#configuración-e-instalación)

---

## Descripción General
Este proyecto se compone de varios microservicios independientes, cada uno diseñado para manejar un dominio específico del negocio:
- **Usuarios:** Gestión de autenticación y perfiles de usuarios.
- **Clientes:** Administración de clientes registrados en el sistema.
- **Productos (Videojuegos):** Inventario de videojuegos disponibles para la venta.
- **Ventas:** Registro y seguimiento de las transacciones de ventas.

## Arquitectura del Sistema
La solución se basa en una arquitectura de microservicios con las siguientes características:
- **Backend:** Microservicios implementados en Spring Boot.
- **Frontend:** Aplicación Web desarrollada en Angular.
- **Base de Datos:** Cada microservicio tiene su propia base de datos de MYSQL.
- **Comunicación:** Los microservicios se comunican a través de **REST APIs**.
- **Balanceo y Gateway:** Se utiliza un API Gateway (Spring Cloud Gateway) para gestionar las solicitudes entrantes.
- **Seguridad:** Implementación de seguridad con **Spring Security** y JWT.
- **Documentación:** Cada microservicio cuenta con documentación de API generada con **Swagger/OpenAPI**.

## Tecnologías Utilizadas
### Backend:
- **Java** (Spring Boot, Spring Data, Spring Security)
- **MySQL** (bases de datos)
- **Lombok** (reducción de código boilerplate)
- **Resilience4j**
- **Mappers**
- **Web Client**

### Frontend:
- **Angular** 
- **Bootstrap**
- **RxJS** 

### Infraestructura:
- Sprint Cloud 

## Microservicios
1. **Microservice-Users:**
   - Gestión de usuarios.
   - Endpoints: registro, login, CRUD de perfiles.
   - Base de datos: Usuarios.
   - [Swagger](https://yearling-eulalie-hiroshysystems01-2f7d912d.koyeb.app)

2. **Microservice-Client:**
   - Gestión de clientes.
   - Endpoints: CRUD de clientes.
   - Base de datos: Clientes.
   - [Swagger](https://fatal-felicity-lourdes-74626af5.koyeb.app)

3. **Microservice-Product:**
   - Gestión de videojuegos.
   - Endpoints: CRUD de productos, búsqueda por categorías.
   - Base de datos: Videojuegos.
   - [Swagger](https://grand-dora-hiroshyusa-4ec6d307.koyeb.app)

4. **Microservice-Sales:**
   - Gestión de ventas.
   - Endpoints: Registro de ventas, estadísticas.
   - Base de datos: Transacciones.
   - [Swagger](https://technical-loise-hiroshysystems-3d94600c.koyeb.app)
     
5. **Microservice-Security:**
   - Gestión de Autenticaciones.
   - Endpoints: Registro de Login.
   - Base de datos: Transacciones.
   - [Swagger](https://biological-natalee-raydberg25-4c59dc23.koyeb.app)

## Frontend
La aplicación Angular centraliza las funcionalidades de los microservicios, ofreciendo:
- Dashboard para visualizar estadísticas.
- Administración de usuarios, clientes, productos y ventas.
- Interfaz moderna y responsive.

## Configuración e Instalación
### Prerrequisitos
- **Java 17+**
- **Node.js 18+**
- **Angular CLI**
- **Docker**

### Pasos para Backend
1. Clonar los repositorios:
   ```bash
   git clone https://github.com/Space-Station-X/microservice-users.git
   git clone https://github.com/Space-Station-X/microservice-client.git
   git clone https://github.com/Space-Station-X/microservice-product.git
   git clone https://github.com/Space-Station-X/microservice-sales.git
   git clone https://github.com/Space-Station-X/microservice-gateway.git
   git clone https://github.com/Space-Station-X/microservice-security.git
   git clone https://github.com/Space-Station-X/eureka-server.git
   ```   
2. Configurar las bases de datos y variables de entorno.
3. Ejecutar los microservicios con:
```bash
./mvnw spring-boot:run
```
### Pasos para Frontend
1. Clonar el repositorio:
```bash
git clone https://github.com/Space-Station-X/frontend.git
```
2. Instalar dependencias:
```bash
npm install
```
3. Ejecutar la aplicación:
```bash
ng serve
```
