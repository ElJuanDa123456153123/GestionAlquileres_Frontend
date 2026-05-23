# 🎨 365Soft - Sistema de Gestión de Alquileres (Frontend)

Aplicación web Angular 21 para la gestión completa de propiedades y alquileres con arquitectura multi-tenant.

---

## 🎯 Características Principales

### Módulos Administrativos
- **Dashboard**: Vista general con métricas y KPIs
- **Propiedades**: Gestión completa de propiedades, unidades y detalles
- **Contratos**: Creación, visualización, firma digital y renovaciones
- **Solicitudes**: Workflow de solicitudes con screening y aprobación
- **Pagos**: Gestión de pagos, múltiples métodos y conciliación
- **Mantenimiento**: Solicitudes, asignación a técnicos, seguimiento de etapas
- **Empleados**: Gestión de empleados con roles y permisos
- **Notificaciones**: Centro de notificaciones en tiempo real
- **Configuración**: Configuración del tenant y ajustes del sistema

### Portales Especializados
- **Portal de Inquilinos**:
  - Contratos y documentos
  - Pagos y métodos de pago
  - Solicitudes de mantenimiento
  - Mensajería con administración
  - QR de pagos móviles

- **Portal Público**:
  - Catálogo de propiedades
  - Mapa interactivo
  - Formulario de solicitudes
  - Información de contacto
  - Preguntas frecuentes

- **Portal de Propietarios**:
  - Estados de cuenta
  - Reportes financieros
  - Contratos y documentos

### Características Técnicas
- **Multi-tenant**: Detección automática por subdominio
- **PWA**: Progressive Web App con service worker
- **Internacionalización**: Español e Inglés
- **Responsive**: Diseño móvil-first
- **Lazy Loading**: Carga optimizada de módulos
- **Material Design**: Componentes de Angular Material
- **TailwindCSS**: Estilos modernos y personalizables

---

## 🛠 Stack Tecnológico

- **Framework**: Angular 21
- **Lenguaje**: TypeScript 5.7.3
- **UI Library**: Angular Material 17
- **Estilos**: TailwindCSS 4.1.18
- **Iconos**: Lucide (1000+ íconos SVG)
- **PWA**: Service Worker integrado
- **Estado**: Servicios RxJS
- **HTTP**: Interceptors para autenticación
- **Docker**: Nginx para producción

---

## 📋 Requisitos Previos

- Node.js 20+
- npm

---

## 🚀 Instalación Rápida

```bash
# 1. Clonar el repositorio
git clone https://github.com/ElJuanDa123456153123/GestionAlquileres_Frontend.git
cd GestionAlquileres_Frontend

# 2. Instalar dependencias
npm install

# 3. Iniciar el servidor de desarrollo
npm start -- --port 4201
```

La aplicación estará disponible en: http://localhost:4201

**Nota:** El backend debe estar corriendo en http://localhost:3000

---

## 📚 Estructura del Proyecto

```
src/
├── app/
│   ├── core/                    # Servicios y modelos centrales
│   │   ├── services/            # Servicios API (admin, tenant, auth)
│   │   ├── guards/              # Guards de autenticación
│   │   ├── interceptors/       # Interceptor HTTP
│   │   └── models/             # Modelos de datos
│   ├── features/               # Módulos funcionales
│   │   ├── dashboard/          # Dashboard principal
│   │   ├── propiedades/        # Gestión de propiedades
│   │   ├── contratos/          # Gestión de contratos
│   │   ├── solicitudes/        # Solicitudes de alquiler
│   │   ├── pagos/              # Gestión de pagos
│   │   ├── mantenimiento/      # Solicitudes de mantenimiento
│   │   ├── empleados/          # Gestión de empleados
│   │   ├── inquilinos/         # Portal de inquilinos
│   │   ├── notifications/      # Centro de notificaciones
│   │   ├── configuracion/      # Configuración del sistema
│   │   ├── portal-publico/     # Sitio web público
│   │   ├── tenant-portal/      # Portal de inquilinos
│   │   └── auth/               # Login y registro
│   ├── shared/                 # Componentes compartidos
│   │   ├── layouts/            # Layouts principales
│   │   │   ├── main-layout/    # Layout admin
│   │   │   ├── header/         # Header superior
│   │   │   └── sidebar/        # Sidebar navegación
│   │   └── pipes/              # Pipes personalizados
│   └── environments/           # Configuración por entorno
public/
├── i18n/                       # Archivos de traducción
│   ├── es/                     # Español
│   └── en/                     # Inglés
├── manifest.webmanifest        # Configuración PWA
└── icons/                      # Íconos de la app
```

---

## 🔧 Comandos Disponibles

```bash
# Desarrollo
npm start                      # Iniciar en puerto 4200
npm start -- --port 4201        # Iniciar en puerto 4201

# Producción
npm run build                   # Compilar para producción
npm run serve-dist              # Servir build de producción

# Calidad
npm run lint                    # Verificar linting
npm test                        # Ejecutar tests unitarios
```

---

## 🌐 Módulos Principales

### Dashboard
- **KPIs**: Ocupación, ingresos, pendientes de pago
- **Gráficos**: Tendencias de ocupación y revenue
- **Accesos rápidos**: Atajos a módulos principales

### Propiedades
- **Gestión**: CRUD completo de propiedades
- **Unidades**: Administración por propiedad
- **Dueños**: Asignación y gestión
- **Catálogo**: Configuración del portal público

### Contratos
- **Creación**: Wizard paso a paso
- **Visualización**: Detalle completo
- **PDF**: Generación y descarga
- **Renovación**: Proceso de renovación
- **Firma Digital**: Integración

### Solicitudes
- **Listado**: Todas las solicitudes
- **Screening**: Verificación de antecedentes
- **Aprobación**: Flujo de aprobación
- **Documentos**: Carga y verificación

### Pagos
- **Listado**: Historial de pagos
- **Métodos**: Múltiples procesadores
- **Aprobación**: Revisión manual
- **QR**: Pagos con QR (Bolivia)
- **Estados**: Seguimiento de estados

### Mantenimiento
- **Solicitudes**: Creación y gestión
- **Técnicos**: Asignación
- **Etapas**: Workflow de estados
- **Mensajes**: Comunicación
- **Fotos**: Evidencia visual

### Portal de Inquilinos
- **Dashboard**: Vista personalizada
- **Contratos**: Documentos y firma
- **Pagos**: Crear pagos y QR
- **Mantenimiento**: Reportar problemas
- **Mensajes**: Contacto con admin

### Portal Público
- **Catálogo**: Propiedades disponibles
- **Mapa**: Ubicación en mapa
- **Solicitudes**: Formulario de aplicación
- **Contacto**: Información de contacto
- **Multiidioma**: Español/Inglés

---

## 🔐 Seguridad y Autenticación

- **JWT Tokens**: Almacenamiento seguro
- **Guards**: Protección de rutas
- **Refresh Tokens**: Renovación automática
- **Interceptors**: Inyección de tokens
- **RBAC**: Permisos por rol

---

## 🎨 Personalización

### Tema y Estilos
- **TailwindCSS**: Configuración en `tailwind.config.js`
- **Material Theme**: Personalización en `app.config.ts`
- **Variables CSS**: Definidas globalmente

### Internacionalización
Los archivos de traducción están en `public/i18n/`:
- `es/`: Español (idioma por defecto)
- `en/`: Inglés

Para agregar un nuevo idioma:
1. Crear carpeta en `public/i18n/{codigo}/`
2. Copiar y traducir archivos JSON
3. Agregar a `src/app/core/services/language.service.ts`

---

## 📱 PWA (Progressive Web App)

La aplicación es una PWA instalable:
- **Service Worker**: Caching inteligente
- **Manifest**: Instalable en dispositivos
- **Offline**: Soporte básico offline
- **Responsive**: Optimizado para móvil

---

## 🐳 Docker

### Desarrollo
```bash
npm start -- --port 4201
```

### Producción
```bash
docker build -t gestion-frontend:prod .
docker run -p 80:80 gestion-frontend:prod
```

---

## 🔗 Integración con Backend

El frontend se conecta al backend API:
- **URL Base**: Configurable en `environments/environment.ts`
- **Endpoints**: Documentados en Swagger del backend
- **Autenticación**: JWT tokens en headers
- **Multi-tenant**: Subdominio en URL

---

## 📖 Documentación API

La documentación completa de la API está disponible en el backend:
- **Swagger**: http://localhost:3000/api
- **Endpoints**: Documentación interactiva

---

## 🐛 Troubleshooting

### Error: "Cannot connect to backend"
- Verifica que el backend esté corriendo en http://localhost:3000
- Revisa la configuración en `environments/environment.ts`

### Error: "Port already in use"
```bash
# Usa otro puerto
npm start -- --port 4201
```

### Error: "npm install failed"
```bash
# Limpia cache y reinstala
npm cache clean --force
rm -rf node_modules
npm install
```

---

## 📄 Licencia

Propiedad de 365Soft - Todos los derechos reservados

---

## 👨‍💻 Equipo de Desarrollo

365Soft Bolivia - 2026
