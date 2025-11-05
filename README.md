# ��️ Gym Manager - GYM_LOBO

Sistema de gestión de socios para gimnasio desarrollado en Flutter. Permite administrar miembros, registrar pagos, gestionar cuotas y visualizar estadísticas en tiempo real con un dashboard completo.

## 📱 Características Principales

### 🔐 Sistema de Autenticación
- Login seguro con usuarios y contraseñas
- Persistencia de sesión
- Interfaz de inicio de sesión moderna

### 👥 Gestión de Socios
- **CRUD completo** de socios (Crear, Leer, Actualizar, Eliminar)
- Información detallada por socio:
  - Nombre completo
  - DNI
  - Teléfono
  - Correo electrónico
  - Fecha de nacimiento
  - Plan de suscripción
  - Precio mensual
  - Fecha de vencimiento de cuota
- Búsqueda avanzada por nombre, DNI, teléfono o correo
- Indicadores visuales de estado de cuota:
  - 🟢 Verde: Cuota al día
  - 🟡 Ámbar: Cuota vencida hace menos de 15 días
  - 🔴 Rojo: Cuota vencida hace más de 15 días

### 💰 Gestión de Pagos
- Registro completo de pagos por socio
- Historial de pagos detallado
- Métodos de pago soportados:
  - Efectivo
  - Tarjeta
  - Transferencia
  - Otros
- Observaciones en cada pago
- Cálculo automático de totales

### 📊 Dashboard Estadístico
- **Métricas en tiempo real:**
  - Total de socios activos
  - Ingresos mensuales
  - Cuotas vencidas
  - Cuotas por vencer (próximos 7 días)
- **Sistema de Recordatorios:**
  - Alertas de cuotas por vencer
  - Listado de cuotas vencidas
  - Información detallada de cada socio con cuota pendiente

### 🎨 Diseño Moderno
- Tema oscuro profesional
- Interfaz intuitiva y fácil de usar
- Animaciones y transiciones suaves
- Diseño responsive
- Paleta de colores consistente

## 🛠️ Tecnologías Utilizadas

- **Flutter** - Framework multiplataforma
- **Dart** - Lenguaje de programación
- **BLoC Pattern** - Gestión de estado
  - `flutter_bloc` - Implementación del patrón BLoC
- **SQLite** - Base de datos local
  - `sqflite` - Plugin de SQLite para Flutter
- **SharedPreferences** - Almacenamiento de preferencias de usuario
- **Intl** - Internacionalización y formato de fechas/números

## 📦 Instalación

### Requisitos Previos
- Flutter SDK (>=3.0.0)
- Dart SDK
- Git

### Pasos de Instalación

1. **Clonar el repositorio**
   ```bash
   git clone https://github.com/ShaniZJ/GYM_LOBO.git
   cd GYM_LOBO
   ```

2. **Instalar dependencias**
   ```bash
   flutter pub get
   ```

3. **Ejecutar la aplicación**
   ```bash
   flutter run
   ```

### Plataformas Soportadas
- ✅ Web
- ✅ Android
- ✅ iOS
- ✅ Windows
- ✅ Linux
- ✅ macOS

## 🚀 Uso

### Primera vez
Al iniciar la aplicación por primera vez, se creará automáticamente:
- Un usuario administrador por defecto:
  - **Usuario:** `admin`
  - **Contraseña:** `admin`
- Una base de datos SQLite local
- 30 socios ficticios de prueba (solo si la base de datos está vacía)

### Funcionalidades Principales

1. **Iniciar Sesión**
   - Ingresa tu usuario y contraseña
   - La sesión se mantendrá activa hasta que cierres sesión

2. **Gestionar Socios**
   - Desde la pestaña "Socios" puedes:
     - Ver lista de todos los socios
     - Buscar socios por nombre, DNI, teléfono o correo
     - Agregar nuevos socios
     - Editar información de socios existentes
     - Eliminar socios
     - Ver historial de pagos

3. **Registrar Pagos**
   - Desde el historial de pagos de un socio:
     - Haz clic en "Registrar Pago"
     - Completa el formulario con:
       - Monto
       - Método de pago
       - Fecha
       - Observaciones (opcional)

4. **Ver Dashboard**
   - Desde la pestaña "Dashboard" puedes:
     - Ver estadísticas generales
     - Revisar recordatorios de cuotas
     - Actualizar información con pull-to-refresh

## 📁 Estructura del Proyecto

```
lib/
├── blocs/              # Gestión de estado (BLoC Pattern)
│   ├── auth_bloc.dart      # Autenticación
│   ├── socios_bloc.dart    # Gestión de socios
│   └── pagos_bloc.dart     # Gestión de pagos
├── models/             # Modelos de datos
│   ├── socio.dart
│   ├── usuario.dart
│   └── pago.dart
├── pages/              # Pantallas de la aplicación
│   ├── login_screen.dart
│   ├── main_navigation_screen.dart
│   ├── lista_socios_screen.dart
│   ├── agregar_socio_screen.dart
│   ├── dashboard_screen.dart
│   ├── historial_pagos_screen.dart
│   └── agregar_pago_screen.dart
├── repositories/       # Acceso a datos
│   └── database_helper.dart
└── main.dart          # Punto de entrada
```

## 🎨 Paleta de Colores

El tema oscuro utiliza una paleta profesional:

- **Primary:** `#2196F3` (Azul vibrante)
- **Secondary:** `#03DAC6` (Cyan/Turquesa)
- **Surface:** `#1E1E1E` (Gris muy oscuro)
- **Background:** `#121212` (Casi negro)
- **Error:** `#CF6679` (Rojo suave)
- **Success:** `#4CAF50` (Verde)
- **Warning:** `#FFA726` (Ámbar)

## 📝 Características Técnicas

### Gestión de Estado
- **BLoC Pattern** para separar la lógica de negocio de la UI
- Estados reactivos que actualizan la interfaz automáticamente
- Manejo de estados de carga, éxito y error

### Base de Datos
- **SQLite** para almacenamiento local
- Migraciones automáticas de esquema
- Relaciones entre tablas (Socios - Pagos)
- Índices para optimización de búsquedas

### Seguridad
- Almacenamiento seguro de credenciales
- Validación de datos en formularios
- Manejo de errores robusto

## 🔄 Futuras Mejoras

- [ ] Exportar datos a Excel/PDF
- [ ] Notificaciones push para cuotas vencidas
- [ ] Generación de reportes mensuales
- [ ] Modo offline completo
- [ ] Sincronización con servidor
- [ ] Múltiples usuarios con permisos
- [ ] Gráficos y estadísticas avanzadas

## 👤 Contribuidor

- **ShaniZJ** - [GitHub](https://github.com/ShaniZJ)

## 📄 Licencia

Este proyecto está bajo la Licencia MIT. Ver el archivo `LICENSE` para más detalles.

## 🤝 Contribuciones

Las contribuciones son bienvenidas. Por favor:
1. Fork el proyecto
2. Crea una rama para tu feature (`git checkout -b feature/AmazingFeature`)
3. Commit tus cambios (`git commit -m 'Add some AmazingFeature'`)
4. Push a la rama (`git push origin feature/AmazingFeature`)
5. Abre un Pull Request

## 📞 Soporte

Si tienes alguna pregunta o problema, puedes:
- Abrir un [issue](https://github.com/ShaniZJ/GYM_LOBO/issues) en GitHub
- Contactar al desarrollador

---

⭐ Si te gusta este proyecto, ¡dale una estrella en GitHub!
