# 🎮 FrankluX — Pack de Overlays para TikTok Live Studio
### Estética Futurista / Sci-Fi / Verde Neón

---

## 📦 ARCHIVOS INCLUIDOS

| Archivo | Descripción | Uso |
|---------|-------------|-----|
| `01_main_overlay.html` | **Overlay Principal** — Marco de gameplay + paneles laterales + widgets | Capa principal del stream |
| `02_alertas.html` | **Alertas** — Seguidor, Donación, Suscriptor, Gift, Top Gifter | Alertas animadas |
| `03_starting_soon.html` | **Starting Soon** — Pantalla de inicio con countdown | Antes del stream |
| `04_brb.html` | **BRB** — Be Right Back animado con visualizador | Cuando pausas |
| `05_stream_ending.html` | **Stream Ending** — Cierre con stats de sesión | Al terminar |
| `06_background.html` | **Fondo Cyberpunk** — Ciudad futurista con Matrix rain | Fondo independiente |

---

## 🎨 IDENTIDAD VISUAL

- **Color principal:** `#00ff88` (Verde neón brillante)
- **Color secundario:** `#00ffcc` (Cian-verde)
- **Fondo base:** `#020a04` (Negro profundo verdoso)
- **Fuente display:** Orbitron (futurista/tecnológica)
- **Fuente UI:** Rajdhani (limpia y legible)
- **Efectos:** Glow, scanlines, glitch, particles, matrix rain

---

## 🖥️ CONFIGURACIÓN EN TIKTOK LIVE STUDIO

### Resolución y Formato
- **Resolución:** 1080 × 1920 px (vertical 9:16)
- **Escala del navegador:** 100%

### Cómo usar cada archivo

#### Overlay Principal (`01_main_overlay.html`)
1. Agregar como **Fuente de Navegador** en OBS/TikTok Live Studio
2. Resolución: 1080 × 1920
3. Colocar **sobre** el gameplay
4. El área central transparente deja ver el juego

#### Alertas (`02_alertas.html`)
- Conectar a tu sistema de alertas (Streamlabs, StreamElements, etc.)
- O usar como referencia visual para configurar alertas individuales
- Cada alerta tiene su propio estilo de color:
  - 🟢 **Seguidor** → Verde neón
  - 🟡 **Donación** → Dorado
  - 🔵 **Suscriptor** → Cian
  - 🩷 **Gift/Regalo** → Rosa neón

#### Pantallas Especiales (Starting Soon, BRB, Ending)
1. Agregar como fuente de escena
2. Cambiar de escena según el momento del stream
3. El countdown en Starting Soon es automático (5 min)
4. El contador BRB anima solo
5. El Stream Ending tiene timer de sesión automático

#### Fondo (`06_background.html`)
1. Agregar como primera capa (más abajo en la pila)
2. Funciona con o sin overlay encima
3. El Matrix rain y las partículas son dinámicas

---

## ⚙️ PERSONALIZACIÓN

### Cambiar el nombre de usuario en redes sociales
Busca `@FrankluX` en cada archivo y reemplaza con tu handle

### Cambiar el tiempo del countdown (Starting Soon)
En `03_starting_soon.html`, busca:
```javascript
let secs = 5*60;  // ← Cambiar 5 por los minutos que quieras
```

### Ajustar colores
El color principal está en `:root { --neon: #00ff88; }`
Cambia ese valor en cualquier archivo para modificar el color

### Agregar tu juego actual (Starting Soon)
Busca `<div class="info-panel-value">TBD</div>` y reemplaza `TBD`

---

## 🎯 TIPS PARA EL STREAM

1. **Orden de capas en OBS:**
   - 1ro: Fondo (background.html)
   - 2do: Captura del juego
   - 3ro: Overlay principal (main_overlay.html)
   - 4to: Alertas (encima de todo)

2. **El overlay principal tiene fondo transparente** — el juego se ve a través del área central

3. **Para exportar como PNG transparente:** Abre el archivo en Chrome → Tomar screenshot con herramienta de recorte (solo los elementos del overlay, no el fondo)

4. **Para usar en OBS:** Fuente → Navegador → URL local (file:///ruta/al/archivo.html)

---

## 📱 REDES SOCIALES

Recuerda actualizar los handles en todos los archivos:
- TikTok: `@FrankluX`  
- Twitter/X: `@FrankluX`
- Instagram: `@FrankluX`

---

*Pack diseñado exclusivamente para FrankluX • Estética FuturisticNeon v1.0*
