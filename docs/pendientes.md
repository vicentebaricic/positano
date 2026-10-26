# Pendientes antes de publicar

## 1. Fotografías (`assets/`)

**Ya integradas** (originales del Instagram en `assets/originales/instagram/`, optimizadas a WebP):

| Archivo | Uso | Origen |
|---|---|---|
| `assets/hero/hero-cafe.webm` (0,8 MB) + `hero-cafe.mp4` + `hero-cafe-poster.webp` | Portada (video) | `assets/originales/video/hero-original.mp4`: recortado (sin el destello de transición de 6,8–7,6 s ni el cierre con logo), sin audio, 540×960, 1,0 MB |
| `assets/ambiente/mattina-brunch.webp` | Momento Mattina | brunch-tostada-prosciutto.jpg |
| `assets/ambiente/pranzo-pastas.webp` | Momento Pranzo | pasta-pomodoro.jpg |
| `assets/galeria/pasillo-boveda.webp` | Galería | pasillo-boveda-piedra.jpg |
| `assets/galeria/nikkei-ramen.webp` | Galería | nikkei-ramen-02.jpg |
| `assets/carta/portada-cucina.webp`, `portada-brunch.webp`, `portada-nikkei.webp` | Tarjetas de carta | carbonara, brunch y nikkei-ramen-01 |
| `assets/identidad/logo-positano.webp/.png`, `favicon.png`, `apple-touch-icon.png` | Logo, favicon e ícono | logo-perfil.png (recorte circular) |
| `assets/identidad/og-positano.jpg` | Al compartir en redes | carbonara |

Las fotos vienen del Instagram en 1080 px. Sirven, pero si existen los originales de cámara, conviene reemplazarlas por versiones más grandes.

**Faltan** (cada hueco muestra la ruta esperada):

| Archivo | Uso | Tamaño sugerido | Contenido ideal |
|---|---|---|---|
| `assets/ambiente/sera-spritz.webp` | Momento Sera | 900×1125 | Spritz o cóctel en la barra |
| `assets/ambiente/forno-focaccias.webp` | Forno & Emporio | 1200×800 | Focaccias y panes |
| `assets/carta/portada-bar.webp` | Tarjeta Carta 03 | 900×1100 | Cóctel o spritz |
| `assets/platos/pizza-positano.webp` | Destacado | 1200×900 | Pizza Positano |
| `assets/platos/pasta-positano.webp` | Destacado | 1000×1250 | Pasta Positano |
| `assets/platos/arancini-porcini.webp` | Destacado | 900×900 | Arancini |
| `assets/platos/carpaccio-pulpo.webp` | Destacado | 900×900 | Carpaccio de pulpo |
| `assets/platos/tavola-italiana.webp` | Destacado | 900×900 | Tavola italiana |
| `assets/platos/limoncello-spritz.webp` | Destacado | 900×900 | Limoncello spritz |
| `assets/galeria/salon-principal.webp` | Galería (grande) | 1400×1600 | Salón con mesas |
| `assets/galeria/detalle-mesa.webp` | Galería | 600×900 | Individual con el mapa, vajilla de gres |
| `assets/galeria/emporio.webp` | Galería | 1000×750 | Vitrina de quesos y fiambres |

## 2. Datos por confirmar

- [ ] **Hora de cierre** de cada día. Tripadvisor (20:00–21:00) y Uber Eats (21:00–22:00) no coinciden. Hoy aparece "por confirmar" con la etiqueta `.sample`.
- [ ] **Servicio de cena:** depende de la hora de cierre. Por eso el formulario no ofrece "Cena".
- [ ] **Precios:** la carta completa (objeto `MENU` en `index.html`) viene de los PDFs de Drive (jul.–sep. 2026). Los ítems con precio `null` aparecen sin precio porque en el texto del PDF no se podía asignar con certeza: lasagna de champiñón, trilogía de lasagnas, pastas rellenas, Pasta Positano, Santorini, Amatriciana, Carbonara, frutti di mare, risottos (salvo el marino), Arma tu plato, milanesa de pollo, saltados, paellas, brownie, brunch individual, Castelmezzano y Siciliano, Benedettini, Strapazzata, omelettes, toast francese, varios cafés y tés, Chandon Brut y Chandon Rosé. Para completarlos, cambia `null` por el número.
- [ ] **Carta Nikkei:** su PDF se subió y está publicada como Carta 04. Confirmar que se sirve en este local; no tiene versión en línea.
- [ ] **Eventos, música en vivo o celebraciones:** no se encontró información, así que la sección no se incluyó.
- [ ] **Instagram `@positano_caffe_cucina`:** aparece en la búsqueda y en el listado de Sluurpy. Confirmar que es la cuenta oficial.
- [x] **Paleta:** ajustada al logo y las fotos reales (carbón ciruela `#231921`, oro `#c99a62`, mármol y papel marfil).
- [ ] **Dominio definitivo:** `canonical` y `og:url`.

## 3. Enlaces e interacciones que requieren configuración

| Elemento | Dónde | Estado |
|---|---|---|
| WhatsApp (`.js-wa`, formulario) | `CONFIG.whatsapp.number` | Vacío: los botones `.js-wa` quedan ocultos y el formulario deriva al teléfono. Al poner el número, se activan solos con mensajes prearmados (`reserva`, `carta`, `general`). |
| PDFs de las cartas | `CONFIG.cartas` | Activos: `assets/carta/carta-cucina.pdf`, `carta-brunch.pdf`, `carta-bar.pdf` y `carta-nikkei.pdf`. Al actualizar una carta, reemplaza el archivo con el mismo nombre y ajusta `size`. |
| Carta en línea | objeto `MENU` | Activa. Abre en Colazioni hasta las 12:30, en Bar desde las 18:00 y en Cucina el resto del día. |
| Teléfono | `CONFIG.phone` | Activo (`tel:+56229547040`). Es un fijo, no se usa como WhatsApp. |
| Mapa | `iframe` de Google Maps (`?output=embed`, sin API key) | Activo. Verificar que el pin caiga en el local. |
| Cómo llegar | `CONFIG.links.directions` | Activo |
| Instagram | `CONFIG.links.instagram` | Activo (por confirmar que es oficial) |
| Precios | `CONFIG.showPrices` | `true`. Con `false` se ocultan todos los precios. |

## 4. Etiquetas `.sample` vigentes

1. Horario: "Cierre: por confirmar".
2. Formulario: "Prepara tu reserva". Se oculta sola cuando se configura WhatsApp.

## 5. Fotos de referencia que NO deben publicarse

En `assets/galeria/` hay fotos descargadas de la web de Eat Greek: `introduction-image.avif` (y su copia `introduction-image (1).avif`), `pizzafire.avif`, `eat-greek-jbr-table-scaled.jpg`, `greek-*.avif`, `grilled-calamari-7.avif`, `beetroot-salad-2.avif` e `ice-tea-with-figs-eat-greek.avif`. Son de otro restaurante y tienen derechos de autor.

- **En uso, de forma provisional:** `introduction-image.avif` en la sección «Fatto in casa», marcada con la etiqueta «Contenido de ejemplo · foto de referencia, reemplazar». Antes de publicar, reemplázala por una foto de Positano. Ya existe una lista: `assets/ambiente/hecho-en-casa.webp` (la tostada del brunch). Lo ideal sería una foto de manos emplatando un plato de Positano, como el carpaccio o el polpo e patate.
- **Sin usar:** las demás. Conviene borrarlas del repositorio antes de publicarlo.
