# FrankluX — Pack de Overlays
### TikTok Live Studio · Estética Futurista · Verde Neón

---

## ARCHIVOS

| # | Archivo | Descripción |
|---|---------|-------------|
| 01 | `01_main_overlay.html` | Overlay principal — marco gameplay + paneles + alertas animadas + contador de seguidores |
| 02 | `02_alertas.html` | Referencia visual de alertas — seguidor, donación, suscriptor, gift, top gifter |
| 03 | `03_starting_soon.html` | Pantalla de inicio con countdown automático |
| 04 | `04_brb.html` | Be Right Back — anillos giratorios + visualizador |
| 05 | `05_stream_ending.html` | Cierre de stream con stats de sesión |
| 06 | `06_background.html` | Fondo cyberpunk independiente — ciudad + matrix rain |
| 07 | `07_camera_overlay.html` | Marco de cámara — 1920×1080, con badge LIVE y nombre |

---

## IDENTIDAD VISUAL

- **Color principal:** `#00ff88` — verde neón
- **Fondo base:** `#030806` — negro profundo
- **Tipografías:** Syne (títulos) · DM Mono (UI) · Space Mono (datos)
- **Estilo:** Futurista sofisticado — HUD técnico, líneas finas, glow contenido

---

## CONFIGURACIÓN EN TIKTOK LIVE STUDIO

### Resolución
Todos los overlays están en **1080 × 1920** (vertical 9:16), excepto el de cámara que es **1920 × 1080**.

### Cómo agregar cada archivo
1. Subir a GitHub Pages (ver sección abajo)
2. En TikTok Live Studio → **Agregar fuente** → **Navegador**
3. Pegar la URL del archivo
4. Configurar la resolución correspondiente

### Orden de capas (de abajo hacia arriba)
```
↑  02_alertas / sistema de alertas externo   ← encima de todo
↑  07_camera_overlay.html  (1920×1080, escalar a gusto)
↑  01_main_overlay.html    (1080×1920)
↑  Captura del juego
↑  06_background.html      (1080×1920)       ← abajo de todo
```

### Pantallas especiales (escenas separadas)
Estas no van encima del overlay principal, reemplazan toda la vista:
- `03_starting_soon.html` → antes de empezar
- `04_brb.html` → cuando pausás
- `05_stream_ending.html` → al terminar

---

## OVERLAY DE CÁMARA (07)

- **Resolución:** 1920 × 1080
- **Uso:** Agregar como Browser Source encima de la fuente de webcam
- **Posición:** Esquina inferior izquierda (por defecto)
- La cámara se ve a través del marco — el fondo es transparente
- Incluye: bordes HUD, badge LIVE animado, nombre FrankluX, indicador REC, scanline y glitch sutil

Para mover la posición, escalar desde las esquinas en TikTok Live Studio directamente.

---

## OVERLAY PRINCIPAL (01) — ANIMACIONES AUTOMÁTICAS

El `01_main_overlay.html` funciona solo sin configuración externa:

**Contador de seguidores**
- Arranca desde el número configurado en `CFG.followers`
- Sube automáticamente con animación y partículas
- Barra de progreso hacia la meta

**Alertas demo rotativas** (cada ~11 segundos)
- 🟢 Nuevo Seguidor
- 🟡 Nueva Donación
- 🔵 Nuevo Suscriptor
- 🟣 Top Gifter

**Para personalizar**, abrí el archivo y modificá la sección `CONFIG`:
```javascript
const CFG = {
  followers: 247,   // ← tu número real de seguidores
  goal: 500,        // ← tu meta
  growMs: 9000,     // ← cada cuántos ms sube un seguidor
  alertMs: 11000,   // ← cada cuántos ms aparece una alerta
};
```

---

## GITHUB PAGES — PUBLICAR LOS ARCHIVOS

1. Crear repositorio en github.com → `franklux-overlays` (público)
2. Subir todos los archivos HTML
3. Settings → Pages → Branch: main → Save
4. Esperar 1-2 minutos
5. URL base: `https://TuUsuario.github.io/franklux-overlays/`

Ejemplo de URL completa:
```
https://TuUsuario.github.io/franklux-overlays/01_main_overlay.html
```

---

## PERSONALIZACIÓN RÁPIDA

| Qué cambiar | Dónde |
|-------------|-------|
| Nombre de usuario en redes | Buscar `@FrankluX` en cada archivo |
| Seguidores iniciales | `CFG.followers` en el archivo 01 |
| Meta de seguidores | `CFG.goal` en el archivo 01 |
| Minutos del countdown | `let secs = 5*60` en el archivo 03 |
| Juego actual | `<div class="info-val">TBD</div>` en el archivo 03 |

---

*FrankluX Stream Pack v2.0 — 7 archivos · Diseño futurista sofisticado*
