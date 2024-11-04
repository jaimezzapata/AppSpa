SPA Reservation System Documentation
1. Descripción del Proyecto
Este proyecto es un sistema de reservas para un SPA, donde los clientes pueden registrarse y hacer citas para servicios de masajes. El sistema tiene roles diferenciados: los administradores pueden visualizar y gestionar todas las reservas, mientras que los usuarios normales solo pueden realizar y ver sus propias reservas. Este proyecto fue diseñado para ser una aplicación web robusta, siguiendo la arquitectura Modelo-Vista-Controlador (MVC) y desarrollado con el stack MERN (MySQL, Express, React y Node.js).

2. Tecnologías y Herramientas
Node.js: Entorno de ejecución de JavaScript utilizado en el backend.
Express: Framework web para Node.js que facilita la creación de APIs RESTful.
MySQL: Base de datos relacional donde se almacenan los datos de usuarios, reservas y servicios.
React: Biblioteca de JavaScript para la construcción de interfaces de usuario en el frontend.
React Router: Librería de enrutamiento en React que permite la navegación dentro de la aplicación.
Sequelize: ORM para Node.js que permite manejar y definir modelos en MySQL de manera más intuitiva.
Postman: Herramienta utilizada para probar y depurar las API.
3. Estructura de Carpetas

📂 SPA-Reservation-System
├── 📂 backend
    ├── 📂 config
        ├── db.js                       # Conexión y configuración de la base de datos
    ├── 📂 controllers
    │   ├── adminController.js          # Controlador para gestionar vista y funciones de admin
    │   ├── appointmentController.js    # Controlador para gestionar reservas
    │   ├── authController.js           # Controlador de autenticación
    │   └── serviceController.js        # Controlador para gestionar los servicios
    ├── 📂 models
    │   ├── Appointment.js              # Modelo de la reserva
    │   ├── Service.js                  # Modelo de los servicios
    │   └── User.js                     # Modelo del usuario con el rol incluido
    ├── 📂 routes
    │   ├── adminRoutes.js              # Rutas para la administración de citas
    │   ├── appointmentRoutes.js        # Rutas para las reservas
        ├── authRoutes.js               # Rutas para las usuarios
    │   └── serviceRoutes.js            # Rutas para los servicios
    ├── server.js                       # Archivo principal del Back
├── 📂 frontend
    ├── 📂 public
│   ├── 📂 src
│       ├── 📂 components
        ├── 📂 pages
            ├── AdminPanel.js           # Panel de administración
│       │   ├── Login.js                # Página de inicio de sesión
│       │   ├── Register.js             # Página de registro de usuario
│       │   ├── Reserva.js              # Página para hacer reservas
        ├── 📂 router
            └── router.js               # Panel para usuarios regulares
        ├── 📂 utils
│       │   └── sweetAlert.js           # Panel para usuarios regulares
│       ├── main.jsx                    # Configuración principal de rutas
    ├── index.html                      # Archivo principal de ejecución



Endpoints

Endpoints del Backend
Autenticación

POST /api/auth/register: Registra un nuevo usuario en el sistema.
POST /api/auth/login: Verifica las credenciales del usuario y permite el inicio de sesión.
Administración (Reservas)

GET /api/admin/appointments: Obtiene todas las reservas en el sistema (solo accesible para administradores).
Reservas

POST /api/appointments: Crea una nueva reserva en el sistema.
Servicios

GET /api/services: Obtiene la lista de servicios de masajes disponibles.
Endpoints del Frontend
/login: Ruta para iniciar sesión en el sistema.
/register: Ruta para registrar un nuevo usuario.
/admin: Panel de administración para ver todas las reservas (solo accesible para administradores).
/user: Panel para usuarios regulares donde pueden ver sus reservas.
/reserva: Página para hacer reservas.