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

1. Crea un proyecto en Google Cloud Console
2. Habilita las APIs: Google Drive API y Google Picker API
3. Crea credenciales OAuth 2.0
4. Agrega los orígenes autorizados (ej: http://localhost:8000, tu dominio)

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
```1