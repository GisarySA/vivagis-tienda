# Vivagis — Tienda Online

## Archivos
- `index.html` — la tienda completa (frontend)
- `vercel.json` — configuración de Vercel

---

## Cómo publicar en Vercel (paso a paso)

### Opción A — Sin código, desde el navegador (más fácil)

1. Entrá a **vercel.com** y creá una cuenta gratuita (con Google o GitHub)
2. En el dashboard, hacé clic en **"Add New Project"**
3. Elegí **"Deploy from template"** o subí los archivos directamente
4. Arrastrá la carpeta `vivagis` al área de deploy
5. En 30 segundos tu tienda está online en una URL del tipo `vivagis.vercel.app`

### Opción B — Con GitHub (recomendado para actualizar fácil)

1. Creá una cuenta en **github.com**
2. Creá un repositorio nuevo (ej: `vivagis-tienda`)
3. Subí los dos archivos (`index.html` y `vercel.json`) al repositorio
4. En Vercel, conectá tu cuenta de GitHub y seleccioná el repositorio
5. Vercel detecta automáticamente el proyecto y lo despliega
6. Cada vez que modifiques un archivo en GitHub, Vercel actualiza la web en segundos

---

## Cómo agregar/modificar productos

Abrí `index.html` con cualquier editor de texto (Notepad, VS Code, etc.)
Buscá la sección `PRODUCTOS` (está comentada claramente).

Cada producto tiene esta estructura:
```js
{
  id: 9,                        // número único, no repetir
  name: 'Nombre del producto',  // nombre visible
  cat: 'Vestidos',              // categoría (Vestidos, Blusas, Pantalones, Sweaters, Conjuntos)
  price: 15000,                 // precio en pesos, sin puntos
  old: 18000,                   // precio tachado (null si no hay oferta)
  emoji: '👗',                  // emoji representativo (temporal hasta tener fotos reales)
  badge: 'new',                 // 'new', 'sale', o '' para ninguno
  bg: '#EDE0D4',                // color de fondo de la card
  sizes: ['S', 'M', 'L', 'XL'],// talles disponibles
  desc: 'Descripción del producto...',
}
```

---

## Configuración rápida

Al inicio del `<script>` en `index.html`, encontrás:

```js
const WHATSAPP_NUMBER = '5491100000000';
```

Reemplazá ese número por el número real de Vivagis (formato internacional, sin +, sin espacios).

---

## Próximos pasos sugeridos

1. **Reemplazar emojis por fotos reales** → subir imágenes a Supabase Storage y reemplazar el emoji por `<img src="URL">`
2. **Panel de administración** → para crear/editar productos sin tocar código
3. **Base de datos Supabase** → para gestionar productos, stock y pedidos dinámicamente
4. **Dominio propio** → en Vercel podés conectar `vivagis.com` gratis
5. **Mercado Pago** → integración futura para pagos online

---

## Soporte
Cualquier cambio o mejora, pedilo al asistente con el contexto de este proyecto.
