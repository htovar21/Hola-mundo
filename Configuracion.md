# �� INSTRUCCIONES PARA CONFIGURACION

## 🎯 OBJETIVO
Este proyecto es un portfolio web personal con integración de MongoDB Atlas que permite gestionar el contenido dinámicamente desde una base de datos en la nube.

## 🚀 CONFIGURACIÓN

### Paso 1: Clonar el repositorio
```bash
git clone <URL_DEL_REPOSITORIO>
cd Landing-Page-Web-Personal
```

### Paso 2: Configurar MongoDB Atlas
```bash
# Copiar archivo de configuración
cp config.env.example config.env
```

### Paso 3: Editar la configuración
**Abrir `config.env` y reemplazar la URI con su propia configuración:**

```env
# Reemplazar con su URI de MongoDB Atlas
MONGODB_URI=mongodb+srv://tovarfigueroa:1234@cluster0.tfq0c23.mongodb.net/Web_personal?retryWrites=true&w=majority&appName=Cluster0
PORT=3000
```

### Paso 4: Instalar y ejecutar
```bash
npm install
npm run test:connection
npm run seed
npm run dev
```

### Paso 5: Verificar funcionamiento
- Abrir: http://localhost:3000
- Verificar que los datos se cargan desde MongoDB Atlas
- Probar el formulario de contacto


## 📁 ARCHIVOS IMPORTANTES

### Configuración
- `config.env` - ⚠️ **CONFIGURAR AQUÍ**
- `config.env.example` - Ejemplo de configuración
- `DATABASE_CONFIG.md` - Guía detallada

### Código principal
- `server.js` - Servidor Express
- `routes/api.js` - API endpoints
- `models/` - Modelos de MongoDB
- `public/` - Frontend

### Scripts útiles
- `scripts/seedData.js` - Poblar base de datos
- `scripts/testConnection.js` - Probar conexión