# Pendientes antes de publicar

## 1. Fotografías (`assets/`)

Cada hueco de la página muestra la ruta que espera. Usa WebP, en calidad 75–82.

| Archivo | Uso | Tamaño sugerido | Contenido ideal |
|---|---|---|---|
| `assets/hero/hero-positano-1600.webp` | Portada (escritorio) | 1600×2000 (4:5) | Mesa servida desde arriba o en 3/4: pasta, pizza y spritz, luz natural |
| `assets/hero/hero-positano-800.webp` | Portada (móvil) | 800×1000 | La misma imagen, reducida |
| `assets/ambiente/mattina-brunch.webp` | Momento Mattina | 900×1125 | Brunch con café y focaccia |
| `assets/ambiente/pranzo-pastas.webp` | Momento Pranzo | 900×1125 | Pasta de la casa en la mesa |
| `assets/ambiente/sera-spritz.webp` | Momento Sera | 900×1125 | Spritz y cócteles en la barra |
| `assets/ambiente/forno-focaccias.webp` | Forno & Emporio | 1200×800 | Focaccias y panes |
| `assets/platos/pizza-positano.webp` | Destacado (grande) | 1200×900 | Pizza Positano |
| `assets/platos/pasta-positano.webp` | Destacado | 1000×1250 | Pasta Positano (centolla) |
| `assets/platos/arancini-porcini.webp` | Destacado | 900×900 | Arancini |
| `assets/platos/carpaccio-pulpo.webp` | Destacado | 900×900 | Carpaccio de pulpo |
| `assets/platos/tavola-italiana.webp` | Destacado | 900×900 | Tavola italiana |
| `assets/platos/limoncello-spritz.webp` | Destacado | 900×900 | Limoncello spritz |
| `assets/galeria/salon-principal.webp` | Galería (grande) | 1400×1600 | Salón con mesas |
| `assets/galeria/barra-cafe.webp` | Galería | 800×1000 | Barra y máquina de café |
| `assets/galeria/detalle-mesa.webp` | Galería | 600×900 | Detalle de vajilla o mantel |
| `assets/galeria/terraza.webp` | Galería | 1200×750 | Exterior. **Confirmar que existe una terraza**; si no, reemplazar por otra foto y quitar la etiqueta `.sample` |
| `assets/galeria/emporio.webp` | Galería | 1000×750 | Vitrina de quesos y fiambres |
| `assets/identidad/favicon.png` | Favicon | 64×64 | Monograma |
| `assets/identidad/apple-touch-icon.png` | iOS | 180×180 | Monograma |
| `assets/identidad/og-positano.jpg` | Al compartir en redes | 1200×630 | Foto de portada con el nombre |
| `assets/identidad/logo-positano.svg` | (opcional) | SVG | Hoy se usa un logotipo tipográfico; si existe un logo oficial, reemplazar `.brand` |
| `assets/carta/carta-cucina.pdf` | Tarjeta Carta 01 | PDF | «Menú Positano.pdf» de Drive |
| `assets/carta/carta-brunch.pdf` | Tarjeta Carta 02 | PDF | «Menú Brunch.pdf» de Drive |
| `assets/carta/carta-bar.pdf` | Tarjeta Carta 03 | PDF | «Menú Bevande e Cocktail Bar.pdf» de Drive |
| `assets/carta/portada-cucina.webp` | Fondo tarjeta 01 | 900×1100 | Plato de pasta o pizza |
| `assets/carta/portada-brunch.webp` | Fondo tarjeta 02 | 900×1100 | Brunch y café |
| `assets/carta/portada-bar.webp` | Fondo tarjeta 03 | 900×1100 | Spritz o cóctel |

## 2. Datos por confirmar

- [ ] **Hora de cierre** de cada día. Tripadvisor (20:00–21:00) y Uber Eats (21:00–22:00) no coinciden. Hoy aparece "por confirmar" con la etiqueta `.sample`.
- [ ] **Servicio de cena:** depende de la hora de cierre. Por eso el formulario no ofrece "Cena".
- [ ] **Precios:** la carta completa (objeto `MENU` en `index.html`) viene de los PDFs de Drive (jul.–sep. 2026). Los ítems con precio `null` aparecen sin precio porque en el texto del PDF no se podía asignar con certeza: lasagna de champiñón, trilogía de lasagnas, pastas rellenas, Pasta Positano, Santorini, Amatriciana, Carbonara, frutti di mare, risottos (salvo el marino), Arma tu plato, milanesa de pollo, saltados, paellas, brownie, brunch individual, Castelmezzano y Siciliano, Benedettini, Strapazzata, omelettes, toast francese, varios cafés y tés, Chandon Brut y Chandon Rosé. Para completarlos, cambia `null` por el número.
- [ ] **Carta Nikkei:** ¿se sirve en Av. Chicureo 847? No está incluida.
- [ ] **Terraza o mesas exteriores:** no está confirmado.
- [ ] **Eventos, música en vivo o celebraciones:** no se encontró información, así que la sección no se incluyó.
- [ ] **Instagram `@positano_caffe_cucina`:** aparece en la búsqueda y en el listado de Sluurpy. Confirmar que es la cuenta oficial.
- [ ] **Paleta:** validar contra la identidad real del Instagram o el local.
- [ ] **Dominio definitivo:** `canonical` y `og:url`.

## 3. Enlaces e interacciones que requieren configuración

| Elemento | Dónde | Estado |
|---|---|---|
| WhatsApp (`.js-wa`, formulario) | `CONFIG.whatsapp.number` | Vacío: los botones `.js-wa` quedan ocultos y el formulario deriva al teléfono. Al poner el número, se activan solos con mensajes prearmados (`reserva`, `carta`, `general`). |
| PDFs de las cartas | `CONFIG.cartas[].ready` | `false`: la tarjeta dice «PDF pendiente» y solo ofrece «Ver en línea». Sube cada PDF y cambia a `true`. Ajusta `size` si el archivo exportado pesa distinto. |
| Carta en línea | objeto `MENU` | Activa. Abre en Colazioni hasta las 12:30, en Bar desde las 18:00 y en Cucina el resto del día. |
| Teléfono | `CONFIG.phone` | Activo (`tel:+56229547040`). Es un fijo, no se usa como WhatsApp. |
| Mapa | `iframe` de Google Maps (`?output=embed`, sin API key) | Activo. Verificar que el pin caiga en el local. |
| Cómo llegar | `CONFIG.links.directions` | Activo |
| Instagram | `CONFIG.links.instagram` | Activo (por confirmar que es oficial) |
| Precios | `CONFIG.showPrices` | `true`. Con `false` se ocultan todos los precios. |

## 4. Etiquetas `.sample` vigentes

1. Galería: "Exterior".
2. Horario: "Cierre: por confirmar".
3. Formulario: "Prepara tu reserva". Se oculta sola cuando se configura WhatsApp.
4. Tarjetas de carta: «PDF pendiente», hasta marcar `ready: true`.
