# 🩺 Gestión de Turnos Médicos

Aplicación web en Vue 3, con autenticación y persistencia de datos en Supabase, con paneles diferenciados por rol para pacientes, médicos y administradores.

---

## 🚀 Tecnologías utilizadas

- **Vue 3** (Composition API)
- **Vite** (build tool)
- **Pinia** (manejo de estado)
- **Vue Router**
- **Bootstrap** (estilos rápidos)
- **Supabase**
  - Autenticación (Auth)
  - Base de datos (PostgreSQL)
  - API REST automática

---

## 👥 Roles disponibles

- `paciente`: puede ver sus turnos y solicitar uno nuevo
- `medico`: puede ver los turnos asignados, editarlos o cancelarlos
- `admin`: acceso a reportes (opcional)

---

## 🧠 Funcionalidades principales

- Registro y login con validación por rol
- Sesión persistente con recuperación automática desde Supabase
- Middleware de protección de rutas (`guards.js`)
- Navbar dinámico según sesión y rol
- CRUD de turnos
- Visualización de turnos para médicos y pacientes; solo estos últimos pueden solicitar un turno
- Visualización de usuarios, desde sesión del administrador, pudiendo desactivar o activar cualquier cuenta
- Visualización de reportes (para admins), con al menos 2 gráficos integrados calculando estadísticas (Paciente x Médico, Turnos x Estado)
- Visualización del perfil del usuario, con la posibilidad de editar campos nombre, teléfono y dirección

---

## 🛠 Estructura del proyecto

```bash
src/
├── components/ # Navbar, Footer, Carousel, Gráfico de turnos
├── views/ # LoginView, RegisterView, TurnosView, etc.
├── router/ # Configuración de rutas y guards
├── services/ # authService.js, usuariosServices.js, turnosServices.js
├── stores/ # userStore con Pinia
└── supabaseClient/ # configuración de conexión
```

---

## Para correr el proyecto

Instalar dependencias:

```bash
npm install
```

Correr en desarrollo:

```bash
npm run dev
```

## Deploy

Deploy en Render:

```bash
https://pnt2-trabajo-final.onrender.com/
```


