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
