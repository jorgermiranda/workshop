# Unidad 01: Instalación del Entorno de Desarrollo

## Introducción

En esta primera unidad vamos a preparar todas las herramientas necesarias para comenzar a programar.

## ¿Qué vamos a instalar y para qué sirve cada cosa?

### 1. **Chocolatey** 🍫
**¿Qué es?** Es un gestor de paquetes para Windows. Piénsalo como una "tienda de aplicaciones" desde la línea de comandos.

**¿Para qué sirve?** Nos permite instalar, actualizar y desinstalar programas de forma automática y sencilla, sin tener que descargar instaladores manualmente desde páginas web.

### 2. **Slack** 💬
**¿Qué es?** Una aplicación de mensajería y colaboración para equipos.

**¿Para qué sirve?** La usaremos para comunicarnos durante el curso, hacer preguntas, compartir dudas y mantenernos conectados como grupo de estudio.

### 3. **Node.js** 🟢
**¿Qué es?** Un entorno de ejecución para JavaScript que funciona fuera del navegador.

**¿Para qué sirve?** Nos permite ejecutar código JavaScript en nuestra computadora, crear servidores web, instalar herramientas de desarrollo y ejecutar aplicaciones web modernas.

### 4. **Visual Studio Code (VSCode)** 📝
**¿Qué es?** Un editor de código desarrollado por Microsoft.

**¿Para qué sirve?** Es donde escribiremos nuestro código. Tiene características como resaltado de sintaxis, autocompletado, extensiones y herramientas integradas que nos ayudan a programar mejor.

### 5. **Cuenta de GitHub** 🐙
**¿Qué es?** Una plataforma en línea para alojar y colaborar en proyectos de código.

**¿Para qué sirve?** Guardaremos nuestros proyectos, colaboraremos en código, crearemos un portafolio de nuestros trabajos y aprenderemos sobre control de versiones.

---

## Proceso de Instalación

### Paso 1: Instalar Chocolatey

1. **Abrir PowerShell como Administrador**
   - Presiona `Windows + X`
   - Selecciona "Windows PowerShell (Administrador)" o "Terminal (Administrador)"

2. **Ejecutar el comando de instalación**
   ```powershell
   Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
   ```

3. **Verificar la instalación**
   ```powershell
   choco --version
   ```
   Deberías ver el número de versión de Chocolatey.

### Paso 2: Instalar Slack con Chocolatey

1. **En el mismo PowerShell (como Administrador), ejecuta:**
   ```powershell
   choco install slack -y
   ```

2. **Verificar la instalación**
   - Busca Slack en el menú de inicio y ábrelo
   - Deberás unirte al espacio de trabajo del curso (luego se te proporcionará el enlace)

### Paso 3: Instalar Node.js con Chocolatey

1. **Instalar Node.js:**
   ```powershell
   choco install nodejs -y
   ```

2. **Verificar la instalación**
   - Cierra y vuelve a abrir PowerShell
   ```powershell
   node --version
   npm --version
   ```
   Deberías ver los números de versión de Node.js y npm.

### Paso 4: Instalar Visual Studio Code con Chocolatey

1. **Instalar VSCode:**
   ```powershell
   choco install vscode -y
   ```

2. **Verificar la instalación**
   - Busca "Visual Studio Code" en el menú de inicio y ábrelo

### Paso 5: Crear Cuenta de GitHub

1. **Ir a GitHub**
   - Visita [https://github.com](https://github.com)

2. **Crear cuenta**
   - Haz clic en "Sign up"
   - Elige un nombre de usuario profesional (lo usarás durante tu carrera)
   - Usa un email que revises frecuentemente
   - Crea una contraseña segura

3. **Verificar email**
   - Revisa tu correo y confirma tu cuenta

4. **Configurar perfil básico**
   - Agrega una foto de perfil
   - Escribe una breve descripción sobre ti

---

## Verificación Final

Al completar esta unidad, deberías tener:

- ✅ Chocolatey funcionando en tu sistema
- ✅ Slack instalado y conectado al espacio de trabajo del curso
- ✅ Node.js y npm funcionando correctamente
- ✅ Visual Studio Code con extensiones básicas
- ✅ Cuenta de GitHub creada y configurada

---

## Solución de Problemas Comunes

### Si Chocolatey no se instala:
- Asegúrate de estar ejecutando PowerShell como Administrador
- Verifica tu conexión a internet
- Algunos antivirus pueden bloquear la instalación

### Si Node.js no reconoce los comandos:
- Cierra y vuelve a abrir la terminal
- Reinicia tu computadora si es necesario

### Si VSCode no abre:
- Busca "Visual Studio Code" en el menú de inicio
- Si no aparece, puede que la instalación haya fallado

---

## Próximos Pasos

En la siguiente unidad comenzaremos con los conceptos básicos de programación y crearemos nuestro primer proyecto usando las herramientas que acabamos de instalar.

¡Felicitaciones por completar la configuración de tu entorno de desarrollo! 🎉
