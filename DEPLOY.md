# 🚀 Guía de Despliegue - GitHub + Vercel

## 📦 Archivos a subir a GitHub

✅ **index.html** - Tu aplicación principal  
✅ **manifest.json** - Configuración PWA  
✅ **sw.js** - Service Worker  
✅ **vercel.json** - Configuración de Vercel  
✅ **.gitignore** - Archivos a ignorar  
✅ **README.md** - Documentación (opcional)

---

## 🎯 Paso 1: Subir a GitHub

### Opción A: Desde la web de GitHub (más fácil)

1. Ve a [github.com](https://github.com) e inicia sesión
2. Haz clic en **"New repository"** (botón verde)
3. Ponle nombre: `calculadora-recetas` (o el que prefieras)
4. Marca como **"Public"** (para que Vercel pueda acceder gratis)
5. Haz clic en **"Create repository"**
6. En la página del repo nuevo, haz clic en **"uploading an existing file"**
7. Arrastra TODOS los archivos (index.html, manifest.json, sw.js, vercel.json, .gitignore)
8. Escribe un mensaje: "Primera versión"
9. Haz clic en **"Commit changes"**

### Opción B: Desde la terminal (si sabes usar Git)

```bash
# 1. Crea el repositorio en GitHub.com primero
# 2. En tu carpeta con los archivos, ejecuta:

git init
git add .
git commit -m "Primera versión de la calculadora"
git branch -M main
git remote add origin https://github.com/TU_USUARIO/calculadora-recetas.git
git push -u origin main
```

---

## 🌐 Paso 2: Desplegar en Vercel

### Primera vez:

1. Ve a [vercel.com](https://vercel.com)
2. Haz clic en **"Sign Up"** o **"Log In"**
3. Selecciona **"Continue with GitHub"**
4. Autoriza a Vercel para acceder a tus repos

### Desplegar tu proyecto:

1. En el dashboard de Vercel, haz clic en **"Add New..."** → **"Project"**
2. Busca tu repositorio **"calculadora-recetas"**
3. Haz clic en **"Import"**
4. En la configuración:
   - **Project Name:** calculadora-recetas (o el que prefieras)
   - **Framework Preset:** Other (déjalo así)
   - **Root Directory:** ./ (déjalo así)
   - **Build Command:** (déjalo VACÍO)
   - **Output Directory:** ./ (déjalo así)
5. Haz clic en **"Deploy"** 🚀

---

## ✅ Listo! Tu app estará en:

```
https://calculadora-recetas.vercel.app
```
(o el nombre que hayas elegido)

---

## 🔧 Configurar tus llaves de donación

**ANTES de subir a GitHub**, edita el archivo `index.html` y personaliza:

```javascript
// Busca estas líneas y reemplaza con tus datos reales:

const llaveDaviplata = 'TU_LLAVE_DAVIPLATA_AQUI';  // ← Tu llave DaviPlata
const llaveNequi = 'TU_LLAVE_NEQUI_AQUI';          // ← Tu llave Nequi

// Más abajo:
const link = 'https://mpago.la/TU_LINK';           // ← Tu link Mercado Pago
const link = 'https://paypal.me/TUUSUARIO';        // ← Tu usuario PayPal
```

---

## 🔄 Actualizar la app después

Cuando hagas cambios:

### Desde GitHub web:
1. Ve a tu repositorio
2. Haz clic en el archivo que quieres editar
3. Haz clic en el ícono del lápiz ✏️
4. Edita y haz clic en **"Commit changes"**
5. **Vercel desplegará automáticamente** en ~30 segundos

### Desde terminal:
```bash
git add .
git commit -m "Descripción de cambios"
git push
```

---

## 📱 Instalar como PWA

Una vez desplegada en Vercel, tus usuarios podrán:

**En Android (Chrome):**
- Aparecerá banner de instalación automático
- O menú → "Agregar a pantalla de inicio"

**En iOS (Safari):**
- Botón compartir → "Agregar a pantalla de inicio"

**En Desktop:**
- Ícono de instalación en la barra de direcciones
- O menú → "Instalar Calculadora..."

---

## 🎨 Dominio personalizado (Opcional)

Si tienes un dominio propio:

1. En Vercel, ve a tu proyecto
2. Pestaña **"Settings"** → **"Domains"**
3. Agrega tu dominio
4. Sigue las instrucciones para configurar el DNS

---

## 🐛 Solución de problemas

**La PWA no se instala:**
- Verifica que estés en HTTPS (Vercel lo hace automático)
- Revisa que `manifest.json` y `sw.js` se carguen sin errores (F12 → Console)

**Los cambios no aparecen:**
- Espera 1-2 minutos (Vercel tarda un poco)
- Limpia caché: Ctrl+Shift+R (Windows) o Cmd+Shift+R (Mac)

**Error 404:**
- Verifica que `index.html` esté en la raíz del repositorio
- No debe estar dentro de una subcarpeta

---

## 💡 Tips Pro

✅ **Activa los despliegues automáticos**: Cada push a GitHub desplegará automáticamente  
✅ **Protege tus llaves**: Si no quieres mostrarlas en el código público, usa variables de entorno  
✅ **Analytics**: Vercel ofrece analytics gratis para ver visitas  
✅ **Ramas**: Puedes crear ramas en Git para probar cambios antes de publicar  

---

## 🎉 ¡Eso es todo!

Tu calculadora estará en línea, instalable como app, y funcionará offline. 

¿Dudas? Revisa la consola del navegador (F12) para ver errores.

**¡Mucho éxito con tu emprendimiento! 🚀**
