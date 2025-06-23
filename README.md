# Portfolio Personal - Héctor Tovar

Un portfolio web personal moderno y responsivo con integración de MongoDB Atlas para gestionar el contenido dinámicamente.

## 🚀 Características

- **Diseño Moderno**: Interfaz limpia y profesional con animaciones suaves
- **Responsivo**: Optimizado para dispositivos móviles y desktop
- **Base de Datos MongoDB Atlas**: Contenido dinámico gestionado desde la nube
- **API REST**: Endpoints para obtener y enviar datos
- **Formulario de Contacto**: Sistema de mensajes integrado con la base de datos

## 🛠️ Tecnologías Utilizadas

- **Frontend**: HTML5, CSS3, JavaScript (Vanilla)
- **Backend**: Node.js, Express.js
- **Base de Datos**: MongoDB Atlas con Mongoose
- **Herramientas**: Nodemon para desarrollo

## 📋 Requisitos Previos

- Node.js (versión 14 o superior)
- Cuenta en MongoDB Atlas (gratuita)
- npm o yarn

## 🔧 CONFIGURACIÓN RÁPIDA

### ⚠️ **PASO OBLIGATORIO: Configurar MongoDB Atlas**

**1. Copia el archivo de configuración:**
```bash
cp config.env.example config.env
```

**2. Edita `config.env` con tu URI de MongoDB Atlas:** (Ya está colocada la uri pero si debe editar config.env)
```env
MONGODB_URI=mongodb+srv://tovarfigueroa:1234@cluster0.tfq0c23.mongodb.net/Web_personal?retryWrites=true&w=majority&appName=Cluster0
PORT=3000
```

**3. Instala dependencias:**
```bash
npm install
```

**4. Prueba la conexión:**
```bash
npm run test:connection
```

**5. Pobla la base de datos:**
```bash
npm run seed
```

**6. Inicia el servidor:**
```bash
npm run dev
```

**7. Abre en tu navegador:**
```
http://localhost:3000
```

## 🔗 OBTENER URI DE MONGODB ATLAS

### Paso 1: Crear cuenta
- Ve a [MongoDB Atlas](https://www.mongodb.com/atlas)
- Crea una cuenta gratuita

### Paso 2: Crear cluster
- Crea un nuevo cluster (gratuito)

### Paso 3: Configurar acceso
- En "Database Access", crea un usuario
- En "Network Access", añade tu IP o `0.0.0.0/0`

### Paso 4: Obtener URI
- Haz clic en "Connect" en tu cluster
- Selecciona "Connect your application"
- Copia la URI y reemplaza `<password>` con tu contraseña

## 📁 Estructura del Proyecto

```
Landing-Page-Web-Personal/
├── config/
│   └── database.js          # Configuración de MongoDB Atlas
├── models/
│   ├── Profile.js           # Modelo del perfil
│   ├── Project.js           # Modelo de proyectos
│   └── Contact.js           # Modelo de contactos
├── routes/
│   └── api.js               # Rutas de la API
├── scripts/
│   ├── seedData.js          # Script para poblar la BD
│   └── testConnection.js    # Script para probar conexión
├── public/
│   ├── index.html           # Página principal
│   ├── styles.css           # Estilos CSS
│   └── script.js            # JavaScript del frontend
├── config.env               #  CONFIGURACION URI AQUÍ
├── config.env.example       # Ejemplo de configuración
├── DATABASE_CONFIG.md       # Guía detallada de configuración
├── server.js                # Servidor Express
├── package.json
└── README.md
```

## 🔌 API Endpoints

### GET `/api/profile`
Obtiene los datos del perfil del desarrollador.

### GET `/api/projects`
Obtiene todos los proyectos ordenados por el campo `order`.

### POST `/api/contact`
Envía un mensaje de contacto.
```javascript
{
  "email": "usuario@ejemplo.com",
  "message": "Mensaje de contacto"
}
```

### GET `/api/contact`
Obtiene todos los mensajes de contacto (para administración).

## 📊 Estructura de la Base de Datos

### Colección: Profile
```javascript
{
  name: String,           // Nombre del desarrollador
  title: String,          // Título profesional
  description: String,    // Descripción del hero
  about: String,          // Texto de la sección "Sobre mí"
  socialLinks: {
    twitter: String,      // URL de Twitter
    github: String,       // URL de GitHub
    linkedin: String      // URL de LinkedIn
  },
  technologies: [String], // Array de tecnologías
  heroImage: String       // URL de la imagen del hero
}
```

### Colección: Project
```javascript
{
  title: String,          // Título del proyecto
  description: String,    // Descripción del proyecto
  image: String,          // URL de la imagen
  githubUrl: String,      // URL del repositorio GitHub
  liveUrl: String,        // URL del proyecto en vivo (opcional)
  technologies: [String], // Tecnologías utilizadas
  order: Number           // Orden de visualización
}
```

### Colección: Contact
```javascript
{
  email: String,          // Email del remitente
  message: String,        // Mensaje
  read: Boolean,          // Estado de lectura
  createdAt: Date         // Fecha de creación
}
```

## 🎨 Personalización

### Modificar el Contenido

1. **Editar datos del perfil**: Modifica el archivo `scripts/seedData.js` y ejecuta `npm run seed`
2. **Agregar proyectos**: Añade nuevos objetos al array de proyectos en `seedData.js`
3. **Cambiar estilos**: Edita `public/styles.css`
4. **Modificar funcionalidad**: Edita `public/script.js`

### Agregar Nuevas Secciones

1. Crea el modelo correspondiente en `models/`
2. Añade las rutas en `routes/api.js`
3. Actualiza el frontend en `public/script.js`
4. Añade los estilos en `public/styles.css`


## 📝 Comandos Útiles

```bash
# Instalar dependencias
npm install

# Probar conexión a MongoDB Atlas
npm run test:connection

# Poblar la base de datos
npm run seed

# Iniciar servidor de desarrollo
npm run dev

# Iniciar servidor de producción
npm start
```


## 👨‍💻 Autor

**Héctor Tovar**
- Twitter: [@HectorT33838505](https://x.com/HectorT33838505)
- GitHub: [@htovar21](https://github.com/htovar21)