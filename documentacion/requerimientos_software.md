
<div align="center">

# UNIVERSIDAD ESPÍRITU SANTO

**Carrera de Ingeniería en Ciencias de la** <br>
**Computación**

<br>

## Poryecto TicketService
## GRUPO 5

Christian Leonardo Suarez Rios<br>
Jose Moises Arias Zavala

<br>

### Especificación de Requerimientos de Software
**Versión 1.0.0**

<br><br>

**07 de febreo, 2026**  
Samborondón, Ecuador
</div>



## 🕘 Historial de Versionamiento

| Fecha    | Versión                    | Descripción                               | Responsable |
|----------|---------------------------------|-------------------------------------------|-------------|
| 07/02/26 | 1.0.0 | requerimientos de software TicketService | Equipo de Desarrollo |

---

## 📘 1. Introducción
El presente documento describe la Especificación de Requerimientos de Software (ERS) del sistema TicketService, 
el cual permitirá la creación, gestión y seguimiento de tickets de soporte técnico de manera centralizada, optimizando 
los procesos de atención y control de solicitudes.

## 👥 Descripción del Grupo

### Grupo 5 – Ingeniería de Software I

 - Christian Leonardo Suarez Rios
 - Jose Moises Arias Zavala

## 🎯 Objetivos

### Objetivo General

Definir de manera clara y estructurada los requerimientos funcionales y no funcionales del sistema 
TicketService, garantizando su correcta implementación y alineación con las necesidades del negocio.

### Objetivos Específicos

 - Identificar los actores que interactúan con el sistema.
 - Especificar los requerimientos funcionales principales.
 - Definir los requerimientos no funcionales que aseguren calidad y rendimiento.
 - Proporcionar una base formal para el desarrollo y validación del sistema.

## 🤝 Stakeholders


| Nombre | Descripción  |
|------|----------------------|
| Administrador | Representa a la organización y gestiona el sistema|
| Usuario | Cliente interno que registra solicitudes|
| Técnico | Personal encargado de atender y cerrar tickets|

### Tabla 1. Listado de los stakeholders

---

## ⚙️ Requerimientos Funcionales

### ID Requerimiento: GP-RF-01
| Nombre | Creación de Tickets  |
|------|----------------------|
| Objetivo | Permitir a los usuarios registrar solicitudes de soporte técnico en el sistema.|
| Fuente | Usuarios del sistema|
| Prioridad | Alta|
| Descripción | El sistema deberá permitir a los usuarios crear tickets ingresando información como categoría, prioridad, descripción del problema y datos de contacto.|
| Precondición | El usuario debe estar autenticado en el sistema.|
| Poscondición | El ticket queda registrado con estado “Abierto”.|
| Stakeholders | Usuario, Administrador|
| Responsable | Equipo de Desarrollo|
---

### ID Requerimiento: GP-RF-02
| Nombre | Gestión y Asignación de Tickets |
|------|--------------------|
| Objetivo | Permitir la asignación y actualización del estado de los tickets.|
| Fuente | Administrador|
| Prioridad | Alta|
| Descripción | El sistema deberá permitir a los administradores asignar tickets a técnicos, cambiar su estado (abierto, en proceso, cerrado) y registrar comentarios de seguimiento.|
| Precondición | Debe existir al menos un ticket creado.|
| Poscondición | El ticket queda asignado y actualizado correctamente.|
| Stakeholders | Administrador, Técnico|
| Responsable | Equipo de Desarrollo|

---
## 🛡️ Requerimientos No Funcionales

### ID Requerimiento: GP-RNF-01
| Nombre | Disponibilidad del Sistema|
|------|------------------|
| Fuente | Organización|
| Prioridad | Media|
| Descripción | El sistema TicketService deberá estar disponible al menos el 99% del tiempo, permitiendo el acceso desde navegadores web modernos y diferentes sistemas operativos.|
| Responsable | Equipo de Desarrollo|

---
