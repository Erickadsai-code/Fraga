# 🚀 GitHub Web - Academia Fraga Reportes

Guía paso a paso para subir a GitHub sin usar terminal.

---

## 📝 PRIMER UPLOAD (Una sola vez)

### **1. Descomprime el ZIP**
```
academia-fraga-clean/
├── index.html
├── reportes/2026/
│   └── marzo-2026.html
├── README.md
└── .gitignore
```

### **2. Crea repositorio en GitHub**
1. Ve a https://github.com/new
2. **Repository name:** `academia-fraga-reportes`
3. **Description:** "Reportes Meta Ads - Academia Fraga"
4. **Public:** ✅
5. Click en "Create repository"

### **3. Sube los archivos (Drag & Drop)**
1. En tu nuevo repo, click en "Add file" → "Upload files"
2. Arrastra la carpeta `academia-fraga-clean`
3. En "Commit message" escribe: `Initial: Dashboard Academia Fraga`
4. Click en "Commit changes"

**¡LISTO!** ✅

---

## 🔄 AGREGAR NUEVO MES (Cada mes)

### **Cuando tengas datos de un nuevo mes:**

#### **Opción A: Por GitHub Web (más fácil)**

1. **Ve a tu repo** → Carpeta `reportes/2026/`
2. Click en "Add file" → "Create new file"
3. Nombre: `abril-2026.html`
4. **Copia el contenido** de `marzo-2026.html` completo
5. **Pega** en el nuevo archivo
6. **Edita los datos:**
   - Cambia "Marzo" por "Abril"
   - Actualiza las métricas
   - Actualiza la tabla
   - Actualiza las acciones
7. Click en "Commit new file"

**Ahora actualiza el dashboard:**

8. Abre el archivo `index.html`
9. Click en el lápiz (editar)
10. Busca esta sección:
    ```javascript
    const availableMonths = [
      { month: 'Marzo', number: '03', year: '2026', available: true },
      { month: 'Abril', number: '04', year: '2026', available: false },  // ← Cambiar a true
    ];
    ```
11. Cambia `available: false` a `available: true` para Abril
12. Click en "Commit changes"

**¡LISTO!** El reporte aparece en el dashboard ✅

---

#### **Opción B: Editar localmente (si prefieres)**

1. Clona el repo en tu computadora
2. Duplica `marzo-2026.html` → `abril-2026.html`
3. Actualiza los datos
4. Actualiza `index.html` (la lista de meses)
5. Git push
   ```bash
   git add .
   git commit -m "Add: reporte abril 2026"
   git push
   ```

---

## 🎯 ESTRUCTURA POR MES

Cada archivo debe llamarse así:
```
reportes/2026/
├── enero-2026.html
├── febrero-2026.html
├── marzo-2026.html      ← Ya existe
├── abril-2026.html      ← Próximo a agregar
├── mayo-2026.html
└── ...
```

Y en `index.html` agregar a la lista:
```javascript
const availableMonths = [
  { month: 'Enero', number: '01', year: '2026', available: false },
  { month: 'Febrero', number: '02', year: '2026', available: false },
  { month: 'Marzo', number: '03', year: '2026', available: true },
  { month: 'Abril', number: '04', year: '2026', available: true },  // ← Nuevo
  { month: 'Mayo', number: '05', year: '2026', available: false },
  // ... continúa con el resto de meses
];
```

---

## ⚡ QUICK REFERENCE

**Para agregar un nuevo mes en 5 minutos:**

1. Crea archivo: `reportes/2026/[mes]-2026.html`
2. Copia contenido de mes anterior
3. Actualiza datos (métricas, tabla, acciones)
4. Edita `index.html` → Pon `available: true` para ese mes
5. Commit
6. ¡Listo! Vercel se actualiza automáticamente

---

## 🔗 Deploy en Vercel

**Si aún no lo hiciste:**

1. Ve a https://vercel.com/new
2. Importa tu repositorio GitHub
3. Click en "Deploy"
4. Espera 1-2 minutos

**Listo!** Tu sitio estará en: `https://academia-fraga-reportes.vercel.app/`

Cada push a GitHub = actualización automática en Vercel ✨

---

## ❓ PREGUNTAS

**P: ¿Cómo edito un archivo que ya existe?**
A: Abre el archivo → Click en lápiz (edit) → Haz cambios → Commit

**P: ¿Se actualiza automáticamente en Vercel?**
A: Sí. Cada commit = redeploy en 1-2 minutos

**P: ¿Puedo cambiar los colores?**
A: Sí. En `index.html` y en cada reporte, busca `:root` en el CSS

**P: ¿Cómo cambio el nombre "Academia Fraga"?**
A: En `index.html`, busca `<span>Academia Fraga</span>` y cambia

---

## 📱 VAS A TENER

```
https://academia-fraga-reportes.vercel.app/
├─ Dashboard (muestra solo meses disponibles)
├─ Marzo 2026 → reportes/2026/marzo-2026.html
├─ Abril 2026 → reportes/2026/abril-2026.html (cuando lo agregues)
└─ Mayo 2026 → "Próximamente" (hasta que tengas datos)
```

---

**¡Mucho éxito!** 🚀
