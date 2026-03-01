<div align="center">

# UNIVERSIDAD ESPÍRITU SANTO  
**Ciencias de la Computación**  
**Ingeniería de Software I**

<br>

## GRUPO 5  
Christian Leonardo Suarez Rios  
Jose Moises Arias Zavala  

<br>

# DISEÑO DE ARQUITECTURA DE SOFTWARE  
## TicketService  
### Versión 1.1.0  

<br>

Febrero, 2026  
Guayaquil, Ecuador  

</div>

---

# 🕘 Historial de Versionamiento

| Fecha | Versión | Descripción | Responsable |
|--------|----------|-------------|-------------|
| 19/01/26 | 1.0.0 | Creación del documento TicketService | Equipo de Desarrollo |
| 28/02/26 | 1.1.0 | Documento completo con trazabilidad y formato IEEE | Equipo de desarrollo |

---

# 📑 Contenido

1. Historial de Versionamiento  
2. Listado de tablas  
3. Listado de gráficos  
4. Introducción  
5. Mapeo del Hardware y Software  
   - 5.1 Diagrama de Infraestructura  
   - 5.2 Diagrama de Arquitectura (Macro)  
   - 5.3 Diagrama de Componentes (Micro)  
   - 5.4 Diagrama de Entidad-Relación  
6. Control de Acceso y Seguridad  
7. Referencias  

---

# Listado de tablas

![Arquitectura](imagenes/Tabla_de_stakeholders.png)

---

## Listado de gráficos


![Arquitectura](imagenes/Infraestructura.png)
![Arquitectura](imagenes/Diagrama_Arquitectura.jpg)
![Arquitectura](imagenes/Componentes.png)
![Arquitectura](imagenes/Entidad_Relacion.jpg)

---



# INTRODUCCIÓN

TicketService es un sistema web diseñado para la creación, gestión y seguimiento de tickets de soporte técnico y órdenes de trabajo dentro de organizaciones educativas y pequeñas empresas.

El sistema permite centralizar las solicitudes de soporte, asignarlas a técnicos responsables, establecer prioridades, controlar tiempos de atención (SLA) y generar reportes de desempeño.

Desde el punto de vista arquitectónico, TicketService está diseñado bajo una arquitectura cliente-servidor en tres capas, garantizando:

- Separación de responsabilidades  
- Escalabilidad  
- Mantenibilidad  
- Seguridad en el manejo de datos  
El objetivo principal del diseño arquitectónico es asegurar que el sistema pueda crecer, ser desplegado tanto en entornos locales como en la nube y soportar múltiples usuarios concurrentes.
---

# Mapeo de Hardware y Software

## Componentes de Hardware

Cliente
- Computadora de escritorio o laptop  
- Navegador web moderno 
- Conexión a Internet o red local

Servidor
- Procesador mínimo 2 núcleos  
- 8GB RAM recomendados 
- Almacenamiento SSD
- ASistema operativo Linux o Windows Server

Base de Datos
- 	Puede estar en el mismo servidor (entorno pequeño)
- 	O servidor dedicado en la nube (AWS, Azure, DigitalOcean)

## Mapeo de Software

Software Cliente
-	Navegador web (Chrome, Edge, Firefox)
-	HTML5
-	CSS3
-	JavaScript

Backend
-	Node.js / Java / Python (según implementación)
-	Framework (Express / Spring Boot / Django)

Base de Datos
-	MySQL o PostgreSQL

Servidor Web
-	Nginx o Apache

Control de Versiones
-	Git (Repositorio en GitHub)

---
El sistema TicketService se implementa bajo un modelo cliente-servidor. 
El cliente utiliza navegadores web modernos en computadoras con conexión a internet o red local.          

El servidor requiere mínimo un procesador de 2 núcleos, 8GB de RAM y almacenamiento SSD, ejecutando Linux o Windows Server. 

El backend puede desarrollarse en Node.js, Java o Python, utilizando frameworks como Express, Spring Boot o Django. 

La base de datos recomendada es MySQL o PostgreSQL, y el servidor web puede utilizar Nginx o Apache.


# Diagrama de Infraestructura

## Descripción del Diagrama

La infraestructura de TicketService se basa en un modelo cliente-servidor.
### Componentes:
1.	Usuarios (Administrador, Técnico, Usuario)
2.	Navegador Web
3.	Servidor Web / Aplicación
4.	Base de Datos
5.	Servidor de Respaldo (opcional)

### Representación textual del Diagrama de Infraestructura
```mermaid
[Usuarios]
     |
     v
[Navegador Web]
     |
     v
[Servidor Web / API Backend]
     |
     v
[Base de Datos]
```
### Descripción Técnica
-	Los usuarios acceden mediante navegador.
-	El navegador envía solicitudes HTTP/HTTPS.
-	El servidor procesa la lógica de negocio.
-	La base de datos almacena la información persistente.
-	El acceso se realiza mediante conexión segura SSL/TLS.

---
La infraestructura se basa en un modelo cliente-servidor. 
Los usuarios acceden al sistema mediante un navegador web que se comunica vía HTTP/HTTPS con el servidor de aplicación. 

El servidor procesa la lógica de negocio y se conecta a la base de datos para almacenamiento persistente.
 
Se recomienda el uso de SSL/TLS para garantizar la seguridad en la transmisión de datos.

---
# Diagrama de Arquitectura
Se adopta una arquitectura en tres capas: presentación, lógica de negocio y datos. 

-	La capa de presentación incluye la interfaz web y formularios.
-	La capa de lógica gestiona tickets, usuarios, roles, SLA y reportes.
-	La capa de datos administra la base de datos relacional. 
-	Esta arquitectura permite escalabilidad, mantenibilidad y separación clara de responsabilidades.
### Tipo de Arquitectura
Arquitectura en 3 Capas (Three-Tier Architecture)
1.	Capa de Presentación
2.	Capa de Lógica de Negocio
3.	Capa de Datos

### Representación del Diagrama de Arquitectura
- Node.js / Java / Python
- Express / Spring Boot / Django

### Base de Datos
- MySQL o PostgreSQL

### Servidor Web
- Nginx o Apache

### Versionamiento
- Git (GitHub)

---

# IV. DIAGRAMA DE INFRAESTRUCTURA

El sistema sigue modelo cliente-servidor.

## Diagrama de Infraestructura

```mermaid
[Usuarios]
     |
     v
[Navegador Web]
     |
     v
[Servidor Web / API Backend]
     |
     v
[Base de Datos]
```



La comunicación se realiza mediante HTTPS con SSL/TLS.

---

## Gráfico 1 – Arquitectura

![Arquitectura](imagenes/Arquitectura.jpg)

---

# V. ARQUITECTURA DEL SISTEMA (MACRO)

## Arquitectura en 3 Capas

### 1. Capa de Presentación
- Interfaz web
- Formularios
- Dashboard

### 2. Capa de Lógica de Negocio
- Gestión de tickets
- Gestión de usuarios
- Control de roles
- SLA
- Reportes

### 3. Capa de Datos
- Base de datos relacional
- Tablas
- Procedimientos

### Justificación

- Separación de responsabilidades
- Escalabilidad
- Mantenibilidad
- Adecuada para aplicaciones web académicas

---

# VI. DIAGRAMA DE COMPONENTES (MICRO)

## Capa de Lógica

- AuthController
- UserService
- TicketService
- AssignmentService
- CommentService
- ReportService
- SecurityModule (RBAC)

## Capa de Datos

- UserRepository
- TicketRepository
- AssignmentRepository
- CommentRepository
- RoleRepository
- CategoriaRepository
- PrioridadRepository
- EstadoRepository

---

## Gráfico 2 – Flujo del Ticket

![Flujo](imagenes/Flujo_de_ticket.jpg)

---

# VII. MODELO ENTIDAD-RELACIÓN

## Entidades

### Usuario
- id_usuario (PK)
- nombre
- correo
- contraseña
- id_rol (FK)

### Rol
- id_rol (PK)
- nombre_rol

### Ticket
- id_ticket (PK)
- titulo
- descripcion
- fecha_creacion
- fecha_cierre
- id_usuario (FK)
- id_prioridad (FK)
- id_categoria (FK)
- id_estado (FK)

### Comentario
- id_comentario (PK)
- descripcion
- fecha
- id_ticket (FK)
- id_usuario (FK)

### Asignación
- id_asignacion (PK)
- id_ticket (FK)
- id_tecnico (FK)
- fecha_asignacion

Relaciones:

- Rol 1 — N Usuario  
- Usuario 1 — N Ticket  
- Ticket 1 — N Comentario  
- Ticket 1 — N Asignación  
- Ticket N — 1 Prioridad  
- Ticket N — 1 Categoría  
- Ticket N — 1 Estado  

El modelo está normalizado y mantiene integridad referencial.

---

# VIII. CONTROL DE ACCESO Y SEGURIDAD

## Modelo RBAC

### Administrador
- Gestión completa del sistema

### Técnico
- Gestiona tickets asignados

### Usuario
- Crea y consulta tickets

---

## Mecanismos de Seguridad

### Autenticación
- Login con correo y contraseña
- Contraseñas cifradas (hash seguro)

### Autorización
- Validación por rol
- Restricción de rutas

### Seguridad de Comunicación
- HTTPS
- SSL/TLS

### Seguridad de Datos
- Claves foráneas
- Validación contra SQL Injection
- Control de sesiones

### Respaldo
- Copias periódicas
- Restauración ante fallos

---

# IX. TABLA DE TRAZABILIDAD DE REQUISITOS

| ID | Requisito | Tipo | Módulo | Entidad |
|----|-----------|------|--------|---------|
| RF-01 | Crear ticket | Funcional | TicketService | Ticket |
| RF-02 | Editar ticket | Funcional | TicketService | Ticket |
| RF-03 | Cerrar ticket | Funcional | TicketService | Ticket |
| RF-04 | Asignar ticket | Funcional | AssignmentService | Asignación |
| RF-05 | Agregar comentario | Funcional | CommentService | Comentario |
| RF-06 | Gestionar usuarios | Funcional | UserService | Usuario |
| RF-07 | Autenticación | Funcional | AuthController | Usuario |
| RF-08 | Generar reportes | Funcional | ReportService | Ticket |
| RNF-01 | Seguridad HTTPS | No Funcional | Infraestructura | Sistema |
| RNF-02 | Control RBAC | No Funcional | SecurityModule | Rol |
| RNF-03 | Integridad referencial | No Funcional | Base de Datos | Todas |
| RNF-04 | Disponibilidad 99% | No Funcional | Infraestructura | Sistema |

---

# X. CONCLUSIONES

El diseño arquitectónico de TicketService garantiza:

- Separación clara de responsabilidades  
- Modelo escalable  
- Seguridad mediante RBAC  
- Integridad de datos  
- Adaptabilidad a entornos académicos y empresariales  

La arquitectura en tres capas facilita el mantenimiento y evolución futura del sistema.

---

# XI. REFERENCIAS

[1] R. Pressman, *Ingeniería de Software*, McGraw-Hill, 2014.  
[2] I. Sommerville, *Software Engineering*, Pearson, 2016.  
[3] IEEE Computer Society, *SWEBOK*, 2014.