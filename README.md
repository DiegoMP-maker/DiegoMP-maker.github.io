# EspañolProf - Plataforma Educativa para Profesores de Español

Una aplicación web completa para profesores de español que permite gestionar estudiantes, crear ejercicios interactivos con IA, y colaborar en tiempo real.

## 🚀 Características

- **Editor colaborativo en tiempo real** con formato de texto y soporte para imágenes
- **Gestión de estudiantes** individuales y grupos
- **Generación de ejercicios con IA** (conjugación, vocabulario, comprensión)
- **Sistema de vocabulario personal** para cada estudiante
- **Sincronización con Google Drive** para respaldo automático
- **Sistema de reservas** integrado con Google Calendar
- **Exportación de sesiones** a HTML con formato profesional

## 🔧 Configuración

### Primera vez usando la aplicación:

1. Abre la aplicación en tu navegador
2. Haz clic en el botón de configuración ⚙️
3. Ingresa tus propias API keys:
   - **Google Client ID**: Obténlo en [Google Cloud Console](https://console.cloud.google.com)
   - **Google API Key**: De tu proyecto en Google Cloud
   - **OpenAI API Key**: De tu cuenta en [OpenAI](https://platform.openai.com)

### Configurar Google Cloud:

1. **Crear proyecto en [Google Cloud Console](https://console.cloud.google.com)**
2. **Habilitar APIs necesarias:**
   - Google Drive API
   - Google Picker API
   
3. **Crear credenciales OAuth 2.0:**
   - Ir a "Credenciales" > "Crear credenciales" > "ID de cliente OAuth 2.0"
   - Tipo de aplicación: "Aplicación web"
   
4. **Configurar orígenes autorizados JavaScript:**
   ```
   https://diegomp-maker.github.io
   http://localhost:8000
   https://localhost:8000
   ```
   
5. **Configurar URIs de redirección autorizados:**
   ```
   https://diegomp-maker.github.io
   http://localhost:8000
   https://localhost:8000
   ```

### ⚠️ Solución de problemas OAuth:

**Error: "Error retrieving a token"**
1. Verifica que el Client ID sea correcto
2. Asegúrate que `https://diegomp-maker.github.io` esté en orígenes autorizados
3. Confirma que las APIs estén habilitadas
4. Verifica que el tipo de aplicación sea "Aplicación web" (no "Aplicación de escritorio")

**Error: "invalid_client"**
- El Client ID no coincide o está mal configurado
- Revisa que copies el Client ID completo sin espacios

**Error: "unauthorized_client"**
- Los orígenes no están autorizados correctamente
- Agrega exactamente: `https://diegomp-maker.github.io`

## 🛡️ Seguridad

- Las API keys se guardan únicamente en tu navegador local (localStorage)
- Nunca se envían a ningún servidor externo
- Cada usuario debe configurar sus propias claves

## 📖 Uso

1. **Configura tus API keys** (solo la primera vez)
2. **Agrega estudiantes** con su nivel (A1-C2)
3. **Genera ejercicios** con IA según el nivel
4. **Guarda vocabulario** personalizado por estudiante
5. **Sincroniza con Google Drive** automáticamente
6. **Descarga las sesiones** con todo el contenido

## 🌐 Demo

Visita: https://diegomp-maker.github.io

## 💻 Desarrollo local

```bash
# Clonar el repositorio
git clone https://github.com/DiegoMP-maker/DiegoMP-maker.github.io.git

# Navegar al directorio
cd DiegoMP-maker.github.io

# Iniciar servidor local
python3 -m http.server 8000

# Abrir en navegador
# http://localhost:8000
```

## 🗺️ Roadmap de Mejoras

### ✅ Implementadas
- [x] Sistema de configuración seguro para API keys
- [x] Integración con Google Drive
- [x] Generación de ejercicios con OpenAI
- [x] Sistema de vocabulario personal
- [x] Sistema de reservas con Google Calendar
- [x] Sistema de progreso y gamificación (badges/insignias)
- [x] Biblioteca de ejercicios pre-generados
- [x] Sistema de evaluación automática
- [x] Pronunciación con Web Speech API

### 🚧 En Desarrollo
- [ ] Solución completa de autenticación Google OAuth ("Error retrieving a token")

### 📋 Próximas Mejoras
- [ ] Modo presentación para clases
- [ ] Grabación y reporte de sesiones
- [ ] Ejercicios interactivos sin IA (sopa de letras, memoria, etc.)
- [ ] Temas visuales y modo oscuro
- [ ] Exportación mejorada (PDF real, certificados)
- [ ] Integración con WhatsApp/Telegram
- [ ] Acentuación inteligente
- [ ] Detector de falsos amigos
- [ ] Conjugador visual con animaciones

### 💡 Ideas Adicionales
- Sistema de notificaciones para tareas
- Calendario integrado con recordatorios
- Foro de discusión para estudiantes
- Biblioteca de recursos (PDFs, videos)
- Estadísticas detalladas por estudiante
- Modo offline con sincronización
- Aplicación móvil (React Native)
- Integración con Zoom/Google Meet
- Dictados con reconocimiento de voz
- Generador de exámenes1