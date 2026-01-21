# 🚗 CarFix - Sistema de Gestión Integral para Talleres

**CarFix** es una solución de escritorio robusta desarrollada en **.NET (C#)** diseñada para la gestión administrativa y operativa de talleres mecánicos. El sistema centraliza la administración de clientes, vehículos, órdenes de reparación, inventario y seguridad, implementando una arquitectura escalable y buenas prácticas de ingeniería de software.

## 🚀 Características Principales

### 🛠 Gestión Operativa
* **Tickets de Reparación:** Creación, asignación y seguimiento de tickets de servicio con estados dinámicos.
* **Historial de Cambios:** Tracking automático de modificaciones en las descripciones de los tickets.
* **Gestión de Flota:** Administración completa de clientes y sus vehículos asociados.

### 📦 Compras e Inventario
* **Gestión de Stock:** Control de productos, stock mínimo y alertas.
* **Proveedores y Órdenes de Compra:** Flujo completo desde la solicitud a proveedores hasta la recepción de mercadería.

### 🔐 Seguridad y Auditoría (RBAC)
* **Control de Acceso Basado en Roles:** Sistema flexible de Usuarios, Grupos y Permisos.
* **Auditoría Completa:** Registro inmutable de acciones críticas (Logins, Eliminaciones, Modificaciones de Tickets y Compras) indicando *quién*, *cuándo* y *qué* cambió.
* **Seguridad:** Encriptación de contraseñas y validaciones de sesión.

### 📊 Reportes
* Dashboard de productividad de técnicos.
* Reportes de movimientos de compras y auditoría de seguridad.

---

## 🏗 Arquitectura y Tecnologías

El proyecto fue construido siguiendo una **Arquitectura en Capas (N-Tier)** para asegurar la separación de responsabilidades y la mantenibilidad.

* **Lenguaje:** C# (.NET)
* **Interfaz (UI):** Windows Forms
* **ORM:** Entity Framework Core (Code First)
* **Base de Datos:** SQL Server
* **Validaciones:** Lógica de negocio encapsulada y validaciones de entrada.

### 🧩 Patrones de Diseño Implementados
El código demuestra el uso de patrones avanzados para resolver problemas comunes:
* **Singleton:** Implementado en las Controladoras (ej. `ControladoraTickets`) para garantizar una única instancia de gestión.
* **Factory Method:** Utilizado en la capa de Vista (`FormularioFactory`) para la creación dinámica de formularios.
* **Observer:** Implementado para notificaciones de eventos (ej. `NotificadorOrdenesCompra`).
* **Repository / Unit of Work:** Abstracción implícita a través del uso de EF Core.

---

## 💻 Instalación y Configuración

### Prerrequisitos
* Visual Studio 2022 (o superior)
* .NET SDK (versión correspondiente)
* SQL Server (LocalDB o instancia completa)

### Pasos
1.  **Clonar el repositorio:**
    ```bash
    git clone [https://github.com/tu-usuario/CarFix-Diploma.git](https://github.com/tu-usuario/CarFix-Diploma.git)
    ```
2.  **Configurar Base de Datos:**
    * El proyecto utiliza **Code First**. Asegúrate de que la cadena de conexión en `Modelo/Context.cs` apunte a tu instancia local de SQL Server.
    * Abre la consola del Administrador de Paquetes (Package Manager Console) y ejecuta:
    ```powershell
    Update-Database
    ```
    *Esto generará la base de datos automáticamente con los datos semilla (Seed Data) de usuarios y permisos iniciales.*

3.  **Ejecutar:**
    * Compila y ejecuta el proyecto `VISTA`.
    * **Credenciales por defecto:**
        * Admin: `admin` / `admin123`
        * Técnico: `tecnico` / `tecnico123`


## 👤 Autor

**Leonel Luchini**
* Analista de Sistemas | Estudiante de Ingeniería
* [LinkedIn](https://www.linkedin.com/in/leonelluchini/)
* [Portfolio](https://leonel-luchini.github.io)

---
*Este proyecto fue desarrollado como parte de un trabajo de diploma académico, demostrando competencias en desarrollo Full Stack .NET y arquitectura de software.*
