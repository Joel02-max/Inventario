# 📦 MyApp - Sistema de Gestión de Inventario

**MyApp** es una aplicación web desarrollada en .NET 8 con arquitectura N-Capas, diseñada para gestionar eficientemente artículos, préstamos y usuarios en una empresa. Ofrece funciones robustas de control de inventario, auditoría de acciones, autenticación basada en roles y generación de reportes profesionales en PDF y Excel.

---

## 🚀 Características Principales

- ✅ Gestión de artículos (CRUD con categorías, códigos y estados)
- 👥 Gestión de usuarios con roles: `Administrator` y `Operator`
- 🔄 Flujo completo de préstamos: solicitud, aprobación, entrega y devolución
- 🔐 Seguridad avanzada: autenticación por cookies, hash de contraseñas con BCrypt, protección CSRF
- 🕵️ Auditoría automática de acciones del sistema
- 📊 Reportes exportables en **PDF** (estado de inventario) y **Excel** (historial de préstamos)
- 📈 Panel administrativo con métricas y filtros por estado

---

## 🛠 Tecnologías Utilizadas

| Tecnología         | Rol                                 |
|-------------------|--------------------------------------|
| .NET 8 / C#        | Backend                             |
| ASP.NET Core MVC   | Interfaz web (frontend)             |
| SQL Server         | Base de datos relacional            |
| Entity Framework   | ORM para acceso a datos             |
| Bootstrap 5        | Diseño responsivo y moderno         |
| QuestPDF           | Generación de archivos PDF          |
| ClosedXML          | Exportación de archivos Excel       |
| Serilog            | Logging estructurado                |
| BCrypt.Net-Next    | Hashing seguro de contraseñas       |

---

## 🧱 Arquitectura N-Capas


/MyApp
├── Entities/ → Entidades y enums del dominio
├── DataAccess/ → EF Core, repositorios, UnitOfWork
├── Business/ → Lógica de negocio, servicios, DTOs
└── Presentation/ → ASP.NET MVC, vistas Razor, controladores


## ⚙️ Configuración y Ejecución

### 1. Clonar el repositorio

```bash
git clone https://github.com/tu_usuario/MyApp.git
cd MyApp
```
2. Configurar la cadena de conexión
Edita appsettings.json en MyApp.Presentation:

json
Copiar código
{
  "ConnectionStrings": {
    "DefaultConnection": "Server=localhost;Database=InventarioBD;Trusted_Connection=True;TrustServerCertificate=True;"
  }
}


🧪 Pruebas Iniciales
Registro de Usuario: El primer usuario registrado será operador.

Asignación de Roles: Un administrador puede gestionar roles desde el módulo de administración.

Préstamos: El flujo de préstamo se gestiona desde el menú correspondiente con estados visibles.
