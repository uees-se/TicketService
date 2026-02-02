
<div align="center">

# UNIVERSIDAD ESPÍRITU SANTO

**Ciencias de la Computación**<br>
**Ingeniería de Software I**

<br>

## GRUPO 5

Christian Leonardo Suarez Rios<br>
Jose Moises Arias Zavala

<br>

### Questions & Answers  
### Caso de Estudio  
**Versión 1.0.0**

<br><br>

**19 de enero, 2026**  
Guayaquil, Ecuador

</div>




## Historial de Versionamiento

| Fecha | Versión                    | Descripción         | Responsable |
|------|---------------------------------|---------------|-------------|
| 19/01/26 | 1.0.0 | Creación del documento TicketService | Equipo de Desarrollo |

---

## 1. Introducción

### Propósito
El presente documento describe el sistema TicketService, el cual permitirá la creación, gestión y seguimiento de tickets de soporte técnico de manera centralizada.

### Alcance
- Gestión de usuarios y roles
- Creación, actualización y cierre de tickets
- Clasificación por prioridad y categoría
- Asignación de tickets
- Reportes de atención

---

## 2. Actores del sistema

### 🧑‍💼 Administrador
Responsable de la configuración, control y supervisión general del sistema.

**Acciones:**
- Iniciar sesión
- Administrar usuarios y roles
- Configurar SLA
- Gestionar tickets y órdenes de trabajo
- Generar reportes y métricas

---

### 🧑‍🔧 Técnico
Encargado de resolver las órdenes de trabajo asignadas.

**Acciones:**
- Iniciar sesión
- Ver órdenes asignadas
- Actualizar estado y avances
- Resolver tickets dentro del SLA

---

### 🧑‍💻 Usuario
Cliente interno que solicita soporte mediante tickets.

**Acciones:**
- Iniciar sesión
- Registrar tickets
- Consultar estado
- Ver historial de solicitudes

---

## 3. Funcionalidades del sistema

| Código | Funcionalidad                    | Actor         | Descripción |
|------|---------------------------------|---------------|-------------|
| F1 | Iniciar sesión | Todos | Acceso según rol |
| F2 | Registrar ticket | Usuario | Crear solicitud de servicio |
| F3 | Consultar ticket | Usuario | Ver estado y progreso |
| F4 | Gestionar tickets | Administrador | Clasificar y priorizar |
| F5 | Asignar órdenes | Administrador | Asignar tickets a técnicos |
| F6 | Gestionar órdenes | Técnico | Actualizar avances |
| F7 | Controlar SLA | Administrador | Medir tiempos de atención |
| F8 | Reportes y métricas | Administrador | Apoyo a decisiones |
| F9 | Gestión de usuarios | Administrador | Roles y permisos |

---

## 4. Diagrama de Casos de Uso

```mermaid
graph TD
    Usuario -->|Registrar| Ticket
    Usuario -->|Consultar| Ticket
    Administrador -->|Gestionar| Ticket
    Administrador -->|Asignar| Orden
    Técnico -->|Atender| Orden
    Administrador -->|Generar| Reportes
```

```mermaid
flowchart LR
    A[Usuario crea ticket] --> B[Administrador revisa]
    B --> C[Asigna a técnico]
    C --> D[Técnico atiende]
    D --> E[Técnico resuelve]
    E --> F[Ticket cerrado]
```

## Gráfico 1. Tickets por Estado

![Gráfico 1. Tickets por Estado](imagenes/tickets_estado.png)

**Descripción:**  
Este gráfico muestra la distribución de los tickets según su estado actual
(Abiertos, En Proceso y Cerrados).