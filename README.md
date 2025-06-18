# Automatización de Inscripciones a Ofertas de Trabajo con n8n

Este proyecto automatiza la extracción y registro de inscripciones a ofertas de trabajo recibidas por correo electrónico desde plataformas como InfoJobs y LinkedIn, almacenando la información en una base de datos Notion. El flujo está gestionado con **n8n** y desplegado mediante **Docker Compose**.

---

## 📦 Contenido

- Flujo n8n que captura correos no leídos de InfoJobs y LinkedIn.  
- Extracción automática de datos clave: puesto, empresa y plataforma.  
- Registro automático en base de datos Notion.  
- Despliegue con Docker Compose para ejecución local o en servidor.
![Imagen-n8n](./capturas/Imagen-Flujo.png)

---

## ⚙️ Requisitos

- Docker y Docker Compose instalados.  
- Cuenta de Notion con base de datos preparada y compartida con la integración de n8n.  
- Credenciales IMAP para el correo donde llegan las notificaciones de ofertas.  
- Archivo `.env` con variables sensibles (usuario, contraseña, zona horaria).

---

## 🚀 Despliegue

1. Clona el repositorio.

2. Crea un archivo `.env` con el siguiente contenido:

   ```env
   TZ=Europe/Madrid
   N8N_BASIC_AUTH_ACTIVE=true
   N8N_BASIC_AUTH_USER=tu_usuario
   N8N_BASIC_AUTH_PASSWORD=tu_contraseña_segura

3. Ejecuta el contenedor con Docker Compose:

4. Accede a n8n en `http://localhost:5678` y configura tus credenciales IMAP y Notion.

5. Activa el flujo para que comience a funcionar automáticamente.

---

## 🛡 Seguridad

- No incluyas credenciales en el repositorio.  
- Usa el archivo `.env` y asegúrate de incluirlo en `.gitignore`.  
- Configura una contraseña segura para el acceso básico de n8n.

---

## 📄 Uso

- El flujo revisa los correos nuevos de InfoJobs y LinkedIn.  
- Extrae los datos relevantes (puesto, empresa, plataforma).  
- Añade un registro en la base de datos de Notion automáticamente.  
- Puedes modificar el flujo para adaptar plataformas o datos.

---

## 🤝 Contribuciones

Contribuciones, sugerencias y mejoras son bienvenidas. Puedes abrir issues o pull requests.