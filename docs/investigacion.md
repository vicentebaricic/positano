# Positano Caffè & Cucina · Investigación y dirección artística

## Alcance real de la investigación

| Fuente | ¿Se pudo consultar? | Cómo |
|---|---|---|
| claudierestaurant.com (Claudie, Miami) | **No visualmente.** El entorno no tiene salida a internet (proxy rechaza el dominio). | Solo resúmenes de búsqueda y prensa (The Infatuation, Time Out, Hospitality Design, Resident). |
| pinos-restaurant.com (Pinos, Sol de Mallorca) | **No visualmente.** Mismo bloqueo. | Resumen de búsqueda del sitio oficial: menú de almuerzo con horario, evento con botón de reserva, página de contacto con dirección/horario/teléfono/correo. |
| daganresto.com (Dagan, Vitacura) | **No visualmente.** Mismo bloqueo. | Resumen de búsqueda: portada con acceso directo a carta y reserva; prensa (DF, La Tercera, Comino). |
| Positano · cartas oficiales | **Sí.** | PDFs en Drive de ciaociao.positano@gmail.com: *Menú Positano* (jul. 2026), *Menú Brunch* (may. 2026), *Bevande e Cocktail Bar* (sep. 2026), *Carta Positano Nikkei* (jul. 2026). |
| Positano · Instagram | **No.** | Sin red y sin permiso para el conector de Meta. |
| Positano · Tripadvisor / Uber Eats | Solo resúmenes de búsqueda. | Usados únicamente para contrastar dirección/teléfono; horarios contradictorios, descartados. |

Ninguna afirmación de diseño de las referencias proviene de haber visto sus páginas. Las adaptaciones se basan en la **estructura documentada** (qué secciones y acciones ofrecen) y en principios generales; deben revisarse con capturas.

## Matriz de decisiones

| Referencia | Elemento observado | Qué funciona y por qué | Adaptación a Positano | Qué evitar |
|---|---|---|---|---|
| Claudie | Identidad "Riviera" (prensa: toldo a rayas, azulejos, luz cálida) | Una identidad costera reconocible en pocos elementos materiales | Paleta de crema de cal, azul tirreno y terracota; tipografía Bodoni (italiana, de Parma) | Copiar rayas, toldos o el lujo nocturno "see-and-be-seen": Positano abre a las 8:00 y es más cotidiano |
| Claudie | Reserva vía plataforma + teléfono | Una sola acción principal, sin ruido | CTA único "Reservar mesa" → teléfono verificado | Inventar un OpenTable o un enlace de reservas |
| Pinos | Carta organizada por momento (almuerzo con horario propio) | El usuario busca por *cuándo* va a ir | Sección "Un giorno a Positano" (Mattina / Pranzo / Sera) y pestañas de carta por momento; la carta abre en la pestaña acorde a la hora | Menús de mediodía con precio cerrado que Positano no tiene |
| Pinos | Página de contacto con dirección, horario, teléfono y correo juntos | Todo lo necesario para decidir en un bloque | Bloque "Visítanos" con dirección, teléfono, horario, mapa y "Cómo llegar" | Publicar un correo inexistente |
| Pinos | Eventos con botón de reserva propio | Conversión por ocasión | **No incluido**: no hay eventos verificados en Positano | Calendarios inventados o eventos pasados |
| Dagan | Portada con acceso directo a carta y reserva | Las dos intenciones principales en el primer pantallazo | Hero con "Reservar mesa" + "Ver la carta" | Más de dos CTAs en la portada |
| Dagan | Concepto contado desde el origen de las recetas | Da identidad sin texto largo | Uso de la cita de Steinbeck que Positano ya imprime en su carta, y nombres italianos que la propia carta usa (Colazioni, Forno, Emporio, Dolci) | Inventar historia familiar, chef o fundación |
| Positano (carta) | Forno & Emporio, limoncello hecho en casa, brunch con nombres de la costa (Amalfi, Siciliano, Castelmezzano) | Son rasgos propios y verificables que lo distinguen | Bloque Forno & Emporio; Limoncello Positano entre los destacados | Presentar la carta Nikkei sin confirmar si se sirve en este local |

## Dirección artística

- **Principal:** editorial y diurna (luz de la costa amalfitana), no club nocturno.
- **Paleta:** crema `#f4ede1`, marfil `#fbf7f0`, tinta cálida `#1f1b17`, azul tirreno `#1d3247` (bandas de cita y reservas), terracota `#a8471f` (único acento y CTA). Modo oscuro derivado del azul.
  *Provisional:* no se pudo verificar contra el Instagram. Si la identidad real usa otro acento (p. ej. amarillo limón o azul mayólica), solo hay que cambiar `--c-accent` y `--c-sea`.
- **Tipografía:** Bodoni Moda (títulos, cursiva como acento) + Instrument Sans (texto e interfaz).
- **Composición:** portada partida (texto 11 / foto 13), momentos escalonados, platos en grilla asimétrica (carrusel deslizable en móvil), galería con tamaños intencionales.
- **Restricciones:** sin tarjetas redondeadas, sin degradados, sin iconos decorativos (solo el del modo claro/oscuro), animación limitada a un revelado corto y desactivada con `prefers-reduced-motion`.
