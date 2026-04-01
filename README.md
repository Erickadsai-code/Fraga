# 📊 Academia Fraga — Reportes Meta Ads

Dashboard de reportes mensuales de Meta Ads para Academia Fraga.

## 📁 Estructura

```
academia-fraga/
├── index.html                    # Dashboard principal (por mes)
├── reportes/
│   └── 2026/
│       ├── marzo-2026.html      # Reporte Marzo 2026
│       ├── abril-2026.html      # (Agregar cuando tengas datos)
│       └── mayo-2026.html       # (Agregar cuando tengas datos)
├── README.md                    # Este archivo
└── .gitignore                   # Configuración Git
```

## 🚀 Cómo Agregar Nuevos Meses

### **Paso 1: Duplica un reporte existente**
```bash
cp reportes/2026/marzo-2026.html reportes/2026/abril-2026.html
```

### **Paso 2: Actualiza los datos**
- Abre `abril-2026.html`
- Cambio los datos (métricas, tabla, acciones)
- Guarda

### **Paso 3: Actualiza el index.html**
En `index.html`, busca la sección `const availableMonths` y agrega:

```javascript
const availableMonths = [
  { month: 'Marzo', number: '03', year: '2026', available: true },
  { month: 'Abril', number: '04', year: '2026', available: true },  // ← Nuevo
  { month: 'Mayo', number: '05', year: '2026', available: false },
];
```

También actualiza la ruta en el mismo archivo:
```javascript
// Busca el switch o if que maneja las rutas:
if (item.month === 'Abril') {
  link = `./reportes/2026/abril-2026.html`;
}
```

### **Paso 4: Sube a GitHub**
```bash
git add .
git commit -m "Add: reporte abril 2026"
git push
```

**¡Vercel se actualiza automáticamente!** 🎉

---

## 🎨 Personalización

### **Cambiar colores**
En `index.html` y en cada reporte, ve a `:root`:

```css
:root {
  --primary: #6366f1;      /* Azul principal */
  --secondary: #ec4899;    /* Rosa */
  --success: #10b981;      /* Verde */
}
```

### **Cambiar nombre**
En `index.html`, línea ~100:
```html
<span>Academia Fraga</span>  <!-- Cambiar aquí -->
```

---

## 📱 Características

✅ Dashboard por mes
✅ Fácil agregar nuevos meses
✅ 100% responsive
✅ Auto-deploy en Vercel
✅ Diseño profesional
✅ Sin necesidad de base de datos

---

## 🔄 Workflow para Nuevos Meses

1. **Tienes datos de Abril** → Duplica marzo-2026.html → Actualiza datos
2. **Actualiza index.html** → Agrega Abril a la lista
3. **Git commit + push** → Vercel se actualiza automáticamente
4. **Listo** → Los clientes ven el nuevo reporte

**Tiempo: 10-15 minutos por mes**

---

## 📚 Archivos Incluidos

- **index.html** - Dashboard (muestra solo los meses disponibles)
- **reportes/2026/marzo-2026.html** - Reporte Marzo 2026
- **README.md** - Este archivo

---

## 🆘 Necesitas Ayuda?

### **¿Cómo duplico un archivo en GitHub Web?**
1. Abre el reporte
2. Clic en el botón "..." (más opciones)
3. Selecciona "Duplicate" o copia el contenido manualmente

### **¿Cómo agrego un nuevo mes?**
1. Duplica el reporte anterior
2. Actualiza datos
3. Agrega mes a `index.html`
4. Git commit

### **¿Vercel no se actualiza?**
1. Espera 2 minutos
2. Recarga la página (Ctrl+F5)
3. Verifica que el commit se envió a GitHub

---

## 🎯 Próximos Pasos

- Tienes estructura lista para todo 2026
- Solo agrega meses cuando tengas datos
- Cada mes = ~15 minutos de trabajo
- Todo automático en Vercel

---

**Última actualización: Abril 2026**
