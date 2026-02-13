# 🧁 Calculadora de Rentabilidad - PWA

Una aplicación web progresiva (PWA) para calcular la rentabilidad de recetas y productos finales, ideal para emprendedores gastronómicos.

## ✨ Características

### 📊 Cálculo Completo de Costos
- **Ingredientes**: Agrega nombre, cantidad y costo de cada ingrediente
- **Mano de Obra**: Calcula el costo basado en horas trabajadas y tarifa por hora
- **Materiales**: Incluye empaques, gas, electricidad y otros costos
- **Cálculo automático**: El total se actualiza en tiempo real

### 💰 Análisis de Rentabilidad
- Costo total de producción
- Costo por unidad
- Ingreso total estimado
- Ganancia total y por unidad
- Margen de ganancia (%)

### 💾 Gestión de Recetas
- Guarda tus recetas localmente en el dispositivo
- Carga recetas guardadas para reutilizarlas
- Elimina recetas que ya no necesites
- Los datos persisten incluso sin conexión

### 📱 PWA (Progressive Web App)
- **Instalable**: Agrega la app a tu pantalla de inicio
- **Funciona sin Internet**: Todos los datos se guardan localmente
- **Responsive**: Se adapta a móvil, tablet y desktop
- **Rápida**: Carga instantánea después de la primera visita

### ☕ Sistema de Donaciones
Integración con tres métodos de pago:
- **DaviPlata** - Para usuarios en Colombia
- **Mercado Pago** - Aceptado en toda Latinoamérica
- **PayPal** - Pagos internacionales

## 🚀 Instalación y Uso

### Opción 1: Uso Directo (Recomendado para pruebas)
1. Abre el archivo `calculadora-recetas.html` en tu navegador
2. La app funcionará inmediatamente

### Opción 2: Servidor Local (Para PWA completa)
Para que funcione como PWA instalable, necesitas servir los archivos desde un servidor:

#### Usando Python:
```bash
# Python 3
python -m http.server 8000

# Python 2
python -m SimpleHTTPServer 8000
```

#### Usando Node.js (http-server):
```bash
npx http-server -p 8000
```

#### Usando PHP:
```bash
php -S localhost:8000
```

Luego abre `http://localhost:8000/calculadora-recetas.html`

### Opción 3: Hosting en Internet
Sube los archivos a cualquier hosting web:
- **GitHub Pages** (gratis)
- **Netlify** (gratis)
- **Vercel** (gratis)
- Tu propio servidor web

## 📖 Guía de Uso

### 1. Información del Producto
- Ingresa el nombre (ej: "Buñuelos de queso")
- Indica cuántas unidades salen de la receta (ej: 50 buñuelos)

### 2. Agregar Ingredientes
- Nombre del ingrediente
- Cantidad (ej: "500g", "2 tazas")
- Costo en pesos colombianos

**Ejemplo:**
- Harina de trigo - 500g - $3,500
- Queso - 300g - $8,000
- Huevos - 4 unidades - $2,000

### 3. Agregar Mano de Obra
- Descripción (ej: "Preparación y cocción")
- Tiempo en horas (ej: 2.5 horas)
- Tarifa por hora (ej: $10,000/hora)

El costo se calcula automáticamente: 2.5 × $10,000 = $25,000

### 4. Agregar Materiales
- Descripción (ej: "Empaques", "Gas", "Servilletas")
- Cantidad
- Costo

### 5. Precio de Venta
- Ingresa el precio al que venderás cada unidad

### 6. Ver Resultados
El resumen muestra automáticamente:
- ✅ Costo total de producción
- ✅ Costo por unidad
- ✅ Ingreso total si vendes todo
- ✅ Ganancia total
- ✅ Ganancia por unidad
- ✅ Margen de ganancia en porcentaje

### 7. Guardar Receta
- Haz clic en "💾 Guardar Receta"
- Tus datos se guardan en el dispositivo
- Puedes cargarla después desde "📋 Ver Recetas Guardadas"

## 🔧 Personalización

### Configurar Donaciones

#### DaviPlata
En el código HTML, busca la función `openDaviplata()` y personaliza con tu número:

```javascript
function openDaviplata() {
    const numero = '3001234567'; // Tu número DaviPlata
    alert(`Dona al número DaviPlata: ${numero}`);
    showToast('¡Gracias por tu apoyo! 💚');
}
```

#### Mercado Pago
Obtén tu link de donación en [Mercado Pago](https://www.mercadopago.com.co/) y actualiza:

```javascript
function openMercadoPago() {
    const link = 'https://mpago.la/TU_LINK_AQUI';
    window.open(link, '_blank');
    showToast('¡Gracias por tu apoyo! 💙');
}
```

#### PayPal
Crea tu link en [PayPal.me](https://www.paypal.com/paypalme/) y actualiza:

```javascript
function openPayPal() {
    const link = 'https://www.paypal.com/paypalme/TUUSUARIO';
    window.open(link, '_blank');
    showToast('¡Gracias por tu apoyo! 💛');
}
```

### Cambiar Colores
En el CSS (dentro del `<style>`), modifica las variables:

```css
:root {
    --primary: #6366f1;        /* Color principal */
    --secondary: #ec4899;       /* Color secundario */
    --success: #10b981;         /* Color de éxito */
    --danger: #ef4444;          /* Color de peligro */
}
```

## 📱 Instalar como App

### En Android:
1. Abre la app en Chrome
2. Aparecerá un banner "Instalar app"
3. O usa el menú ⋮ → "Agregar a pantalla de inicio"

### En iOS:
1. Abre en Safari
2. Toca el botón de compartir 
3. Selecciona "Agregar a pantalla de inicio"

### En Desktop:
1. Abre en Chrome/Edge
2. Mira el ícono de instalación en la barra de direcciones
3. O usa el menú → "Instalar Calculadora de Rentabilidad"

## 🗂️ Archivos del Proyecto

```
├── calculadora-recetas.html   # Aplicación principal
├── manifest.json              # Configuración PWA
├── sw.js                      # Service Worker (funcionalidad offline)
└── README.md                  # Este archivo
```

## 💡 Consejos de Uso

### Para Buñuelos (Ejemplo Real)
**Ingredientes base:**
- Harina de maíz: 500g - $4,000
- Queso costeño: 400g - $12,000
- Huevos: 4 und - $2,400
- Mantequilla: 50g - $1,000

**Unidades producidas:** 40 buñuelos  
**Precio de venta sugerido:** $1,500 c/u  

La app te mostrará si es rentable y cuánto ganas por cada buñuelo.

### Tips:
- 💡 Incluye TODO: hasta el gas y los empaques
- 💡 Valora tu tiempo (mano de obra)
- 💡 Actualiza precios regularmente
- 💡 Guarda variaciones de la misma receta
- 💡 Compara márgenes entre productos

## 🐛 Solución de Problemas

**La app no se instala:**
- Verifica que estés usando HTTPS o localhost
- Asegúrate de que el Service Worker esté activo
- Prueba en modo incógnito

**No guarda los datos:**
- Verifica que las cookies/localStorage estén habilitadas
- No uses modo incógnito para datos permanentes

**No funciona offline:**
- Asegúrate de haber visitado la app al menos una vez online
- Verifica que el Service Worker esté registrado (F12 → Application → Service Workers)

## 🔐 Privacidad

- ✅ Todos los datos se guardan SOLO en tu dispositivo
- ✅ No hay servidor externo
- ✅ No se envía información a internet
- ✅ Tus recetas son 100% privadas

## 📄 Licencia

Libre para uso personal y comercial. ¡Disfruta y que sea rentable! 🚀

## 🤝 Contribuciones

¿Tienes ideas para mejorar la app? ¡Las sugerencias son bienvenidas!

---

**Desarrollado con ❤️ para emprendedores**

¿Te fue útil? ¡Invítame un café! ☕
