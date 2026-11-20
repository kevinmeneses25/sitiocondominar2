# CONDOMINAR · Sitio web

Sitio de CONDOMINAR, software de administración de condominios hecho en Quito, Ecuador.
Es HTML, CSS y JavaScript puro: no necesita instalar nada ni compilar.

## Estructura

Todos los archivos van juntos en la raíz del repositorio, sin subcarpetas:

```
index.html                Página completa (estilos y script incluidos)
vercel.json               Configuración de Vercel
*.jpg / *.png             Fotos, logo, mascota y halo
*.woff2                   Fuentes Ubuntu e Inter
CREDITOS.md               Origen y licencia de las fotografías
```

## 1. Subir a GitHub

1. Entra a github.com, haz clic en **New repository**, ponle un nombre (por ejemplo `condominar-sitio`) y créalo.
2. En el repositorio vacío, haz clic en **uploading an existing file**.
3. Selecciona **todos los archivos** de esta carpeta y arrástralos juntos.
4. Haz clic en **Commit changes**.

Con Git desde la terminal:

```bash
cd condominar-sitio
git init
git add .
git commit -m "Sitio CONDOMINAR"
git branch -M main
git remote add origin https://github.com/TU-USUARIO/condominar-sitio.git
git push -u origin main
```

## 2. Publicar en Vercel

1. Entra a vercel.com e inicia sesión con tu cuenta de GitHub.
2. Haz clic en **Add New… → Project** y elige el repositorio `condominar-sitio` (si no aparece, da permiso a Vercel sobre ese repositorio en **Adjust GitHub App Permissions**).
3. En la configuración:
   - **Framework Preset:** Other
   - **Root Directory:** `./`
   - **Build Command** y **Output Directory:** déjalos vacíos
4. Haz clic en **Deploy**. En menos de un minuto el sitio queda en una dirección `https://condominar-sitio.vercel.app`.

Cada vez que subas un cambio a GitHub, Vercel publica la nueva versión sola.

## 3. Conectar el dominio condominar.com

1. En Vercel, abre el proyecto → **Settings → Domains** → escribe `condominar.com` y también `www.condominar.com`.
2. Vercel te muestra los registros DNS que debes crear donde está registrado el dominio (normalmente un registro **A** apuntando a `76.76.21.21` y un **CNAME** de `www` hacia `cname.vercel-dns.com`; usa siempre los valores que te muestre Vercel).
3. Cuando el DNS se actualice (de minutos a unas horas), Vercel activa el certificado HTTPS automáticamente.

Importante: al apuntar el dominio a Vercel, el sitio actual de condominar.com deja de mostrarse. Hazlo solo cuando el nuevo sitio esté aprobado.

## Antes de publicar

- Conectar los botones "Agendar demostración" a la agenda real (hoy abren un correo a hola@condominar.com).
- Enlazar Blog, Guía, Quiénes somos y Política de privacidad.
- Validar con el equipo de producto las funciones de la sección Decreto 462.

## Cambiar una foto

Sube un archivo nuevo con **el mismo nombre** (JPG, idealmente de 1400 px de ancho). No hace falta tocar el HTML.

---
Elaborado por Kevin Meneses, Head of Marketing (Studio Ojo).
