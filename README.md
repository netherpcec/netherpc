# NetherPC EC — Sitio web

Página web de NetherPC EC, tienda de componentes y PCs gamer en Ecuador.

Sitio estático (HTML/CSS/JS), sin dependencias ni build. Listo para desplegar en Vercel o Netlify.

## Estructura

```
netherpc-web/
├── index.html      ← toda la página (estilos y scripts incluidos)
├── vercel.json     ← configuración de Vercel
└── README.md
```

## Cómo personalizar

Todo lo editable está en `index.html`:

1. **Número de WhatsApp** — busca la constante `WHATSAPP` en el `<script>` (cerca del final) y los enlaces `wa.me/593999999999`. Reemplaza por el número real, formato internacional sin `+` ni espacios (ej. `593987654321`).
2. **Productos** — edita el array `products` en el `<script>`. Cada producto tiene: `cat`, `name`, `price`, `old` (precio anterior o `null`), `stars`, `reviews`, `badge` y `emoji`.
3. **Email y dirección** — en el `<footer>`.
4. **Color de marca** — variable `--brand` al inicio del `<style>` (actual: `#00b4d8`).

## Desplegar en Vercel

1. Sube esta carpeta a un repositorio de GitHub.
2. Entra a [vercel.com](https://vercel.com) e inicia sesión con GitHub.
3. "Add New Project" → selecciona el repo → "Deploy".
4. Vercel detecta el sitio estático automáticamente. No necesita configuración de build.
5. Para el dominio propio: Settings → Domains → añade tu dominio y sigue las instrucciones de DNS.

## Desplegar en Netlify (alternativa)

Arrastra la carpeta directamente a [app.netlify.com/drop](https://app.netlify.com/drop) — se publica al instante.

## Notas

- Los productos usan emoji como placeholder. Para usar fotos reales, reemplaza el `card-img` por una etiqueta `<img>` y guarda las imágenes en una carpeta `/img`.
- El botón de cada producto abre WhatsApp con un mensaje pre-llenado. Es una vitrina con contacto directo, no un checkout. Si más adelante quieres carrito y pagos, esa lógica se añade aparte.
